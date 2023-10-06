## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:fbe8956a375e5d7d7eb03ac6293e498be61ea1d5f8d0b277dda814ad8b5e732f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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
$ docker pull rabbitmq@sha256:0e6c28e7d79cc337b0fde7a16587d382ec2022bfe64a3e7a54d10c1643d8d392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71041071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e37986d5bed177671d00edc2d0b8545dacf705624d83204a8bf740258b59bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 23:45:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 03 Oct 2023 23:45:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.6","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.6?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.3","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.3?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_VERSION=3.12.6
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.6","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.6?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 03 Oct 2023 23:45:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 23:45:42 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2023 23:45:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 03 Oct 2023 23:45:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23749d8ebabbc57f2cc5e562e0cc02d2b7a4375595e64054958140160d700790`  
		Last Modified: Fri, 06 Oct 2023 01:07:22 GMT  
		Size: 40.1 MB (40075658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa48703636c395f750e1e6e5daf44c45db50ba4e2a138c802e581356b44b706`  
		Last Modified: Fri, 06 Oct 2023 01:07:20 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f49954322d35a425dc895fc1ec4523233d2f917db6470abb5f47073081d0b9`  
		Last Modified: Fri, 06 Oct 2023 01:07:21 GMT  
		Size: 7.5 MB (7545713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4c204f7b873b79a78a6a943a8ed46acfb5440bdfd8a0a539831fe0d703934e`  
		Last Modified: Fri, 06 Oct 2023 01:07:21 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b507e5e0ff006bfb2a78bb0da7b001d0872787d88b647346ca511307a0a0fe4`  
		Last Modified: Fri, 06 Oct 2023 01:07:22 GMT  
		Size: 2.3 MB (2297429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc19add11fb9d40777b6ba169f3d30ec6cae65bb84f88ddebaa80374d2233f8d`  
		Last Modified: Fri, 06 Oct 2023 01:07:23 GMT  
		Size: 17.7 MB (17717782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752b91f7475158d7881b29f5b59d54f15a23a20c697f00a5818217934549a5ff`  
		Last Modified: Fri, 06 Oct 2023 01:07:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee28840cf9d57f8aa737480fb573328e039cc71bb21f6c0aeebe00a85ea3481`  
		Last Modified: Fri, 06 Oct 2023 01:07:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f08ed9a1a3f3d1b30e337d783ba962a975561792c9546c07f80678e692ca1e`  
		Last Modified: Fri, 06 Oct 2023 01:07:23 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c4d351e8a1c9029858c2a8c9a2fc8c9be7645ae6b6f408d27dfd88f72e4709`  
		Last Modified: Fri, 06 Oct 2023 01:07:24 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d4e4e2997b2f0f54802cdf36e4b1085a16724f66d433de06544bde06b9d4c905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135dd09e3764242109ed0f97456c91923a30b913f91aff953f10798156eab2ff`

```dockerfile
```

-	Layers:
	-	`sha256:ee004fd6e3189bfe6fda070ec0d4ff69fa42782c715d073965a92498f3879300`  
		Last Modified: Fri, 06 Oct 2023 01:07:20 GMT  
		Size: 791.2 KB (791154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb3e27f9b3ea2017d7d2a51612a50d9d3662d5ae518ccab92c7731016e4b47a`  
		Last Modified: Fri, 06 Oct 2023 01:07:20 GMT  
		Size: 2.3 MB (2338323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0204271eba4e79ec6d19f04998b70e079ee2b6bb419286682e5ac05dff7001cb`  
		Last Modified: Fri, 06 Oct 2023 01:07:20 GMT  
		Size: 2.3 MB (2337377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f8bcfad0ee399527d4dcfa337e7887d90d71265ec53bc835cab20f5690e09f`  
		Last Modified: Fri, 06 Oct 2023 01:07:20 GMT  
		Size: 69.3 KB (69266 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:6478d609695fcf8798ecaf0a6581cc7dbecaab098fceb617537cc8e143548110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61042731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0032781d41a37a62de4a6309291b496ccc296ce0d06e4f47107b63b2b4728b88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 23:45:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 03 Oct 2023 23:45:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.6","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.6?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.3","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.3?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_VERSION=3.12.6
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.6","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.6?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 03 Oct 2023 23:45:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 23:45:42 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2023 23:45:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 03 Oct 2023 23:45:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a3be95759a045709ab38906f7cf6f6e6bf3c68df81e46b393e362cc33ad0db`  
		Last Modified: Fri, 29 Sep 2023 03:17:28 GMT  
		Size: 32.4 MB (32389317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc8f2c66a22c3b9ebbb50e974c41ddb7a016794bba130b2aca1e9e89b67206c`  
		Last Modified: Fri, 06 Oct 2023 01:48:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8010ee9455ad640f04a250c4eef24e3f975f689e8b43998f81e406f032e218`  
		Last Modified: Fri, 06 Oct 2023 01:48:53 GMT  
		Size: 6.4 MB (6375332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3e9093b844eee3450d02a4da96768722eac913a433a7d81b460a61f9caa604`  
		Last Modified: Fri, 06 Oct 2023 01:48:52 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b7f348a49c5f9c87473bb6c42cfe22be37143425b162d52ad08e5a0a2e585e`  
		Last Modified: Fri, 06 Oct 2023 01:48:52 GMT  
		Size: 1.4 MB (1412513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd88cead7c601ae9dc2ff716428f91a9e975611c8604be184f3ea092c5c300f9`  
		Last Modified: Fri, 06 Oct 2023 01:48:52 GMT  
		Size: 17.7 MB (17717744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4decd4db3f5149b825cd72ab60bd3cee10d0350692ee9a018a670d0461c50a6`  
		Last Modified: Fri, 06 Oct 2023 01:48:50 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6047e6716914622a4e1793084f35d596ef5de8930475efd1609c918dfeeb3`  
		Last Modified: Fri, 06 Oct 2023 01:48:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e3b7f00d08ad39c29c1cdd7e67a54bc0eae4307a793cf86f6b2ed9938df2c8`  
		Last Modified: Fri, 06 Oct 2023 01:48:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6d56c42a22dd89fa1e38f1d8e4408955fb81d22f1258c28c2da685b468be8b`  
		Last Modified: Fri, 06 Oct 2023 01:48:50 GMT  
		Size: 829.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:06e644735fbb39fc4378583d1e8aa3eb03fc2a9d2b136c60f749c88b90dff3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60267354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccead02731f56fa8c16f9e528cc183746b56da1ac36527a21fe566d79563a61e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b54b25b49d8347ed6149acb265176b78663285f2d55be185289c2301e98bc3`  
		Last Modified: Fri, 29 Sep 2023 04:53:01 GMT  
		Size: 32.3 MB (32267798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a3ac682cff16f1bfd95c8f6d7287a3522d94626374d85d28316331fa5a1d1f`  
		Last Modified: Fri, 29 Sep 2023 04:52:58 GMT  
		Size: 6.1 MB (6080042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcef1a60595cd13fc0d6833c1d2c2aad363a64b15d1e6e02c8bcd4a2cd18517`  
		Last Modified: Fri, 29 Sep 2023 04:52:58 GMT  
		Size: 1.3 MB (1300453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b603a9dc8913fc0913c55e10266af832bca388bf3ad2f60aa4353d7de16ff2c9`  
		Last Modified: Fri, 29 Sep 2023 04:52:59 GMT  
		Size: 17.7 MB (17717405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239cbf4963cad77fab49fd9c3045880daf1ba67777b1f8737ab4cde54c585824`  
		Last Modified: Fri, 29 Sep 2023 04:52:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822b30415da2ef2bbe91fd4e30ffebf099760a455825e7e04bb935ca2c3590da`  
		Last Modified: Fri, 29 Sep 2023 04:53:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288d1096a46e54c0ba4a0d6b3eeb79ff25746c6d1d4fc7511d533e5539129a9e`  
		Last Modified: Fri, 29 Sep 2023 04:53:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beccad4bd4c0421c3e31a98523af8931c9f7088e4187cc40024a9c694b53c737`  
		Last Modified: Fri, 29 Sep 2023 04:53:01 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3b26d852677416da43dc695e70f4e001cd4cf8ac7261e33a853548b1b372836b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.7 KB (845700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c535e0be1cd6dde9188aab7b1a9ff5b701f77ee72612d6c048364d2ec1d5b7ed`

```dockerfile
```

-	Layers:
	-	`sha256:fe165ce812aa48cf028619c7ceeeb03289a0c520a3f77e778e57f8062c6394d7`  
		Last Modified: Fri, 29 Sep 2023 04:52:58 GMT  
		Size: 784.0 KB (783961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d38751bbe5e43ed98746eaf237414ba5b339de0466ba0bf1084ad081d03fcb`  
		Last Modified: Fri, 29 Sep 2023 04:52:58 GMT  
		Size: 61.7 KB (61739 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:0350149cc499c727e60a1428384c92b0af3ed73b1e876bcd5ffdb704745cfcc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68431539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35a2a591395233cf17bd344f4f6b2f89138d0e19fd1f1d55d49e1460d3556c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc88776f25bc7a218134623254b6c2d572d6f6e753134e433a7a2fe68c9dea7`  
		Last Modified: Fri, 29 Sep 2023 05:02:25 GMT  
		Size: 37.9 MB (37873917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5c9a36641e9e898bd2558e32585cb96b8108afe2f223afb0162e85e06fdcbe`  
		Last Modified: Fri, 29 Sep 2023 05:02:24 GMT  
		Size: 7.1 MB (7137749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16eb7c85d44acece0dde95052bc6c32607bae2356c57b4ed0a55fd362f965459`  
		Last Modified: Fri, 29 Sep 2023 05:02:23 GMT  
		Size: 2.4 MB (2368785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a707216104048d323105e0304dbe10f5a121fb77786fc2722c81fe0affeb97`  
		Last Modified: Fri, 29 Sep 2023 05:02:24 GMT  
		Size: 17.7 MB (17717503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0320049f02ce064961fb6c0e20251c2281e3be81a7d56058268cea7682a778db`  
		Last Modified: Fri, 29 Sep 2023 05:02:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8558da8e8c4e21fdc87662841e006a199dc57d4e0436d6020bdc41854e42642`  
		Last Modified: Fri, 29 Sep 2023 05:02:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8ec1680bc5df46ffba344077689c7a895be34039d379f8d2bb8f421ee3c1cf`  
		Last Modified: Fri, 29 Sep 2023 05:02:26 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3f60ef87c9dca2a664677f1e4257474d543de75546c45c38c59e4c215b53a4`  
		Last Modified: Fri, 29 Sep 2023 05:02:26 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bd49615a91d1011f9c452ffc1092ea4f20876730ea47ab8361dec9fe4b5369e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.5 KB (849516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20da5e2c4bffd82f4c77226133cef1da5f1622947fec1436053e759b4293bfa`

```dockerfile
```

-	Layers:
	-	`sha256:a56899b325aa21d8cb2a29253210ed887c6d5dbf66ffddfe7e6ba49396809c71`  
		Last Modified: Fri, 29 Sep 2023 05:02:23 GMT  
		Size: 788.0 KB (787954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ef714902e01149d00b01065e7483fa614fb0cc25441cc984a21df59fcb2c62`  
		Last Modified: Fri, 29 Sep 2023 05:02:23 GMT  
		Size: 61.6 KB (61562 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:df6ba4d659206661f72d720f88b8be7e1d7d60458e7f618aeab98feaf0ef26e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62418432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b49293b360dc942a895c9cea9efec7c7ee3a8e79f485bc972f16e6f2132b1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:38:19 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Thu, 28 Sep 2023 20:38:20 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 23:45:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 03 Oct 2023 23:45:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.6","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.6?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.3","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.3?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_VERSION=3.12.6
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.6","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.6?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 03 Oct 2023 23:45:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 23:45:42 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Oct 2023 23:45:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 03 Oct 2023 23:45:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd40bad1975f6f3ec6ac5d8ffb1f47c7ffc0efb83d84b0c72d0b05a66ae05f7c`  
		Last Modified: Fri, 06 Oct 2023 01:07:17 GMT  
		Size: 32.6 MB (32623535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a132056f079eddf9120516df83031b40a9e8df1df923a580720df7d78b4f3bc1`  
		Last Modified: Fri, 06 Oct 2023 01:07:14 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306063e977ab534dfa842abcbb48dfb1de9c450cba8724bd32d186fb1e8ac18`  
		Last Modified: Fri, 06 Oct 2023 01:07:15 GMT  
		Size: 7.4 MB (7437036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ffe6ee2e97bd83ef9bfb73052ef7047bca1032b594e67dd0625d170384caef`  
		Last Modified: Fri, 06 Oct 2023 01:07:14 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c99855826b752d60a87ab9f7aa237887872a99048dc4d71286f68e7267f4bdc`  
		Last Modified: Fri, 06 Oct 2023 01:07:15 GMT  
		Size: 1.4 MB (1401888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a7265edaaf7856720eb841ad5e98e8c3c115425b9cd6b9ddf1f80550cc7df5`  
		Last Modified: Fri, 06 Oct 2023 01:07:17 GMT  
		Size: 17.7 MB (17717692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a62150e8d7eeeac4a95694162b8b697112c16eefee28885793b9e9594074ce`  
		Last Modified: Fri, 06 Oct 2023 01:07:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9cf4ab27ff7f3bda3c4031185cf5d92429c40b2cf9d0b9d65a9d86963f8592`  
		Last Modified: Fri, 06 Oct 2023 01:07:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b222e41248689af23835ad500f5f1ea782339dc92796676f0d5f15f3e9770cad`  
		Last Modified: Fri, 06 Oct 2023 01:07:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbff2bdf4faa5e7f3cc3a9d7a5d42607c90f3129384a2ab5f4360afbd4baf0b4`  
		Last Modified: Fri, 06 Oct 2023 01:07:18 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7e387611bf9bc081105fb061a4512ab437b1ae0debff533bdaa4f85badae70c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 KB (69000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc25e8f8e7bd2fcc0580bb8fccdf472ae1c723ba6046adc3a67d61c6a5c07ff`

```dockerfile
```

-	Layers:
	-	`sha256:a2bc64baa09caad614ddb443619a8cefd185dcaff2bb43bf3e79940c9ab40842`  
		Last Modified: Fri, 06 Oct 2023 01:07:14 GMT  
		Size: 69.0 KB (69000 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:9d44912dddde0257b3a870e48f46f2ee0601b4ec6dfefd7aef943dc28366a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63345028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc65ea6ecba53f9c0099cfb3c27f0fea196ed4bcaf99c3a89bab333305b2050`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ea48fb8e2adea535eac2d1ac17f729c5f4092d101c43ebeaaf612f0c0e9120`  
		Last Modified: Fri, 29 Sep 2023 07:11:56 GMT  
		Size: 32.8 MB (32805323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759d72df008fb60517f4bc048f7c55f1ead6c4d0065bca1659062305f0a144d1`  
		Last Modified: Fri, 29 Sep 2023 07:11:54 GMT  
		Size: 8.0 MB (7951780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f6bfd8b3f74fca0b96a6b90a5003e2252bca08626fb4c79effd1cd61d0f830`  
		Last Modified: Fri, 29 Sep 2023 07:11:53 GMT  
		Size: 1.5 MB (1522255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aef37334f4372b1f3d42190366f8783b189928c2bffda854976c27bc3250b28`  
		Last Modified: Fri, 29 Sep 2023 07:11:55 GMT  
		Size: 17.7 MB (17717399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa580cd5dccb6a1a1c874f5ccc9c81bf49575dcfe771c52212f3259e05e2dca`  
		Last Modified: Fri, 29 Sep 2023 07:11:54 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74ac1d755ffae2eec182482985bcbdd044ad668ac6ff2e5ef608a20f38d788d`  
		Last Modified: Fri, 29 Sep 2023 07:11:55 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1508ceb0e9a40848aefb775f783fe8e0d2840ae855671131a38eda11c689f40`  
		Last Modified: Fri, 29 Sep 2023 07:11:56 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc00933cef80d1d4046d8535c7721e9df47caffb656de7e4b128e3e03d6d4b62`  
		Last Modified: Fri, 29 Sep 2023 07:11:56 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d1f1c23bdeb057685edf934286de7c5a89469401b1dcd3f98c2436d3aa85a716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.6 KB (843648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57f4bc7821a3f13283e2e24a5067ac92130b71b75b27e1c5ceb7ec19dff841b`

```dockerfile
```

-	Layers:
	-	`sha256:6a67ea906579cf26a5d1fd3e4e57b42bf61f8bbb7c17a38f3454f913aea4c403`  
		Last Modified: Fri, 29 Sep 2023 07:11:53 GMT  
		Size: 782.0 KB (782041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d2eb1d4a1278bce584ff2094074bf8045c7fcc3d2766f3b8d33e97596a9296f`  
		Last Modified: Fri, 29 Sep 2023 07:11:53 GMT  
		Size: 61.6 KB (61607 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:7449fe3dc85ce126061d968caaa598464d9bc1b01899288eebbdebd238c9f365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61335530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8a5c7e07ac77c9dd60220c5c8351455619695c1a1d4206eba0b61d728efa70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86917adcb065022f143f482b32276bda784cf8021acbfe99aac4e672db7fabc`  
		Last Modified: Fri, 29 Sep 2023 07:13:16 GMT  
		Size: 32.5 MB (32478704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d062359744e621236d31f0f76b657e2219593470beee0eba06bd160f52857d1c`  
		Last Modified: Fri, 29 Sep 2023 07:13:15 GMT  
		Size: 6.4 MB (6427065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e465c5c0a8578504ee73936a552e410629d032316105800e7224ab39236bc4`  
		Last Modified: Fri, 29 Sep 2023 07:13:15 GMT  
		Size: 1.5 MB (1495512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af34b696cdd5713dd581af620194352129a0d43ff0e488a50e35dd0d41fafa`  
		Last Modified: Fri, 29 Sep 2023 07:13:16 GMT  
		Size: 17.7 MB (17717390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f531e534a6b23ffe4cbaf1e2652ecf67e9c9f5b393686ba9403d76ff717169`  
		Last Modified: Fri, 29 Sep 2023 07:13:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc43d5465dcd9842d23ca971c31884c592d22e075c0ac68ca3f0794011f79a5`  
		Last Modified: Fri, 29 Sep 2023 07:13:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2778a1c1d8391a8329bf0afc21eb7d68388bf423f53a8189b25374f50470d0`  
		Last Modified: Fri, 29 Sep 2023 07:13:17 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38ce99d661bc2fafc55555b5bdf8c8f0df064fbf800f19df6a6b15ac69fb9d2`  
		Last Modified: Fri, 29 Sep 2023 07:13:17 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8dc7a09d6d53bb7381d790381e5689c4b12012564028f4252394b8a603b280f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97423bc9568286ec05b6997e30b199c7d5b694c584918e0f893f78f0ac18b127`

```dockerfile
```

-	Layers:
	-	`sha256:859f2b9b54f4704703eecfdd44a0e43d1b121fc5cbfc38f7b0a8dfc3af6c9109`  
		Last Modified: Fri, 29 Sep 2023 07:13:14 GMT  
		Size: 782.0 KB (781995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3158d91ac4a5381b8badaeefcf1c91e9cf575597939eded6b8801d9065f3d65`  
		Last Modified: Fri, 29 Sep 2023 07:13:14 GMT  
		Size: 61.6 KB (61552 bytes)  
		MIME: application/vnd.in-toto+json
