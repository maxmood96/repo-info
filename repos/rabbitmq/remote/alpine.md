## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:41778a3c6b89702e6d49d57b028bc8d74a7b32599c9b1d2cddbefa5d966c7b58
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

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:ba27d105fd2f228b4463a69e29e11cbef038ee16bd1f2a3331cb52ad05cb7caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71052162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3133d9cb0f07d33a457764f7caa4043b9920be7fac285f8f06f8124b282b3263`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Oct 2023 23:13:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 24 Oct 2023 23:13:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 24 Oct 2023 23:13:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 24 Oct 2023 23:13:57 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 24 Oct 2023 23:13:57 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 24 Oct 2023 23:13:57 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 24 Oct 2023 23:13:57 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Oct 2023 23:13:57 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 24 Oct 2023 23:13:57 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 24 Oct 2023 23:13:57 GMT
ENV RABBITMQ_VERSION=3.12.7
# Tue, 24 Oct 2023 23:13:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 24 Oct 2023 23:13:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 24 Oct 2023 23:13:57 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Oct 2023 23:13:57 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.7","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 24 Oct 2023 23:13:57 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 24 Oct 2023 23:13:57 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 24 Oct 2023 23:13:57 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 24 Oct 2023 23:13:57 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 24 Oct 2023 23:13:57 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 24 Oct 2023 23:13:57 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 24 Oct 2023 23:13:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Oct 2023 23:13:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Oct 2023 23:13:57 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 24 Oct 2023 23:13:57 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be89895b14c94c69021ceaaf971e23c33b5d976f18351dee532afd5d991bf4`  
		Last Modified: Fri, 27 Oct 2023 17:04:50 GMT  
		Size: 40.1 MB (40076653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1beab4cb18fbd3591e20902f8c895cf655e1c92ec653de7dbe34c989a32258`  
		Last Modified: Fri, 27 Oct 2023 17:04:47 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f4e813dbea40de3cda9544282d0970a0b4ee45493c70287f62306f409f827c`  
		Last Modified: Fri, 27 Oct 2023 17:04:48 GMT  
		Size: 7.6 MB (7550211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2193adad4c47da4d02a07ed9e518494120bef20cca5519504592ed1dfa14817`  
		Last Modified: Fri, 27 Oct 2023 17:04:47 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4fd05600e7697755ac1acdedd233100fe797b06e72c35564b6368a4b1770b3`  
		Last Modified: Fri, 27 Oct 2023 17:04:49 GMT  
		Size: 2.3 MB (2297453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795f889bf826b1932c55a1a7701e1994cb2024acefde15fafdd8b28a81b9f3a`  
		Last Modified: Fri, 27 Oct 2023 17:04:50 GMT  
		Size: 17.7 MB (17723345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905bae0d500b873960ee36dfa9239ee67a40f2a51eb31c071c72fc5d98053544`  
		Last Modified: Fri, 27 Oct 2023 17:04:50 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54647c819b7d63a4dec5053de31562c1d5259ce484ad126a9536048b048b4c2`  
		Last Modified: Fri, 27 Oct 2023 17:04:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58690bd35b79baed7ffc9732bfc0b956b954d2ce0cf88de024aba3f692837301`  
		Last Modified: Fri, 27 Oct 2023 17:04:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42fbbaf7794561d96a9ea8633dd7e37f7dfaa6b3a15052b9ce2dc83bee7a536`  
		Last Modified: Fri, 27 Oct 2023 17:04:51 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2e3d950ed56832a82ab33e60dac6a9377c3a58a87d4fd462170306f1bf4b45a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7586c3a31543bdde4befdbf22f514ba41b8675529c5687cf15afdf839b32001`

```dockerfile
```

-	Layers:
	-	`sha256:911474141954fcac97b3d055163101e845070076e8687b43063e9276b8ef1235`  
		Last Modified: Fri, 27 Oct 2023 17:04:47 GMT  
		Size: 760.4 KB (760353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e4a7ccfd1a2c80df3eff8a5d93933b7efe820dc57554b88114f1709bcfef73`  
		Last Modified: Fri, 27 Oct 2023 17:04:48 GMT  
		Size: 2.3 MB (2280847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:404000381f1b46a4b20d8688b2c63da92e8f59a98b273ceee723246be77e309a`  
		Last Modified: Fri, 27 Oct 2023 17:04:48 GMT  
		Size: 2.3 MB (2279957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c5446ced16464276eed72dedb31bbc559c355dc541c02e49904beb172c45ab4`  
		Last Modified: Fri, 27 Oct 2023 17:04:47 GMT  
		Size: 69.3 KB (69266 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:fa0a8115056d7c90f45dff7523e9c99b8e2e6db34f940b97717fd06e1a1e1780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61061388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e25f70c46943b07cd58c2717090bebee9feb94025a3aab20d647ad54d1e11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 31 Oct 2023 17:27:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_VERSION=3.12.8
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.8","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.8?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 31 Oct 2023 17:27:40 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 31 Oct 2023 17:27:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b05de52c518eafc854587c546fb6622f496b882d90b7a2ed47c08d91eb41e8`  
		Last Modified: Fri, 27 Oct 2023 17:09:49 GMT  
		Size: 32.4 MB (32388988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaa232c0eb9e703f5d0b314525727cd6bccec33ea17d7674977eadd4cd38b56`  
		Last Modified: Fri, 27 Oct 2023 17:09:44 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa975259a2a63b60c4eb7818a4ad0540995a4ef5047104fe1b556d7b7e9c336`  
		Last Modified: Fri, 27 Oct 2023 17:09:45 GMT  
		Size: 6.4 MB (6382898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9767d780bf5584c2cad3cd9abfd5d52313fd1321c68521650ec773016a6d315`  
		Last Modified: Fri, 27 Oct 2023 17:09:44 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc30bd075c6c3a5b88f28da3f248d6a109536e6f95efd4d0dbb720bce8ef034`  
		Last Modified: Fri, 27 Oct 2023 17:09:44 GMT  
		Size: 1.4 MB (1412520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a84920928da45dd0252663ec61762062095dda3a9972d543fe166621c8e8879`  
		Last Modified: Wed, 01 Nov 2023 00:02:04 GMT  
		Size: 17.7 MB (17729169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d3b4cfe8f5ad5a6d9950b8cc368ec3c4fb267ece5d4f6ccfad88ebffee5dd4`  
		Last Modified: Wed, 01 Nov 2023 00:02:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13914b3b4c9636477960ff8cd24e9fe02d3f345c260185ee8f1be38d5a37a7bb`  
		Last Modified: Wed, 01 Nov 2023 00:02:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f31230d875dff60fe11ad156baf46f885e4182fdd2a1587f57f4a76a6740e6c`  
		Last Modified: Wed, 01 Nov 2023 00:02:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a2a33a60f68e2f14785808a893b76a681cb553b535180429435d22221368a`  
		Last Modified: Wed, 01 Nov 2023 00:02:02 GMT  
		Size: 828.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:096a600c3d723f06f0c32a8965e5cf1e8ce127526106383e0ca733144329b9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60285412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953a2f58fd32eec7e8f09afea531f95e50f5d50767741e0218c7508427e98ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 31 Oct 2023 17:27:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_VERSION=3.12.8
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.8","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.8?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 31 Oct 2023 17:27:40 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 31 Oct 2023 17:27:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f57e652bf551759f9169cf7cbc65a05f05678d004fb4ecf84bbcb2ce36eb87`  
		Last Modified: Fri, 27 Oct 2023 17:51:19 GMT  
		Size: 32.3 MB (32271017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f327defd88b9aa4fddd69dee7ffebd3b13314b7841fc6c136fa4838e309016d`  
		Last Modified: Fri, 27 Oct 2023 17:51:16 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f463091713f46b393a8ec9a3be629a5c67b73263f8d101dd87a6ec7599de0249`  
		Last Modified: Fri, 27 Oct 2023 17:51:18 GMT  
		Size: 6.1 MB (6082548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385564d576ce6ba34e74067f4819742b82ac5ab8f4fa3f3b39834b27d0eefe2`  
		Last Modified: Fri, 27 Oct 2023 17:51:17 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4080c6f809b4aadf1a7dcb3b7042f5ba8d014b7e1bf1128277f41807cb4db2`  
		Last Modified: Fri, 27 Oct 2023 17:51:18 GMT  
		Size: 1.3 MB (1300444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9193feaf6bb1af2dbf9bf53e8422d887926351676154e5d13109c5340764c7`  
		Last Modified: Wed, 01 Nov 2023 00:19:13 GMT  
		Size: 17.7 MB (17728973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27775173ad00109046d30995c27a6133c4eabb248c4b6b618cb0c5f54ef7c688`  
		Last Modified: Wed, 01 Nov 2023 00:19:12 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029c0fddbc26b50fa080a5df5e0b03032eb4a9685d10a65f72daa5c817b491a4`  
		Last Modified: Wed, 01 Nov 2023 00:19:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041069165a1bcc1cee7193b3f227a868216266f26fab6d3f9781c2658b8f8009`  
		Last Modified: Wed, 01 Nov 2023 00:19:12 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5b93db94b160b74d9bf4e99b4c5349e088d98942baedfe2e0daa03aca08339`  
		Last Modified: Wed, 01 Nov 2023 00:19:13 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c0471f379766f224666ffded852f13ed3a67a014e009062ba1c5da58b9f820b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21dd8dd62029e990054417e9e57060fb4cf495214c4d19c873f28b4d70d5177a`

```dockerfile
```

-	Layers:
	-	`sha256:9993f8b5a0c8ac4d5a6a17308a9a93a68f4ed659af4cd6a659ea4969db73460e`  
		Last Modified: Wed, 01 Nov 2023 00:19:12 GMT  
		Size: 756.3 KB (756325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7453eb3846c2ce9ceb1cc2e7435970a62785c08ca261429b3b54f79d08f2b8`  
		Last Modified: Wed, 01 Nov 2023 00:19:12 GMT  
		Size: 2.2 MB (2201690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b75433aa8dbf252e337dd20706e2a2a71d1ef6111e15a8d2b963fcaf9f88b2`  
		Last Modified: Wed, 01 Nov 2023 00:19:12 GMT  
		Size: 2.2 MB (2200800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb665e772a2e2bb067b55c51b601a0a97f0b2bef2aa3fb5971a45b6bbb1eb7dc`  
		Last Modified: Wed, 01 Nov 2023 00:19:12 GMT  
		Size: 69.3 KB (69313 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:aa5fa8b60c9e1a6c6f34c18a8242079100e9b7299710fdd6738ce7e2dd00f6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68453840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a8d7f4a9a79082c4a0a61e77225e61100d8694936a2a06681c2b4ba6bb2d4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 31 Oct 2023 17:27:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_VERSION=3.12.8
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.8","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.8?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 31 Oct 2023 17:27:40 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 31 Oct 2023 17:27:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196d3fd38f39c8756a92c06767d0da13ac0823d00198f79d9bce4fe20e2a3a6a`  
		Last Modified: Fri, 27 Oct 2023 17:52:52 GMT  
		Size: 37.9 MB (37874049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86d5275580d5e06411a30f007c63c83d1a18d534bebfaa25bde9157037a08a`  
		Last Modified: Fri, 27 Oct 2023 17:52:49 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99910fe121b7470d23958b20a4288b048b92ec93dc5bfadbd8e8091998e5afba`  
		Last Modified: Fri, 27 Oct 2023 17:52:50 GMT  
		Size: 7.1 MB (7147436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1b5b553370dd9791261eb07815e1a7b5468dae1f8a95d4b73861744cbac6ea`  
		Last Modified: Fri, 27 Oct 2023 17:52:50 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b81e0e6313a3ead53ce1edcedfe133674e1a67e490963067c485e9d6d24ff7`  
		Last Modified: Fri, 27 Oct 2023 17:52:51 GMT  
		Size: 2.4 MB (2368792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2136024e99cfd239a9760962256bfd1dcb8e900048750de163f1b748d89e8302`  
		Last Modified: Wed, 01 Nov 2023 00:15:15 GMT  
		Size: 17.7 MB (17729211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12a008ce383bcbdd7edec32966140016a22fb7da24e8712b51a6cda262c2a47`  
		Last Modified: Wed, 01 Nov 2023 00:15:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0392a14097a4d7ed650a36fc820c3077f6a8f0ea47c1497bbfbc0840e61c47`  
		Last Modified: Wed, 01 Nov 2023 00:15:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344604bc6298f0d94d8c6757fe188c85b675f94f6ea404db408eac20654bc70e`  
		Last Modified: Wed, 01 Nov 2023 00:15:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40438117456a8dd725965588017b97f019ed4410aaa18f721d6185d76a38dae8`  
		Last Modified: Wed, 01 Nov 2023 00:15:14 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:267444791c906f247ea71ce4a68449b38afdde2e8270c1322d2b79118a3a5057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fcfc6b17dead07e436933c9f6ce2d028b1451742b2d8c3cf84649bd51a6277`

```dockerfile
```

-	Layers:
	-	`sha256:6eb8cd9f555bbdb630abe99036c021646dd6d600c93ba156b27dec14e49a8c44`  
		Last Modified: Wed, 01 Nov 2023 00:15:13 GMT  
		Size: 760.4 KB (760364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b1b03bd0ef50ade0f222bac505e9ae0222d16a0c93d50c29dc853949ce5a26`  
		Last Modified: Wed, 01 Nov 2023 00:15:13 GMT  
		Size: 2.3 MB (2296112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a8d17cc1491c97f0d437358dddb0e124eae75a7a8abe13dca69bf8c1bf3cc8`  
		Last Modified: Wed, 01 Nov 2023 00:15:13 GMT  
		Size: 2.3 MB (2295222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b894eb1352fff6fed0aa24f7f6424ef487ddcb6893316af7c57fc6d8042694`  
		Last Modified: Wed, 01 Nov 2023 00:15:13 GMT  
		Size: 69.1 KB (69110 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:4c3f610f79a094748981d5dd6f3a1acae00923b064cb47f16683383e10e365ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62439481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d624f09c9fcc2b912bb2a420234e7cb1e144dd161dd24a97df84b607d49c5a8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:38:19 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Thu, 28 Sep 2023 20:38:20 GMT
CMD ["/bin/sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 31 Oct 2023 17:27:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_VERSION=3.12.8
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.8","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.8?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 31 Oct 2023 17:27:40 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 31 Oct 2023 17:27:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7084bb4371909a4112132e957798d4b5e7b50751077d645e59cd3604215428d2`  
		Last Modified: Wed, 01 Nov 2023 00:08:56 GMT  
		Size: 32.6 MB (32624623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc02584d5330d01f3c7b0339d95c22295337150e12f43414aac19939a818970`  
		Last Modified: Wed, 01 Nov 2023 00:08:54 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26efdf331dbe9ea75e002721b8d804e79e40472c57b073a422f626b66d803e06`  
		Last Modified: Wed, 01 Nov 2023 00:08:55 GMT  
		Size: 7.4 MB (7445765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f283ef0c9903e04c158f080244f27a16e718c75e46ecb2bca266f1d959cbc`  
		Last Modified: Wed, 01 Nov 2023 00:08:54 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881f1f4cc75515fc575c3ceb089acc544fc52d98e4a8f8a55ea230ef30f95342`  
		Last Modified: Wed, 01 Nov 2023 00:08:56 GMT  
		Size: 1.4 MB (1401887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd41d86339012cc649dd94138a2d35fb741e45f0e9221c50a2256b939c52426`  
		Last Modified: Wed, 01 Nov 2023 00:08:57 GMT  
		Size: 17.7 MB (17728923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb867b3c114cf41c2f851556efb691b881687e838c3439ec1620e3c9fda0c4d6`  
		Last Modified: Wed, 01 Nov 2023 00:08:56 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ad88ac80f833d6d54b077df19944255557c71944bff93520129310b5306e5d`  
		Last Modified: Wed, 01 Nov 2023 00:08:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e29799fc2d6f3831bf629ad3a67bdf208589d60e9c51490c5303aee3552ee66`  
		Last Modified: Wed, 01 Nov 2023 00:08:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90f15fca4ec148efcff160597b9826ac8803fa5519930724b93aa08e95f48b4`  
		Last Modified: Wed, 01 Nov 2023 00:08:57 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:93aca3e41147cd53b8799d9560d7841a74e7c3ac028db80c58acd2e59f4cad4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 KB (68999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bb69509fe5c75b80aadde7174872ab1e4d229026d6c9ce297537d6f266c29a`

```dockerfile
```

-	Layers:
	-	`sha256:43d003fcb5a04cfeb673e9901edd25026438627dcaa4b5123b35f0908acfd27b`  
		Last Modified: Wed, 01 Nov 2023 00:08:54 GMT  
		Size: 69.0 KB (68999 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:1981ffca699fdc1b37ee1836b67890dcaa5f2d53902a0360f8e2ffcb4a29a186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63366073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c6655b619262c21f740ea6f31247c9d6851d9eef2b7154d65b4e7c2a71a026`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 31 Oct 2023 17:27:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_VERSION=3.12.8
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.8","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.8?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 31 Oct 2023 17:27:40 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 31 Oct 2023 17:27:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c683d3bbe8f22650d7212d298915ede8a21140c201e6ca5071a45567baba24af`  
		Last Modified: Fri, 27 Oct 2023 17:36:46 GMT  
		Size: 32.8 MB (32804837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a763a9de36c15c741c7d357e1c5c520eaff5a227df81f070bc5a0efe2bb5dc0`  
		Last Modified: Fri, 27 Oct 2023 17:36:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e236127e7ef69fa54b3e90d87f61f0cf35855c0d23d1462f90a88e7c49a9e3`  
		Last Modified: Fri, 27 Oct 2023 17:36:44 GMT  
		Size: 8.0 MB (7960983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2de82464687dcdcea1488224511aaab7c076f9064c4a3104da89b19bc1184d6`  
		Last Modified: Fri, 27 Oct 2023 17:36:43 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0b96369929775d635052541ff0f4ba42e95cccb22aff4a37b9a18475109b7d`  
		Last Modified: Fri, 27 Oct 2023 17:36:45 GMT  
		Size: 1.5 MB (1522239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d876439f429f9a0579ea58889a4e30f911614272fa06d48f4650d564018845`  
		Last Modified: Wed, 01 Nov 2023 00:08:57 GMT  
		Size: 17.7 MB (17728961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea864302dc1938f52a6b6b6c2ce68e961883fbd596fe7969fc44bfbb828bf261`  
		Last Modified: Wed, 01 Nov 2023 00:08:55 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6001fad6ffa9b8035ee676018e0197b2f0ebca985d9b21ebf0b521419e2952a3`  
		Last Modified: Wed, 01 Nov 2023 00:08:55 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b53712cf6d320fa7329db59d478ce6f8a94569af5fcbf2f7b7656a98b478d2`  
		Last Modified: Wed, 01 Nov 2023 00:08:56 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c3b474a6532e395891cd658f59d24a427f58b10a7b3927b8be33d4ef81d9d9`  
		Last Modified: Wed, 01 Nov 2023 00:08:57 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c32608b7171e99f9c9342e041607484d38e81b5e508fe689da98795d1aea2a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dafeb6a4ba81e49bd773553c64e4f0eacec8093b245f378bc8a28ae8a2c9097`

```dockerfile
```

-	Layers:
	-	`sha256:abf9bd9f36c1ee11a58983642b484b8238bf1b3f598bfb4ebe4e4926ac76449a`  
		Last Modified: Wed, 01 Nov 2023 00:08:56 GMT  
		Size: 754.7 KB (754687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0485deb9059d2d0ae9c0666421fc2a03bd2090bd8c4ae88a481a1ce7b50981fc`  
		Last Modified: Wed, 01 Nov 2023 00:08:55 GMT  
		Size: 2.3 MB (2274161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21cba5464f4377209f933f83d70effdf2beaac0875ee6ae74860809f5772b558`  
		Last Modified: Wed, 01 Nov 2023 00:08:56 GMT  
		Size: 2.3 MB (2273271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69d488e87f850d3de73a5626d7ad6ef5cb61ff3a73aa7f54ce8a5932642fb8f`  
		Last Modified: Wed, 01 Nov 2023 00:08:55 GMT  
		Size: 69.2 KB (69159 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:ced038c98e55a2315fd0c8ed2736532ce56cf77ab0993915a89a2c0be6df2aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61353238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a3fbcb9b5658584faf1e505eafc1616d69d2812f32cce40c79cb723fd342d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 31 Oct 2023 17:27:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_VERSION=3.12.8
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.8","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.8?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 31 Oct 2023 17:27:40 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 31 Oct 2023 17:27:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d77b2163ba1a757bf93da3911dbd17becdda540d9226ccbf8c91e3e9401caa3`  
		Last Modified: Fri, 27 Oct 2023 19:15:42 GMT  
		Size: 32.5 MB (32478957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b95da36a2ad80551437da3d0ef4374b2297eb20cb1ede14e47086aad0207831`  
		Last Modified: Fri, 27 Oct 2023 19:15:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a57676d109eb9427b6a261221e9c773de3cf251045d6f0bf6049c891b87e9a4`  
		Last Modified: Fri, 27 Oct 2023 19:15:40 GMT  
		Size: 6.4 MB (6432210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923cf9c0996c6d47c2b9a291cf3edccd23f01ed3d7b38f61b48e35fa9dea1298`  
		Last Modified: Fri, 27 Oct 2023 19:15:40 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cf8de2ab34adb2e862fbf73387b9307c0112125e5cd3ccc377d129238927fa`  
		Last Modified: Fri, 27 Oct 2023 19:15:41 GMT  
		Size: 1.5 MB (1495512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776d324b69e4835e116b919d9b97eed55c36c48349f74ac99175241b2970dd6`  
		Last Modified: Wed, 01 Nov 2023 00:03:34 GMT  
		Size: 17.7 MB (17728926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e161ccec6437e189f7f830effc2efecd6ff23f8e6cdf5a427cbc5de653a4afbb`  
		Last Modified: Wed, 01 Nov 2023 00:03:33 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfa4618476ec1a13923652311450df73f0fcaf0b685bb8fa61df8fcf7287733`  
		Last Modified: Wed, 01 Nov 2023 00:03:33 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44359ad12f1d414faf978820cbd0e3114ad5e3043208d6d0503f9667b8018be`  
		Last Modified: Wed, 01 Nov 2023 00:03:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9585cd610033570cc5102b12c0e6a2cb8d96babb04127e2c1a0deeb22d582d`  
		Last Modified: Wed, 01 Nov 2023 00:03:34 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:23bdd72aa1bc3ed59e8d1ff4cb0cf5f16ae0e30bed9ddfa467b4231ee7eb3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4253f3b9829e36c9eaf3594bd6b8f162c24f4df1098518c338afa67eec5f9357`

```dockerfile
```

-	Layers:
	-	`sha256:87eb671a5dae42470cbe585af5bb62d6b91e0e137b789abf7077e3cae19e8f58`  
		Last Modified: Wed, 01 Nov 2023 00:03:33 GMT  
		Size: 754.7 KB (754653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:319d4fc92e51f8ebe2a1e7deec5ba79fafe5e3283e04c58f8e1a26d4f362ffd0`  
		Last Modified: Wed, 01 Nov 2023 00:03:33 GMT  
		Size: 2.2 MB (2207141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff5b72da5b78c3b16d8760561ae71894d276a0d60681d2b735a73878d556531e`  
		Last Modified: Wed, 01 Nov 2023 00:03:33 GMT  
		Size: 2.2 MB (2206251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eed5c1261598754d54109e5b8944e8ac78f57f1869a4ea04c82fab8ff68260b`  
		Last Modified: Wed, 01 Nov 2023 00:03:33 GMT  
		Size: 69.1 KB (69100 bytes)  
		MIME: application/vnd.in-toto+json
