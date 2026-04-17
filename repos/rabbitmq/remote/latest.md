## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:d3356b10fd1afd503b58f53d267e9561338501d5ba4e9cf2f62b4250e55fece4
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

### `rabbitmq:latest` - linux; amd64

```console
$ docker pull rabbitmq@sha256:9e671986fc1a3923a06814a68fd23aabe6d7f038363cfe31efe0160d5509bb04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113011166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7f9f3c79eecd128471a195c5a7ad420389e89e07b5c26f3c2fb0d3636f5b27`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6e396870f9970e80bd35a9fd309da48d10b0c0c0558ecddbc7412e2f12497da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18840880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268f028e67d37862ae2c847ee7448384eeab871d9fb6b5730630c993d334aede`

```dockerfile
```

-	Layers:
	-	`sha256:145a6873d703f4b3387e0a15a1cd7cf43954f8b03984dee64b69d3280b06ad9e`  
		Last Modified: Wed, 15 Apr 2026 20:54:16 GMT  
		Size: 2.5 MB (2486623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6010b54d764a4fdcfbcae747704d91e1ac9dd49b088aed8e59611dfe9e99499`  
		Last Modified: Wed, 15 Apr 2026 20:54:16 GMT  
		Size: 5.4 MB (5378513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cf0ad737fa32be6c6f732a7be0ac137a97b082b74cc40a24e816d625581ffd`  
		Last Modified: Wed, 15 Apr 2026 20:54:16 GMT  
		Size: 5.5 MB (5535288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b43ded82ce88bd39a51edc55eaad4d8bf3e96e22b1c29f8959f37dd3dc15d8b`  
		Last Modified: Wed, 15 Apr 2026 20:54:16 GMT  
		Size: 5.4 MB (5380255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f2e2f729186cbb82a4b449158c40edf354b7b265907af4fe80a936f87f7605`  
		Last Modified: Wed, 15 Apr 2026 20:54:17 GMT  
		Size: 60.2 KB (60201 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:3f338ba0cb77906ee98a23b8714790f8355bd6bb9c2344d1f90e9c9886c58008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95379706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c6a1ae638cc78b41effd7893bbca4a11639cf48e19d96b4d61284a08b7d7c5`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bd752b09c13a29cfb8581ad728b4ead19b2e3c7fbc906f4f13471a47ca8d3da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18295594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6059f68fa7774348278c2f771883c4d81ae81bb7805a4f814822b32367e7ae3e`

```dockerfile
```

-	Layers:
	-	`sha256:84f8afc64c97c46186e7cac66b8a61b7b685d6fcf36196b6acb566a4adc58a24`  
		Last Modified: Wed, 15 Apr 2026 20:50:10 GMT  
		Size: 2.5 MB (2487423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c1cd308ab5c90ca9c24f4356481f312387ce056f84accfb3c6d73ccfc1a963`  
		Last Modified: Wed, 15 Apr 2026 20:50:10 GMT  
		Size: 5.2 MB (5197271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86961a4656729dfe16ca92e31c83eb1b9d8671d97d68262ea4fd22b7a266d931`  
		Last Modified: Wed, 15 Apr 2026 20:50:10 GMT  
		Size: 5.4 MB (5351489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d998a3a08bc59a1ba2eed623cea148435f1648fe3cec69361ffc5603b3ef887`  
		Last Modified: Wed, 15 Apr 2026 20:50:10 GMT  
		Size: 5.2 MB (5199013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc508a978db6fe16057978a0059ade76c8b8becf3356a0ffa4b8e63c73b9444`  
		Last Modified: Wed, 15 Apr 2026 20:50:11 GMT  
		Size: 60.4 KB (60398 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:6910902996574084f1dc4e19d0f1ec6208cde6e15f03dd3b61c7061f8a1894e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110875079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8f03be3ca0238783f31e7113d3bc675d9ecd81f72a2aaa802b31e6e965e331`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8c614bba2cd256279eff6597f616210e051631922a1c81cff5bbe791a00b817a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18899848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc112b961f0537c369dca9bbd0a976ff6ca578c0f6176909d427867c4049667`

```dockerfile
```

-	Layers:
	-	`sha256:1d7754eaa3a43ba57df9857d4370f7f81ac9f22f5f757441d0f622c7b6f07c93`  
		Last Modified: Wed, 15 Apr 2026 21:00:47 GMT  
		Size: 2.5 MB (2487683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1170feb98ea15df722ba0b6c14ffac079a211e47fd691b4778f7371201df4ad9`  
		Last Modified: Wed, 15 Apr 2026 21:00:47 GMT  
		Size: 5.4 MB (5397730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7c93e76fefd6634cf56f30ca7d86d751427d6d836f8121da5f27f39ebd39da`  
		Last Modified: Wed, 15 Apr 2026 21:00:47 GMT  
		Size: 5.6 MB (5554523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d64eeea9f1fd1f075e5f072294ff10654992dbf93e4c841b83ef7cd851944e`  
		Last Modified: Wed, 15 Apr 2026 21:00:47 GMT  
		Size: 5.4 MB (5399472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13415594e037adb0718167b738e85a2322c9e0999048f72b46bbad3911028ff7`  
		Last Modified: Wed, 15 Apr 2026 21:00:48 GMT  
		Size: 60.4 KB (60440 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:25b87a82ae8067357d4deca9c160482e609edbbe4efdc49aa4551c737d27a544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111398853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad4d52c3846f31fa27768befb2afeb5b13ba26789e271f3b2c2420aa0f1327b`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3208d392ec2ce48dbcd9f25cd30824bffb5e0c9e94d67e3e323550457784e337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18755232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2ce4632139c86fdf44aa7f37b778067408e7faf253cb8207f1291833fb3d97`

```dockerfile
```

-	Layers:
	-	`sha256:da109b609c801f077312f2dce3a854c76b9443cdd2f1c6702bc3f810333b19c3`  
		Last Modified: Wed, 15 Apr 2026 23:00:50 GMT  
		Size: 2.5 MB (2491076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60dfa26b4d1d7a4aa28f4d19c19aec6e5f8ae3749d0468312a393ef1a0ef5d0c`  
		Last Modified: Wed, 15 Apr 2026 23:00:51 GMT  
		Size: 5.3 MB (5348449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f18c605f30b30eb87bacd369614ae8634003d683629e31de1d743f01be8b380`  
		Last Modified: Wed, 15 Apr 2026 23:00:51 GMT  
		Size: 5.5 MB (5505254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73847eeed3582679a91cfb8634d23cd1108f61354575c7f9ba12daa232ddab93`  
		Last Modified: Wed, 15 Apr 2026 23:00:53 GMT  
		Size: 5.4 MB (5350191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272dcdd92231f7e65c3d7bf4a90088df5594d80b0c34a5bacd0d4d8469bb8399`  
		Last Modified: Wed, 15 Apr 2026 23:00:52 GMT  
		Size: 60.3 KB (60262 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:862ce448e47e69423e4c06620c8da3e5c34900626e591c9a67663f8c7d0e2f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104881514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0062e1a36736ab5ea52402ea9fa5338513576c63a3f4d6bebc5802c4f6ff380b`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:540a7b6c8a4aa63bc0051f27872e301c1768443856d1fce37790818cdf1258c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18723828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e32391dfa1955755baae7f0e4f150fa15a8a02dcc9f3c99417417349a6e4f5e`

```dockerfile
```

-	Layers:
	-	`sha256:612aeeb93c6c9fb3660c257f9024aa107afc4e12d4528fb1596c0c289a04b27a`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 2.5 MB (2478990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51682fdaefdeff35670ef43b246a8c21e9a1fb3da0331a32755f320f3dc880a7`  
		Last Modified: Fri, 17 Apr 2026 00:15:39 GMT  
		Size: 5.3 MB (5342870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dae7d7a28d72dd6d870b53b873ff693961dcf89839582527b71bba57e11b190c`  
		Last Modified: Fri, 17 Apr 2026 00:15:40 GMT  
		Size: 5.5 MB (5497086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c0cd5330774c97bebada29708d5e1e33ca9355ea09f44444ab19ac8ede2394d`  
		Last Modified: Fri, 17 Apr 2026 00:15:39 GMT  
		Size: 5.3 MB (5344612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8193cc2eeb1646930012cf8746c1dcb071ec491ad710bf1344f6422e3361fed`  
		Last Modified: Fri, 17 Apr 2026 00:15:40 GMT  
		Size: 60.3 KB (60270 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:a0cbffe6f1a7cdc1166f2379af5179e56c7360c5c1dc38b0b21146094dca0caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105124100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49d2a3af3f1ec5a51e5274ad980944366a5c5f63d7af7fa86f858d93be3670c`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:79f8a84ef94a5b1b6901865470927a3afdd1f27e3d90a1de76ead4bfcc0903d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18380972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04f2e9724ac66010e9631b2536e33c80f36bf8c7e3914521d63b4b26aec0b7a`

```dockerfile
```

-	Layers:
	-	`sha256:feba3a2dff408cb3f0ffe778240dc481fffe45413db9ffdd1442667ff543a7ce`  
		Last Modified: Wed, 15 Apr 2026 23:22:43 GMT  
		Size: 2.5 MB (2488733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a24fe4fd8aabe6f29d5465ad3938760ffb94f45cf631d7eb9d6cf391e2909d`  
		Last Modified: Wed, 15 Apr 2026 23:22:45 GMT  
		Size: 5.2 MB (5224942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f0a5509375277db08928c204d811625fc7395b26085371d6228b69bafa7102`  
		Last Modified: Wed, 15 Apr 2026 23:22:45 GMT  
		Size: 5.4 MB (5380412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc67e3c6ed15f8a8131a851df4eef141a551f078739f1c9e72fb07fc66070995`  
		Last Modified: Wed, 15 Apr 2026 23:22:44 GMT  
		Size: 5.2 MB (5226684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be000ec2ab8346c9b68cd325b3edb522a66f92546d50220903ec2e5bc5f5da93`  
		Last Modified: Wed, 15 Apr 2026 23:22:45 GMT  
		Size: 60.2 KB (60201 bytes)  
		MIME: application/vnd.in-toto+json
