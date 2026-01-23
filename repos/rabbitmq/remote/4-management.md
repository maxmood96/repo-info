## `rabbitmq:4-management`

```console
$ docker pull rabbitmq@sha256:de5e4499e76421415329f6cf960debeaeda530a4060c9295350a17274afc44e1
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
$ docker pull rabbitmq@sha256:d0c13625657b00dcfac95a85deac7fbfe73df6020c933537c799cb62a9da5e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117822360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cc5aaef01949b2e1b2898a40af4a94196ffd89ecb1b6f96571f5d6a3f312a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 22:56:49 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Jan 2026 22:56:49 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Jan 2026 22:56:49 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Jan 2026 22:56:49 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Jan 2026 22:56:49 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:56:49 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:56:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Jan 2026 22:56:50 GMT
ENV RABBITMQ_VERSION=4.2.3
# Thu, 22 Jan 2026 22:56:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Jan 2026 22:56:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Jan 2026 22:56:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:57:11 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:57:12 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:57:12 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:57:12 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:57:12 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:57:12 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:57:12 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:57:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:57:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:57:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:57:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:57:12 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:13:18 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:13:29 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:13:29 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9bd8e79152b418ccad3bc28905f359bd4e4b96c42c3630c2ea2788698720e4`  
		Last Modified: Thu, 22 Jan 2026 22:57:37 GMT  
		Size: 46.3 MB (46261502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470566b0f28418a221298329a32e4500cfa9c74f8a138b928a2d9f6d762b2955`  
		Last Modified: Thu, 22 Jan 2026 22:57:36 GMT  
		Size: 9.0 MB (8994560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92643268a2d2aa07166cb80bdd6e63af85eac10c1f922a42b51ed7f12257e235`  
		Last Modified: Thu, 22 Jan 2026 22:57:35 GMT  
		Size: 9.7 KB (9706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1277fca3a045fef53350c7add4364a4d4af240ef4cb225758ab4b852de185e4`  
		Last Modified: Thu, 22 Jan 2026 22:57:37 GMT  
		Size: 27.9 MB (27940361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19a3c8d755dd3ce4e9a4cd3e7181d3e0a40740e2c18c835cb411118acde2246`  
		Last Modified: Thu, 22 Jan 2026 22:57:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9f3cdd70e8a5f0176df8c4c61a13b6cc3af8970cdd97faeb93ad64f9b6b474`  
		Last Modified: Thu, 22 Jan 2026 22:57:28 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228abd1859213f944f71ed093762923bf770e0bbd1455b7d23d3f8e9f3b1166a`  
		Last Modified: Thu, 22 Jan 2026 22:57:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d677b922baee1e363a3ed92512a6b436cf902138bdf047235331d8c05033334`  
		Last Modified: Thu, 22 Jan 2026 22:57:38 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52028b24bdc4d8c363bc58c26ec398acbb1754782434b8aafba05b70a4894ec`  
		Last Modified: Thu, 22 Jan 2026 23:13:38 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85e615bd61dbddade62634c0825ce17d5ee4f71a41acd6c747ad8f81faf999c`  
		Last Modified: Thu, 22 Jan 2026 23:13:38 GMT  
		Size: 4.9 MB (4888206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4614673972faf88a22ce32c9dae31a1017f55be94cc76177d008cdea7e3fca23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38707cd038a2d4c541fcefe6d7253d3548a0c7a25f0a1e56e0fc3d4f46b82d0d`

```dockerfile
```

-	Layers:
	-	`sha256:76254a0bfb1a0830d80d3af37d8655807b71726723a700820c6fd6d1fb1d4b1e`  
		Last Modified: Thu, 22 Jan 2026 23:13:38 GMT  
		Size: 2.5 MB (2486661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c408c33fbb7d74fa5cf694e5dc2d0671c1eb9b8f3d2be601a616279188aebbba`  
		Last Modified: Thu, 22 Jan 2026 23:13:38 GMT  
		Size: 16.3 KB (16269 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:a8f86c86ea7fe795dcf4b2b2b1d430af4dafdf36e1d8e8798f69cc7f5f8d7937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95312641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb551d6bfae8db7dd30dbb2423cb700bfe5614fde04e11d53a850b71af057f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:59 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:02 GMT
ADD file:9e6534a5b837dcbcc4b9596878a4feeb07210fb34c7385aeee0217ff03c2460e in / 
# Tue, 13 Jan 2026 05:40:03 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 22:56:03 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Jan 2026 22:56:03 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Jan 2026 22:56:03 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Jan 2026 22:56:03 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Jan 2026 22:56:03 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:56:03 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:56:04 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Jan 2026 22:56:04 GMT
ENV RABBITMQ_VERSION=4.2.3
# Thu, 22 Jan 2026 22:56:04 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Jan 2026 22:56:04 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Jan 2026 22:56:04 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:56:24 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:56:25 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:56:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:56:25 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:56:25 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:56:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:56:25 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:56:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:56:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:56:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:56:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:56:25 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:13:33 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:13:33 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:13:33 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a56277e49d30e9a430d5cefad3038f88470a8681e48b806fff292791ed54f1fc`  
		Last Modified: Tue, 13 Jan 2026 06:35:51 GMT  
		Size: 26.9 MB (26853837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9584e5d317ff5536f945db57635b206d4bdebc9d038177801b3731a8d4c312ab`  
		Last Modified: Thu, 22 Jan 2026 22:56:50 GMT  
		Size: 33.3 MB (33295172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4b0769845825dd9805c17fdb685c5a4280cf2f5171bedbaf1722320a99e4a4`  
		Last Modified: Thu, 22 Jan 2026 22:56:48 GMT  
		Size: 7.3 MB (7309055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5e0613ec9867efc41aa185bc3e7d4e25976135bc904a8aab0280933c1781f9`  
		Last Modified: Thu, 22 Jan 2026 22:56:48 GMT  
		Size: 9.7 KB (9721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161e2d96ce7326f5a94d8499a1cffc3a239606b5f0492e94387484dac9f876e`  
		Last Modified: Thu, 22 Jan 2026 22:56:50 GMT  
		Size: 27.8 MB (27842803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bb6594e5b2d8b1e973a73e9f8df5f9671e0f7d587779c7edfb0c1f69ea66bb`  
		Last Modified: Thu, 22 Jan 2026 22:56:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1f049551c883723e82ecccf213ba1f4ac11fcad47889b08d30a8f64e590dcf`  
		Last Modified: Thu, 22 Jan 2026 22:56:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9332f38e46cc8141c1a824c975b97b6ed9ca663ba63d9541d44ac1380ea08339`  
		Last Modified: Thu, 22 Jan 2026 22:56:51 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc92c88c34997cabbb0391414b8de8f71f6eb2fe04dd5fdafc9f83dda37385f2`  
		Last Modified: Thu, 22 Jan 2026 22:56:51 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddaaeff2e383ca7ea40d4acebe65f64937ae11527b9131a808bb9c373cb54b`  
		Last Modified: Thu, 22 Jan 2026 23:13:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bd109a90ac3c418f24c32de84a8ea358322946a04ab4d07b948104f7b690ad7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4c503ccf8fc0668ce45d26046f2ca51f72e32e2d87bc133666a1e78240904b`

```dockerfile
```

-	Layers:
	-	`sha256:c73d883761151505c332a461618c91e06a6a41b02a0f08f31c4c95b276c221aa`  
		Last Modified: Thu, 22 Jan 2026 23:13:40 GMT  
		Size: 2.5 MB (2487461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b42cd25a1c4c5221829ab0ab7c1bea3fc4569c18372d03c1771539cd84b262`  
		Last Modified: Thu, 22 Jan 2026 23:13:40 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:df0aa3c65b150761ef63748b47f170781ab1a70469cebb78d860b8fa580c4ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115436725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c6b69315be315530f0d06bcdc3b37410d75a603bd2c95aa8241e557ac95923`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 22:56:01 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 22 Jan 2026 22:56:01 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 22 Jan 2026 22:56:01 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 22 Jan 2026 22:56:01 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 22 Jan 2026 22:56:01 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:56:01 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:56:03 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 22 Jan 2026 22:56:03 GMT
ENV RABBITMQ_VERSION=4.2.3
# Thu, 22 Jan 2026 22:56:03 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 22 Jan 2026 22:56:03 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 22 Jan 2026 22:56:03 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:56:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:56:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:56:27 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:56:27 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:56:27 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:56:27 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:56:27 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:56:27 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:56:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:56:27 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:56:27 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:53:20 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:53:32 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:53:32 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b0f83ee1832fef1a2d17569188ea0f644dcf82432ef6b0233764c9bdb45cf`  
		Last Modified: Thu, 22 Jan 2026 22:56:54 GMT  
		Size: 44.4 MB (44355919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3e3407597e910fe721e5e24ba7c9491e489c9577a13d0e1e46ed5c1b262d98`  
		Last Modified: Thu, 22 Jan 2026 22:56:53 GMT  
		Size: 9.7 MB (9716269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598ebb36654408af99158b82cc470a43d44b07ebdcf22a0de7c28a21de3b9bee`  
		Last Modified: Thu, 22 Jan 2026 22:56:52 GMT  
		Size: 9.6 KB (9630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ddfc586f89c47409459e258c47a9588bfeae70dabcb161994d761997add2ac`  
		Last Modified: Thu, 22 Jan 2026 22:56:53 GMT  
		Size: 27.8 MB (27848954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408b0a01b6bbe13ec11e13de724ebd784108276d112b88f89868acb32eaaab10`  
		Last Modified: Thu, 22 Jan 2026 22:56:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30afc465793ba4b581ae2e77f9ff10510d620a1059d9d65729967dd34e81891a`  
		Last Modified: Thu, 22 Jan 2026 22:56:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5634291f85c913c6b1830dbf6d741712d4b980235381a165cef8faf80baf7243`  
		Last Modified: Thu, 22 Jan 2026 22:56:54 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c112ae2ec78f211a987418c44b3c3309e172078f29b94c2cb1cbcf9e4f967e`  
		Last Modified: Thu, 22 Jan 2026 22:56:54 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab251b16b6009e0e3a39cca38b28a4345e31a7a6012c7ba54b008d1006155b7e`  
		Last Modified: Thu, 22 Jan 2026 23:53:40 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8d78833def1b5fe252010cd247ded3125ee6f309781bd080bf3c2144604dbe`  
		Last Modified: Thu, 22 Jan 2026 23:53:40 GMT  
		Size: 4.6 MB (4640107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0fe43f9150701a5e859fa5f59312cf9af6a469ac43ee3d88fa3089a5fdfac546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd95e2faba564c90880a124208b38519bc4e4cc137abc56c162fc429196e7f8`

```dockerfile
```

-	Layers:
	-	`sha256:702013150e84d7ecb729ad7caf836e658b8d691d7a828928924cb3dcf1331014`  
		Last Modified: Thu, 22 Jan 2026 23:53:40 GMT  
		Size: 2.5 MB (2487721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c7c3a011a436d93296a9ecbc68b357949373879291d57f45c74fa8100a7ccbd`  
		Last Modified: Thu, 22 Jan 2026 23:53:40 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:6bbb2b856d58530c4951ba7b16509188f3f97b0b22e4e97e68162f636026cf04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111324663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7fe6606e84c9fbe31de10008f0c016e9057f6c1b0e78d6a9d34dbdb89ffc2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:20:17 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Jan 2026 23:20:17 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Jan 2026 23:20:17 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Jan 2026 23:20:18 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Jan 2026 23:20:18 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:20:18 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Jan 2026 23:20:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 15 Jan 2026 23:20:20 GMT
ENV RABBITMQ_VERSION=4.2.3
# Thu, 15 Jan 2026 23:20:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Jan 2026 23:20:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Jan 2026 23:20:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:53:44 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:53:47 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:53:47 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:53:47 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:53:47 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:53:47 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:53:47 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:53:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:53:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:53:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:53:49 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:53:49 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:14:11 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:14:12 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:14:12 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b66004f60715e2b64d2a5b9596535176d35315e17d9cc24e0564aba21e57fa`  
		Last Modified: Thu, 15 Jan 2026 23:22:16 GMT  
		Size: 39.5 MB (39509660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2122401978ab0aaf97b2cf0682999fd386bed109a43efad2f84c13ea3d4a26d`  
		Last Modified: Thu, 15 Jan 2026 23:22:15 GMT  
		Size: 9.6 MB (9598288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5557fd0a5fd75aa541e9086de6f73193fc426c57f71d521ba5e7bbfc7324160d`  
		Last Modified: Thu, 15 Jan 2026 23:22:13 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8835b723ccb709ccaa2a09d00859b3e526a20d141896221f7a8e59628ed382b5`  
		Last Modified: Thu, 22 Jan 2026 22:59:08 GMT  
		Size: 27.9 MB (27898874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8314ba87806e1d1ee35b50c3439f9e708555227ded392f5d25a6ddf50f01b6a8`  
		Last Modified: Thu, 22 Jan 2026 22:59:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e47897d19ad5e0be44c8cf2bf2aa84f4455998c7d8633d1313d7b5c6bda73d`  
		Last Modified: Thu, 22 Jan 2026 22:59:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4182241c6c49a2fb8b79fc3139bd341fc8b26e7a600b52d5a0529da8643e1c34`  
		Last Modified: Thu, 22 Jan 2026 22:59:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1d832f8f2ffccdae1a68d7395d32c915cfcd1f70e19795ca529e46852d0c88`  
		Last Modified: Thu, 22 Jan 2026 22:59:08 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15849797cbf85ce1b019ffef0c6ff648ca017f745a4bc5f70751f0f01cf1271a`  
		Last Modified: Thu, 22 Jan 2026 23:14:34 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2cc739fd572314a06f266c77c1c1f0089656e764e1d017d24b561aee30045b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91748533333df00fac27acbe14e7d28b27c4c8d0f6bdd4ee62af8bc6d155c5dd`

```dockerfile
```

-	Layers:
	-	`sha256:223604c6f902aca715cb6eede340f11b1a129e654dc7d254077ba9f51af7ad28`  
		Last Modified: Thu, 22 Jan 2026 23:14:34 GMT  
		Size: 2.5 MB (2491114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2138060970774d497aa3c5ec7dc91f2378b0702ad385aba0d3860264c2e2c4de`  
		Last Modified: Thu, 22 Jan 2026 23:14:34 GMT  
		Size: 16.3 KB (16310 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:794afb797cc585425f8327e8abd3123ed876e086870981c9f7505a828fc750e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104738145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18168f304a854013b0ed2b36966f3429a611157ba70908c73860c392f667bfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 06:14:56 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:14:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:15:46 GMT
ADD file:8d0655de001e92042901c645c76202ac355acb6fa186561e7344a0829ffd983d in / 
# Tue, 13 Jan 2026 06:15:51 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 05:45:03 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 20 Jan 2026 05:45:03 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 20 Jan 2026 05:45:03 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 20 Jan 2026 05:45:03 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 20 Jan 2026 05:45:03 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 05:45:03 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 20 Jan 2026 05:45:07 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 20 Jan 2026 05:45:07 GMT
ENV RABBITMQ_VERSION=4.2.2
# Tue, 20 Jan 2026 05:45:07 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 20 Jan 2026 05:45:07 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 20 Jan 2026 05:45:07 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 05:47:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 20 Jan 2026 05:47:25 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 20 Jan 2026 05:47:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 20 Jan 2026 05:47:25 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 20 Jan 2026 05:47:25 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 20 Jan 2026 05:47:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 20 Jan 2026 05:47:25 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 20 Jan 2026 05:47:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 20 Jan 2026 05:47:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 05:47:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Jan 2026 05:47:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 20 Jan 2026 05:47:25 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 12:18:29 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 12:18:29 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 12:18:29 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f151392858868452ec0f1f8d2947624e8dcdecf23bce587cfbd7c38a3264f9df`  
		Last Modified: Tue, 13 Jan 2026 06:36:06 GMT  
		Size: 31.0 MB (30953090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f865c3cf5cb5e2e29bc5328978ade4982fe3edd0a739a8134c7586e2210a041`  
		Last Modified: Tue, 20 Jan 2026 05:53:49 GMT  
		Size: 35.1 MB (35148175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1c22ab97d06d858a6db08293ffb9c5927330f12ae0c31ec396aeffa431a4ad`  
		Last Modified: Tue, 20 Jan 2026 05:53:42 GMT  
		Size: 10.8 MB (10831067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98baffe03837661139ddc29674da80d3f0070fd8faa1f899231251ab6ab25f39`  
		Last Modified: Tue, 20 Jan 2026 05:53:35 GMT  
		Size: 9.7 KB (9665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d47aad0170863beda75bf6d0afa42a45a696f73aba7873b6a1835c4095b17b7`  
		Last Modified: Tue, 20 Jan 2026 05:53:48 GMT  
		Size: 27.8 MB (27794087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24718e1bf5dceabc7bd31042c3f7006dc7666877091e12d35f7bdb7b211a0f40`  
		Last Modified: Tue, 20 Jan 2026 05:53:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e69050f85fca0ab2773a695870030005691ee34088e8888a0acb5d59d69480`  
		Last Modified: Tue, 20 Jan 2026 05:53:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73cd98ed71134759141bc9d26ba71e52814ad490e07d31645381017d1aef412`  
		Last Modified: Tue, 20 Jan 2026 05:53:44 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a0893180261f0217d2b4d638d89f2c33fe70bf1e9d3fd49066c984ab19c252`  
		Last Modified: Tue, 20 Jan 2026 05:53:44 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e0551d10188ce40b5870888f715ae5fb077b6a58184b94cfa05dacd2cbc4fd`  
		Last Modified: Thu, 22 Jan 2026 12:19:47 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1a7880533878d4333b411cd31fb8e743f7842a5abd862bf7c54561feefb4a593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474bbe2d8f07145344c4152568e5979d481236d02b2261ec94fa26d895c833a9`

```dockerfile
```

-	Layers:
	-	`sha256:85a3911b8734204a678d3b80626c114ec755607b261ec014768e016b003196db`  
		Last Modified: Thu, 22 Jan 2026 12:19:47 GMT  
		Size: 2.5 MB (2479028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a212adc89d07a3240ae64a0d6dd4fe0a6d12216b9a1831086b664b6e39224c6`  
		Last Modified: Thu, 22 Jan 2026 12:19:47 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:b5781d3c63de439c8b8798857ff937750e866fcd30c385210757ddc0763e3f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105047431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160d7bcea6e603136ea3f5964c443b8de31799b10680644d459a3983be9984f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:25:39 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Jan 2026 22:25:39 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Jan 2026 22:25:39 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Jan 2026 22:25:39 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Jan 2026 22:25:39 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:25:39 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Jan 2026 22:25:41 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 15 Jan 2026 22:25:41 GMT
ENV RABBITMQ_VERSION=4.2.3
# Thu, 15 Jan 2026 22:25:41 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Jan 2026 22:25:41 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Jan 2026 22:25:41 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 22:52:44 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 22 Jan 2026 22:52:45 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 22 Jan 2026 22:52:45 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 22 Jan 2026 22:52:45 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 22 Jan 2026 22:52:45 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 22 Jan 2026 22:52:45 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 22 Jan 2026 22:52:45 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 22 Jan 2026 22:52:45 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 22 Jan 2026 22:52:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Jan 2026 22:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jan 2026 22:52:45 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 22 Jan 2026 22:52:45 GMT
CMD ["rabbitmq-server"]
# Thu, 22 Jan 2026 23:13:22 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Thu, 22 Jan 2026 23:13:22 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-x86_64-unknown-linux-gnu'; digest='62e2c22df73b1f8f04bda5630cb9c32cc60ce2fa28487de0337c039625f5cbda' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.23.0/rabbitmqadmin-2.23.0-aarch64-unknown-linux-gnu'; digest='9ed29731a27d5aeba44fde8a64a55e04592db915028468a428069cefeee0fc29' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Thu, 22 Jan 2026 23:13:22 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 06:36:13 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec13ac7aea7104212abef800bfc438cd0de05f42a1dd9163fabc27207a2ff98`  
		Last Modified: Thu, 15 Jan 2026 22:26:36 GMT  
		Size: 38.6 MB (38581121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b13df2dbcf1da99013535f651cb22ff97843ad28ef7aeb91ac111d4d9045dd6`  
		Last Modified: Thu, 15 Jan 2026 22:26:35 GMT  
		Size: 8.6 MB (8623247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7b65a57f61456819bb64b22c0490766aa106c3f7602aceddb79d113e81f181`  
		Last Modified: Thu, 15 Jan 2026 22:26:35 GMT  
		Size: 9.8 KB (9815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88865b4c47fcc5b71dfb0cc570f8215298ed7573763528e463d182bacb2b05`  
		Last Modified: Thu, 22 Jan 2026 22:58:29 GMT  
		Size: 27.9 MB (27921995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1161e323827ebe1106ad9bbad4ef0d52de746689d39abf08283e06682c0d32df`  
		Last Modified: Thu, 22 Jan 2026 22:58:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f049b202bd428beb2780665c5a9c65f0a124a0027360ad3666eb78c1e669d6f5`  
		Last Modified: Thu, 22 Jan 2026 22:58:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa932b694e1228d2e8059840b8b11ddf84129c3f192d3d263d7b0aa0f59d27e8`  
		Last Modified: Thu, 22 Jan 2026 22:58:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b8fd967b675aca4a11d335734a47efa06f451cb9a169c46479bb1993ae1640`  
		Last Modified: Thu, 22 Jan 2026 22:58:29 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43edd8abeaf7c8b473a4e58fc0bba8beca9f8aafaeb4c6957d7d3938fb1f2312`  
		Last Modified: Thu, 22 Jan 2026 23:13:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4416564514d7578e844634e7dabcbf799005334a517b4cdd1af9b7171786ae68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2505035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce640c15c99ecaf07332bcd0e54e1a2930682092c825933d2d4b4d42abd98f8`

```dockerfile
```

-	Layers:
	-	`sha256:4699f9d0a4d58c835158946c7f66f30b332b8498402deed8fbd73be58c915560`  
		Last Modified: Thu, 22 Jan 2026 23:13:34 GMT  
		Size: 2.5 MB (2488771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6864cd68c61370aac6d4dd46f29d47e3d5cf85a7386fedc223c52883d58baeb`  
		Last Modified: Thu, 22 Jan 2026 23:13:34 GMT  
		Size: 16.3 KB (16264 bytes)  
		MIME: application/vnd.in-toto+json
