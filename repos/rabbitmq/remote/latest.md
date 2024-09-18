## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:5dcc2a3a81aa8d3c2f2ee8faf358248fcad8755b967ae55626e64fe06ad2eae9
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
$ docker pull rabbitmq@sha256:2bf9e939ab39155dd16e509d218d3f986fcb7a98b639c58d66a9a3249b4a1b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106650393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5d86e8f167b14d89922caa06bf5a1510254a08cf71d08161be25f5408fe342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.0
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb35719f13dc84dc93821f818be6ab98369b1a4672976660ef57b0038b61fd2`  
		Last Modified: Wed, 18 Sep 2024 19:04:25 GMT  
		Size: 45.4 MB (45447572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588bd6f0e68e8506a0a42bf6370df4160a6007a696910353ca2cf885d1434a97`  
		Last Modified: Wed, 18 Sep 2024 19:04:24 GMT  
		Size: 8.2 MB (8169250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4312b9780a9c022ebc0a73ef86c4419e95270e7e65af6dfa80ebef9ce10216`  
		Last Modified: Wed, 18 Sep 2024 19:04:24 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a845e3a813be0ee34596320d4974a197d54f0af1d84dd6098146761a0f3b62`  
		Last Modified: Wed, 18 Sep 2024 19:04:25 GMT  
		Size: 23.3 MB (23272509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13167ae876c4ae893d8ed986eba4d9bb19102e6a447b53831f88d81a3d27427`  
		Last Modified: Wed, 18 Sep 2024 19:04:25 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23228179a8958b141b2753253f783723b5e182207d2a5dd7e261502cca713276`  
		Last Modified: Wed, 18 Sep 2024 19:04:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ddea22df41c637bca5b5bf9d39d5caef7f99e8dd91bce1f622e3b5a8538f1`  
		Last Modified: Wed, 18 Sep 2024 19:04:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8fbf9a51a4c12833b98ab72c3cb104fdffc97a057116c527c0813cfac4269`  
		Last Modified: Wed, 18 Sep 2024 19:04:26 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7f38bd41aa3123921a68bc7d7673090893fdbac534282d87950f607945391cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18116182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb89ec5ea080625a9c0eec17286b9010b330169e46fdc872dd211dfc59b1bfd5`

```dockerfile
```

-	Layers:
	-	`sha256:8e96573e719369f88f1663fbee6985b5051a9b650a2f6083de58f71f4720737f`  
		Last Modified: Wed, 18 Sep 2024 19:04:24 GMT  
		Size: 2.3 MB (2343732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f25d2d462693206bf76e80f576c71f465ae34dc219f3b083fd62a051c9ee2886`  
		Last Modified: Wed, 18 Sep 2024 19:04:24 GMT  
		Size: 5.2 MB (5189949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d427345f20b59c7c7ba23c058af8de603a918d23d4aa08f5d1d88b462f0d3e`  
		Last Modified: Wed, 18 Sep 2024 19:04:24 GMT  
		Size: 5.3 MB (5330046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe98544985ad8c96c77632391d6f67d741f524b2a1d058c33f3a3a82cade9be`  
		Last Modified: Wed, 18 Sep 2024 19:04:24 GMT  
		Size: 5.2 MB (5191471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db6655d6dfdccceaaf3dc723c54efc3df2a5b30f3c5417e802d6fda241661265`  
		Last Modified: Wed, 18 Sep 2024 19:04:25 GMT  
		Size: 61.0 KB (60984 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:8490efb7dbaa6073cdecb716578b383d832471a4f35400f573cdbaa89b05f851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89222290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcb3c28f30d6329b1c46d70c032ffa4b194fdc5767cb7e727c1fe0b32403aef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.0
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:eb7e9efa9f9d063fec8aeb787b87620ae79d524925cdea2e8c267bdd96cac928`  
		Last Modified: Tue, 27 Aug 2024 17:08:17 GMT  
		Size: 26.9 MB (26865525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4eb81e19e008def654bc092bd0d34a7142120758f6c1873d7331d0b0208501c`  
		Last Modified: Tue, 17 Sep 2024 02:20:37 GMT  
		Size: 33.1 MB (33120962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2502431ef7910f292e4a9d0f7bafe973a91014cb350260b862949a61079181c1`  
		Last Modified: Tue, 17 Sep 2024 02:20:36 GMT  
		Size: 6.7 MB (6667920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cfd9a54b206afb355157305e502e6219ef454b804062b9fc26eb99f2c73d72`  
		Last Modified: Tue, 17 Sep 2024 02:20:35 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fb0746ab4cd449ef5b7ed580076edc19f4fb50e0f6ad9018c438baf19aaccf`  
		Last Modified: Wed, 18 Sep 2024 18:58:31 GMT  
		Size: 22.6 MB (22556614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0b9642520577361f442d133e61e3a79d5abc8fc3f82ffdd8357035f2545662`  
		Last Modified: Wed, 18 Sep 2024 18:58:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beafecdedcd79e782c6ab243c60092ad4f5cdb0df46859eecbae1a25f271b06a`  
		Last Modified: Wed, 18 Sep 2024 18:58:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577ca700fe4eefaa87c827b5ad583a5b8adeaf978bf1447215f6b09279983ea4`  
		Last Modified: Wed, 18 Sep 2024 18:58:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9851d327efba34976d69d0ea40e45c4b8c33132e3be340aa330e9e33eb5914`  
		Last Modified: Wed, 18 Sep 2024 18:58:32 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7381a55c1ec1ae0d2d2cdef1e8bdd1acea16f0128b7f66cc349d1d069d27990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17580409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7092176c9c254c077428205b34367cd3f9d58e88d4ac731343693230f3ed9d5`

```dockerfile
```

-	Layers:
	-	`sha256:dbcf5be252f379a64abc9faea10d0e5d374c3f07018260cc0ef068d313d8106f`  
		Last Modified: Wed, 18 Sep 2024 18:58:31 GMT  
		Size: 2.3 MB (2344741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f29f5f62008ef37701aef5ccd1a380b7527383a2b43d738b7eb7cc8184fce5`  
		Last Modified: Wed, 18 Sep 2024 18:58:31 GMT  
		Size: 5.0 MB (5011671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:843a4969a0e168a6a3fc884ee0ff3a56a74d858f6cef3c7a5202f57e4201467b`  
		Last Modified: Wed, 18 Sep 2024 18:58:31 GMT  
		Size: 5.1 MB (5149633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1bbb281d6bb7b4d59c2fccdfecd95ac31db3e16cc1db8a566b2d03d349a590e`  
		Last Modified: Wed, 18 Sep 2024 18:58:31 GMT  
		Size: 5.0 MB (5013193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b20fcce366683f98e228c82a43e73dfee0a6db16936dae878b4011a4e5602423`  
		Last Modified: Wed, 18 Sep 2024 18:58:32 GMT  
		Size: 61.2 KB (61171 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:f812fda86fd381655e5ebd41719ca870145f76e73f76f97fc1939264d87408a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104304744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5d3dd95e5e753800a2596c8d65d0e278378d7f80ebaf4f5b4ada482af01c67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.0
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547eca683c77aeb4ceebef69bb98a6942657d60ae733bcacdaae0cdbad28807b`  
		Last Modified: Tue, 17 Sep 2024 02:49:01 GMT  
		Size: 43.5 MB (43478555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f39ec5e5d2461e710e856c8c1d09a2a7319d3853b0a46b176fb4442c790cc6`  
		Last Modified: Tue, 17 Sep 2024 02:49:00 GMT  
		Size: 8.9 MB (8934211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e0bc84bde268a3664b171f86ac3f88246c88ab0b7b8929bfea1302fcca833`  
		Last Modified: Tue, 17 Sep 2024 02:48:59 GMT  
		Size: 9.5 KB (9465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b221418f93cda5ddf1f23ebf10088f5e0208d4f927a3af1fed23c99dcbdf35fe`  
		Last Modified: Wed, 18 Sep 2024 19:01:51 GMT  
		Size: 23.0 MB (22995164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed7bd61c901aeac6b209628cf58817b938a5b7614bd2b39417df1c30d6a7aa1`  
		Last Modified: Wed, 18 Sep 2024 19:01:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beafecdedcd79e782c6ab243c60092ad4f5cdb0df46859eecbae1a25f271b06a`  
		Last Modified: Wed, 18 Sep 2024 18:58:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee77f59249bd67b2b421560c40156fb0a90aa2d7e237d389ada4673a5d7d13`  
		Last Modified: Wed, 18 Sep 2024 19:01:50 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d0f121bdfa36c09b1b5122e0728d074c37be01f51f414efc1c959429bd503`  
		Last Modified: Wed, 18 Sep 2024 19:01:51 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:dc810b1432923c8afcfd36972128ad61576f5d285eb93e6414ef0dc70a2830ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18176742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab5923c99e681d403a79e19a00b71625541488574f968df003ba2a471a94a8e`

```dockerfile
```

-	Layers:
	-	`sha256:b56c610a48ad83438ea2c27d1393d310029ffaad7aa4bfbc62070ffcc1e0871e`  
		Last Modified: Wed, 18 Sep 2024 19:01:51 GMT  
		Size: 2.3 MB (2344792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce941f1d17f175eea24ff2e566e3d994b9a2226c7eba3e242030b1ee0ad095f7`  
		Last Modified: Wed, 18 Sep 2024 19:01:51 GMT  
		Size: 5.2 MB (5209676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4625ecffa0dbde0d58cba5cfd198cb29997c20faaa71fed3c692a77e7324a1cf`  
		Last Modified: Wed, 18 Sep 2024 19:01:51 GMT  
		Size: 5.3 MB (5349791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3509b18a96b5bbc02620ab3c2ba75530341a0549ec1995f74ba3247a434c972`  
		Last Modified: Wed, 18 Sep 2024 19:01:50 GMT  
		Size: 5.2 MB (5211198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a1d95b5d519db48d8aba8c03b46865e4dd6668938d815cfbbc6c7435cfc2518`  
		Last Modified: Wed, 18 Sep 2024 19:01:51 GMT  
		Size: 61.3 KB (61285 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:f7d70ef37b2c3ac32e92ef459f7ae43bbd4ecb0d158fc05b294f6bde236f0e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105701136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9abd568a9fbbd3a30c4280b81f7b39d753807fbe34c6b18b490c50a8ce40ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.0
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae12c93b42b1f5880b2b7fdac9201786e362f11134a3011163fbf779bc63a0c`  
		Last Modified: Tue, 17 Sep 2024 01:59:54 GMT  
		Size: 39.2 MB (39155450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df1a7bb15f08cf4f1e98ca99d7b0cfce8bc13361fc57368b06d089d4089f948`  
		Last Modified: Tue, 17 Sep 2024 01:59:53 GMT  
		Size: 8.7 MB (8689238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39128545dcc5b74866a4c37ac73cd13dc7bdeb526be46bbcbfd80816da7eee3`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301bc5f194316b9b6443f4a19ed1ce640bdc20d87c20eb755af44a25bdc8ed76`  
		Last Modified: Wed, 18 Sep 2024 19:02:14 GMT  
		Size: 23.5 MB (23452963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48eb72168b33d17c9d50e96aa19a9670fb1977275f7d22d2697376f461b7e1b2`  
		Last Modified: Wed, 18 Sep 2024 19:02:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d97344502ec0220f5f1a3ce5a9a67d81b185a6fda01f8ea56afd3b4caa73e`  
		Last Modified: Wed, 18 Sep 2024 19:02:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb799ab6fd3042a4fbdf3ddb421c906d67af33ce946784f6918dbbf865f68f72`  
		Last Modified: Wed, 18 Sep 2024 19:02:13 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11e4a38dba6b864665a532f595c44f0e2e59677cf10090ca43b80c49cc8362b`  
		Last Modified: Wed, 18 Sep 2024 19:02:14 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:12a3ccbd33e3f0b33f16e04c4f9af0254c1de0ac66c436462ee10c93ae16c1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18033481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb37d18a9bd6c5f2214d3a5401aa6914ad1b93fb404a894f7d057120c70077f`

```dockerfile
```

-	Layers:
	-	`sha256:197cf9446b488f1512652db5a05b4ff3e819095835e080d26140ccd4da6820ed`  
		Last Modified: Wed, 18 Sep 2024 19:02:13 GMT  
		Size: 2.3 MB (2348086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c8ed5991a4e749bad18f713087a6d57dd588551afefb370a7064354e8d9ef5`  
		Last Modified: Wed, 18 Sep 2024 19:02:13 GMT  
		Size: 5.2 MB (5160902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e586cab04bf3a27f5692be89d057da1317b9ebef92360c9577c0249dd3b6639`  
		Last Modified: Wed, 18 Sep 2024 19:02:13 GMT  
		Size: 5.3 MB (5301029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9594b7caaf76fde5b8fbe93fcdf68171e00c04ed2693bea6276279409cf25af0`  
		Last Modified: Wed, 18 Sep 2024 19:02:14 GMT  
		Size: 5.2 MB (5162424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bcf26713ca804de3b1b4c50225545fc8037a7275de6bec8d6277f681367274`  
		Last Modified: Wed, 18 Sep 2024 19:02:14 GMT  
		Size: 61.0 KB (61040 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:db5656fe612ac645ef859495c19dd6602e17b6dbaf41c27343406ebb7937764e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98576611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fee60c23b6152612edb88e4abba02bcc674558501b2884c9ee7edf63e39c328`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.0
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:651d7149a766bf9e12f26204ac9f977fa21fa3adbb24c0d2746c0b1cb99c8924`  
		Last Modified: Tue, 27 Aug 2024 17:08:30 GMT  
		Size: 30.9 MB (30949308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d857a6a002e9fecd6c4fed15dd85c6c7febaf7a9149e5bfadbaf083cdb1e07`  
		Last Modified: Tue, 17 Sep 2024 04:04:36 GMT  
		Size: 34.9 MB (34941624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3d855f63fbc2dd7c0b7c0fd227bc9b480c4c82882cc5851ccb86f32a8d8b28`  
		Last Modified: Tue, 17 Sep 2024 04:04:32 GMT  
		Size: 9.8 MB (9783464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d0a2d7021dda83a82ae4161fb70a188abe40d0fedf8146ec44e3a74d59a944`  
		Last Modified: Tue, 17 Sep 2024 04:04:28 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daea108cc39c6e857d1cefcd5d3ddaee57adf8a04c0257cdc4f113bbb877cd7`  
		Last Modified: Wed, 18 Sep 2024 19:07:17 GMT  
		Size: 22.9 MB (22890968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6e5a196f0f88e24b38abe9a41ac1c42461839aafc4965aaa94341876026324`  
		Last Modified: Wed, 18 Sep 2024 19:07:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d7e4c7065fc92dbaaf5b32783cfa43b19ab35d49fbdddf687205f6d7c6902b`  
		Last Modified: Wed, 18 Sep 2024 19:07:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecf45bfa8162fa94a3f994248be9d2476e3a24b22b387b2d491476783e1d8c`  
		Last Modified: Wed, 18 Sep 2024 19:07:14 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f3dd86c5484146571fc001bae1d200d1498eb0de3106d591e39ccb7586e39`  
		Last Modified: Wed, 18 Sep 2024 19:07:14 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d2a0f97366357402912d1718bdc9e969965f6e0838b504879903b75c123da81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17994344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e39073845d851c3a3fd2033a6b8d854f0d114a20f7aaaff346b6161bfd6333`

```dockerfile
```

-	Layers:
	-	`sha256:155216c50fdd6384f490c62ebd5732cc6804be2c178c08f784590ca8acae242f`  
		Last Modified: Wed, 18 Sep 2024 19:07:14 GMT  
		Size: 2.3 MB (2336634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfb76d768433988654c36daf0fa78b43f0d1dc48a13ba480ef3ce0c2c587eaec`  
		Last Modified: Wed, 18 Sep 2024 19:07:14 GMT  
		Size: 5.2 MB (5152396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e025fe4a24d135323b5e35b649844273956388efaca0c7d116dfa97ce41144da`  
		Last Modified: Wed, 18 Sep 2024 19:07:14 GMT  
		Size: 5.3 MB (5290356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b5a6ee8b96cca48ff529ce4f0ca8419c9ea3ea3e8c2418c8494c5530bb4e444`  
		Last Modified: Wed, 18 Sep 2024 19:07:15 GMT  
		Size: 5.2 MB (5153918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c5b6873e77e16141a94cf52fb5604daae218506bbcbac9a03dee6513d96656`  
		Last Modified: Wed, 18 Sep 2024 19:07:15 GMT  
		Size: 61.0 KB (61040 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:dce9eb552cf92e964a6ac2c320ecb88711cbceddd5e147628a6e99c546574fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98785149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956579c6daddc71cae3622c26b52218c307630740235134012dafca7234ecaef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 18 Sep 2024 16:57:52 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_VERSION=4.0.0
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 18 Sep 2024 16:57:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 16:57:52 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 18 Sep 2024 16:57:52 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 18 Sep 2024 16:57:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 18 Sep 2024 16:57:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 16:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 16:57:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 18 Sep 2024 16:57:52 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:43b981c5954bdfa7626a4bec06cf075f7bb2df6698b5c0b42b5b5770109637c6`  
		Last Modified: Tue, 27 Aug 2024 17:08:36 GMT  
		Size: 30.0 MB (30024629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa05ab9b97b42f7997fce79630852028f7ebfed588e2b3e2e897b95b89bec18`  
		Last Modified: Tue, 17 Sep 2024 02:28:57 GMT  
		Size: 38.3 MB (38260472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab857053fa6d133ee8ab1aa5a40a857754dbe098c5ff8315c408be8efc5ff1`  
		Last Modified: Tue, 17 Sep 2024 02:28:57 GMT  
		Size: 7.5 MB (7546297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d969711d8f29a6599306abfdc526f3327653341c04ee4d5ba5637d3863c866d1`  
		Last Modified: Tue, 17 Sep 2024 02:28:56 GMT  
		Size: 9.6 KB (9607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99329c690deae4646b8f73559d91db3ecf9bde8e1b8be849b0e059c35d31b5f3`  
		Last Modified: Wed, 18 Sep 2024 19:02:00 GMT  
		Size: 22.9 MB (22942396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498bea16e20f320cd450366f80a7a2beadd3a5910ccc02f7d5f01746ce492080`  
		Last Modified: Wed, 18 Sep 2024 19:01:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d248a5df7c2901150ccfef770b70b1276fc8ae0679aac04fddb8ca5e2ca256d`  
		Last Modified: Wed, 18 Sep 2024 19:01:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34ecdf8bdbc6319b673d2b92b511344067b2aa7a34cccd529923af846f2d552`  
		Last Modified: Wed, 18 Sep 2024 19:01:59 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1d6daaea8bfae3d6715900c705d5c89711d58c28a3ccdc78247ad828bed3db`  
		Last Modified: Wed, 18 Sep 2024 19:02:00 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0844a6e2c09b84bb4b638488ee3a17c90a1ca865525fd66717d62c5f2c008388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17664236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975ec63a4c2cdf3f852b8a26149a6c94132a307929b4dac86070f2f277a4840c`

```dockerfile
```

-	Layers:
	-	`sha256:7494064397483b81876a28414cfd23bd1bc92c497da10a1d9be6e96c994546af`  
		Last Modified: Wed, 18 Sep 2024 19:01:59 GMT  
		Size: 2.3 MB (2345952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:579aefcffcdc7b20e4a146bee5b73cd602f6bdc2f2bb854883dd62a69d5333a8`  
		Last Modified: Wed, 18 Sep 2024 19:01:59 GMT  
		Size: 5.0 MB (5038925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f2e5cbbf73a01c8ac21404afde55abfc6f4794e166c67033f24751e79e1791`  
		Last Modified: Wed, 18 Sep 2024 19:01:59 GMT  
		Size: 5.2 MB (5177928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5540b5b3bc645758dc22508da6981797466a2b48f30c7fc724e2e699809b165f`  
		Last Modified: Wed, 18 Sep 2024 19:01:59 GMT  
		Size: 5.0 MB (5040447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:866f5c48eda81503170ac0a37a14a631e097486f8875daa20af1f73b6f380369`  
		Last Modified: Wed, 18 Sep 2024 19:02:00 GMT  
		Size: 61.0 KB (60984 bytes)  
		MIME: application/vnd.in-toto+json
