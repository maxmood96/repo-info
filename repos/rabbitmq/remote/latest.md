## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:c8ccb74a3acab14a4840304999a4add4ffb3e2edd1baed41a37efe3babc7a209
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:latest` - linux; amd64

```console
$ docker pull rabbitmq@sha256:f43ae65591338ef7f8cfc1e69ac004bc9e35332a3fec07999a3d3f3f99b94c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102025642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cc95a2cb57ad51cee2ab200fdfe30e9cb4af3f211a6c2c2d7e00b962735a15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 23:45:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 03 Oct 2023 23:45:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.6","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.6?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.3","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.3?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_VERSION=3.12.6
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.6","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.6?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:37aaf24cf781dcc5b9a4f8aa5a99a40b60ae45d64dcb4f6d5a4b9e5ab7ab0894`  
		Last Modified: Mon, 25 Sep 2023 10:30:37 GMT  
		Size: 29.5 MB (29538209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1d95d44ab9fe3447d651859aabeab343773e48a31b7b43225c15dea12bf59`  
		Last Modified: Fri, 06 Oct 2023 01:08:10 GMT  
		Size: 44.4 MB (44442234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccda69f74c54c97c03bfa88d267dcc366cac86190e4cc8b18d68b6f87a98cd51`  
		Last Modified: Fri, 06 Oct 2023 01:08:08 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b82b25475a79a0151d887272fa0647bac04c7ad88eb964d965077d44e57f4da`  
		Last Modified: Fri, 06 Oct 2023 01:08:08 GMT  
		Size: 7.5 MB (7456675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81ad3ad655559365c9eabdcad79d68e659377683ea8e93d305416794d79d760`  
		Last Modified: Fri, 06 Oct 2023 01:08:08 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454005d37fa07ed5f07a9f5ede4d33b270103545e8e91e0afa5701bb93e537f9`  
		Last Modified: Fri, 06 Oct 2023 01:08:09 GMT  
		Size: 10.7 KB (10724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0850c2e24796dd889129b12496f088a19a427f37bcc3d8c3cb1c98ac655b2c65`  
		Last Modified: Fri, 06 Oct 2023 01:08:10 GMT  
		Size: 20.6 MB (20575275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1699e1e8a360946a93e9dca01270dcf4a7f913150a0317de409259f07e606c3`  
		Last Modified: Fri, 06 Oct 2023 01:08:09 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e9da1f72de032601d0ef8bdfd13eeaf400f52bde80143920466517acfc48c6`  
		Last Modified: Fri, 06 Oct 2023 01:08:09 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e31f2a2f5d4fddefdeaf19461b2dd3973319f3e5f896bdf6c69cf7ac71aeb9`  
		Last Modified: Fri, 06 Oct 2023 01:08:10 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1218f53f35069a6b4873f4a6df460406da2b03a6b0580f90c325a87a2e434f`  
		Last Modified: Fri, 06 Oct 2023 01:08:11 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b499454d143133ca758f45e2524c7379cd7bdd0b8d4c37d0e8305a1bc627104d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14736344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288704bc6ab4467ff3d2aa51e428678e71a01c59e8dd06371325a998c75fd7c2`

```dockerfile
```

-	Layers:
	-	`sha256:8d617c36b1fddaa829046081a1ec738a6ba8c9707f3ee0165abad4eafe84e47a`  
		Last Modified: Fri, 06 Oct 2023 01:08:08 GMT  
		Size: 2.5 MB (2482738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285f94e899cb67d0b4ce07ef9f37afde29f0f4984549d35d8b1a8d17fb8023f9`  
		Last Modified: Fri, 06 Oct 2023 01:08:08 GMT  
		Size: 4.1 MB (4061180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d648772b65465b62ab496f7e1cde241492d8c08171341ff738a4ec82312820cf`  
		Last Modified: Fri, 06 Oct 2023 01:08:08 GMT  
		Size: 4.1 MB (4062136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fe3c3e9b95f65332ebc5c903db31306ff99abb72334648406f6276b3c3bd92d`  
		Last Modified: Fri, 06 Oct 2023 01:08:08 GMT  
		Size: 4.1 MB (4061190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a897733e2c0fb6af22dc6cc29a57d4d0c9976fab155fa03b4d4981d0b622f6`  
		Last Modified: Fri, 06 Oct 2023 01:08:09 GMT  
		Size: 69.1 KB (69100 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:50915c492bf42c1c68ce0255743c5a23770486c5e1760f85643c5391313f66b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85938048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bc06414e3f49c6ea652ddad788af7fdc41f8764e7617080e1245f842327f91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 25 Sep 2023 10:19:15 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:19:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:19:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:19:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:19:18 GMT
ADD file:0008d56422c09f73afbcd40ace46d311e36ba0d60eef05198ea3665172ba3433 in / 
# Mon, 25 Sep 2023 10:19:18 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 23:45:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 03 Oct 2023 23:45:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.6","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.6?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.3","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.3?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_VERSION=3.12.6
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.6","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.6?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:1adfa548dcf4236495853b0c0ac47ba789ff1a5d1cd640c102ab0ff13d8ca08d`  
		Last Modified: Mon, 25 Sep 2023 10:30:49 GMT  
		Size: 26.6 MB (26631526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db38432b797869a26144d7a6c1acc5a40c8396cd9a31c5a65d653cb8c086f53a`  
		Last Modified: Tue, 03 Oct 2023 07:44:51 GMT  
		Size: 32.7 MB (32743737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a62895f073268297e6e04bb8e0794e3732f65342db053320e1b835d7e11fba`  
		Last Modified: Fri, 06 Oct 2023 03:20:30 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39c51502e143ec31dd6b50257a34bf5c3cb420eef1b921081254774de602b7`  
		Last Modified: Fri, 06 Oct 2023 03:20:30 GMT  
		Size: 6.1 MB (6056477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39428d1f27917b21a36a342474dac930183d9bd9fc46e387f7f9cdbe600fb8cf`  
		Last Modified: Fri, 06 Oct 2023 03:20:30 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a4daa5db6507526ca3e18443879f4dce292f92e698d0601775040fb65b93d2`  
		Last Modified: Fri, 06 Oct 2023 03:20:30 GMT  
		Size: 10.7 KB (10738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f374f842d014929f48fed21c31fc4b074863e94c31262cb12c51769b498b4b`  
		Last Modified: Fri, 06 Oct 2023 03:20:32 GMT  
		Size: 20.5 MB (20493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2887f51529f815357527e73e58634b7bd76fd9840d6a4ee2a7877335cf125023`  
		Last Modified: Fri, 06 Oct 2023 03:20:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a5758629a9e4d71cec8c317e1240a8c757b99c708a2a297760cd5407b80709`  
		Last Modified: Fri, 06 Oct 2023 03:20:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ab44e7c44e1c1617962452af5eba9ad0807e97b48ccf50a9bd0e144160415e`  
		Last Modified: Fri, 06 Oct 2023 03:20:31 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad657e4d2c843ad9b20a2aec1fb5a0ac5070ba1dda3868d1db3a607ccefd4b1`  
		Last Modified: Fri, 06 Oct 2023 03:20:32 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9edc4425d2a8dd7111511d006465c3bd8bb905c128581a1652c55e2393e8cfd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14364581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be423f3cd69a713d8e93c6e6c7e6e55e871d48c6f1bd86628af611fdc22e92a`

```dockerfile
```

-	Layers:
	-	`sha256:e0ef326af11227335614568789d7f9479a800812a284d8be7e529cd476764b1b`  
		Last Modified: Fri, 06 Oct 2023 03:20:30 GMT  
		Size: 2.5 MB (2491262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9beef99ea72adc947598664fe94dc9c7694350570635d439e7d6ddcde28653ec`  
		Last Modified: Fri, 06 Oct 2023 03:20:30 GMT  
		Size: 3.9 MB (3934400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c325cae6cf51577b5c9004db3e572fcf6e07e53a8fa823d8c7fa4521a8b7ab9`  
		Last Modified: Fri, 06 Oct 2023 03:20:30 GMT  
		Size: 3.9 MB (3935356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce672b73d6d561cf0b32812ff82e291fd234c55770f47a1b8c8ee31d7b6ed84d`  
		Last Modified: Fri, 06 Oct 2023 03:20:30 GMT  
		Size: 3.9 MB (3934410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:202cb6c8ac46056b3d86756be6b308793fa0274486345859ac3993af9cb4712f`  
		Last Modified: Fri, 06 Oct 2023 03:20:31 GMT  
		Size: 69.2 KB (69153 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:30d1ce9ce5df817a30d62af04d0a68544e9bab9abf5aee95a2409317bae947f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97240219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92d7f857572ce2182befb6b4cfcdf25afd3bb7fe41d2bc7b6ca7c9f310229a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 23:45:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 03 Oct 2023 23:45:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.6","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.6?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.3","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.3?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_VERSION=3.12.6
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 03 Oct 2023 23:45:42 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 03 Oct 2023 23:45:42 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 23:45:42 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.6","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.6?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Tue, 03 Oct 2023 23:45:42 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:c391327a0f1df5790bcb00ac010a1a3924c9e4387ce36b290bc16fd9f4cc5740`  
		Last Modified: Mon, 25 Sep 2023 10:30:43 GMT  
		Size: 27.4 MB (27351199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4da95b2215d02a38627e2a09e9a4b44586d0a244a07dc92ccedf3fb6a5b6e5`  
		Last Modified: Tue, 03 Oct 2023 05:02:58 GMT  
		Size: 42.3 MB (42277776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3817a5570bd46360c10e368f41981e84e0aa8629e77a2501b71eda52b25dfa27`  
		Last Modified: Fri, 06 Oct 2023 03:09:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041871392182442cc42209e75d45c5bb2978c350fe6cc8f06d3b634ee7779f38`  
		Last Modified: Fri, 06 Oct 2023 03:09:06 GMT  
		Size: 7.1 MB (7113718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5449242e9b77c80fca8d840f978cdd48da0f334b65c62fd975be209ddfe06936`  
		Last Modified: Fri, 06 Oct 2023 03:09:06 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3466b2dc3f6015ba6d0b9c09d9d2f90fafe53d4a1a6a604d50c04eb4cc44`  
		Last Modified: Fri, 06 Oct 2023 03:09:06 GMT  
		Size: 10.7 KB (10741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b9f969efb1cc887c1df3248d67e253edb7335cdd285925ee0a1486983a8c8e`  
		Last Modified: Fri, 06 Oct 2023 03:09:08 GMT  
		Size: 20.5 MB (20484251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1351881706eec81a2dfae17008ff7d4d6865495347a767df07165bdc1cdfef9b`  
		Last Modified: Fri, 06 Oct 2023 03:09:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0d56a9cf2c171e485c7245a8a73653d0e43ba67a2cc294d47856b754098fdd`  
		Last Modified: Fri, 06 Oct 2023 03:09:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6ff2879c538fdfa17820916b7dff7151f0872ea868ff659561aa1e7573b05c`  
		Last Modified: Fri, 06 Oct 2023 03:09:11 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1696c6be29ac58dc165ec3d9625c0ce66170d23af26b35cd771b02a690c081`  
		Last Modified: Fri, 06 Oct 2023 03:09:08 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f0822196fa0dbebe86f6bb8bcb29cdf405e78866c6f6ff29e5708465adaef976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14750568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d85bd294fbce8f787a2c16f33df40cac793e9cd6e35376f2cfbaf495d838d2a`

```dockerfile
```

-	Layers:
	-	`sha256:f6e5634387bd6245f7604236e11ea7ab9e15c54b6df51424c97901d169d2afb4`  
		Last Modified: Fri, 06 Oct 2023 03:09:06 GMT  
		Size: 2.5 MB (2485193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e6ba98f3318a114eb2dac55f877469e358979cc4df33dc1da3e04d12fed5f76`  
		Last Modified: Fri, 06 Oct 2023 03:09:06 GMT  
		Size: 4.1 MB (4065153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71060edf93e132bd3c6dfea45930629fcf7c8d0b6ab8c54c053df4c09f7cedd7`  
		Last Modified: Fri, 06 Oct 2023 03:09:06 GMT  
		Size: 4.1 MB (4066109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db556f73e17d1827b0f002302f37c7e27a02c0c522f3368dd7eb8e5fa741209b`  
		Last Modified: Fri, 06 Oct 2023 03:09:06 GMT  
		Size: 4.1 MB (4065163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b074ded1a11c1f9e50dd006c8b39a498b7e47a865824e25dc2e9f38fb14896f4`  
		Last Modified: Fri, 06 Oct 2023 03:09:07 GMT  
		Size: 69.0 KB (68950 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:969b612d3bf81f2889a71223fe7bdc9f0613421c59a38145d22385f51491e9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101685453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736a9384d6cfafb128471d95c1825ec21f1b0b04aa87baf0a977b9055d358a73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ARG RELEASE
# Fri, 22 Sep 2023 11:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 22 Sep 2023 11:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 22 Sep 2023 11:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:4e52928c778d7e98d90ccfcaacd039ae1fdde494dfa310adbe229d7051c30918 in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/bash"]
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:53cc531c2e6e7ce32a82e9a21f71c9b4d11b0ccd1ef71c8c9e1493d2ec8969ad`  
		Last Modified: Mon, 25 Sep 2023 10:30:56 GMT  
		Size: 34.6 MB (34564928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97aef48693da5c49679d5202d3230c9570c8d84ce317c5f00bb1f92d8da819c`  
		Last Modified: Tue, 03 Oct 2023 12:32:28 GMT  
		Size: 38.8 MB (38759224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a744c3ecbe384d1aa0b1db751b04465822e8fbf553b1e1d86b664d47a2553e`  
		Last Modified: Tue, 03 Oct 2023 12:32:27 GMT  
		Size: 7.8 MB (7836667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2712640de2c82733c76795d99c98affa55b062cb81e39a9880a7869837061dca`  
		Last Modified: Tue, 03 Oct 2023 12:32:26 GMT  
		Size: 10.7 KB (10675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f765c51a8229ddad07801c2a6e1edae4640f9af1c7d30966a6b4ad7f4b635fed`  
		Last Modified: Tue, 03 Oct 2023 12:32:28 GMT  
		Size: 20.5 MB (20512210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68945de65462365405288c9fdb44f5ff2be308a093c0f31abed33e6bf666ed83`  
		Last Modified: Tue, 03 Oct 2023 12:32:27 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0cb93fe9f3b2b8f45a50376048e3d38ad8c0039fddb72cf78ccc80a4bc1ac2`  
		Last Modified: Tue, 03 Oct 2023 12:32:28 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48d0ad3f94a3bc955cee8bea40762e77087ff9e4e336ec51254264f2ec5ae7`  
		Last Modified: Tue, 03 Oct 2023 12:32:28 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837ae40dda5eb1c62e4740e01f01c92dfada59734bf7532a357ff1f14aa54b28`  
		Last Modified: Tue, 03 Oct 2023 12:32:29 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:277fde91dbcccb8f5f38771ae53e6a482c7e950878adb7785e0acd435bac15e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1902a6bb96d54bd454d240c0dd24182ebf9997e6c632e8a12ec3886292677aa4`

```dockerfile
```

-	Layers:
	-	`sha256:9953b2df0ae85ef0613499696e07131e0170e2dbfa6e5975fb093938728cd8de`  
		Last Modified: Tue, 03 Oct 2023 12:32:26 GMT  
		Size: 2.5 MB (2494539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d56bf940d4d1487c6b4cf0cc2ad7352985b10627504b61bd61a5365db237237`  
		Last Modified: Tue, 03 Oct 2023 12:32:26 GMT  
		Size: 61.4 KB (61394 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:56e33b6a8d73a9cc85d1c5224906768bdf169c74ba76eb3cb6ff019e90b09e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92506148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f00a0a79baa525ecf47a28226cf7d6039c16a495967cde12d24fcf6d76d171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ARG RELEASE
# Fri, 22 Sep 2023 11:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 22 Sep 2023 11:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 22 Sep 2023 11:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:78683f2464233172a7cd0d6adc4c7d9fb3ef05fa67ca22e6fbaca0325496a536 in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/bash"]
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:594ea103c983265390944410c6ac8624359909261a656484e971d00ca0ff8b20`  
		Last Modified: Mon, 25 Sep 2023 10:31:02 GMT  
		Size: 28.0 MB (28024260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e4d4082baa76c3dfc33fca371d62fa0e37cdd8187183d624f9dca9a8d0d5b3`  
		Last Modified: Tue, 03 Oct 2023 14:26:31 GMT  
		Size: 37.4 MB (37420826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45caa6fd2337ca4a7aa09068ffe5ca7e5ab653eff15540e2a031fbcb73617929`  
		Last Modified: Tue, 03 Oct 2023 14:26:29 GMT  
		Size: 6.5 MB (6505062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42b22e0fd34e434b311eb589702ca6141c2adc8dbd6fb702bd25b6b28be8ff7`  
		Last Modified: Tue, 03 Oct 2023 14:26:29 GMT  
		Size: 10.7 KB (10731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927222b9a7e530ea74612afb69f8410164b276f835ff74539a7819992d10e1d3`  
		Last Modified: Tue, 03 Oct 2023 15:05:11 GMT  
		Size: 20.5 MB (20543515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477a93049b826bad4bd252b9f14e016c76fbf18bd305765ce11828cd023883f`  
		Last Modified: Tue, 03 Oct 2023 15:05:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebd5954175fa17871f931a4209e0f2a9c005700e35125d66cd29cc019f9208e`  
		Last Modified: Tue, 03 Oct 2023 15:05:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbc09db40ef9bd1de128f101de3766b1fc7803e16416f65a9e9d6791080d3c3`  
		Last Modified: Tue, 03 Oct 2023 15:05:09 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f096ee2793dafb60947a1d01b2c3eef0392273e346cae7c7bc1e9d140149fe2`  
		Last Modified: Tue, 03 Oct 2023 15:05:10 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0587e3afbc17e1fddb9ef3a37907590e5c832550721087db7255b5d3ca47e28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cc8e9824ecae4dc80e431c7e090c1fdd29f217fdd6704fdb7cc9287bf88892`

```dockerfile
```

-	Layers:
	-	`sha256:2325bdb13ff4421b2df8ce5cf01f0a833582f0caafacc9c4f6b2bbcc2841b175`  
		Last Modified: Tue, 03 Oct 2023 15:05:10 GMT  
		Size: 2.5 MB (2479055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bbfa1a08d7694127642e714f149c86e18cff55e8f74bea058c35af25fb2e51`  
		Last Modified: Tue, 03 Oct 2023 15:05:10 GMT  
		Size: 61.2 KB (61177 bytes)  
		MIME: application/vnd.in-toto+json
