## `rabbitmq:management`

```console
$ docker pull rabbitmq@sha256:6431bbd0f22df99ace800138399367d7d6181442dfff09feb2795e15d4bd4b7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:21d7d22bf8a177072637779fd425f6bdfc550d617056a67d00c8db817676bfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125291269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4844207e9656c5f96293d4657b231d72b2258bf9892f6cc5b8e3205c1d26a388`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 17:29:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:29:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:29:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:29:45 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:29:45 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:29:45 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:29:46 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 14 Nov 2025 17:29:46 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 17:29:46 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:29:46 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:29:46 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:30:03 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 17:30:04 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 17:30:04 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 17:30:04 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:30:04 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 17:30:04 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 17:30:04 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 17:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:30:05 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 17:30:05 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 17:48:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 17:48:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2760f0fd5db3da1af6be68f4c2b4ca2a50ef9e587af3681b8e99dd638b4a7e7f`  
		Last Modified: Fri, 14 Nov 2025 17:31:06 GMT  
		Size: 46.3 MB (46261402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c184a31dffdfcf71b5282cb9bf6ee5780721f72f266b9b70888bdce38c33cba`  
		Last Modified: Fri, 14 Nov 2025 17:31:02 GMT  
		Size: 9.0 MB (8994548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9b8a16985f5cd81c03c80789d2197c2b4f86ba11764d1e7237011aa0a0fe8`  
		Last Modified: Fri, 14 Nov 2025 17:31:01 GMT  
		Size: 9.7 KB (9686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623da80641076621ba0ac480e30163b1fe23a33b1a8b753911fcbd772e46bf04`  
		Last Modified: Fri, 14 Nov 2025 17:31:05 GMT  
		Size: 27.8 MB (27829755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a7293aef563a0479c77ca95a6f34aa5a88dfc395b5f0abfe21b1eae1b4b6dd`  
		Last Modified: Fri, 14 Nov 2025 17:31:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e66df75ee2648c48cb25fbeec7692ca9ef39a8dfd8d89d99b1bef61644e12`  
		Last Modified: Fri, 14 Nov 2025 17:31:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea4e69ba5ae6c7d8db64d6fa5f885c6cf0de251623f7fa9efc795232b39e92`  
		Last Modified: Fri, 14 Nov 2025 17:31:01 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa37f9ae475395edc22efeff6d9d68f734ad13a803d67b76151918b92f323341`  
		Last Modified: Fri, 14 Nov 2025 17:31:01 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ef2592078664486f7a45585add6f81d4a8249c10a04d615643e25d2aaf3231`  
		Last Modified: Fri, 14 Nov 2025 17:48:25 GMT  
		Size: 12.5 MB (12469440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2d5387a8487b4f5fb50125382f562ed994933798a834ec72744519f40caeb9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3110238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4540f48988a625a76ea49f6fc7b80fe35da3fce149fec15b4b470982c37fe88e`

```dockerfile
```

-	Layers:
	-	`sha256:a24e66f073a8850dc3ed5d1a671c0b34af9f19c1c7d8745cfa8a2441c49a05c0`  
		Last Modified: Fri, 14 Nov 2025 19:53:29 GMT  
		Size: 3.1 MB (3098881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5cc0c74f85e713ca62dfc843de152847cc2f4af0241463391107dc849af1c24`  
		Last Modified: Fri, 14 Nov 2025 19:53:29 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:eaccddb37472da575d26c8859ae36c825cca52abc2567d90b9a9d386cc4ac324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106683361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a23039f334c8fcde06807fe2cca08ce850d68ca857989585faf207fd01bd8cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:17 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:17 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:20 GMT
ADD file:dd3740083ecd2e2b1e178f1771ef73043bc7be6c831492453a755b873d8b531b in / 
# Thu, 16 Oct 2025 19:25:21 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 17:31:18 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:31:18 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:31:18 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:31:18 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:31:18 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:31:18 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:31:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 14 Nov 2025 17:31:20 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 17:31:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:31:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:31:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:31:45 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 17:31:46 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 17:31:46 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 17:31:46 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:31:46 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 17:31:46 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 17:31:46 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 17:31:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:31:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:31:46 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 17:31:46 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 17:45:48 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 17:45:48 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:6cdc0abf996c3192bfbda4018d34c282871d4be33fb369176002cb2199673adf`  
		Last Modified: Fri, 17 Oct 2025 08:06:35 GMT  
		Size: 26.9 MB (26852672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8623e59ffbdbdb7944c7e809476350f45b3abc57f3d7f0876cc02f942bdfa9cd`  
		Last Modified: Fri, 14 Nov 2025 17:32:25 GMT  
		Size: 33.3 MB (33295235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f606f0289758ef3b7f7e3af0a504ca2352b914a0d4747212529ba8c55006afd4`  
		Last Modified: Fri, 14 Nov 2025 17:32:22 GMT  
		Size: 7.3 MB (7309038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4338adcebcd498c54c5ddd23c2d29bb483e2c148d64917443d142b238f85126a`  
		Last Modified: Fri, 14 Nov 2025 17:32:22 GMT  
		Size: 9.7 KB (9743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38076be7b7b976ae1eba9c5a9fdf8636be8b60a62a6d60c63e09ddfe164b0268`  
		Last Modified: Fri, 14 Nov 2025 17:32:26 GMT  
		Size: 27.7 MB (27731347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f30af7c334f61344effe645288c947cfb43d6d7b8b524614236fdc093190521`  
		Last Modified: Fri, 14 Nov 2025 17:32:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b80cbbc0423b5f4186b5c2af1546adc539a2f1ebbd9746721593e434d68295`  
		Last Modified: Fri, 14 Nov 2025 17:32:22 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057a9091f9523871fca618ea2ae28c85b3698376b96fc9b5fdac21c5dd97d48b`  
		Last Modified: Fri, 14 Nov 2025 17:32:22 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30322dbec18930f83fdb1ebfdfcaaf122d91ccdaf8335130fd8abbdfcc5f72a4`  
		Last Modified: Fri, 14 Nov 2025 17:32:22 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab3e844d4dd9060a543200ab2697781ce275d9af61bebfb7d7767c9635c4ca2`  
		Last Modified: Fri, 14 Nov 2025 17:46:04 GMT  
		Size: 11.5 MB (11483578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:47d97212a538f7e9d33836a79c7543b4ae21354b5544b13a39f73b9e2f9942d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3111275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6108bd59088174dcf939b01f6706d50aa7cab0c00ef347e32cc63745308bc46b`

```dockerfile
```

-	Layers:
	-	`sha256:ca1e64e672bd12c57efa2c781bdc5def7913c68ade9aab468b2bf570ed98592a`  
		Last Modified: Fri, 14 Nov 2025 19:53:34 GMT  
		Size: 3.1 MB (3099837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e782d6806d9fe0caf473a7ac87f42be45d768b3001c307f9dae38a1001d1acb0`  
		Last Modified: Fri, 14 Nov 2025 19:53:34 GMT  
		Size: 11.4 KB (11438 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:9f00c6e66b63ff8af03ced3644c28a68e67bfc224401469534fe1f6871bcf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123015580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f86f19649d7a6e132e26f2d623da6fe9e22d090431f2d1935caf93bfc3fe66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 17:29:59 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:29:59 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:29:59 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:29:59 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:29:59 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:29:59 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:30:00 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 14 Nov 2025 17:30:00 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 17:30:00 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:30:00 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:30:00 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:30:23 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 17:30:24 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 17:30:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 17:30:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:30:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 17:30:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 17:30:24 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 17:30:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:30:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:30:24 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 17:30:24 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 17:47:29 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 17:47:29 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3562962342b162dea5dd0c0111f603c9b2320c93a5a071f9cf20c0d753af751f`  
		Last Modified: Fri, 14 Nov 2025 17:31:34 GMT  
		Size: 44.4 MB (44355573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8428284b1251b825707a89bf9ba191ab08bca2d236fd8a6f9d049654083dd792`  
		Last Modified: Fri, 14 Nov 2025 17:31:31 GMT  
		Size: 9.7 MB (9716287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead5c64215ad3dd4a57c9e8a8dce03ef2d6d40bcb3d1bc9a330bd3a62f9d0340`  
		Last Modified: Fri, 14 Nov 2025 17:31:30 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0418ded1a7c9828409e2859a6aac58cfcb9c7d5d609788d4cdfd078b703b3e6`  
		Last Modified: Fri, 14 Nov 2025 17:31:32 GMT  
		Size: 27.7 MB (27738782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc16d1172522978604450140676ae292fe65360c922dc184f3fb6cff057f913d`  
		Last Modified: Fri, 14 Nov 2025 17:31:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9594f6e3c36e804a60a922e193fa8e32471fea9d4b14411b6af3f28187daf6`  
		Last Modified: Fri, 14 Nov 2025 17:31:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202ce16244b5526a96afe769aa10abd63f274feb04211eaed5b5673180c24c28`  
		Last Modified: Fri, 14 Nov 2025 17:31:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bf358c39cbfaf126187a7626e3065deeed5ecebc39eac3870f3b80b47db153`  
		Last Modified: Fri, 14 Nov 2025 17:31:30 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2aa92cfd3756887a507bd919c1fdfab37375875e97d91edc52552482c75149`  
		Last Modified: Fri, 14 Nov 2025 17:47:46 GMT  
		Size: 12.3 MB (12331562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0120a917bdb315257b77aa97a608f92d4a771620ce857471fd0062ca3ece15bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3111455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2b5dbeb9c835e17b1c1aace62cd15d7f785f07894d764992489afd22d2c1d8`

```dockerfile
```

-	Layers:
	-	`sha256:9d51fe3c63d061181e1e2d2a2db7fe6cdeea421c5affd7526831453f84dfbf1d`  
		Last Modified: Fri, 14 Nov 2025 19:53:39 GMT  
		Size: 3.1 MB (3099993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da02edf6cdf90898a786f1898fe4ab3e2245d2937fd5ebafcc2bba7e1efc1424`  
		Last Modified: Fri, 14 Nov 2025 19:53:39 GMT  
		Size: 11.5 KB (11462 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:6f140ca0fc5b5f3724d455f84f053d79f2c77fd16e33402d89227d0eb94a19b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124179386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3310f3f051e071e77446596357940a7d32366098e29a7fa76eba23a747a8f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 19:13:02 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 19:13:02 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 19:13:02 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 19:13:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 19:13:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 19:13:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 19:13:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 14 Nov 2025 19:13:13 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 19:13:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 19:13:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 19:13:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 19:13:53 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 19:13:56 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 19:13:56 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 19:13:56 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 19:13:56 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 19:13:56 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 19:13:57 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 19:13:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:13:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:13:57 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 19:13:57 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 20:10:33 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 20:10:33 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aca544a4c75276e59b4240a78ef3e6b84b3ff47d98f91017896374d7904778`  
		Last Modified: Fri, 14 Nov 2025 19:15:28 GMT  
		Size: 39.5 MB (39509671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c3605c27538c6ca4cb7e43022bbad01ce80ad26cc9b1435768014a94927828`  
		Last Modified: Fri, 14 Nov 2025 19:15:24 GMT  
		Size: 9.6 MB (9598405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79e6621a2b18898e95def5a9fcbd0740f40e098b840e4bc7aaac4e5c5859eef`  
		Last Modified: Fri, 14 Nov 2025 19:15:23 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f435b125c7b8daac4f80cc28626bebf7998fe65a0da7f4ddccec74b6a6035069`  
		Last Modified: Fri, 14 Nov 2025 19:15:26 GMT  
		Size: 27.8 MB (27790213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa43db6149d61c0f97f182d03367bdc837b9a9a7b2c5525b9711f23a636cf2c`  
		Last Modified: Fri, 14 Nov 2025 19:15:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5e8c55ab75440365848c1ed76f32405aeb4ad5162c361d420561eed1f32de6`  
		Last Modified: Fri, 14 Nov 2025 19:15:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c43e655a0517e787f95ae411ca328d3c151cb5388578ede0d6d97ccca1d93fc`  
		Last Modified: Fri, 14 Nov 2025 19:15:23 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d519d9b85cf32c56c678798212868c1e24f8df5bebcaf2aa1cad814c28f28ad1`  
		Last Modified: Fri, 14 Nov 2025 19:15:23 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbc14dd88ccdbdf2a01f937f5ad1df7acf6f04c55de1e37188e8de56fd83643`  
		Last Modified: Fri, 14 Nov 2025 20:11:05 GMT  
		Size: 13.0 MB (12965295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f6ce7dbe26c4a5f283ceaca1d51835476ac88e3c24a346fba17ff087266d3b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3115019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b3edaf15828547fed55dca41088dec9aabed9636099ff3b3474be17715ecff`

```dockerfile
```

-	Layers:
	-	`sha256:5593006684f00aac6a289e81c0e5b1f4edbb4f2882c78673452764f89d19edfa`  
		Last Modified: Fri, 14 Nov 2025 22:53:01 GMT  
		Size: 3.1 MB (3103618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854f7d78b27b0f46cc24c0e4d164f526cb9bab316f75c4e8bcf1dfb926f95ef4`  
		Last Modified: Fri, 14 Nov 2025 22:53:02 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:ef1801951e536d5093e0ab2e8639d20e9f768fbcb7740a1bed4ee03755a2560a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117020573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8925e8889dc661a9fa964c504f009538458de07da4d5e11445580f9b6d53a1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:53:04 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:53:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:53:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:53:05 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:53:45 GMT
ADD file:6c2a12ec42d9e6c7e02041a8483a3a93ab9b91131ca66ecb93506ba161a4909d in / 
# Thu, 16 Oct 2025 19:53:49 GMT
CMD ["/bin/bash"]
# Sat, 15 Nov 2025 14:46:31 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 15 Nov 2025 14:46:31 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 15 Nov 2025 14:46:31 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 15 Nov 2025 14:46:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 15 Nov 2025 14:46:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 14:46:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 15 Nov 2025 14:46:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 15 Nov 2025 14:46:36 GMT
ENV RABBITMQ_VERSION=4.2.0
# Sat, 15 Nov 2025 14:46:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 15 Nov 2025 14:46:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 15 Nov 2025 14:46:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 14:48:47 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 15 Nov 2025 14:48:56 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 15 Nov 2025 14:48:56 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 15 Nov 2025 14:48:56 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 15 Nov 2025 14:48:56 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 15 Nov 2025 14:48:56 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 15 Nov 2025 14:48:56 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 15 Nov 2025 14:48:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 14:48:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 14:48:56 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 15 Nov 2025 14:48:56 GMT
CMD ["rabbitmq-server"]
# Sat, 15 Nov 2025 19:38:58 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Sat, 15 Nov 2025 19:38:58 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4f36e1b0a2cc427e5979b49608ef4e52795313f083fdc941cab616d5ab2b861b`  
		Last Modified: Sat, 15 Nov 2025 10:03:37 GMT  
		Size: 31.0 MB (30952148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606650a61dbbc93efe83db6c01f31098ae14abd4834968121b22948aa3594218`  
		Last Modified: Sat, 15 Nov 2025 14:55:42 GMT  
		Size: 35.1 MB (35148108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894681447bb26bf478bea3393756ebd369dbe3c51970e4acdedc0b1d8f9876e8`  
		Last Modified: Sat, 15 Nov 2025 14:55:39 GMT  
		Size: 10.8 MB (10831054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ace5028ea6ad662e89ea950028a3569eea4433bdf62c87e8ce84d58b6133cc`  
		Last Modified: Sat, 15 Nov 2025 14:55:38 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110dd21cb3cb1a8a3ab579a93df301083dfeca83ec65108f6c4af3c770bbc37e`  
		Last Modified: Sat, 15 Nov 2025 14:55:41 GMT  
		Size: 27.7 MB (27742692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8a91204b386493268efcf737c6c90ccdeffb3deddb160e53780fc42339faa`  
		Last Modified: Sat, 15 Nov 2025 14:55:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214e07473aea72005cc73c1e350dc25b487559dc27e4abed21285709167e8f49`  
		Last Modified: Sat, 15 Nov 2025 14:55:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16f81928dd84d68b234dc52bede6a86beca95f9b3b64801cff64b44a4482a0b`  
		Last Modified: Sat, 15 Nov 2025 14:55:39 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948b66cab75aed92cda7987774651319d24f14442a11e14b1ec7136497123849`  
		Last Modified: Sat, 15 Nov 2025 14:55:39 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2863933c889b81326a973e16a6b9c43478887e2881b8d854ef714cafb9bcddf`  
		Last Modified: Sat, 15 Nov 2025 19:40:54 GMT  
		Size: 12.3 MB (12335148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:793c4cb18668072e9035a4d56b496c99a1b38198decda7ba520a757b1a4489cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3102728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ed980b8e399b7b160c3f5fb8c7b7997a362c5263dc24fff00170829b8a0002`

```dockerfile
```

-	Layers:
	-	`sha256:4f2eca2657609d27863bae2baa753f1ec8efc9e77826e4509f726b2d5c3c4690`  
		Last Modified: Sat, 15 Nov 2025 22:52:56 GMT  
		Size: 3.1 MB (3091324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8723cedab44315cd1fa9ccd0df766092e3e2b031da646b77988fc9e9193d540`  
		Last Modified: Sat, 15 Nov 2025 22:52:57 GMT  
		Size: 11.4 KB (11404 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:36380fc6c2892a38e19aab93ec73708f0b7ed72c0ee0f18c006fe0923138073c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117616410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c33eef9536c0a4538f5efbbe3c764bd375b9f2d17f7cf03b153d8dc827dcad4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:14 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:16 GMT
ADD file:f7335d462150d31c3c91b13ccd3e927bc9a1b9c6664fa8905ccf68bbe3d86cd3 in / 
# Thu, 16 Oct 2025 19:25:16 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 17:32:37 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 14 Nov 2025 17:32:37 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 14 Nov 2025 17:32:37 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 14 Nov 2025 17:32:37 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 14 Nov 2025 17:32:37 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:32:37 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:32:38 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 14 Nov 2025 17:32:38 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 14 Nov 2025 17:32:38 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 14 Nov 2025 17:32:38 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 14 Nov 2025 17:32:38 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 17:32:52 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 14 Nov 2025 17:32:53 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 14 Nov 2025 17:32:53 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 14 Nov 2025 17:32:53 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 14 Nov 2025 17:32:53 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 14 Nov 2025 17:32:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 14 Nov 2025 17:32:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 14 Nov 2025 17:32:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:32:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 14 Nov 2025 17:32:54 GMT
CMD ["rabbitmq-server"]
# Fri, 14 Nov 2025 18:00:18 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 14 Nov 2025 18:00:18 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becfaa46b24ce0d23e3b38f61afed95e4e32f74c45305bc6851131fe06112c14`  
		Last Modified: Fri, 14 Nov 2025 17:33:36 GMT  
		Size: 38.6 MB (38581223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8fbc3d039beb8621ada316e309eeee4b477db2d477f9e64a78a5ded784081a`  
		Last Modified: Fri, 14 Nov 2025 17:33:34 GMT  
		Size: 8.6 MB (8623275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38c9640e22f4e110edbf01a64d8ee92a2f6fc7818e530a67a6e464570ee5abb`  
		Last Modified: Fri, 14 Nov 2025 17:33:33 GMT  
		Size: 9.8 KB (9809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75680dd23f21730db649a5772693cee8b91ee898ee8963042aea28d505e2e577`  
		Last Modified: Fri, 14 Nov 2025 17:33:37 GMT  
		Size: 27.8 MB (27812994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf7a61e94cbd8d1197ddbfc20069ad41040ed6dc396b072ca1afdd5a4a1f43b`  
		Last Modified: Fri, 14 Nov 2025 17:33:33 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a3b2aa1727153da888ca537e815e9487f911c6a1f57af1b53371f655044f7b`  
		Last Modified: Fri, 14 Nov 2025 17:33:33 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fea6dc36a204a4449b8ef6b76ac38223042385563cdb5a9d046bd010623191`  
		Last Modified: Fri, 14 Nov 2025 17:33:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508f3106f63387e03facfb978aef392425848d257c9938a476d2fd5749a23c1d`  
		Last Modified: Fri, 14 Nov 2025 17:33:33 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7dd2792cf5dd0f11c4cc262fc4c2709648f0e7a09a4415d279758258c56468`  
		Last Modified: Fri, 14 Nov 2025 18:00:44 GMT  
		Size: 12.7 MB (12679765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2a196279491ef6b77334b87aac1773049139761b7d90a540ff5fb03b0a1296ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3112297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf464ab01a107d7aaa3e43139837ea71d5685b69934b4c08dab5d0d4b6974c1d`

```dockerfile
```

-	Layers:
	-	`sha256:af4f6591d9fdbc4c7d539aae5fcb78e65cadd736faaa3d3dd3fbeecf641a90e1`  
		Last Modified: Fri, 14 Nov 2025 19:53:50 GMT  
		Size: 3.1 MB (3100939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388ed7c82c8fdce740282f82c24dea5a7ca39959ac0f9fd9deb296f184fe2c8b`  
		Last Modified: Fri, 14 Nov 2025 19:53:50 GMT  
		Size: 11.4 KB (11358 bytes)  
		MIME: application/vnd.in-toto+json
