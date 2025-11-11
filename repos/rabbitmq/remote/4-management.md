## `rabbitmq:4-management`

```console
$ docker pull rabbitmq@sha256:feafdaeb9b10160cc7be31d15060389e2543aad358cd4f476a17b4fbddbfaa09
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
$ docker pull rabbitmq@sha256:f011f92e74b100d390704825f8380b2b2317d58e5bea790fe84f7215623cd62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125285205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3d94609256322568b92daa58ce25bddb415ddd4daa8d21dbbd007f9a303871`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 19:33:17 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:33:17 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:33:17 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:33:17 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:33:17 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:33:17 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:33:18 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 10 Nov 2025 19:33:18 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 10 Nov 2025 19:33:18 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:33:18 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:33:18 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:33:36 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:33:37 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:33:37 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:33:37 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:33:37 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:33:37 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:33:37 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:33:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:33:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:33:37 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:33:37 GMT
CMD ["rabbitmq-server"]
# Mon, 10 Nov 2025 19:48:17 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Mon, 10 Nov 2025 19:48:17 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c224677294271e0dff64aab562311eddaf457226c489ad4a36d92862e746ae`  
		Last Modified: Mon, 10 Nov 2025 19:34:11 GMT  
		Size: 46.3 MB (46257196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d5ec29237baed720a9b09502be8ecea43ac0cc4a6776e5e5ba19c4b58befb1`  
		Last Modified: Mon, 10 Nov 2025 19:34:08 GMT  
		Size: 9.0 MB (8994544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d92d338bdc0607e27429f91c6afc466ecc3f2558e064b366d66c95f2a460b9`  
		Last Modified: Mon, 10 Nov 2025 19:34:06 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f41fb2dec1715da4d6c5dbba92b4c3ee6d971877e474b263f58d1b5a52ece75`  
		Last Modified: Mon, 10 Nov 2025 19:34:10 GMT  
		Size: 27.8 MB (27829739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0624e4bf233123650dfe637a5467169772aba409c66e77fbb2d9e2a9496a7944`  
		Last Modified: Mon, 10 Nov 2025 19:34:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c87aaba0849a9a9951e44d947f3e357234cb9da3a52160aac7e8df8cf421661`  
		Last Modified: Mon, 10 Nov 2025 19:34:06 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa47faad2be73f080ca404f389965759fd0d15e537dc7c54a60d1517abbe8c61`  
		Last Modified: Mon, 10 Nov 2025 19:34:06 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce5bec46020173f65ad7dfd15fdd46832e713a9e4032ec537594f95e5a648b3`  
		Last Modified: Mon, 10 Nov 2025 19:34:06 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547e848114b77a8b3ce6abacec27971208b2509b57d7d3378fe1a0fe5a201b6a`  
		Last Modified: Mon, 10 Nov 2025 19:48:39 GMT  
		Size: 12.5 MB (12469164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:bda07d708367ad4983eb58e04c61ddeee584aecdcc8b666621dd7ede2b9f4d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3110223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50c520d1cf9d5b92275d0fcfede4e33447daaab0a28192cac9388943aec9d4a`

```dockerfile
```

-	Layers:
	-	`sha256:aa5cd12950d9be128139054c57bfda849669bac13abd78532ab43bdaecef6f93`  
		Last Modified: Mon, 10 Nov 2025 22:53:46 GMT  
		Size: 3.1 MB (3098865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968ec29c5fc98f5d5c919a2e694525125a9d602b08734f3396d1fa550a39a3f9`  
		Last Modified: Mon, 10 Nov 2025 22:53:47 GMT  
		Size: 11.4 KB (11358 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:23957cf5d7a4cd3a39798c842af56f6ab3a69e7ed536cc64160c0920a328f556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106673945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecc2be4cc35fbc0fa1cc36f4b625d5b3c7b480380d438333ef724905c9b2d25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 19:31:41 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:31:41 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:31:41 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:31:41 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:31:41 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:31:41 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:31:43 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 10 Nov 2025 19:31:43 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 10 Nov 2025 19:31:43 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:31:43 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:31:43 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:32:07 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:32:08 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:32:08 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:32:08 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:32:08 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:32:08 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:32:08 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:32:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:32:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:32:08 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:32:08 GMT
CMD ["rabbitmq-server"]
# Mon, 10 Nov 2025 19:44:34 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Mon, 10 Nov 2025 19:44:34 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6843622e88f4908794dfddef8e3d05038d7c46856edb69b7bf6fbc8cc878ef72`  
		Last Modified: Mon, 10 Nov 2025 19:32:44 GMT  
		Size: 33.3 MB (33286016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b22b00ee01b2e8f20e43f671da3082b889cb3cbed774b574758440d08df9569`  
		Last Modified: Mon, 10 Nov 2025 19:32:41 GMT  
		Size: 7.3 MB (7309026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea001f4fb89b3401097c81aafbb971c5ddc8bd0af365d61dcd94e2a25c60b7db`  
		Last Modified: Mon, 10 Nov 2025 19:32:39 GMT  
		Size: 9.8 KB (9767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc3f431b9009a683da038328b0f9e519bd7780f7661f6aa87f9b5a74b07b1b`  
		Last Modified: Mon, 10 Nov 2025 19:32:43 GMT  
		Size: 27.7 MB (27731812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b44403b55401fdfc85aabcb01b4263d5d254ff404713a96a5120c91cc78472`  
		Last Modified: Mon, 10 Nov 2025 19:32:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49967f342b07dbd173980ea2b52d66f04d1c6eb30a8b78c92797e5490b86593`  
		Last Modified: Mon, 10 Nov 2025 19:32:39 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6a2364f38e58d0bae029af1dd53f0f3816459eadd52173e786b5f309055e98`  
		Last Modified: Mon, 10 Nov 2025 19:32:39 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d8a2dc18baddfd2a6d45f7fb4d578e258a8e75b0f156b5af5d4b5352cca970`  
		Last Modified: Mon, 10 Nov 2025 19:32:39 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76e010f93a3e64a82b00ce049bb5bed23a3d763564f102ad1f24852839da256`  
		Last Modified: Mon, 10 Nov 2025 19:44:47 GMT  
		Size: 11.5 MB (11483847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c34b68362c3de3476d3230aaef994884af02c9631a70cd7e6ac423214fc8a621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3111259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9581e7cc56901e1aac9318028cca749d0ef6748d2bd1d757d2413726809b1baa`

```dockerfile
```

-	Layers:
	-	`sha256:e4506271c831d7bdbb908c90edaeb29e5b457bc5f73547767a8bfd6cf01b0265`  
		Last Modified: Mon, 10 Nov 2025 22:53:51 GMT  
		Size: 3.1 MB (3099821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:419a465b91d7f3f16a86015e393add5e4ae9df55703a82eb6256534a710dbde7`  
		Last Modified: Mon, 10 Nov 2025 22:53:52 GMT  
		Size: 11.4 KB (11438 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:ad6eeda2336a7e57ae3dda4b7ec23917b5a7d1ded67548b081f9517f0fbf79fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123008534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713ac1659c1dc5d3cb1f5015377f3be65f98112ede2625a3d7c0ac8f31a9ba1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 19:31:28 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 10 Nov 2025 19:31:28 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 10 Nov 2025 19:31:28 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 10 Nov 2025 19:31:28 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 10 Nov 2025 19:31:28 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:31:28 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:31:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 10 Nov 2025 19:31:30 GMT
ENV RABBITMQ_VERSION=4.2.0
# Mon, 10 Nov 2025 19:31:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 10 Nov 2025 19:31:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 10 Nov 2025 19:31:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:31:49 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 10 Nov 2025 19:31:50 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 10 Nov 2025 19:31:50 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 10 Nov 2025 19:31:50 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 10 Nov 2025 19:31:50 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 10 Nov 2025 19:31:50 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 10 Nov 2025 19:31:50 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 10 Nov 2025 19:31:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:31:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:31:50 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 10 Nov 2025 19:31:50 GMT
CMD ["rabbitmq-server"]
# Mon, 10 Nov 2025 19:50:56 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Mon, 10 Nov 2025 19:50:56 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c04de8b38c3c2e316b0910112d1ff5c639b5f72cc0e196c047654c6b6a39ed`  
		Last Modified: Mon, 10 Nov 2025 19:32:32 GMT  
		Size: 44.3 MB (44348706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839c89d839a023dd8a30473139c20871faa1cb7872508f984d4bfa5a6f579b13`  
		Last Modified: Mon, 10 Nov 2025 19:32:27 GMT  
		Size: 9.7 MB (9716294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42433137a8b043bfae37b44976e2b6768f0328a7dcece64bd5db75676f9957`  
		Last Modified: Mon, 10 Nov 2025 19:32:26 GMT  
		Size: 9.7 KB (9659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab84ca738f4c9410894d842c7f5539afbb6cc781005a9f4a7f6ae80963502f5c`  
		Last Modified: Mon, 10 Nov 2025 19:32:28 GMT  
		Size: 27.7 MB (27738902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd61b2d1cad4471aa5a67c59f46e2d937cc7b7e4ab99c9deca1e7bfaa6e1ab61`  
		Last Modified: Mon, 10 Nov 2025 19:32:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4269f2b8f80b9426fe488c3fc8955b7d42806fc35a94e3ba55d967d3e6504c`  
		Last Modified: Mon, 10 Nov 2025 19:32:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aa9ef09af52580096443e4d386ab52aacca14438f7810b2e96f13a510edf6e`  
		Last Modified: Mon, 10 Nov 2025 19:32:26 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6d75c270a36ad485de286a11778f6c8b9bd512f2d2507d698b50470803e5fe`  
		Last Modified: Mon, 10 Nov 2025 19:32:26 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa4c3467560865421bc9bfd9deb8e2172caadba8ea2ba35b96525824dab1044`  
		Last Modified: Mon, 10 Nov 2025 19:51:14 GMT  
		Size: 12.3 MB (12331512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a738567dfe78a5afcaec79faee41a27b91fe36c976c18aab376615e64e127b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3111438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a13c269fcf34b0ce273c1b3c399c37acfc543d042fe0bcba88517becbd8a13`

```dockerfile
```

-	Layers:
	-	`sha256:39326b05582f0a62d3b61d83c101f798646e3e57c9b5df50faf46c67bd1378ca`  
		Last Modified: Mon, 10 Nov 2025 22:53:57 GMT  
		Size: 3.1 MB (3099977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb5ecd8ba5b377df1097154b7754e061db021fdcbede013065e2f690e8c0d11`  
		Last Modified: Mon, 10 Nov 2025 22:53:58 GMT  
		Size: 11.5 KB (11461 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:4907e44c806909ab6db9dfa45cda89d7b4c57a88cbb3519cf35e1d42e891a745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124176094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf144579395bb28c5d848092fc95e70ec256c4b477e6374867d1f210c5a36e71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 20:15:31 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:15:31 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:15:31 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:15:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:15:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:15:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:15:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 31 Oct 2025 20:15:34 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:15:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:15:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:15:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:16:06 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:16:08 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:16:08 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:16:08 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:16:08 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:16:08 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:16:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:16:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:16:09 GMT
CMD ["rabbitmq-server"]
# Fri, 31 Oct 2025 21:10:55 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 31 Oct 2025 21:10:55 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325c79e41fcbae266047468ab66dd41e4bed0764c393f9ea319ebc79b392058b`  
		Last Modified: Fri, 31 Oct 2025 20:17:13 GMT  
		Size: 39.5 MB (39507485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77621a0e3fff9fc8ac739734dfa4eb76d4cb8d5834a36d9611f0eba97c7b0bf0`  
		Last Modified: Fri, 31 Oct 2025 20:17:11 GMT  
		Size: 9.6 MB (9598260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a65b4282ca15ef9699fc52fa4f24cd04f4648074930016324bd1d11c90e0a`  
		Last Modified: Fri, 31 Oct 2025 20:17:10 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25893926e802da69ba63554a3fea6158a1019a241a02d32ea73a6b83ff0e7c`  
		Last Modified: Fri, 31 Oct 2025 20:17:17 GMT  
		Size: 27.8 MB (27790248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fb8bc1c9188da7471131e1a70cf90785225a53f85d45a35fc223f73a08e5e3`  
		Last Modified: Fri, 31 Oct 2025 20:17:10 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91b57ae7e6e351f2dbd6c85259b63187db37e676b2d7da884cba1a9746fe38c`  
		Last Modified: Fri, 31 Oct 2025 20:17:10 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84642b48189059d841d4e668c2fa037ba122cdcd8782d153a262fb4d8a2c18bb`  
		Last Modified: Fri, 31 Oct 2025 20:17:10 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168010fff49a23baf3b2779b3ac43eafac34608bd2de8c8e11889e5e7f53d803`  
		Last Modified: Fri, 31 Oct 2025 20:17:10 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6942c895e0a7ee917f6c3867959620313808aeed21c7c0fad8a2f40d481fba96`  
		Last Modified: Fri, 31 Oct 2025 21:11:31 GMT  
		Size: 13.0 MB (12965192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ee04771bbcae7ea61ec0756346aa271206eeaad40b444977ebeb8aeae83f1dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3115004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b06cf96a3669ec1336ec2b89d5564a2dc98830d067189a5437be6c31e5ad328`

```dockerfile
```

-	Layers:
	-	`sha256:04e329bdca07d2450a998eef88dd8b63a75d8740c6e525ca2500b07e9dccadc7`  
		Last Modified: Sat, 01 Nov 2025 00:53:25 GMT  
		Size: 3.1 MB (3103602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77af16234cf4d2b236e5f1d0c36c349a1211a1e7933093877e40531e52a53e54`  
		Last Modified: Sat, 01 Nov 2025 00:53:25 GMT  
		Size: 11.4 KB (11402 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:a57a7d7c342c0fd1635e7dac677c89bde63528d6db38acac89d1a55adb6bdb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117020064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb311b9736ec7692405b8b5c3d7bf82ba94c602c922a9ae058aea5cc67207d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:48:30 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:48:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:48:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:48:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:49:22 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Wed, 01 Oct 2025 13:49:27 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 21:39:11 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 21:39:11 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 21:39:11 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 21:39:12 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 21:39:12 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 21:39:12 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 21:39:15 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 31 Oct 2025 21:39:15 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 21:39:15 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 21:39:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 21:39:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 21:41:23 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 21:41:33 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 21:41:33 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 21:41:33 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 21:41:33 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 21:41:33 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 21:41:33 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 21:41:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 21:41:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 21:41:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 21:41:34 GMT
CMD ["rabbitmq-server"]
# Sat, 01 Nov 2025 03:02:44 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Sat, 01 Nov 2025 03:02:44 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2629f518d6cbb00d4d487d070a2124827dbb18a9a5616c1a693a75cd17dadc08`  
		Last Modified: Fri, 31 Oct 2025 21:48:10 GMT  
		Size: 35.1 MB (35147461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f16af7a584e6aca60eb34083c925779fbadbdacd03737762df5059fe029fd2`  
		Last Modified: Fri, 31 Oct 2025 21:48:05 GMT  
		Size: 10.8 MB (10831068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3c6ef3950944d27d9706dfddb8ee695e98d3f90f56e09d3aa5491bba349361`  
		Last Modified: Fri, 31 Oct 2025 21:48:04 GMT  
		Size: 9.7 KB (9705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea74b800bb1b6e256eb6cb2d79492accd8fb72d186418e9af745be395bb382d7`  
		Last Modified: Fri, 31 Oct 2025 21:48:07 GMT  
		Size: 27.7 MB (27743222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b3b77c1fcc5c7da4bdb63d63dd9802154a11a3390463cce53396d2a0c0b5cb`  
		Last Modified: Fri, 31 Oct 2025 21:48:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0f6c84a191a2f5156135d6df6417a952bd852bca5395b5c18d4f64cda66239`  
		Last Modified: Fri, 31 Oct 2025 21:48:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc33f0cfa3fd6c829672eb63cad8720c2cc3873870a51269f8d80ab8a80702`  
		Last Modified: Fri, 31 Oct 2025 21:48:04 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a3190674041ccc6d07a38ca8ccec5a2146a8d13f8dba92b708ae4933d16ad`  
		Last Modified: Fri, 31 Oct 2025 21:48:04 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f455c742190a4163561fdfca5a475250e79d7ad5ed793be160dabf194c734411`  
		Last Modified: Sat, 01 Nov 2025 03:04:36 GMT  
		Size: 12.3 MB (12335476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b51eb7b5a3f61a6d20722e9eff8d6e47d06dfc54ae0589c94d811b2ef6e42103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3102712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c137ac48bbc39ce334fe75cccf8c239719daa9099dfab8e0a337c1eed1cc01b2`

```dockerfile
```

-	Layers:
	-	`sha256:7ef4adbe5bff90af68ba958217f6a8d83659aa521c37e00edb75be9decd2598c`  
		Last Modified: Sat, 01 Nov 2025 03:52:47 GMT  
		Size: 3.1 MB (3091308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b14f2e946a7095250fde1195dc03e65875759644a4453acb29062b5a962e52`  
		Last Modified: Sat, 01 Nov 2025 03:52:47 GMT  
		Size: 11.4 KB (11404 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:0e6ebb11bdeae3737f22497ebdb54ea6f8048b47cfda080c0e07bd686703533d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117610259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31cc4af5131a4c5544b7d0f937f02d17860843ee70513ef02d866da6861881d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:05 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:07 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Wed, 01 Oct 2025 13:02:07 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 20:16:45 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 31 Oct 2025 20:16:45 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 31 Oct 2025 20:16:45 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 31 Oct 2025 20:16:46 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 31 Oct 2025 20:16:46 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:16:46 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:16:47 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 31 Oct 2025 20:16:47 GMT
ENV RABBITMQ_VERSION=4.2.0
# Fri, 31 Oct 2025 20:16:47 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 31 Oct 2025 20:16:47 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 31 Oct 2025 20:16:47 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:17:02 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 31 Oct 2025 20:17:02 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 31 Oct 2025 20:17:03 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 31 Oct 2025 20:17:03 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 31 Oct 2025 20:17:03 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 31 Oct 2025 20:17:03 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 31 Oct 2025 20:17:03 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 31 Oct 2025 20:17:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 20:17:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 20:17:03 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 31 Oct 2025 20:17:03 GMT
CMD ["rabbitmq-server"]
# Fri, 31 Oct 2025 21:10:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 31 Oct 2025 21:10:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adad4ec1beb8e787df134f5b75b78a8e09e7382027a28049e234fc86fc7af9c1`  
		Last Modified: Fri, 31 Oct 2025 20:17:48 GMT  
		Size: 38.6 MB (38576724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08af553f8baf7da90caedeee0333c05edb0b3b0bb927cef815ae27a0ef2f68`  
		Last Modified: Fri, 31 Oct 2025 20:17:46 GMT  
		Size: 8.6 MB (8623241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c432a8f4ac2866b377933753f44ef485c5c5656b07df969b7bb578ae67929a92`  
		Last Modified: Fri, 31 Oct 2025 20:17:43 GMT  
		Size: 9.8 KB (9803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7ff7598ceb04263af76f09ef8b58c8b7719fa60f9cd364ab4f6f55db550eab`  
		Last Modified: Fri, 31 Oct 2025 20:17:48 GMT  
		Size: 27.8 MB (27813098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d51f6cb93828eac615f33a5885b52ee41ac7f6cd5981d5eb1e8a10216faae7`  
		Last Modified: Fri, 31 Oct 2025 20:17:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02a45d4c8a3f61ce80b801a6e1d56b183ee659fe81e637021aeb7e771e616f`  
		Last Modified: Fri, 31 Oct 2025 20:17:43 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990c723b404939b0afd5515acb0b7bc21f264a9ddf49d31248b2e1792258723b`  
		Last Modified: Fri, 31 Oct 2025 20:17:43 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7604013d0381f3f17f100745e8646e89704f022870f801f0ada9675309e1f66`  
		Last Modified: Fri, 31 Oct 2025 20:17:44 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bc9aa7a559a0280bdc49d43344cf09a480b1831396a27d0ce3ef646ee7c543`  
		Last Modified: Fri, 31 Oct 2025 21:11:24 GMT  
		Size: 12.7 MB (12679498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:efd6f2325b2448703ba61a2f5966d6fbb92e038dd96022e2d60c5659488ea23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3112281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56a39b0477f6c706883eccbf5e03f35aa9da1a18d474a03e092e23e2aa6383a`

```dockerfile
```

-	Layers:
	-	`sha256:f83e3e6b18d90a8288c92e60fc663561cbe5bd94cf6b7f400c7d75ab653f9ace`  
		Last Modified: Sat, 01 Nov 2025 00:53:31 GMT  
		Size: 3.1 MB (3100923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e0b1b73b0a5dbab4c7e15a86cb14aa86a05b40aa779dd1fe06584ae60839e7`  
		Last Modified: Sat, 01 Nov 2025 00:53:32 GMT  
		Size: 11.4 KB (11358 bytes)  
		MIME: application/vnd.in-toto+json
