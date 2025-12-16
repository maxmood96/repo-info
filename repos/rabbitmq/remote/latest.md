## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:a2604857deaf68beaab7cc1951dc07524a84c4d8f136db69da0636c35ed61274
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
$ docker pull rabbitmq@sha256:01ca61f955a1514358d8e6b16132beeaa2f755b58c434875114e1a19b19d67e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112873961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df7ca7f8409a9c0317bbbba38689b566b329869a173b50d2f3e58c7a3f393f8`
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
# Tue, 16 Dec 2025 00:08:59 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 16 Dec 2025 00:08:59 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 16 Dec 2025 00:08:59 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 16 Dec 2025 00:08:59 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 16 Dec 2025 00:08:59 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:08:59 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 16 Dec 2025 00:09:00 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 16 Dec 2025 00:09:00 GMT
ENV RABBITMQ_VERSION=4.2.2
# Tue, 16 Dec 2025 00:09:00 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 16 Dec 2025 00:09:00 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 16 Dec 2025 00:09:00 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:09:19 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 16 Dec 2025 00:09:20 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 16 Dec 2025 00:09:20 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 16 Dec 2025 00:09:20 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 16 Dec 2025 00:09:20 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 16 Dec 2025 00:09:20 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 16 Dec 2025 00:09:20 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 16 Dec 2025 00:09:20 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 16 Dec 2025 00:09:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Dec 2025 00:09:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Dec 2025 00:09:20 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 16 Dec 2025 00:09:20 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37939810e88fd8cba34b05388f1453400e40dcd87b177de6b9ce2f584c34e543`  
		Last Modified: Tue, 16 Dec 2025 00:09:56 GMT  
		Size: 46.3 MB (46261541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd960ab3c8377e7d4e4bdb0940f1c1daad569821f141718c11650fcfd6554efe`  
		Last Modified: Tue, 16 Dec 2025 00:09:54 GMT  
		Size: 9.0 MB (8994559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e49b13700c5a84f785b47e486bbef6ea0e3b0b15de3fbf4397c7f7e55f12d8`  
		Last Modified: Tue, 16 Dec 2025 00:09:51 GMT  
		Size: 9.7 KB (9680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301e38d0245a2187a2f624b892963624c6ce85732cb6afe41a4f633dd0efe4c2`  
		Last Modified: Tue, 16 Dec 2025 00:09:54 GMT  
		Size: 27.9 MB (27881747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca3ae779fd9f836d1dcb08517e881e538bc17e1db5b8b2c7e2f3393a2b7488`  
		Last Modified: Tue, 16 Dec 2025 00:09:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad36e3b6040a794642e61387cd460cb6db75d8c69a27ac1cc9b519336d1c10b`  
		Last Modified: Tue, 16 Dec 2025 00:09:52 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c714900b34f22edfa9211ee181cd4d786fcb7833e8417a243dad5a0ddf667993`  
		Last Modified: Tue, 16 Dec 2025 00:09:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b22d1d2a9efde13c3c35b0d928ad91b8cc92f17e2da69740558b1ee6829fa37`  
		Last Modified: Tue, 16 Dec 2025 00:09:51 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1636ef82eaa9c60a2c67cad3d19eb7b128e16ff31e7fa8dc8796eea1e6c40a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18840297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0f87dfa79d96f91b5bceb5b878ecaec656b5bccf7d475881d6af77e4612194`

```dockerfile
```

-	Layers:
	-	`sha256:e36d88db67146b395cf88c1e8fdf85e453c83285496c7baca40b080e843a965e`  
		Last Modified: Tue, 16 Dec 2025 01:52:37 GMT  
		Size: 2.5 MB (2486587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa59ae648dbb1d5606400cb2f41e64801f5c420cc935a43520ca186e89a349d0`  
		Last Modified: Tue, 16 Dec 2025 01:52:38 GMT  
		Size: 5.4 MB (5378389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97389df0c6c5d1abe7d2b08d0e5e89df3badcbd47976b2c53d1f2eb2c788ac8e`  
		Last Modified: Tue, 16 Dec 2025 01:52:39 GMT  
		Size: 5.5 MB (5534998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec20115987c87af5b28b1e87fd27740bdaace4567717b398e6420730af5027fb`  
		Last Modified: Tue, 16 Dec 2025 01:52:40 GMT  
		Size: 5.4 MB (5380131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888362af6c1a1faee90d8d50577fa54acef3c40db9060c98907bf15860df1f56`  
		Last Modified: Tue, 16 Dec 2025 01:52:42 GMT  
		Size: 60.2 KB (60192 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:ebb9bcfbaa27f35d18b26e8d813f3d2ef7dc0cdf40a3e8c4fbbc5ff4faa58504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95250423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e50d6f4b75e4eca17bdc30d79432c16cfc4f86959fc92e161e053969656ea3`
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
# Tue, 16 Dec 2025 00:06:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 16 Dec 2025 00:06:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 16 Dec 2025 00:06:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 16 Dec 2025 00:06:51 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 16 Dec 2025 00:06:51 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:06:51 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 16 Dec 2025 00:06:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 16 Dec 2025 00:06:53 GMT
ENV RABBITMQ_VERSION=4.2.2
# Tue, 16 Dec 2025 00:06:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 16 Dec 2025 00:06:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 16 Dec 2025 00:06:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:07:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 16 Dec 2025 00:07:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 16 Dec 2025 00:07:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 16 Dec 2025 00:07:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 16 Dec 2025 00:07:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 16 Dec 2025 00:07:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 16 Dec 2025 00:07:16 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 16 Dec 2025 00:07:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 16 Dec 2025 00:07:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Dec 2025 00:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Dec 2025 00:07:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 16 Dec 2025 00:07:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6cdc0abf996c3192bfbda4018d34c282871d4be33fb369176002cb2199673adf`  
		Last Modified: Tue, 16 Dec 2025 10:09:21 GMT  
		Size: 26.9 MB (26852672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb94c3b234eb8d2335f0b47377fef092dd893319f63de5c66913edeb4fc0cad`  
		Last Modified: Tue, 16 Dec 2025 00:08:05 GMT  
		Size: 33.3 MB (33295190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8eaaa9ca98ccf6c105ba126950e8b1a9a9ef8f46b769a446ed827f80c5b2222`  
		Last Modified: Tue, 16 Dec 2025 00:07:58 GMT  
		Size: 7.3 MB (7309016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90622a3110b8e907a6e8caab5df26c08b49127f84ebfdc13307e189b2e9fff2`  
		Last Modified: Tue, 16 Dec 2025 00:07:56 GMT  
		Size: 9.8 KB (9780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83328399df426fa918070ad35e1609b0ef626a9e96f71fa755d47e92bce182c8`  
		Last Modified: Tue, 16 Dec 2025 00:07:59 GMT  
		Size: 27.8 MB (27782018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617272002b1371c2c4801263106085cb9d84b52c33eaac9375f01a8e5af38415`  
		Last Modified: Tue, 16 Dec 2025 00:07:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7803548e413dff01e1939bd3415f921d133ed81569ee687230af62d626c4a282`  
		Last Modified: Tue, 16 Dec 2025 00:07:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c5321202e3342185329ec4399d10df173bde352bec23135ef2bf470e5c66e7`  
		Last Modified: Tue, 16 Dec 2025 00:07:56 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e54b0d4f0da8d8b615384b989d031873c4f161f30b9e8ff2b9057b7c5230440`  
		Last Modified: Tue, 16 Dec 2025 00:07:56 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:06d7a659083bed053115c2c696ec0d86f534fa6e26de32539cdb98abd4308073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18295079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec503bfd226281f0ec3d3023413969c6c72091d8eb609608b568bf5bed4b6056`

```dockerfile
```

-	Layers:
	-	`sha256:adf17aaf9f8d65e764038445b2ed88c2a8731c57cb917f167549b7e29760d794`  
		Last Modified: Tue, 16 Dec 2025 01:52:52 GMT  
		Size: 2.5 MB (2487387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14e071419720ba8724b214d9d7f987d708031f45f896e3f0b37422a215ffef2`  
		Last Modified: Tue, 16 Dec 2025 01:52:54 GMT  
		Size: 5.2 MB (5197169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7be15868800c00a021e8a7d0d0c4c414999cc4b0d9ec05a3e6e51ebe343713b1`  
		Last Modified: Tue, 16 Dec 2025 01:52:57 GMT  
		Size: 5.4 MB (5351223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4557378742621f2bf9e849dfd60ace4cfc03064a08055ce53a51c8226a6252b`  
		Last Modified: Tue, 16 Dec 2025 01:52:58 GMT  
		Size: 5.2 MB (5198911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b7f790c87c3312b58ddd5a6fe91518c88001258a137d18295e46933840c156`  
		Last Modified: Tue, 16 Dec 2025 01:52:59 GMT  
		Size: 60.4 KB (60389 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:a88c55cae51978700d88d4f774aba77330035571fa20b006abf36d9f0bd6c9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110735622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbad84af1348bc58105ee9ac8f1651a06438d4c5ca1c763ed213709ba174fbe`
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
# Tue, 16 Dec 2025 00:08:49 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 16 Dec 2025 00:08:49 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 16 Dec 2025 00:08:49 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 16 Dec 2025 00:08:49 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 16 Dec 2025 00:08:49 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:08:49 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 16 Dec 2025 00:08:50 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 16 Dec 2025 00:08:50 GMT
ENV RABBITMQ_VERSION=4.2.2
# Tue, 16 Dec 2025 00:08:50 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 16 Dec 2025 00:08:50 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 16 Dec 2025 00:08:50 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:09:11 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 16 Dec 2025 00:09:12 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 16 Dec 2025 00:09:12 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 16 Dec 2025 00:09:12 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 16 Dec 2025 00:09:12 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 16 Dec 2025 00:09:12 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 16 Dec 2025 00:09:12 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 16 Dec 2025 00:09:12 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 16 Dec 2025 00:09:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Dec 2025 00:09:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Dec 2025 00:09:12 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 16 Dec 2025 00:09:12 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9298c157bee586a6bbe38cbbf11cfc393d0004b5e0f76c471e49edb719e6068`  
		Last Modified: Tue, 16 Dec 2025 00:09:50 GMT  
		Size: 44.4 MB (44355188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e17162cb01d7e07b8c0c188a10d5e313228ca5aff31dade23cfe7753a16e35b`  
		Last Modified: Tue, 16 Dec 2025 00:09:46 GMT  
		Size: 9.7 MB (9716233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7226f31bb2556d407ff1de54bf3b6152d0e06ec7275c9346c0bda1f349cd9b52`  
		Last Modified: Tue, 16 Dec 2025 00:09:45 GMT  
		Size: 9.6 KB (9641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d8edac46be124a453b5750680e17baad346bd24a9112cfba1f7c87b4d3907e`  
		Last Modified: Tue, 16 Dec 2025 01:09:57 GMT  
		Size: 27.8 MB (27790859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb17837911bc24f85792c5eeca3c8d29aa7652ee6aabef1bcd7928e15e5beba`  
		Last Modified: Tue, 16 Dec 2025 00:09:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f307b23cb7bc3f532f494958cff3eac5c1c258f4f1d19c24daa72f882f6613`  
		Last Modified: Tue, 16 Dec 2025 00:09:45 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aaa8c394a3a848a3e2aa803550b40e1efa7903f6f32e149e2ec52242a5b190`  
		Last Modified: Tue, 16 Dec 2025 00:09:47 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ff1ec8d0faa00e093483e799135293aa6c3fd37b81826ba1b02b7f51eea965`  
		Last Modified: Tue, 16 Dec 2025 00:09:46 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e166b2ea409e36ba467c286a0f7985806f50b8e15adf511189e1cef4952642fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18899277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e7f0488c215a3baaa6766e889531c2804e3ce24cb1ed9585934b401209c3da`

```dockerfile
```

-	Layers:
	-	`sha256:d5197211085c3f2e2aa77bfda59a59816c9dd8d9b8c1f2e97d9dc82819e53e03`  
		Last Modified: Tue, 16 Dec 2025 01:53:09 GMT  
		Size: 2.5 MB (2487647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a802039c63b0c78e08c3e404f2fddd54a9521f4902e709a1b3c7f8be12d0d18`  
		Last Modified: Tue, 16 Dec 2025 01:53:11 GMT  
		Size: 5.4 MB (5397610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af34cf8a0047430fd905c742840f0ad4ffb05a62801cd5f33bc2f4f6c2ba26bd`  
		Last Modified: Tue, 16 Dec 2025 01:53:12 GMT  
		Size: 5.6 MB (5554237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccada1ec22f61551117798681fb072e3bc15cc1740d726a26edf35f88b6589bf`  
		Last Modified: Tue, 16 Dec 2025 01:53:13 GMT  
		Size: 5.4 MB (5399352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eec51cd2b3c573429baf5dc1123c3afce3febb2a55e80cd87075da11aaf85071`  
		Last Modified: Tue, 16 Dec 2025 01:53:14 GMT  
		Size: 60.4 KB (60431 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:023bdbb88ceb5a527018ce47e5d2898215bd0aaa1235a4109f66e2a6ba466a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111265202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76d0742cf92323ef843037a6316c40281753daf88b12083d607e4ab3b22f09d`
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
# Sat, 13 Dec 2025 00:27:10 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:27:10 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:27:10 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:27:11 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:27:11 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:27:11 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:27:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 13 Dec 2025 00:27:13 GMT
ENV RABBITMQ_VERSION=4.2.2
# Sat, 13 Dec 2025 00:27:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:27:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:27:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:02:23 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 16 Dec 2025 00:02:25 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 16 Dec 2025 00:02:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 16 Dec 2025 00:02:25 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 16 Dec 2025 00:02:25 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 16 Dec 2025 00:02:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 16 Dec 2025 00:02:25 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 16 Dec 2025 00:02:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 16 Dec 2025 00:02:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Dec 2025 00:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Dec 2025 00:02:27 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 16 Dec 2025 00:02:27 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fb2b05b9bfac5a6b13d155f7dc5ad103bb9c4b74e30ed58847c84024a0f6c4`  
		Last Modified: Sat, 13 Dec 2025 00:29:12 GMT  
		Size: 39.5 MB (39509500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc09ded348e01cbd39b71918fd46c1e6fd27557ebbee7d783d45fa46bd80063`  
		Last Modified: Sat, 13 Dec 2025 00:29:07 GMT  
		Size: 9.6 MB (9598278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a049bd8c3708de6ccca1af25490726499f99c8b81c31117e7e9ee7aba4e4c5`  
		Last Modified: Sat, 13 Dec 2025 00:29:06 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487430538073fef51cb46e03620223284341f4a6214f84722dcd4043ad27d6e`  
		Last Modified: Tue, 16 Dec 2025 00:08:36 GMT  
		Size: 27.8 MB (27841620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a050894a70d3b116cd8681eedb7c2caca88a66742cdbb112cd2512e417e3de`  
		Last Modified: Tue, 16 Dec 2025 00:08:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd11e81bb9afd6a9074317791f8698f52272a0f33956644932ffa675bca9cb0`  
		Last Modified: Tue, 16 Dec 2025 00:08:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b3d8552e02b8406c100cee0581060e1201f578529959d4c15cbbd9867d0353`  
		Last Modified: Tue, 16 Dec 2025 00:08:29 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08293556bd31f51da2cd16e41f67d50d14c53a8a226e147169f14845428d38ca`  
		Last Modified: Tue, 16 Dec 2025 00:08:29 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c60ae83f10ab5ab0ddf6e03247df9f9131397c8b537e084336def3aed92db6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18754668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d267a27527b7e45d12659933a371a4664376e3451727f4fb07b643c8267192`

```dockerfile
```

-	Layers:
	-	`sha256:2d0f02e5437eeb027ead70ccf5a2c1e3c0eb646bfda4b35614189e722e5deea5`  
		Last Modified: Tue, 16 Dec 2025 01:53:25 GMT  
		Size: 2.5 MB (2491040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b279dbc881bb5c88451ea23f7c85cf69e6b0d3da15758a4db81a378c89030470`  
		Last Modified: Tue, 16 Dec 2025 01:53:28 GMT  
		Size: 5.3 MB (5348331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc8ec19a081c8dd4c5dd5686760ae4b340be8754b1efabab6911d66660604ab`  
		Last Modified: Tue, 16 Dec 2025 01:53:29 GMT  
		Size: 5.5 MB (5504970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57750fb38b3347e92f19a994023859ddb61bb1dbbaa91bb35d087de83b291f0`  
		Last Modified: Tue, 16 Dec 2025 01:53:31 GMT  
		Size: 5.4 MB (5350073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd805145acf936c7353d13810abaac9d4492e6805466a69e2ad8190fbb778161`  
		Last Modified: Tue, 16 Dec 2025 01:53:32 GMT  
		Size: 60.3 KB (60254 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:2106d97365616430e8ae59a1ec43391784fd628998b73af346a39ac6c20a6bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104700953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c3a3463f43ab5267c0a0f1ed71413e5ff81172a298186a031d8e9febaddcc4`
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
ENV RABBITMQ_VERSION=4.2.1
# Sat, 15 Nov 2025 14:46:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 15 Nov 2025 14:46:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 15 Nov 2025 14:46:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 14 Dec 2025 12:38:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sun, 14 Dec 2025 12:38:34 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sun, 14 Dec 2025 12:38:35 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sun, 14 Dec 2025 12:38:35 GMT
ENV HOME=/var/lib/rabbitmq
# Sun, 14 Dec 2025 12:38:35 GMT
VOLUME [/var/lib/rabbitmq]
# Sun, 14 Dec 2025 12:38:35 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sun, 14 Dec 2025 12:38:35 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sun, 14 Dec 2025 12:38:35 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sun, 14 Dec 2025 12:38:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Dec 2025 12:38:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Dec 2025 12:38:35 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sun, 14 Dec 2025 12:38:35 GMT
CMD ["rabbitmq-server"]
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
	-	`sha256:ee7c33dcd3f16fc76095ce402dc9bae04d4a566a02652726944080b23942b9ce`  
		Last Modified: Sun, 14 Dec 2025 13:45:10 GMT  
		Size: 27.8 MB (27758224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3c281512c59a4940df008c0c7a3fde48520fd6fab92a34f15f9ad8be198606`  
		Last Modified: Sun, 14 Dec 2025 13:45:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795a26b42a58dc726b489f6a531cc0f84f8afa881a916dca71faa4cced613955`  
		Last Modified: Sun, 14 Dec 2025 13:45:03 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa99b661d3a6872e519eb11e7e5edfbc7c6e59727e8c723acf38ecbb9c884a6`  
		Last Modified: Sun, 14 Dec 2025 13:45:03 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5378fb1ac6c25f72d4a50092cc573f0398b786ef828229db341f6aaf6cad99f`  
		Last Modified: Sun, 14 Dec 2025 13:45:03 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cce7741cdeb79880a3e13f419646678501c118ffcd41dcdbaa6ed7f8a262d40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18724568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04ee2085e3c077b760dd023a3d0d5690f1e7970034ef43d79c74e58148e37aa`

```dockerfile
```

-	Layers:
	-	`sha256:28fe58e7bf3ff56530a6525a3d087a7cb4d270c84de7939f3396c70343926041`  
		Last Modified: Sun, 14 Dec 2025 19:52:57 GMT  
		Size: 2.5 MB (2480221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:945a67bdcb8b49c47b1dd46babd80539c20b1d6bf1f81a9bdd5e789638ce0156`  
		Last Modified: Sun, 14 Dec 2025 19:52:58 GMT  
		Size: 5.3 MB (5342764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e50775887405de1fa8752b18f69d29507436eea3c6518a375f501491c60a0ab4`  
		Last Modified: Sun, 14 Dec 2025 19:52:59 GMT  
		Size: 5.5 MB (5496816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57a6a299198941e7c34648cc859dfbacc91f19f3e46961f8a68d0beca3083ac5`  
		Last Modified: Sun, 14 Dec 2025 19:53:03 GMT  
		Size: 5.3 MB (5344506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea2186d1d636812de61039a1dfbd9166e4bf9bc88c51125de7c636900dffab1`  
		Last Modified: Sun, 14 Dec 2025 19:53:04 GMT  
		Size: 60.3 KB (60261 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:bc7b4f7972d2ce5a45e9e80581f3a4dfca3ba3e033f14d8ae0a631513757dfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104988474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b165b6c8446a48a4f8835c6b9b58b06ee0e08a4d10ba6270e58f93c3c7895a7a`
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
# Sat, 13 Dec 2025 00:26:24 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:26:24 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:26:24 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:26:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:26:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:26:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:26:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 13 Dec 2025 00:26:25 GMT
ENV RABBITMQ_VERSION=4.2.2
# Sat, 13 Dec 2025 00:26:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:26:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:26:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:01:47 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 16 Dec 2025 00:01:48 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 16 Dec 2025 00:01:48 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 16 Dec 2025 00:01:48 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 16 Dec 2025 00:01:48 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 16 Dec 2025 00:01:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 16 Dec 2025 00:01:48 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 16 Dec 2025 00:01:48 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 16 Dec 2025 00:01:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Dec 2025 00:01:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Dec 2025 00:01:48 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 16 Dec 2025 00:01:48 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Mon, 15 Dec 2025 22:07:51 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febfe086cd68bf68b2e134d354c4622571ed56d6b4734e2bb1b6a1f0784b7ef3`  
		Last Modified: Sat, 13 Dec 2025 00:27:28 GMT  
		Size: 38.6 MB (38581029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4c5fed9133ab96b9caf901771c5e17cc6db3496cdb190fd6a3d1ae79d12cba`  
		Last Modified: Sat, 13 Dec 2025 00:27:27 GMT  
		Size: 8.6 MB (8623220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52460cff6d9032b093cd24414e11ae4f3a8192bef37587ae9ceb8a41e4facea7`  
		Last Modified: Sat, 13 Dec 2025 00:27:29 GMT  
		Size: 9.8 KB (9821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb207d237dd39a60ebddaa90f395dc9bc56e91cb639debb9b0fc0a65a99ac860`  
		Last Modified: Tue, 16 Dec 2025 00:07:46 GMT  
		Size: 27.9 MB (27865063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a355ec85aa2b8cd716d0c134f59cbcf0a3414a5742b579b1416364e0c4138ad0`  
		Last Modified: Tue, 16 Dec 2025 00:07:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3653b862f538aefa561a5ec3e0332f9b4091e86dd3c28319c9e0f782cc94a50a`  
		Last Modified: Tue, 16 Dec 2025 00:06:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db78d4bfeb4e4b6e8b6e032d751d4bc4ae451fe68eab8d5061d2cf5ce70177d4`  
		Last Modified: Tue, 16 Dec 2025 00:07:42 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f92fe74c4d5da54ac4900a4b136a9c073765662ac76f3370a7db886d5b616b`  
		Last Modified: Tue, 16 Dec 2025 00:07:42 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:83ba37c3f5bc1ac918bcf5211a931acd64f10fe0240bf5ae9861548665599b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18380444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdf316d235d752a458544fd681e3c8343530c33a3f11796546510bab973e31e`

```dockerfile
```

-	Layers:
	-	`sha256:7b4aaad60a06d54bbd9cd4560c1c9fb36e513dea6bc3557648011aa6ea8fd516`  
		Last Modified: Tue, 16 Dec 2025 01:53:54 GMT  
		Size: 2.5 MB (2488697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50827c704e6472906c019a2a57a7929af9d16d980ced424d00a27a95e95d1977`  
		Last Modified: Tue, 16 Dec 2025 01:53:55 GMT  
		Size: 5.2 MB (5224836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c847cfbcaa043464aabed611695303cf6db43b401adcc28ef4e088ce1ad950d`  
		Last Modified: Tue, 16 Dec 2025 01:54:06 GMT  
		Size: 5.4 MB (5380141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba587c5524f46111d1ddd7a818fa5298ea96fdffcd4876142213c7b2c6e3b73a`  
		Last Modified: Tue, 16 Dec 2025 01:54:07 GMT  
		Size: 5.2 MB (5226578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a97995619797a7b44ab4c27ecaad55f389ff07e78b91444f696a0227a3aabb9f`  
		Last Modified: Tue, 16 Dec 2025 01:54:08 GMT  
		Size: 60.2 KB (60192 bytes)  
		MIME: application/vnd.in-toto+json
