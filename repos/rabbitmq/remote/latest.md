## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:2e603d91072d7f3ddb942bacd324a18804bd7ed67780087103464e4c546bdf0e
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
$ docker pull rabbitmq@sha256:805b7b948f84b1452190e5b7509d8b5293ae83feb65ec4a0acb7627d442e9bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112837288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444e08bd94c66fba59dfd7593b6006e7aecc65ae536461901b1bf21b8170dd9e`
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
# Sat, 13 Dec 2025 00:24:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:24:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:24:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:24:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:24:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:24:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:24:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 13 Dec 2025 00:24:34 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:24:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:24:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:24:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:24:53 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:24:53 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:24:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:24:54 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:24:54 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:24:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:24:54 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:24:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:24:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:24:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:24:54 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8315ec435c58b4aea4aa27bb027388715bf7c9a8afeaf59f17f1cd5b4f326d61`  
		Last Modified: Sat, 13 Dec 2025 00:25:35 GMT  
		Size: 46.3 MB (46261500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd2b2443da044c9e836ee5bbc86caff8120ef2ad79123d8681b8d5138b41664`  
		Last Modified: Sat, 13 Dec 2025 00:25:33 GMT  
		Size: 9.0 MB (8994563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a621c60d1a6ebb76151b7c2c21154569df6aee7d4ec3008303c59be1d1fdec1`  
		Last Modified: Sat, 13 Dec 2025 00:25:35 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14785bf8db68ef3d2e62dc27a47a425ac85dbf3e37ee38d7f8d510544fba26e`  
		Last Modified: Sat, 13 Dec 2025 00:25:33 GMT  
		Size: 27.8 MB (27845093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88d4557ff18b829456950a5065d338e569f6c48fdd2c99dde1e148663ea1663`  
		Last Modified: Sat, 13 Dec 2025 00:25:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb850ab0096034f96eedebcb4587e5f1f44b5f74ed19068eb8ee2a0ccd744939`  
		Last Modified: Sat, 13 Dec 2025 00:25:32 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf7230be1f492d8c2b8427967cf4df121ea479c114fe3d5d9e0ddc23f581620`  
		Last Modified: Sat, 13 Dec 2025 00:25:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e060efb34f5aef295d114036b441347f05b066523affc3c112b25d5d56b7da`  
		Last Modified: Sat, 13 Dec 2025 00:25:45 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:72c0b92ebe815bbc8d0bb21b0ad5514b04d4bdafaa08cd75d8e0b1ddcdb1ce74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18841564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670a0c409b6315e6de713795db38bd76448efb73d901e1bd4baf00cdbdccd10f`

```dockerfile
```

-	Layers:
	-	`sha256:8257b2266e7cda40de7d99655d05e88abba4ab50b8e86605a37d3559dde048ee`  
		Last Modified: Sat, 13 Dec 2025 01:52:36 GMT  
		Size: 2.5 MB (2487854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3deb3b9eb81adae371703ab83c50edcbd158661c67c1646dac9b665d8dbc3767`  
		Last Modified: Sat, 13 Dec 2025 01:52:38 GMT  
		Size: 5.4 MB (5378389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c176c6d78baac60882cab604f9fc0d8eeed613d59435f9e96ebb1c864a6493`  
		Last Modified: Sat, 13 Dec 2025 01:52:39 GMT  
		Size: 5.5 MB (5534998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f691de4a7f9483d64b9be094f43aa5fed61365845d832dcf1a8d587c0e307b34`  
		Last Modified: Sat, 13 Dec 2025 01:52:40 GMT  
		Size: 5.4 MB (5380131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47f9a0de1b9556657cce444e89171fed87a6bd99dbd4a1fc92d2d56be505a905`  
		Last Modified: Sat, 13 Dec 2025 01:52:41 GMT  
		Size: 60.2 KB (60192 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:85704c85200811a27feb6b8de778ceec761e355afb2bea032c9434a861f46aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95215241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8cbef63f6bc69475d08865f6825a08d1bc20e5d17735453b3802312f4529da`
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
# Sat, 13 Dec 2025 00:25:00 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:25:00 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:25:00 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:25:00 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:25:00 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:00 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:01 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 13 Dec 2025 00:25:01 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:25:01 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:25:01 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:25:01 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:24 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:25:24 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:25:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:25:25 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:25 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:25:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:25:25 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:25:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:25:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:25:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:25:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:25:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6cdc0abf996c3192bfbda4018d34c282871d4be33fb369176002cb2199673adf`  
		Last Modified: Fri, 17 Oct 2025 08:06:35 GMT  
		Size: 26.9 MB (26852672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93a454bcf8a6c9d47fa004d6cc246774cf37719d29f3272e42689c6785529e4`  
		Last Modified: Sat, 13 Dec 2025 00:26:07 GMT  
		Size: 33.3 MB (33295322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e2141dde4510da35941072991d7dc66d5b9ffeb7f010f9ea9e1b7fc194b74f`  
		Last Modified: Sat, 13 Dec 2025 00:26:03 GMT  
		Size: 7.3 MB (7309042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ffc4fc4237556f8a62712b00e51e457f1c7302f262ba490fdacbee28fdb4e3`  
		Last Modified: Sat, 13 Dec 2025 00:26:03 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb419269e405dc3215560919b4f36be3760b8c304259d3e1945a55dd3a1b129`  
		Last Modified: Sat, 13 Dec 2025 00:26:10 GMT  
		Size: 27.7 MB (27746715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0ba3110b00287eed5cd61be0e92ef1354758ba76c6cbb89d78adb2fbaf2153`  
		Last Modified: Sat, 13 Dec 2025 00:26:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f14753d13ceb7bdaebc351f9f547f5d04548b74d62d45053d7d885f687f29d`  
		Last Modified: Sat, 13 Dec 2025 00:26:03 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be52623d5f0144847e8a3f39d0fc567cf6d2161a0a42277dfc1fc441005cd264`  
		Last Modified: Sat, 13 Dec 2025 00:26:03 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc2b80e78d11583a2a0b4d080a2cea68d0c31f96c82f25dceee163f82ef4fc2`  
		Last Modified: Sat, 13 Dec 2025 00:26:04 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:783855b121e8ea190da1cbf5559415c23e6fb51cf192096c9e4013aef5bee248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18296346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d920e49f4983fedd44566bbcecdb950717d67fae20d6155c326dfe30ecfb1`

```dockerfile
```

-	Layers:
	-	`sha256:7031344fdda88d754a17717dda07135ae58945fad3d10f7344d29de6d9cfa0b9`  
		Last Modified: Sat, 13 Dec 2025 01:52:48 GMT  
		Size: 2.5 MB (2488654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1daa1b42d7a791e0265b41dc6decc2b7f351a3deaf04ffe5f81993c67664d4`  
		Last Modified: Sat, 13 Dec 2025 01:52:49 GMT  
		Size: 5.2 MB (5197169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4d74a7a3c1b7f761a317450ebb0a57688a707b8f96d58253bff23e04617b33f`  
		Last Modified: Sat, 13 Dec 2025 01:52:50 GMT  
		Size: 5.4 MB (5351223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5ed3008c2423c0945d03cfa09d0d6a28110cf03d43ee444184f57b09cc7c3cc`  
		Last Modified: Sat, 13 Dec 2025 01:52:51 GMT  
		Size: 5.2 MB (5198911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4ff397eacd237cb3206bba1f2080120f0e1bac800b389b6f477274ccfd96d64`  
		Last Modified: Sat, 13 Dec 2025 01:52:52 GMT  
		Size: 60.4 KB (60389 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:d73567439097f3d39f99d9e2d3f5f82f521a08e427df72ebb5b3606d1f37969a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110699643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d057061d39bdc3aab8672df09c5539d1ab86a32282b001f39cf79c007eb92b90`
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
# Sat, 13 Dec 2025 00:24:55 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 13 Dec 2025 00:24:55 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 13 Dec 2025 00:24:55 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 13 Dec 2025 00:24:55 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 13 Dec 2025 00:24:55 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:24:55 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:24:57 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Sat, 13 Dec 2025 00:24:57 GMT
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:24:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:24:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:24:57 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:25:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:25:23 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:25:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:25:23 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:25:23 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:25:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:25:23 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:25:23 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:25:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:25:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:25:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:25:23 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d68c70a0d123f56808bdfb5a7dc852015375bada3e9e3857ea735592da7e58`  
		Last Modified: Sat, 13 Dec 2025 00:26:05 GMT  
		Size: 44.4 MB (44355315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f61517e74040007d2322e0ccb7be8f200f491f550dcf6c1fe1fce46571fce7`  
		Last Modified: Sat, 13 Dec 2025 00:26:02 GMT  
		Size: 9.7 MB (9716235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0400900a18e106ded23528a372ea40133a9850667568a550ca007e52fa323b8c`  
		Last Modified: Sat, 13 Dec 2025 00:26:02 GMT  
		Size: 9.7 KB (9684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea721010389de04dec8c6e300d3b86445d690fffb4300303fe8eedfaf3b789e`  
		Last Modified: Sat, 13 Dec 2025 00:26:03 GMT  
		Size: 27.8 MB (27754705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f878a8c4b5b8eba04deca68dd4c280c12ed260c10bb101f873ccccba667c1a1f`  
		Last Modified: Sat, 13 Dec 2025 00:26:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fa203980a21aa13cb310be243f19384ba5ad58e59c45e3c28e9c3c5e2b885`  
		Last Modified: Sat, 13 Dec 2025 00:26:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0e7c6da4d4df11c5bfc9f860703728a3766b32cfa783eb9705368a4d4cbfc9`  
		Last Modified: Sat, 13 Dec 2025 00:26:02 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c81949bf730e50f8f96f7c02fc1d21d0effa7bb751b3d976c2e1b4a2d14c6c`  
		Last Modified: Sat, 13 Dec 2025 00:26:01 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cf8e86c51403ac11a972b4b4a7c6646746af99f2f0aad508dbde2e61d23c6b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18900544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bba74e9a872f5e75c0354088588b4ac00e119537cfc6f1416a93a3ac80fbef8`

```dockerfile
```

-	Layers:
	-	`sha256:43d9ce3488f5a3d232ef888e5289ddd70be7761d8f3cc5a853b0ce96116166d4`  
		Last Modified: Sat, 13 Dec 2025 01:52:59 GMT  
		Size: 2.5 MB (2488914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9ebf34bcc62d8c9d26a2910f12b2bada981b535ded9af64e503e167ff1df7f`  
		Last Modified: Sat, 13 Dec 2025 01:53:00 GMT  
		Size: 5.4 MB (5397610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f926fbe6727f9340492dffa25ddcd2dbb949a6ac1516e64434ad0bb32ec22f5a`  
		Last Modified: Sat, 13 Dec 2025 01:53:01 GMT  
		Size: 5.6 MB (5554237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0aad9c84c059345979e8401af43c1e7d1d409be4bff162c167fb11f3c439dad`  
		Last Modified: Sat, 13 Dec 2025 01:53:03 GMT  
		Size: 5.4 MB (5399352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a6d22609a3d5d86e22454833a38de21bcee2c1e6bfc09cfcf06626bd2596708`  
		Last Modified: Sat, 13 Dec 2025 01:53:03 GMT  
		Size: 60.4 KB (60431 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:205143eb1cb674cd9c079a7b38c9a86fae31b83eaf92eef98511b5009b8bd38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111229573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56dcfa865c49a047cf6a3c442d56d30ea3e303c770117c305dc21bbf4d0822f1`
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
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:27:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:27:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:27:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:27:55 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:27:57 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:27:59 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:27:59 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:27:59 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:27:59 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:27:59 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:28:00 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:28:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:28:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:28:00 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:28:00 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
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
	-	`sha256:d1676c6f520bd42dc8b2a4c2ddcb5e83e4978d41ffa2845ce4a16a5f3bd4a78b`  
		Last Modified: Sat, 13 Dec 2025 00:29:08 GMT  
		Size: 27.8 MB (27805987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec160e72080b8f9e9c7cd33962927b649327cf8db9a70e6101df4bc2a1f5097`  
		Last Modified: Sat, 13 Dec 2025 00:29:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad11d492c1851156fa5813c3153b0d7abe04dec70e1b40ac3184d0c3aa09b05`  
		Last Modified: Sat, 13 Dec 2025 00:29:06 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9c0be63221f4bed6ea45bc1b10c5c09ede89c9671c55e884ba430d1440afd1`  
		Last Modified: Sat, 13 Dec 2025 00:29:06 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a674c419887bb42561be3dfe71afef5a168da6a805b990bfe7bd374993fcce6`  
		Last Modified: Sat, 13 Dec 2025 00:29:06 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:da7ea0abe5f53ffe068315e126fa7c5826632b5af06cc83cb012b25c513d9717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18755935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd13ab19bd2b40b4c5e90923b88de71ed818da467ea7f40c6555a4ffc970d40a`

```dockerfile
```

-	Layers:
	-	`sha256:01ff1efa8ad16204275b53f62e056c14790200e88a009cbb38fed2b4b31e1d82`  
		Last Modified: Sat, 13 Dec 2025 01:53:11 GMT  
		Size: 2.5 MB (2492307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ea3c5777ebd40332c2349c445f5c07fc30172969f0971a6f979efeb8f32557`  
		Last Modified: Sat, 13 Dec 2025 01:53:12 GMT  
		Size: 5.3 MB (5348331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a6927918a6f37549d5067b80e5d855a9f75df765b71c33ee1aa2488f12384d`  
		Last Modified: Sat, 13 Dec 2025 01:53:14 GMT  
		Size: 5.5 MB (5504970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:565be6575042ac2373cd8e22ccc037f7e751da7300c11827c0f754ba37734ec0`  
		Last Modified: Sat, 13 Dec 2025 01:53:15 GMT  
		Size: 5.4 MB (5350073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46564f031ea1e5c4bc374d3433135cf04e308fa86cf7ac59ee7de85470119c02`  
		Last Modified: Sat, 13 Dec 2025 01:53:16 GMT  
		Size: 60.3 KB (60254 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:4073e91a8543bfb87d95f1e51f678bfc5df118d91f4c842f8fbc50acfee336ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104700944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216ca27187daf21df7a4e0a7a2e20fd21a75abb81567464c54310b235bc559b`
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
# Tue, 18 Nov 2025 02:07:06 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 18 Nov 2025 02:07:15 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 18 Nov 2025 02:07:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 18 Nov 2025 02:07:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 18 Nov 2025 02:07:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 18 Nov 2025 02:07:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 18 Nov 2025 02:07:16 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 18 Nov 2025 02:07:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 18 Nov 2025 02:07:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:07:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 18 Nov 2025 02:07:16 GMT
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
	-	`sha256:19b4bf9104636ca1401983244b1716aec5ea4e9f927160b6a48cb9733c4c3666`  
		Last Modified: Tue, 18 Nov 2025 03:17:16 GMT  
		Size: 27.8 MB (27758214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9f4e0b9f1ccd082384104a464df2eebaa194d1927a3c6c3e756bd9b50dfdbc`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be3ceb28403430901d0e4e2ca5736a8cd336328d2cf842a89d932a6c9633051`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccbba1ffc329f8aba69e5168671d96d93885802356fc3421130bead91af084c`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34337440b2d44efb13a1a3a0de245cee5dec16798af8dfb50a4f83ce6e9face0`  
		Last Modified: Tue, 18 Nov 2025 03:17:13 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:aa0800cd9d3f3cc5e294d26aade69cb4c997fd9c993c0095be5be0c6d2f0dea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18724462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b3c51588d84e182e63aabad1a20c0236143c7129065422999c1d706bb0073a`

```dockerfile
```

-	Layers:
	-	`sha256:eecf8ccce51be259f36758c8cd59d445b5656430e4619b8af7b654fd71746481`  
		Last Modified: Tue, 02 Dec 2025 13:53:18 GMT  
		Size: 2.5 MB (2480221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24638711d950e4510c60b75b69ff370e6e8cc88b3826a5541f36c3e63f13bf20`  
		Last Modified: Tue, 02 Dec 2025 13:53:19 GMT  
		Size: 5.3 MB (5342764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e194c8c20244bd8430c2784e1ddf1416aabf5923195761c35fa93fe4d4623a09`  
		Last Modified: Tue, 02 Dec 2025 13:53:20 GMT  
		Size: 5.5 MB (5496816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af47c760c0914ff98b14caaefdd5fba05676df1bf4084acbbc30726bd6b367c4`  
		Last Modified: Tue, 02 Dec 2025 13:53:22 GMT  
		Size: 5.3 MB (5344506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d2bd70ca7a889baae1f53996be2a7ef73d5caabf9b7ccd7e1730223f0ca151b`  
		Last Modified: Tue, 02 Dec 2025 13:53:22 GMT  
		Size: 60.2 KB (60155 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:583961530a28e5cf9ed551d19cfdb697e4320122fac9a1b26d58f7941a1cc84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104951954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4da1f1c523fd492a5d640b981a7fff70534864a7b47963c960067b22160b62`
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
ENV RABBITMQ_VERSION=4.2.1
# Sat, 13 Dec 2025 00:26:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 13 Dec 2025 00:26:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 13 Dec 2025 00:26:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 00:26:42 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Sat, 13 Dec 2025 00:26:43 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 13 Dec 2025 00:26:43 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 13 Dec 2025 00:26:43 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 13 Dec 2025 00:26:43 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 13 Dec 2025 00:26:43 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 13 Dec 2025 00:26:43 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Sat, 13 Dec 2025 00:26:43 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 13 Dec 2025 00:26:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Dec 2025 00:26:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Dec 2025 00:26:43 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 13 Dec 2025 00:26:43 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
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
	-	`sha256:2a313db9956097dd4cd6f77141efda823557ce4b98e6678a963db3d5d5dcb2cf`  
		Last Modified: Sat, 13 Dec 2025 00:27:29 GMT  
		Size: 27.8 MB (27828541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aa819ab84f5c3382b347faaaf7d71c84f62fd76bb68dedcb26655ab1393100`  
		Last Modified: Sat, 13 Dec 2025 00:27:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23249015ad879810cca2fae265d58e3c12e86de8f7f885e4826a4352e0af2380`  
		Last Modified: Sat, 13 Dec 2025 00:27:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0c9275c534b433bf137e799b630cf2e6ecff35dd52d652480a268a04196305`  
		Last Modified: Sat, 13 Dec 2025 00:27:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0ee8ffd179b6c0a6e8839a3d7cb5c1293f158dd926e5b168346cc7a472c670`  
		Last Modified: Sat, 13 Dec 2025 00:27:26 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a15a54cb6191ffd356a991dd821b4fa92e94b866e4b7816e2176c2d78ae9e60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18381711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307e558870114168a2c373767de19fddab4840e965d7c91d46ee034dda10baba`

```dockerfile
```

-	Layers:
	-	`sha256:29f5704c179c005c4d04e7e90e961f584019dde4fc6400128b3ebb44c48e09d6`  
		Last Modified: Sat, 13 Dec 2025 01:53:30 GMT  
		Size: 2.5 MB (2489964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7a3fcbd2a90b778c02aae366cfea09240e063f1145fe37f0741ee92ed7e8829`  
		Last Modified: Sat, 13 Dec 2025 01:53:34 GMT  
		Size: 5.2 MB (5224836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4123a3bbb134d2e8402a7a0eb2c36ae933ef22b0c7871b0d6e91afb4b3e51bd`  
		Last Modified: Sat, 13 Dec 2025 01:53:35 GMT  
		Size: 5.4 MB (5380141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0099b59e7815772080efeffd963c0f897d18ebd3e6eb23970de96530c5d444c7`  
		Last Modified: Sat, 13 Dec 2025 01:53:37 GMT  
		Size: 5.2 MB (5226578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e770fc280ad485d4e0b2854e59dfbbc5b3a51c469739c13c33a3e1c4fbe781`  
		Last Modified: Sat, 13 Dec 2025 01:53:38 GMT  
		Size: 60.2 KB (60192 bytes)  
		MIME: application/vnd.in-toto+json
