## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:3b744aeff128cb7d8dd89207520c134b4c686b93f8cd7779db80069d4a30b4bc
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
$ docker pull rabbitmq@sha256:33fc44b5dad6acabb614bf7315fe4dce95aa716d6696d4b341784bc1a56b39ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106650079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a921b87dc5b53db7f7d514e99af890c421bc6e7acf955c481f58af30d1a7a07c`
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
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae94e6aef3569434d5416ca1ea0412e9923a465ac5beb18762f94486f681181`  
		Last Modified: Tue, 24 Sep 2024 01:07:16 GMT  
		Size: 45.4 MB (45447517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad525572aae85d626b851f11182b391fa8ced1197f01017fec16003f15ffb3e`  
		Last Modified: Tue, 24 Sep 2024 01:07:15 GMT  
		Size: 8.2 MB (8169261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01adf267ddca9e9d485e7e4682e36273581e559a0793ac0cd3284c7266ccbc8`  
		Last Modified: Tue, 24 Sep 2024 01:07:15 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14495391f6cb1d47398e59d472e67839c7659c695f6fe70ff72519305c2e30fc`  
		Last Modified: Tue, 24 Sep 2024 01:07:16 GMT  
		Size: 23.3 MB (23272262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8666b435d033f484da404382713760379d0cced31429c30ca70a6c2479f25788`  
		Last Modified: Tue, 24 Sep 2024 01:07:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a05209e70faabab23f335faa9f0f1430c0a5138e02bbfb45db94e563f52a2e`  
		Last Modified: Tue, 24 Sep 2024 01:07:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90a98e5e04357c17921dc944f06bc2170bb37133b6d435a41039323b3c27bb`  
		Last Modified: Tue, 24 Sep 2024 01:07:16 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45842602427a325389c3bb4ee665f1894145d92631f7d9d1a7190603ed588a8b`  
		Last Modified: Tue, 24 Sep 2024 01:07:17 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b5aa1d9d2f1a5b68a7ef13b6aa1b6a129d6a7d70eb7e3aac23652734005c8e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 KB (60765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15736744e19188e5587e75db3454eb463c97217a791a580128fed4af17ba511`

```dockerfile
```

-	Layers:
	-	`sha256:1ad1de1dd269956d5887b504273f3707d774be53fa944c77184166e7976c868f`  
		Last Modified: Tue, 24 Sep 2024 01:07:15 GMT  
		Size: 60.8 KB (60765 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:e166aa7a582bd3062b55a59f8e4994ccbddec40c71254016fa3ab790905b014f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89222503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d227a943159bb9578b4679b1699c1f21b5a8507ed76e590076eeaf5358f760`
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
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
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
	-	`sha256:c78d26a7bfb37ec934a244b00156611e3002233e4da8fb0b57f17d261e08ab7d`  
		Last Modified: Tue, 24 Sep 2024 01:02:20 GMT  
		Size: 22.6 MB (22556824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f722533165416e85a27a107d4938df7781fabcc4355162ea941d472a9af6cfc`  
		Last Modified: Tue, 24 Sep 2024 01:02:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87f380583265e2562d420c9357cbeac949a32f42946b38e3e5a04d758b87dd7`  
		Last Modified: Tue, 24 Sep 2024 01:02:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b953a9f1546f860acc957276a7eb924099066ed6172b69564aa42d0f23dc9e5e`  
		Last Modified: Tue, 24 Sep 2024 01:02:18 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42f49252b863cca0dc332306799f5e8ed1ddccb2e3021f2598e5a8591a0aa01`  
		Last Modified: Tue, 24 Sep 2024 01:02:19 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:76af12330a450a29abcbea22797bf1e153e234d9d49cbf13f7f55c96cf9fb22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17578057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9f879372095eb7c6cc5f4c74239eaab6e13806717dbfddfd06d62c01f3a49`

```dockerfile
```

-	Layers:
	-	`sha256:d7f80736fffea0591ab38af9eeb3d9b9c5e94c8883c109a3a3b0dec211a2162d`  
		Last Modified: Tue, 24 Sep 2024 01:02:19 GMT  
		Size: 2.3 MB (2342391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08af2d6bda52ae29e0ad712f4373fc9e8eb2dd1cdc0c79c1492b58ba132740bb`  
		Last Modified: Tue, 24 Sep 2024 01:02:19 GMT  
		Size: 5.0 MB (5011671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a48a26e41280c7a9d58f91e43ffea873e13b9a85267b25d5f14e78a717b1eec`  
		Last Modified: Tue, 24 Sep 2024 01:02:19 GMT  
		Size: 5.1 MB (5149633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2bd378f52ce7623dfde4fd4cedb1630a14cd8c968825a1973cf006afea53cb`  
		Last Modified: Tue, 24 Sep 2024 01:02:19 GMT  
		Size: 5.0 MB (5013193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a821823f227abcd3117606f5ff7908de035db7061a90f92ab46eced366dae142`  
		Last Modified: Tue, 24 Sep 2024 01:02:20 GMT  
		Size: 61.2 KB (61169 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:f57ab80d4e74c2a8cf094039771c6bc1a7838d172798ee4f8365df27862ebe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104304963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7300b2f7f2bf094144a294a914d4559a2a5bae9d82eaec489242ad0dcd9cd726`
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
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
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
	-	`sha256:1f2f8406c038b8e9e325b83f489874e26b32d2c116d04498872e68fa9179eea8`  
		Last Modified: Tue, 24 Sep 2024 01:19:15 GMT  
		Size: 23.0 MB (22995384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d167709271e9f678bb0c63071516f2a7ea7de51a20a9f8616e8994554b1175`  
		Last Modified: Tue, 24 Sep 2024 01:19:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5b7d6e2e34ee9fa60539f5ba6e3cb5a808b1b3f0fa40d7d9e76e376a1e434c`  
		Last Modified: Tue, 24 Sep 2024 01:19:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582ce731caf68fd13cbf29bfc6f924501444ce4fbe9609dc070ee718a7b59d48`  
		Last Modified: Tue, 24 Sep 2024 01:19:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de889d2618aaca87eb34dc5090417fb1d505312431e18484128d347e84e3e8e`  
		Last Modified: Tue, 24 Sep 2024 01:19:15 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b480125abd59b9588153eed4929d64a2a0b38b52f88b3c61b29eeea20bd2c31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18174392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f27d2c363e81754eeca16cdf077232ef801eca997dcc40ae89b919a9e9113d`

```dockerfile
```

-	Layers:
	-	`sha256:fb5128038293057dd5cc5736353ebf559d08f3afadcfccf98f0cda3c432794ca`  
		Last Modified: Tue, 24 Sep 2024 01:19:14 GMT  
		Size: 2.3 MB (2342442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ef0073cd7d69f9103a4c32fa5e650010406792149fff3ea7b335ef656f56a4`  
		Last Modified: Tue, 24 Sep 2024 01:19:14 GMT  
		Size: 5.2 MB (5209676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752fc970c3f6ec60adce258b472e39e1f28c20e5afc6b3f6743b4259efae6060`  
		Last Modified: Tue, 24 Sep 2024 01:19:14 GMT  
		Size: 5.3 MB (5349791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d40ef51f9da1d3a23b634b276e1956a4a4bfc3f4d3574744a8ad973aa6865a9`  
		Last Modified: Tue, 24 Sep 2024 01:19:14 GMT  
		Size: 5.2 MB (5211198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a686d3439e37c903ce20e766847a8bce4e26806239f55558b62902d483ce3c38`  
		Last Modified: Tue, 24 Sep 2024 01:19:15 GMT  
		Size: 61.3 KB (61285 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:579eae8afd518bf102356fda89e6c74ab636f5ec511ba518f20f09c60eacd38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105700766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08e75a200809c8b4822c606e752249ebfc0c370256d32f415cf60cc9a11d591`
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
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
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
	-	`sha256:830a5c3247755ac80661d24b0eda7bf1b4a98228175816a9bd2981a3b84ea986`  
		Last Modified: Tue, 24 Sep 2024 01:23:31 GMT  
		Size: 23.5 MB (23452596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b8212e7c5357821db90de2d7aaacf4c84d80b51d3912891622c36ea9050004`  
		Last Modified: Tue, 24 Sep 2024 01:23:30 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73700bd07cc49dc2b40ee9b8b89bd32cde35388d288c08d1230b3563a3c13fe`  
		Last Modified: Tue, 24 Sep 2024 01:23:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60ddc61a922f1f3d91c53ea52ae53ddc821bd80e9ff77f23ff9e6579352cd43`  
		Last Modified: Tue, 24 Sep 2024 01:23:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b2c4016f75d32c8944901e98e7737ed2eab00675d5c048df77b797fb770639`  
		Last Modified: Tue, 24 Sep 2024 01:23:31 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7e384714d1e8a53c3ad3b1e07a582511ba82f43b5d6e7402f4d10decc2384e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18031131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665a90c0df9690968fb01d4235a212b220ea80b1cb1077bfd59e58049f95e70c`

```dockerfile
```

-	Layers:
	-	`sha256:218c32df37430430d908218f361d3f23d9c55f26e17044e4a4fe7b4b013f7861`  
		Last Modified: Tue, 24 Sep 2024 01:23:30 GMT  
		Size: 2.3 MB (2345736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b8613b53999d0a8be452cdf43ae3756af11a48217a2c02786ede77f793f1c3`  
		Last Modified: Tue, 24 Sep 2024 01:23:30 GMT  
		Size: 5.2 MB (5160902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad748c883022eb2486d7f4539ab79c9989b4d8b1403d7c0059d2fdc3086b5e13`  
		Last Modified: Tue, 24 Sep 2024 01:23:30 GMT  
		Size: 5.3 MB (5301029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51f27623f0ca20b83a8861b76a7d37fb2963a346f25064f70b1f0c3b2e4de408`  
		Last Modified: Tue, 24 Sep 2024 01:23:30 GMT  
		Size: 5.2 MB (5162424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b764cacb0fb34014896369a43686a9762e1f54fe9884732fd6b0c0366a96ec05`  
		Last Modified: Tue, 24 Sep 2024 01:23:31 GMT  
		Size: 61.0 KB (61040 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:1080c5544efd51bd7670656f7d1378af218f1ae647aa567609c0a2fdd38c721c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98575669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aef2e84a7dcc5d72d2ad8acde9e9bbf88d56fee1db68b277a81a6fcd3f9174`
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
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
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
	-	`sha256:f912c3bb21214a4436a247453efd43a8dc974f42e0c58e09d8bc78867a9831b9`  
		Last Modified: Tue, 24 Sep 2024 01:16:58 GMT  
		Size: 22.9 MB (22890027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dd74bccfebadf99947b3f4ab2b69faefeb096c6a89e6e3e22b24c73bdce771`  
		Last Modified: Tue, 24 Sep 2024 01:16:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579ea6e4618abb7c3d5c97c12647762671fefd38f6c7a4c0cabe3b96101fbf81`  
		Last Modified: Tue, 24 Sep 2024 01:16:54 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e358ffde7c2bbc01fe4a312768d3f43fac74066062c3b228ccdfa52aa8652d2`  
		Last Modified: Tue, 24 Sep 2024 01:16:54 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164843d5e3a68fb82a3fa05158028d21bc7d679ec114bb31915d54a9e7588f7`  
		Last Modified: Tue, 24 Sep 2024 01:16:55 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7f245b46f9587c7abc0586d8feb1397f58f64f5d7ec83d24aa22c82ff0d8dd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17991994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5f7a2f58b8785975df6567589492d10ec6b3772073bc5acf2f3ff587e92c15`

```dockerfile
```

-	Layers:
	-	`sha256:09dec0e4b4df0b76cb1cba721be1dc4f4ee83dd632461e45f9f29992dc958a39`  
		Last Modified: Tue, 24 Sep 2024 01:16:55 GMT  
		Size: 2.3 MB (2334284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0faa5e6b13f7ca86f1f8c54854d7ebd8b61ef0ad3e6051dc114ffd035c6972c`  
		Last Modified: Tue, 24 Sep 2024 01:16:55 GMT  
		Size: 5.2 MB (5152396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8dd4d69808feb34c60e7d364bf857fb4e2fad5461ffe818af8262531766611`  
		Last Modified: Tue, 24 Sep 2024 01:16:55 GMT  
		Size: 5.3 MB (5290356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838bb1a00ae8784637f9639f30b56ef424ce7f375672e968d3e01d9fe4452973`  
		Last Modified: Tue, 24 Sep 2024 01:16:55 GMT  
		Size: 5.2 MB (5153918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e670217522727e4d44b82c212b1c2877d465d1f62ffe174d03d12cfffe8acb9`  
		Last Modified: Tue, 24 Sep 2024 01:16:56 GMT  
		Size: 61.0 KB (61040 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:e8f21ea31b1705cf756f53b069510c95cae6ab7feee5f789b1497461abd4c128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98785165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5ee5bbecf3cd40cabf2061cc8083ed0b0b0e1f74ab02c5bcbc428380a5f2fd`
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
# Sat, 21 Sep 2024 11:05:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 21 Sep 2024 11:05:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_VERSION=4.0.2
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 21 Sep 2024 11:05:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Sep 2024 11:05:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 21 Sep 2024 11:05:30 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 21 Sep 2024 11:05:30 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 21 Sep 2024 11:05:30 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Sep 2024 11:05:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Sep 2024 11:05:30 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 21 Sep 2024 11:05:30 GMT
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
	-	`sha256:ee9fe2f79cc2ba1710f039ccb0e73192d8a8f5bc55c0ea6b6bcc3836d0dc63e9`  
		Last Modified: Tue, 24 Sep 2024 01:27:51 GMT  
		Size: 22.9 MB (22942414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222162206ab7b563b37b161036e79ae5e392163625bbe2bd68258327823c87e3`  
		Last Modified: Tue, 24 Sep 2024 01:27:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baafc3906912389a8ff2967c2d4ea42595a78533b841a87aa7cb8af9cb76935c`  
		Last Modified: Tue, 24 Sep 2024 01:27:51 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d980a146ba1880b865eb3dfdf87afb728803529255ec54a0abd3e312996ae7`  
		Last Modified: Tue, 24 Sep 2024 01:27:50 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91fdde00d55bef925d9033776f0c8d80c804250ccb637e8843769022f75a882`  
		Last Modified: Tue, 24 Sep 2024 01:27:51 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c7364bb1eed1d26e9ddcd87fb19aee06b27a6283e83a739e09a2d6077e1d81f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17661886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08675690b816aa4509041bc2421253d91a38b00c88ffc9ec3e17ed8bbe97b62e`

```dockerfile
```

-	Layers:
	-	`sha256:5d0d68fa38492a6d264a0c142bb9356dded734ef4ba8e9c1dd041224fc8c2379`  
		Last Modified: Tue, 24 Sep 2024 01:27:50 GMT  
		Size: 2.3 MB (2343602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63dc62e3d3c2ebfd68f0f4626b1b104668d3a46c8aa1077e2ec319f1991e5216`  
		Last Modified: Tue, 24 Sep 2024 01:27:51 GMT  
		Size: 5.0 MB (5038925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa69c850261609d8f27ab45096c8a67acc46e99be32449eb08973ac7cfa60bb4`  
		Last Modified: Tue, 24 Sep 2024 01:27:51 GMT  
		Size: 5.2 MB (5177928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039cb783ffed445422c05eba020ed095478cc5a1d35519794760efed94a35f7a`  
		Last Modified: Tue, 24 Sep 2024 01:27:51 GMT  
		Size: 5.0 MB (5040447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f2422040b352a2d242168a8bd3d46799bccebbfd56f07f2b1aea7c807d589b`  
		Last Modified: Tue, 24 Sep 2024 01:27:51 GMT  
		Size: 61.0 KB (60984 bytes)  
		MIME: application/vnd.in-toto+json
