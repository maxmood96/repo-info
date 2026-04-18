## `rabbitmq:4-management`

```console
$ docker pull rabbitmq@sha256:e37bc7e28b50551a5e26892327e8d54afac56a5c3709719e6f3909146f14ea4b
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

### `rabbitmq:4-management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:1a59a679b8479f3fdfbd8affab0bb85083bd3532586e2eddf95b59aade92a5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117611365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1242040efe2a799d7b5199cfeea2b4084e8ef878cb4cadcb7ab8ce231f120eef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:33 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 15 Apr 2026 20:53:33 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 15 Apr 2026 20:53:33 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 15 Apr 2026 20:53:33 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 15 Apr 2026 20:53:33 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:53:33 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 15 Apr 2026 20:53:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 15 Apr 2026 20:53:34 GMT
ENV RABBITMQ_VERSION=4.2.5
# Wed, 15 Apr 2026 20:53:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 15 Apr 2026 20:53:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 15 Apr 2026 20:53:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:53:54 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 15 Apr 2026 20:53:55 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 15 Apr 2026 20:53:55 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 15 Apr 2026 20:53:55 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 15 Apr 2026 20:53:55 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 15 Apr 2026 20:53:55 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:53:55 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 15 Apr 2026 20:53:55 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 15 Apr 2026 20:53:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:53:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:53:55 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 15 Apr 2026 20:53:55 GMT
CMD ["rabbitmq-server"]
# Wed, 15 Apr 2026 21:45:13 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 15 Apr 2026 21:45:23 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 15 Apr 2026 21:45:23 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9994cef22e7d769e5e33648b3f6e1b1e443e3a305b2d2bbf8bdfcb2a1fd7e50`  
		Last Modified: Wed, 15 Apr 2026 20:54:18 GMT  
		Size: 46.3 MB (46300771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4429a0fe7add3e8da4330532f2572b3f1e746a0473f596f7a97bd2285ff10780`  
		Last Modified: Wed, 15 Apr 2026 20:54:16 GMT  
		Size: 9.0 MB (8990322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a792dd200b13a02926e3ebe9bdfb6d16f701a0b607fd0ed0371bb4fed5ceb4`  
		Last Modified: Wed, 15 Apr 2026 20:54:16 GMT  
		Size: 9.7 KB (9666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52adc8b3bc46766fb1133e7d9b87e208dff93827366ab17d2ef31367021fc8c`  
		Last Modified: Wed, 15 Apr 2026 20:54:17 GMT  
		Size: 28.0 MB (27975685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fc1b7cd666d84cad07ae4185ec3164ddcf0c03febc76002f7f79b7a650a48a`  
		Last Modified: Wed, 15 Apr 2026 20:54:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e72957fd500d8778bc0602548f1202c1557f51f252764a5dcc73d95b78d26`  
		Last Modified: Wed, 15 Apr 2026 20:54:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807d9b0a3eea434290eca723cfad9fb276eb3ff20890bb46cfa90c35abe3858d`  
		Last Modified: Wed, 15 Apr 2026 20:54:18 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02683eedbb39012bdce62432134b5af72d37735b98c309332636f4d361033025`  
		Last Modified: Wed, 15 Apr 2026 20:54:19 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce310932f181b06ca2c87ab39747db2c646aab15d7a27575913a29ff4d0dfa5c`  
		Last Modified: Wed, 15 Apr 2026 21:45:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba077858afdd3e02f27beeb6ce425a56b4f06541cf10f1464f765f2dd45c7244`  
		Last Modified: Wed, 15 Apr 2026 21:45:31 GMT  
		Size: 4.6 MB (4599924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3131d0f6666427fd9a574531f82b5c49fa9ef79155f2480710aa30ed80592e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f154f7b6458af755797b2e9531095984be59fdc9b26fa4736ddb55b8d2bdffee`

```dockerfile
```

-	Layers:
	-	`sha256:f27659479734d0945f2f89aa649701e5173b2b378d4875fb4982eb9470334023`  
		Last Modified: Wed, 15 Apr 2026 21:45:31 GMT  
		Size: 2.5 MB (2486697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b2f1b62a8ebf262ff58f2c1a5881ad097bddec72f2f3b99ad6a07f7d9d2bf0`  
		Last Modified: Wed, 15 Apr 2026 21:45:31 GMT  
		Size: 16.3 KB (16268 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:f350e7dc18db00828c762f1b07f7c1b20214f8458ca20a846dc0a4a457627c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95380014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21598d134d5be05e0730bb06c36076f511803f31faaf0cc6c817258ed0ade17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:27 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 15 Apr 2026 20:48:27 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 15 Apr 2026 20:48:27 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 15 Apr 2026 20:48:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 15 Apr 2026 20:48:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:48:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 15 Apr 2026 20:48:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 15 Apr 2026 20:48:29 GMT
ENV RABBITMQ_VERSION=4.2.5
# Wed, 15 Apr 2026 20:48:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 15 Apr 2026 20:48:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 15 Apr 2026 20:48:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:49:45 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 15 Apr 2026 20:49:46 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 15 Apr 2026 20:49:46 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 15 Apr 2026 20:49:46 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 15 Apr 2026 20:49:46 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 15 Apr 2026 20:49:46 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:49:46 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 15 Apr 2026 20:49:46 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 15 Apr 2026 20:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:46 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 15 Apr 2026 20:49:46 GMT
CMD ["rabbitmq-server"]
# Wed, 15 Apr 2026 21:38:42 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 15 Apr 2026 21:38:42 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 15 Apr 2026 21:38:42 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11747c2a31317532383ddfd5e409486ddac81d7d5318a6b8a715608cb8849511`  
		Last Modified: Wed, 15 Apr 2026 20:49:14 GMT  
		Size: 33.3 MB (33324332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ee22005cc1b7f06e2b8e6671cb78ab1fca185d7441e786f1d8d083bfb223a9`  
		Last Modified: Wed, 15 Apr 2026 20:49:13 GMT  
		Size: 7.3 MB (7306836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f0cf7935b0f7db61711f9e05eaf6f4c9109cc707f8d2e691505a6a011dd4ec`  
		Last Modified: Wed, 15 Apr 2026 20:49:13 GMT  
		Size: 9.7 KB (9734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df8bfbaf8b80e21c716f61fb875d2a260363a3c5b9ad5d616fcc0b399e60475`  
		Last Modified: Wed, 15 Apr 2026 20:50:11 GMT  
		Size: 27.9 MB (27877370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fec861a13bc7ebb6c50ae3eea3e81ac83528ee66630761f5af27507a7901c4`  
		Last Modified: Wed, 15 Apr 2026 20:50:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b25aa648fab557e73a733c3460a5843ae84f9cd81005044dce18966be26bce`  
		Last Modified: Wed, 15 Apr 2026 20:50:10 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c36d651425f8613d1ec15ec016993c17bd55d9d5483b592847ebcae888a42d9`  
		Last Modified: Wed, 15 Apr 2026 20:50:10 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02733f8735dcbcd54da8af5acd4f24d1b9da72d7ebea8ca36ab039907ae14cd1`  
		Last Modified: Wed, 15 Apr 2026 20:50:11 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9f7c7691b287a700baccc1decc9adc5b0ccde833ecd90369f065981eb07e88`  
		Last Modified: Wed, 15 Apr 2026 21:38:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b9c0b1772f7cde33cd8fdde728fc3adaffb2df076432de0c78e8dcb86a5f32cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bdb7a41809a3b7fc60c5e870e4bfd9d884bff926a4bd5c95701e0e6a9df25c`

```dockerfile
```

-	Layers:
	-	`sha256:137fc6ae0c68a43b1a8732c562b89e569b64f9b26af86ad8befa279fd1c6e3f0`  
		Last Modified: Wed, 15 Apr 2026 21:38:49 GMT  
		Size: 2.5 MB (2487497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d0a4515b48e5a3f76017008a167d929e95382e427aa06488c587593d1dde03`  
		Last Modified: Wed, 15 Apr 2026 21:38:49 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:3745d34b311ce4dc5e954df170d988c63b6d4bb06aa32375c4a94b42777cd5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115234793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab691815375bbcd44491e2b54bf8fdf4640c56fa583b82275c8cc887345cf43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 15 Apr 2026 20:59:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 15 Apr 2026 20:59:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 15 Apr 2026 20:59:56 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 15 Apr 2026 20:59:56 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:59:56 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 15 Apr 2026 20:59:57 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 15 Apr 2026 20:59:57 GMT
ENV RABBITMQ_VERSION=4.2.5
# Wed, 15 Apr 2026 20:59:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 15 Apr 2026 20:59:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 15 Apr 2026 20:59:57 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:00:21 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 15 Apr 2026 21:00:22 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 15 Apr 2026 21:00:22 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 15 Apr 2026 21:00:22 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 15 Apr 2026 21:00:22 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 15 Apr 2026 21:00:22 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:00:22 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 15 Apr 2026 21:00:22 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 15 Apr 2026 21:00:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:00:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:00:22 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 15 Apr 2026 21:00:22 GMT
CMD ["rabbitmq-server"]
# Wed, 15 Apr 2026 21:57:46 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 15 Apr 2026 21:57:59 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 15 Apr 2026 21:57:59 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378b8e39888afd0dfc939d9c15f076d59fd2408b79c0cc61eb0b518ab370394e`  
		Last Modified: Wed, 15 Apr 2026 21:00:49 GMT  
		Size: 44.4 MB (44387909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6520bc9106107094d71b919d79e5a93589d698bfbd9b395d4b8f3441749c50`  
		Last Modified: Wed, 15 Apr 2026 21:00:47 GMT  
		Size: 9.7 MB (9714865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8836b5dd01504f435d686e6a53ef22ece85cbfcae25b6f3d0025f7e6f4753f`  
		Last Modified: Wed, 15 Apr 2026 21:00:47 GMT  
		Size: 9.6 KB (9617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648274137820505850aa5cfcd44249e6ddf2f4dd5e37a4cf7523c02fa57aa657`  
		Last Modified: Wed, 15 Apr 2026 21:00:48 GMT  
		Size: 27.9 MB (27885156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc65dbf62d3e124da789e4d7acd2e89bceb08c41eeb173fa46101a7664984bc1`  
		Last Modified: Wed, 15 Apr 2026 21:00:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6302c90619e75b245e20461b1fbbc0f43713dcf6a61641d5554cb39b00a331f2`  
		Last Modified: Wed, 15 Apr 2026 21:00:49 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b34dec753714cb856c05eabb9f691ef67a8eb6094dd27375fe17873163ccf`  
		Last Modified: Wed, 15 Apr 2026 21:00:50 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c280c4a1ab00264ba619c9df617428115414efba627bd4e53c423ada45217da5`  
		Last Modified: Wed, 15 Apr 2026 21:00:54 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef0c8a5490d38cf8b1f40e634bbb616b911f93124ed28d8d691ef5bb6915a3b`  
		Last Modified: Wed, 15 Apr 2026 21:58:07 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09987c7a23b48d14d40e195f7dffd6a982db1833866f5adce91aa5342845e20`  
		Last Modified: Wed, 15 Apr 2026 21:58:07 GMT  
		Size: 4.4 MB (4359437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d95c5cf6fea93effecda21f7a69c32bd36608366ba7f1ebf8abeb24b23a95908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cbd3723a6d9871d77a0dd239ce3e350a2d85ddcf3eb3fd81ba67c5d716b84d`

```dockerfile
```

-	Layers:
	-	`sha256:b7c029163138e5c69c1231563740433efc158394835f215cab2a2a9e3d901cfb`  
		Last Modified: Wed, 15 Apr 2026 21:58:07 GMT  
		Size: 2.5 MB (2487757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48a856bd3d372ab23c0365219f74ec92d8312503697e793620feb734a2dad4e`  
		Last Modified: Wed, 15 Apr 2026 21:58:07 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:e76b0bb37d43afa0281ce2c4aff87231906fbb1eed0dbd84fdedd953b594d5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111399158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8840dc98372886a9d1d5525ec402630cf1b6f2c64ddbced0542f3d0d46165e9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:52:11 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 15 Apr 2026 22:52:11 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 15 Apr 2026 22:52:11 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 15 Apr 2026 22:52:12 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 15 Apr 2026 22:52:12 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:52:12 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 15 Apr 2026 22:52:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 15 Apr 2026 22:52:14 GMT
ENV RABBITMQ_VERSION=4.2.5
# Wed, 15 Apr 2026 22:52:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 15 Apr 2026 22:52:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 15 Apr 2026 22:52:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:54:27 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 15 Apr 2026 22:54:29 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 15 Apr 2026 22:54:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 15 Apr 2026 22:54:30 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 15 Apr 2026 22:54:30 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 15 Apr 2026 22:54:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 22:54:30 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 15 Apr 2026 22:54:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 15 Apr 2026 22:54:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:54:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:54:31 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 15 Apr 2026 22:54:31 GMT
CMD ["rabbitmq-server"]
# Thu, 16 Apr 2026 01:52:46 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 16 Apr 2026 01:52:47 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 16 Apr 2026 01:52:47 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72dab2bfdfb55bcc42af3ca4c70d040914ee2f04f1629e5834202261211b789`  
		Last Modified: Wed, 15 Apr 2026 22:53:39 GMT  
		Size: 39.5 MB (39538575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807f8b04d042fb67c4fc94f9e138b99f6dec77b7dc82a8891e23b7cd421e169f`  
		Last Modified: Wed, 15 Apr 2026 22:53:38 GMT  
		Size: 9.6 MB (9599875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0e4560a6a2bc207fad87950ae0b223cee77ddc7cb5a0deb1eca36cae620f34`  
		Last Modified: Wed, 15 Apr 2026 22:53:37 GMT  
		Size: 9.7 KB (9666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56defb0fdc3c2d20e5aac2345d955f9058a297fcadd42b6b0ed693881c329ad2`  
		Last Modified: Wed, 15 Apr 2026 23:00:52 GMT  
		Size: 27.9 MB (27934812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339ceefa92f05d09cfd39afad30fb8c26a94a34099c9caddbb5866fb209c7a4`  
		Last Modified: Wed, 15 Apr 2026 23:00:51 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703d0f7544fb721bf851238bf87d1e341f7b0601cb02926edf26deaab00bb32f`  
		Last Modified: Wed, 15 Apr 2026 23:00:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800e675fac294024f505d3a50000f1d0adb95678511af4d672854e3696e57c4e`  
		Last Modified: Wed, 15 Apr 2026 23:00:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed3c8483a6a9c2c4060185d68f6f6270f43642ef01fc20d25cbedcfd1cb3e69`  
		Last Modified: Wed, 15 Apr 2026 23:00:52 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c212c564cd0a3b76d3c54a20b52b7143f4ff8305d2451a7d3fda336ad35a92`  
		Last Modified: Thu, 16 Apr 2026 01:53:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bd7394df490175f93ab32ccd6adac3974c5beab281b9f2622b3903558d2b5371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d7b5cb0426234e8a2c8a5d46343cd347ef3b1518c3fd35b18dc4089a96f2a5`

```dockerfile
```

-	Layers:
	-	`sha256:8df1680793ef289db44fb470eb52d82b99f16c3ab4c09467bc547a7f703b3c7e`  
		Last Modified: Thu, 16 Apr 2026 01:53:04 GMT  
		Size: 2.5 MB (2491150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca23fa1114efd274248b565510c38afcd9616d2485c5a2ef4c0813e92d25925f`  
		Last Modified: Thu, 16 Apr 2026 01:53:04 GMT  
		Size: 16.3 KB (16310 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:bdbe6f199405c34589e00391380b2c9d490de020fcb47ca772720ceeb6bb8f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104881819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d209241b2390db055412a90843bff9e6f537350b6ccecde866300ca2dc0682`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 22:34:41 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 16 Apr 2026 22:34:41 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 16 Apr 2026 22:34:41 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 16 Apr 2026 22:34:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 16 Apr 2026 22:34:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 22:34:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 16 Apr 2026 22:34:46 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 16 Apr 2026 22:34:46 GMT
ENV RABBITMQ_VERSION=4.2.5
# Thu, 16 Apr 2026 22:34:46 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 16 Apr 2026 22:34:46 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 16 Apr 2026 22:34:46 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:07:57 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 17 Apr 2026 00:08:06 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 17 Apr 2026 00:08:06 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 17 Apr 2026 00:08:06 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 17 Apr 2026 00:08:06 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 17 Apr 2026 00:08:06 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 17 Apr 2026 00:08:06 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 17 Apr 2026 00:08:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 17 Apr 2026 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:08:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:08:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 17 Apr 2026 00:08:06 GMT
CMD ["rabbitmq-server"]
# Sat, 18 Apr 2026 01:58:23 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Sat, 18 Apr 2026 01:58:23 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Sat, 18 Apr 2026 01:58:23 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007dbb664d45ad89dcc5cf1a51d680a7bd71652d98a4cbb86324d5e0fe9eac67`  
		Last Modified: Thu, 16 Apr 2026 22:43:37 GMT  
		Size: 35.2 MB (35179625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e815c1968ccbba87e7965cc21b498d0423c920cd977b0ac3a32b16cd9bb71543`  
		Last Modified: Thu, 16 Apr 2026 22:43:31 GMT  
		Size: 10.8 MB (10836905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f16cb2fd46be90e288a6694bcbaf5d4768fc5005a13e359d3b22ca091529e3b`  
		Last Modified: Thu, 16 Apr 2026 22:43:24 GMT  
		Size: 9.7 KB (9669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83e3bee431dd0655880f5ae1b01452952e7fdc645bc4b49f1e2b8c918d04650`  
		Last Modified: Fri, 17 Apr 2026 00:15:43 GMT  
		Size: 27.9 MB (27888243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1f581bad97e75f71031c7ccc25ee23d8884264083749a67193dbf0fdd40b2c`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7955e6bb8940c2de978e27fa7453d8d68528dbe84bae78f936bb39d287eefc8`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc98ea82b634d888475472beac00427614209574987fe8d24ee3394fe11722`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e287aeee79a3fcc141c316a25c32a05ef95f7bd1ab4f0c161d0c555231c853`  
		Last Modified: Fri, 17 Apr 2026 00:15:40 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdc0cbed1ef01e1824b7410e422a29f7b63a7c2869b3017f328048d018a6f9b`  
		Last Modified: Sat, 18 Apr 2026 01:59:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:faf4d51462c2ea9963d0f93f7db1daa274d65df3565418433ef10f11c471188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce10a928196dc137424b21359a1b6c8d167f72307f7bece7b8725588b4885a09`

```dockerfile
```

-	Layers:
	-	`sha256:6ab0cfb7a6b33fd405cd2ebdb55e3031fa1c62b457f3a943c1ca1af5bb7489e4`  
		Last Modified: Sat, 18 Apr 2026 01:59:42 GMT  
		Size: 2.5 MB (2479064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6169d2d5ebdc2dc4b07520f102f8b6e80e5e56bc71239b454ce548d336ac5fa`  
		Last Modified: Sat, 18 Apr 2026 01:59:42 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:956a0a3c485f627210e61b90b9989d652a5431d0be6dd9fab886e1ac7f8d5f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105124405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aedaa80146577fbfdd91e0314e5d55c6ce6d38f88528b100537373d446185e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:18:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 15 Apr 2026 23:18:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 15 Apr 2026 23:18:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 15 Apr 2026 23:18:57 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 15 Apr 2026 23:18:57 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 23:18:57 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 15 Apr 2026 23:19:01 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 15 Apr 2026 23:19:01 GMT
ENV RABBITMQ_VERSION=4.2.5
# Wed, 15 Apr 2026 23:19:01 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 15 Apr 2026 23:19:01 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 15 Apr 2026 23:19:01 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 23:20:56 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 15 Apr 2026 23:21:03 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 15 Apr 2026 23:21:05 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 15 Apr 2026 23:21:05 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 15 Apr 2026 23:21:05 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 15 Apr 2026 23:21:05 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 23:21:05 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Wed, 15 Apr 2026 23:21:08 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 15 Apr 2026 23:21:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 23:21:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:21:11 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 15 Apr 2026 23:21:11 GMT
CMD ["rabbitmq-server"]
# Thu, 16 Apr 2026 01:09:52 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 16 Apr 2026 01:09:52 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 16 Apr 2026 01:09:52 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ae37f273ed13ce21d880f4a168b47d4dec01628813fe4f85997f2d89c34d47`  
		Last Modified: Wed, 15 Apr 2026 23:22:47 GMT  
		Size: 38.6 MB (38621494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee82d74245fd232697a9bbadab42c90ebe67b5e35294e5aa7e9053c8b5a1a3b`  
		Last Modified: Wed, 15 Apr 2026 23:22:45 GMT  
		Size: 8.6 MB (8621410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53467294f1aa7da1ee749af3155907e26b0d8e613975cde9463d1a0411527443`  
		Last Modified: Wed, 15 Apr 2026 23:22:42 GMT  
		Size: 9.8 KB (9792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8efec3032bc68f24c7aa85010c17f325ea6e1f5bd0fd14ccddedf8fcec664f`  
		Last Modified: Wed, 15 Apr 2026 23:22:46 GMT  
		Size: 28.0 MB (27957506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190d436c55a00b44ef232cf3ef2c802e31720698d11daf291eea313f5b68a723`  
		Last Modified: Wed, 15 Apr 2026 23:22:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d60c2811bd0f613317187b039106af6f4b6248eea7d5abd03bbc18fbfc319d7`  
		Last Modified: Wed, 15 Apr 2026 23:22:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9273da074c3c5b2efaf2d117ffe05d1834ffc72d1bd1dbfb54515332acf8bdc`  
		Last Modified: Wed, 15 Apr 2026 23:22:46 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1235a8acae875b7eee8b2f588c51b56b806cd3cd6d1c8b77d8225aeb86dc64`  
		Last Modified: Wed, 15 Apr 2026 23:22:47 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7661e0167957fd0982170866172b1ec68455baff2c064d0a471e55e5a065b490`  
		Last Modified: Thu, 16 Apr 2026 01:10:03 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ef96de7a55b6066d92d8d456e0852e016a26f5000e6fae05fce9602ae81361c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2505070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f46256179e35fa6a579c9172448558cbf6ccae3231a0563db615c9bb28f833b`

```dockerfile
```

-	Layers:
	-	`sha256:0c4fe5892e2c8704ca7c43d7e1943781857d898d6c5cf31a7631006d43450199`  
		Last Modified: Thu, 16 Apr 2026 01:10:03 GMT  
		Size: 2.5 MB (2488807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:213b5aecb657cfaf02888825a7bb4a82eecde308f84c286cd1d34b2502c78acf`  
		Last Modified: Thu, 16 Apr 2026 01:10:03 GMT  
		Size: 16.3 KB (16263 bytes)  
		MIME: application/vnd.in-toto+json
