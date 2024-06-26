## `rabbitmq:management`

```console
$ docker pull rabbitmq@sha256:402a93c4c3143ac683ea390b1460f9ce5408d3965bb59e95cb761cc78dfb26cc
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

### `rabbitmq:management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:05eb5fe2787ff04b982f4afdd29bd3996e0ce090ad6cc9d7be4ee36456525aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114967459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ec5b263b8edd5488f4897a2151de380b366ce3836a00955189bf34bd5b2ffd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ARG RELEASE
# Thu, 22 Feb 2024 21:58:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.3
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2002039f7c6b76c0f5ec18542bda1eabb801ff24ddc4454e385ee7843555a1dc`  
		Last Modified: Tue, 25 Jun 2024 23:03:37 GMT  
		Size: 46.0 MB (46017251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51928a74aa46ad255fbc9ac41e7d0f79ea05b7d7adea48a73df41b586c544e7b`  
		Last Modified: Tue, 25 Jun 2024 23:03:36 GMT  
		Size: 7.5 MB (7483790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f6b07298e873abb31a118ab638c36ad282e65eeebfbbf3e0cab9780b0c4dd8`  
		Last Modified: Tue, 25 Jun 2024 23:03:36 GMT  
		Size: 10.7 KB (10732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69266ff0da84bb4b5f361b47091c73ff265b75677ed00a6b8bbbcd33273c7bc4`  
		Last Modified: Tue, 25 Jun 2024 23:03:37 GMT  
		Size: 21.6 MB (21588836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7162427828b9669f34e546f3c43fd06f1ed2d91a5ce97b0656d5a18c118298d9`  
		Last Modified: Tue, 25 Jun 2024 23:03:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731e1b720c331f92e9acc44953c36c37c53d19588c131cac4d148bb55f89f6a7`  
		Last Modified: Tue, 25 Jun 2024 23:03:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87fa99f505b59b22705685ffbfd50bf0df855cbea276a310a0a10149d2972a4`  
		Last Modified: Tue, 25 Jun 2024 23:03:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a028596922473fd855a78ea5fa21b4885dc278d4afbd8bf121a325e93e68bfd`  
		Last Modified: Tue, 25 Jun 2024 23:03:38 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476d794a39448bb2c9f6ecd61751c5732938a838d56aa173f1e1025b6f29bb31`  
		Last Modified: Tue, 25 Jun 2024 23:55:52 GMT  
		Size: 10.3 MB (10331349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:02fa60cc34be462e25fd589a330ea8459c7d65cd029d7d1577b4dbaf82f34e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3438172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955aa6a0137affad0cfd1db38316077bade018f364d2d07d001545662ede2583`

```dockerfile
```

-	Layers:
	-	`sha256:f6ba3bc79057ce92e20015afa62c1e3bdf3bd8785618e59239f6d9c5707edbe8`  
		Last Modified: Tue, 25 Jun 2024 23:55:52 GMT  
		Size: 3.4 MB (3426796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1577c39b2e5a18da11ada68152725f5d7bcc08f38bde859bdb247fcbbb735a9c`  
		Last Modified: Tue, 25 Jun 2024 23:55:51 GMT  
		Size: 11.4 KB (11376 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:1ffc944f262f59c19347a0654c7a0034d48981fa7790dbd6eabdefae826c61cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97202392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6cdd008582d39d0004cef7e209ae6c99f0688558eb618a4cffe037c99a6d17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ARG RELEASE
# Thu, 22 Feb 2024 21:58:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.3
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a7d6949ac966fed9a061428466d68cc616d739583d012661c3c826f017b64981`  
		Last Modified: Mon, 03 Jun 2024 10:46:59 GMT  
		Size: 26.6 MB (26639042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0bdbc0f25bbff55e48c20545ce8a89e2e6f95a0cc8f14c22f246a6e751fd1a`  
		Last Modified: Tue, 25 Jun 2024 23:04:50 GMT  
		Size: 33.5 MB (33497519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128651c0c62d865026b4eb74ab2d2902682ecdbce8f6163254b22ecae2d0ca73`  
		Last Modified: Tue, 25 Jun 2024 23:04:49 GMT  
		Size: 6.1 MB (6077330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18843e16fc6203359a16eafc4f87f06c89cea9ece57e48f089bae1d1689977e4`  
		Last Modified: Tue, 25 Jun 2024 23:04:48 GMT  
		Size: 10.7 KB (10727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4ed1110b7aeb8e7bb835777b1515ac5393d5866475eefbec429045435ac9d8`  
		Last Modified: Tue, 25 Jun 2024 23:04:50 GMT  
		Size: 21.5 MB (21505508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22332bb790935d767f5148e6b08559b49dbe383c75750cb39cf2e6cb0e624cf`  
		Last Modified: Tue, 25 Jun 2024 23:04:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96643ba31553100cdf17d6222d9a794af376aa4fde09bffee8340df548336c`  
		Last Modified: Tue, 25 Jun 2024 23:04:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f7e6161de83b06e421c1a6f4654d49b4c52b3c7687e8be987d0b2627615149`  
		Last Modified: Tue, 25 Jun 2024 23:04:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dd5bf910dfb4a2cc67c369a1573b64ae21e6b31599e914e48672ea524748e2`  
		Last Modified: Tue, 25 Jun 2024 23:04:51 GMT  
		Size: 837.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d19bf67447d6fbb634d644d242fb88a1cc03db668963d55fcd5baad818ecaa3`  
		Last Modified: Tue, 25 Jun 2024 23:56:06 GMT  
		Size: 9.5 MB (9470513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a7c2091d40b401cb04509fd075b292c40c08d08a8b424945120deffc7e085480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3439072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637e5403ea3eb603abe1b3b6c433509a496487d92b5526205c2eae0173bbeee6`

```dockerfile
```

-	Layers:
	-	`sha256:b3aadcef956545be00a45e48a984299f52eb98885fc5d28472bac4dfda8aaa4c`  
		Last Modified: Tue, 25 Jun 2024 23:56:05 GMT  
		Size: 3.4 MB (3427621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182edb5fc268cf1bca474fae3b0a2f526436d0da3386fb276c7ed4d188495da3`  
		Last Modified: Tue, 25 Jun 2024 23:56:05 GMT  
		Size: 11.5 KB (11451 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:d9d86d2917f8df3d958b007f40e2f8a022ec5caf0e687d40dce513a97d4bed8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110444171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9715abd34c6716a85ebdde05d332230fd7d00f2130e6bfbffa53f199a89fb78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ARG RELEASE
# Thu, 22 Feb 2024 21:58:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.3
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2b1204d9b12b9f62d4682ff4efee5af710284e24e1f1baa40e7bad3b682cdb`  
		Last Modified: Tue, 25 Jun 2024 23:45:04 GMT  
		Size: 44.1 MB (44089614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daee8a9aeba9da7a2fd0d784def0fb7c42651747035efd6347c696ea19b4edb`  
		Last Modified: Tue, 25 Jun 2024 23:45:04 GMT  
		Size: 7.1 MB (7133053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c991c043aefce68d753e0ea072540011395ac45e7f53de6cff1e9f472cd5285`  
		Last Modified: Tue, 25 Jun 2024 23:45:03 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07723356596b6a1ed649c231dcb864ffc0af5857c4c61f1bb0947483a8fe5422`  
		Last Modified: Tue, 25 Jun 2024 23:45:04 GMT  
		Size: 21.5 MB (21497625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a8239c56915f0fc309ef4111e8411322134b9640552f0781d42eb0ee7fe045`  
		Last Modified: Tue, 25 Jun 2024 23:45:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeb679ae401c3eebcea0b6c08d04f0f0069a8e2c293f27741999b71a59f584b`  
		Last Modified: Tue, 25 Jun 2024 23:45:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0176b5a5df08f0be43768b5ed264f0c06d0e541f5f289701a95f897f9b7ff2c`  
		Last Modified: Tue, 25 Jun 2024 23:45:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43185b159d4041f3aafe2adbbf05abb4f62e305c2df5af6ba576856214589b70`  
		Last Modified: Tue, 25 Jun 2024 23:45:06 GMT  
		Size: 837.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4969ae367d27596a23e0fb71cef50d35f30546338addee68aa3a1e2eceee16`  
		Last Modified: Wed, 26 Jun 2024 01:04:23 GMT  
		Size: 10.3 MB (10349620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c3f82d781062d765d5aa351665c0825e02aeb34497021a854eff92066cc19fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3438882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19384b48618e3f5fde18f6b117311628cde48084a2d7f26f27f733592907702c`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a6977072da0028650cc73917ad99659edb23b1e1bd2242fe5ea15468b504e`  
		Last Modified: Wed, 26 Jun 2024 01:04:22 GMT  
		Size: 3.4 MB (3427122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f701a04b570dce6bc0f4da7d1dce56f3425fca0b0ccfdfad688661e3efea2dc`  
		Last Modified: Wed, 26 Jun 2024 01:04:21 GMT  
		Size: 11.8 KB (11760 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:0e4578cefe8516a371e45ac3bc6f2a318bd3c1db4254945754f94a8848a17576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114152717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce8d0e2d325e35a5de695dd736d5118b6eed1b402206b63c7092a918f593501`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ARG RELEASE
# Thu, 22 Feb 2024 21:58:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.3
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deec3610e9ad9c05027c70af709de3b62ae7dbd66d9de250755c4223ede124a`  
		Last Modified: Tue, 25 Jun 2024 23:59:49 GMT  
		Size: 39.6 MB (39598590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf047dd3c552c3a917481a315f6e6a97a6545462e12ee35e17987f8c788449b`  
		Last Modified: Tue, 25 Jun 2024 23:59:49 GMT  
		Size: 7.9 MB (7868577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce20e921a25832c8a72769e6474c978ccda2634211056dd75e3ab6b599970f7`  
		Last Modified: Tue, 25 Jun 2024 23:59:47 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82f6d80c078b57e6132bc1870d685b241a02d3dd64fe4233067df3489373453`  
		Last Modified: Tue, 25 Jun 2024 23:59:49 GMT  
		Size: 21.5 MB (21523752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca2f46fc876e43476b0a9336a1c455aec66061eeeb995b640cda4d98f4fe73`  
		Last Modified: Tue, 25 Jun 2024 23:59:49 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0ee135df3e4fb751ee5ca218b57b856713c8f20002675308a60cd1e79278c`  
		Last Modified: Tue, 25 Jun 2024 23:59:50 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0263818dbb16b9c02e7fac6ce5dbcdca04eebd7ad80335d2eb67b1e31311ff1`  
		Last Modified: Tue, 25 Jun 2024 23:59:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef1234b67889e4810a5de9f327bcce5b7dbe0e40a2779d729a6fc0a8b854f77`  
		Last Modified: Tue, 25 Jun 2024 23:59:51 GMT  
		Size: 836.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b303fda7948630805fa8c02117641bece30f5d263cead7a58593b1403279431`  
		Last Modified: Wed, 26 Jun 2024 05:08:46 GMT  
		Size: 10.7 MB (10688700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a1b67ae32ec2cee8cc38bd7150361720d74162fe903e9af7222f4d8b1803a289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3442258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7a9967dbac82cb564bebfd3e4c42a460bf5a579b2e19aca0af3b720d437149`

```dockerfile
```

-	Layers:
	-	`sha256:5f330f5e8f3d9af0239d252669014538d4431cef25cfa5beb49d9c1f38505cfd`  
		Last Modified: Wed, 26 Jun 2024 05:08:45 GMT  
		Size: 3.4 MB (3430839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c998e91723233253d2d4898005a0ba42f6582cf7e4ab416ce9b587264c935b`  
		Last Modified: Wed, 26 Jun 2024 05:08:44 GMT  
		Size: 11.4 KB (11419 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:6d2fea4a1bc4983a3c4df8e489b366a0c81b2a4b56da0a03cc1193a4a8e21f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104535173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaf5acad3d7b1f27ac7a66dc5603967129256ad1895dea09e219d97025cde68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 22 Feb 2024 21:58:15 GMT
ARG RELEASE
# Thu, 22 Feb 2024 21:58:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 21:58:15 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 21:58:15 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Feb 2024 21:58:15 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_VERSION=3.13.3
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Feb 2024 21:58:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Feb 2024 21:58:15 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Feb 2024 21:58:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Feb 2024 21:58:15 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Feb 2024 21:58:15 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Feb 2024 21:58:15 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 22 Feb 2024 21:58:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5c5d18337ca1a058f08644def5e9a808cce5fbd31d9506f5d195ed6c2a3cd2`  
		Last Modified: Tue, 25 Jun 2024 23:37:20 GMT  
		Size: 38.2 MB (38235546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834ca69b596f66628731ce49a7f9dc4ea88b5c4495120776cf76364e9dcb64e0`  
		Last Modified: Tue, 25 Jun 2024 23:37:19 GMT  
		Size: 6.5 MB (6535470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfce93ff6db040c85af0198be55cebb63abad3272f920ed96b909c690daf4af`  
		Last Modified: Tue, 25 Jun 2024 23:37:19 GMT  
		Size: 10.8 KB (10767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eb3d5ad307852694eed76f3ce3379e41fd3624b5c59bdaedbc4b8599b707c0`  
		Last Modified: Tue, 25 Jun 2024 23:37:20 GMT  
		Size: 21.6 MB (21556982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37828c38f354f89dc43a069d3f5822ddc17d499702b5ae6d6daeef8eb730c09a`  
		Last Modified: Tue, 25 Jun 2024 23:37:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710138391f67412c475a2e6b7c8e35502d75a2fdb1d108cf34c8968a39608cd6`  
		Last Modified: Tue, 25 Jun 2024 23:37:20 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a214976ffbfbacbd36533ed2eaf78bdb1ae2024548130ad1e3a3a68c5a5a4`  
		Last Modified: Tue, 25 Jun 2024 23:37:21 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0febc37627ef32df570a2066cfa87cfffa01011cac1a80fc9355f79924b70d45`  
		Last Modified: Tue, 25 Jun 2024 23:37:21 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eb70283e993d5849a69efba9acc47f4671f710331f1cef960405875daafa54`  
		Last Modified: Wed, 26 Jun 2024 00:19:05 GMT  
		Size: 10.2 MB (10194137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0bcbd4047e8c42d741e0ac6f1190feeaa76e6c0160f1011efee74bfee29f9eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3439725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60509a1594d1f031d131ea2aba7c165445e1a0304ee494fbde04f15efd2f4a9a`

```dockerfile
```

-	Layers:
	-	`sha256:b24f27c48480ba2a2409cb2762e8a481b0e39fdea6d316d42c273b5f14d90da9`  
		Last Modified: Wed, 26 Jun 2024 00:19:05 GMT  
		Size: 3.4 MB (3428349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91c47404dccdd3ff69d625827273fb422938f2cfe682aa0c764506545ffef0bc`  
		Last Modified: Wed, 26 Jun 2024 00:19:05 GMT  
		Size: 11.4 KB (11376 bytes)  
		MIME: application/vnd.in-toto+json
