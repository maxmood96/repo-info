## `rabbitmq:3-management`

```console
$ docker pull rabbitmq@sha256:29ded394fc8639f891e0c80fac7b8f594bb8edaa83e15dc8c5795ef8d6c15f6a
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

### `rabbitmq:3-management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:c996f253cdd9a462595c846d01fb799684c4a5a9362590e12287c2c17a5a7520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116466163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e685a2b8c9fa4656cccd7eb12447cb9394b115718d85b6e479fdf3a7d2542bb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ARG RELEASE
# Fri, 20 Sep 2024 21:15:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Sep 2024 21:15:09 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d1f44794c993fbc45976fa00358de76af33389d8356dd5243ae2f9aba5530`  
		Last Modified: Sat, 14 Dec 2024 01:35:24 GMT  
		Size: 45.5 MB (45465014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bc35f205f79490703cefb09110363e832bb222eaab52a6c790f90da3f4ef8e`  
		Last Modified: Sat, 14 Dec 2024 01:35:24 GMT  
		Size: 7.5 MB (7464557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae78677340ad293430810db9c4b4d696a7a9eb4b67cf30e977d7603e28f41a7a`  
		Last Modified: Sat, 14 Dec 2024 01:35:23 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4546f4074dac3752f4cc6935dfe431551330c8798dec9cb849b522d11aedec6`  
		Last Modified: Sat, 14 Dec 2024 01:35:24 GMT  
		Size: 21.3 MB (21313980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4431bdb90a4cbb458cc03fd152f6a8557700176bf658da5c84dae12420746`  
		Last Modified: Sat, 14 Dec 2024 01:35:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18e4e86d7daa4509a3482f60353582bf51ed804d30928c572e299a2572ec11b`  
		Last Modified: Sat, 14 Dec 2024 01:35:25 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb48d524e9120076b41b4d9d55bc14f226060774dc3107e0bff51ad31b5b12dd`  
		Last Modified: Wed, 08 Jan 2025 00:34:50 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dfc1785660130d1b63b011002c8ca6e2e9b0255e61b8a3e2357bd35371d281`  
		Last Modified: Sat, 14 Dec 2024 01:35:25 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2c807d46cb03cc05652253c571cb8f3742cd031b0830afcb999d010e4e3043`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 12.5 MB (12459436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d25087176e4ac4363592322dce42d2aeb0e3f7998f8055c453b00866d4b20997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b67cb0a1ae632d5334d8d426862b10754e4fed70764190361991bf31d771e7`

```dockerfile
```

-	Layers:
	-	`sha256:850a63a04f852cc273886067667e4aafde7d60f6a8e0f268f92e5452ee3f1dc6`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 2.9 MB (2946159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ca0f0a707a2bfa9f17610da69b948868a40f343d4f7966d46e505d8d2645a6`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 11.1 KB (11099 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:cc6fac78e89a570ccbaaf0845c7a140443f1bc88ee52ce2c846d8148dda0898d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98765850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0721525d58688f70ad23f864374d442442710c08c73f02e2639c53d3fe02e9ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ARG RELEASE
# Fri, 20 Sep 2024 21:15:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Sep 2024 21:15:09 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c03c5a15e72b179286cdabba558ae8d463a8d054828d8b77e160d0ac48f524`  
		Last Modified: Sat, 14 Dec 2024 01:57:29 GMT  
		Size: 33.1 MB (33137234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19801a36d2d50efc007f031e714680232d3016c99814e9ef3b7362f7080f4f5f`  
		Last Modified: Sat, 14 Dec 2024 01:57:28 GMT  
		Size: 6.1 MB (6060323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ff15580534aa0649b4e7ce1d9e18fee6c2eb46fa9f906d8786dfd5ed0d1517`  
		Last Modified: Sat, 14 Dec 2024 01:57:27 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd01486ff8f65e288a5c0a0b3c6ecb79a3e99d2d14554c03def098d1a65f10f`  
		Size: 21.2 MB (21215396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ecc32bb7a6681fb578341358e73a1c80cb76ec54fa26b3738e2b2e4caee637`  
		Last Modified: Sat, 14 Dec 2024 01:57:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b3b2e8ea74dcda553e1c9d8a8367f01b8d50d205a5289480a77a31a2e494d3`  
		Last Modified: Sat, 14 Dec 2024 01:57:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfd850d0264621ea9ff03a798b9a14d01b829ec4223b6ef5c23297cde192b24`  
		Last Modified: Sat, 14 Dec 2024 01:57:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93789c7731160f84dac32c30c76a7142c6ddfaab853eebdade0e48868be892c7`  
		Last Modified: Sat, 14 Dec 2024 01:57:30 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16eb214078dcef63b8629e961bf91001c5d54e5452818ce864d51695565fed4b`  
		Last Modified: Sat, 14 Dec 2024 02:18:40 GMT  
		Size: 11.5 MB (11471975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0590bd4d82d5f527523fc02d459c8a5f25eba1ca4aefdcd90b17154583887fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24761802ad35db32404374921a9eacc727c0db38fb2ef929d93dc051ae07ff27`

```dockerfile
```

-	Layers:
	-	`sha256:f2b7959067560dab33808555f7d9cf0a47a0d4fd05171199820067dc3375fa93`  
		Last Modified: Tue, 07 Jan 2025 23:57:39 GMT  
		Size: 2.9 MB (2947104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d39ac94ad2ab7250fcb1a6621a4a66b130181d766fb5224dbffa7722b44f08`  
		Last Modified: Sat, 14 Dec 2024 02:18:38 GMT  
		Size: 11.2 KB (11167 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:c2b6d80433393569c58e5b57b5316f09da846aa620c6b5059fb2670b4358ca2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113096529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eddce06f5949143e3e7e8877e6fa58c67000fefda1e27801fbe832b88bdbe15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ARG RELEASE
# Fri, 20 Sep 2024 21:15:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Sep 2024 21:15:09 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Wed, 08 Jan 2025 00:53:35 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8f03f2cb0e5175aebe5a0bd16260435158a61c5ab85e644f976f7b2e816b99`  
		Last Modified: Sat, 14 Dec 2024 01:58:09 GMT  
		Size: 43.5 MB (43491807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfbb238c88d4822b4a9ceae75806e88689190c5deaa1f9cda877849cb04e97b`  
		Last Modified: Sat, 14 Dec 2024 01:58:08 GMT  
		Size: 7.1 MB (7148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94ce5364dab951a3b1643b651dfcb1c5327f7e2e7cc914b5b5ae22fb57b9d1c`  
		Last Modified: Sat, 14 Dec 2024 01:58:07 GMT  
		Size: 9.4 KB (9426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ebe66341c924285f0e8ba8df8fa4cd266e1fba1184e268ac6e3f2e88316a63`  
		Last Modified: Sat, 14 Dec 2024 01:58:08 GMT  
		Size: 21.2 MB (21222973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a91e40973a893cdb7b9ada301ba48b55b2da8813d34823daec9945098f18e22`  
		Last Modified: Sat, 14 Dec 2024 01:58:08 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f1ab067e10b3b8d3a5ce0f740ed39a419f0ae145625415491391f74cf7e62`  
		Last Modified: Sat, 14 Dec 2024 01:58:09 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc7f7205f1f311c4557b850a0887c05d77ae32a0f763b1c52fe874f3d5326fa`  
		Last Modified: Sat, 14 Dec 2024 01:58:09 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902882b04cfabc7d96f866d75cbccf057b8f53ec0c26cb57a2ae8ab624f91ef8`  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8e9c8ba923f7183d38961b42af57e70f0ed49f0394b0157c6ee160379bcd06`  
		Size: 12.3 MB (12329350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0c7882ebf5e7f32fe3b8cf1933be29ba61d3eb004299d222307d14e109fcc05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352e8a5c5e339a3e1401605dea1f21a63021ee85ba25431d16b7aabbfa0a7288`

```dockerfile
```

-	Layers:
	-	`sha256:a56b2086a52d8701b8b776604622db2b4c48d191bd18cf747d7003286fbfeec1`  
		Last Modified: Sat, 14 Dec 2024 02:12:43 GMT  
		Size: 2.9 MB (2947259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:387c49d7d63598353dcfbba4ec71f8d4685cfd6b1b275db737256ef71a2f20e8`  
		Size: 11.2 KB (11191 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:a8d1d56e4b69b1eba20136d746d5c49ecccc62ad538eb0f739802b6082897f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115703339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b1b99d6e60c9bcf9c9837846e2c00a2988846382e4c62adb1043813f6b967d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ARG RELEASE
# Fri, 20 Sep 2024 21:15:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Sep 2024 21:15:09 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15bc5ba0f4bf56f900b9ea8619b97f25b6c900c625e11b7b473f454fd0ffd38`  
		Last Modified: Sat, 14 Dec 2024 01:53:54 GMT  
		Size: 39.2 MB (39173814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4137b235e080cf10e99422b0760b3d07ec55c25c17ffa770a2632e6e244d9e9`  
		Last Modified: Sat, 14 Dec 2024 01:53:53 GMT  
		Size: 7.9 MB (7876987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59436a64249ed63ff72c1e971f5d0d0548eb77e5371c24c89253ab5ce0273f15`  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49daec1a6527265e31a5eda0b95d2488b33528d8b06cbe94607cc668e7aeaac`  
		Last Modified: Sat, 14 Dec 2024 01:53:53 GMT  
		Size: 21.3 MB (21274655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81797088a4e604c1085101da0074127a5edcde9505ae6e00b6a9591ec9431435`  
		Last Modified: Sat, 14 Dec 2024 01:53:53 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5202a18f0bfda46e267151bd1c7f2be522dc2fdb62fd315216a4e79d53e3d57b`  
		Last Modified: Sat, 14 Dec 2024 01:53:54 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c74919f9d3aa96929ce299ab90967e8c20af2a2d0b7c0890984b76a405ddc1`  
		Last Modified: Sat, 14 Dec 2024 01:53:54 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6201a6409d5cc916123076b3fb553eeb65920d29bf1ff3d021cf6c6b31691bfe`  
		Last Modified: Sat, 14 Dec 2024 01:53:54 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f181f27b422f413267153fb1ac704c62deacb897f264da54322a8a0fd95151c`  
		Last Modified: Sat, 14 Dec 2024 02:10:00 GMT  
		Size: 13.0 MB (12977880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a22035164fc09bcecf98fa948969d52b8843146d6af3062810ae54ea2cf414a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2961918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c5e80302a33c8374ed09c6eb7d986fb67e7125202c6e00c1530c363fe83145`

```dockerfile
```

-	Layers:
	-	`sha256:49bbbccd5b8d1d4ab0e1e2e704023c1fb576d219944ab46eccaa4d48fdeeb0d8`  
		Last Modified: Sat, 14 Dec 2024 02:09:59 GMT  
		Size: 3.0 MB (2950781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0acfc024169acbedaa7d5f47aaa2d9f85dea20e8aa451bbcfdd5d9a3e6ae8a79`  
		Last Modified: Sat, 14 Dec 2024 02:09:58 GMT  
		Size: 11.1 KB (11137 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:f2d1385676f0780603d5e101ff0d3446a01796a2bac115cc82ddf4f929f3dffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108191521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091f368c42c6d5a551664e50aa82b8e85e79db5318ca9a8d9380d4ac82e30f5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ARG RELEASE
# Fri, 20 Sep 2024 21:15:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Sep 2024 21:15:09 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5121deea568e73477f24ed937ca7b93967eaac18e4cfafa273905f7e5611bd`  
		Last Modified: Sat, 14 Dec 2024 04:51:57 GMT  
		Size: 35.0 MB (34956558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2eb054edf39168aec282dead0a749514079b6fc5cd0b7184da650d64f2cd84`  
		Last Modified: Sat, 14 Dec 2024 04:51:53 GMT  
		Size: 8.7 MB (8694434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a40572e77024adf53d9ff7effac65f0cedba9c279426a1aa9a10aeebe93ce1`  
		Last Modified: Sat, 14 Dec 2024 04:51:50 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b448117aac43c8f7893fb69960c6904d2144462e20e38a1bfa3e296e60e82e`  
		Size: 21.2 MB (21226461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49210088cf61a7c11d277b77a1f51d4cd63d9ca49dd854033684309ae77be704`  
		Last Modified: Sat, 14 Dec 2024 04:51:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b116d50a29b22fa71f015d6d9c9e651d1793177ea372f37d64f7a14cc028058`  
		Last Modified: Sat, 14 Dec 2024 04:51:52 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9902fb2efc7877dee1f4bba7bb7aa56ccbd7e688651f1604559c546f7c9c3026`  
		Last Modified: Tue, 07 Jan 2025 23:57:00 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe1f6e57ef1a2666e179775cb11e35f22d3dfb4efd680225daffec0e9443ca9`  
		Last Modified: Sat, 14 Dec 2024 04:51:54 GMT  
		Size: 836.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2812931c2b539f7d86995138b56ffb26e7881320a3a7038e471e43e05483929`  
		Last Modified: Sat, 14 Dec 2024 06:08:49 GMT  
		Size: 12.3 MB (12321986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9a2cc81a5947cfc73e1413f2198559e05b5e8cddb323009a2a007d8e294d1d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2949940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdd564a2c213dbf5540ab0050a97900f8920a45a3207d421359db86bdc96102`

```dockerfile
```

-	Layers:
	-	`sha256:0ed5b00b0df860e9b64e15ce1c75620ded8e9d46120e4516ff05662eec113175`  
		Last Modified: Sat, 14 Dec 2024 06:08:47 GMT  
		Size: 2.9 MB (2938803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c8005f6bdec3c783e9d6954654897a04dec91c70a46cac2a0436f8ba1556e1`  
		Last Modified: Sat, 14 Dec 2024 06:08:46 GMT  
		Size: 11.1 KB (11137 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:68685a11259c0b375359439dfaec4e35a67b1e31ac20d986aa402ad2e7f2b069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109058521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0d43c506f7dd39a9937a2bc7ce0ab973e78f5620334e5348ffffc3b1e52606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Sep 2024 21:15:09 GMT
ARG RELEASE
# Fri, 20 Sep 2024 21:15:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Sep 2024 21:15:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Sep 2024 21:15:09 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Sep 2024 21:15:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_VERSION=3.13.7
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Sep 2024 21:15:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Sep 2024 21:15:09 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Sep 2024 21:15:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Sep 2024 21:15:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Sep 2024 21:15:09 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Sep 2024 21:15:09 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Fri, 20 Sep 2024 21:15:09 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae04d840c47bfbe6f0c8bf26cf7bee2e643eff4a22d56bf3b529e273e0a89a3d`  
		Last Modified: Sat, 14 Dec 2024 01:54:37 GMT  
		Size: 38.3 MB (38273934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d06226c29564803d4ca941079955c47b8cdbee77bb118b04f752357a36379a0`  
		Last Modified: Sat, 14 Dec 2024 01:54:36 GMT  
		Size: 6.8 MB (6760840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba7c1333d5f88570ac56aae02677f6d6fccc186a6d7cfdfaa11ce95495d6767`  
		Last Modified: Sat, 14 Dec 2024 01:54:36 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf278e9a28c6f1db0235de5d1250c3d8cca034fab7534b12eb11b92045fe5740`  
		Last Modified: Sat, 14 Dec 2024 01:54:37 GMT  
		Size: 21.3 MB (21297428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac74956eb78ff2e996e6ece9d8439f7f556f64163012c4ad48f4549e71f8ffd`  
		Last Modified: Sat, 14 Dec 2024 01:54:37 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a6cefadaf52a372435e968d410a4d84a6ed9870721a7ffe7c7dba282d5586c`  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94338eee49ee72bc26bfdc8ba59cf78de664449a32c4cdb8aa6919a8dd1e6593`  
		Last Modified: Sat, 14 Dec 2024 01:54:37 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49181cdce14a9af45394cf148e0bb9c428892176061e73481391b47fd18377a`  
		Last Modified: Sat, 14 Dec 2024 01:54:38 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153512ea8c39c15abfb9ecc4512c1b6152a6db6e78c5e161f25e7ee270da75e2`  
		Last Modified: Sat, 14 Dec 2024 02:13:54 GMT  
		Size: 12.7 MB (12694158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1a87b808f96ab358faf8f52bcbfa6ed6c36016e7c571873647039ec99044cd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2da745264206096e43aef77a0dc5f71f68c6c25792e390f297c5537255009e6`

```dockerfile
```

-	Layers:
	-	`sha256:483741ef1e3e7394a080de6fdbfe50f2ce83206d22908cb0239c22f84696df20`  
		Last Modified: Sat, 14 Dec 2024 02:13:53 GMT  
		Size: 2.9 MB (2948221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c2b07a36e8e9711c3f8949065b7f9136f643ca74b4230a53cd35a2fdb1c6565`  
		Last Modified: Sat, 14 Dec 2024 02:13:52 GMT  
		Size: 11.1 KB (11099 bytes)  
		MIME: application/vnd.in-toto+json
