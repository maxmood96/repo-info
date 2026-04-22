## `rabbitmq:4-management`

```console
$ docker pull rabbitmq@sha256:e43ca03df740d48770641b56ce1a26913c74a31e47c1ed36a58e8d91c10731b9
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
$ docker pull rabbitmq@sha256:4dcdb029e9fe34686c9a0d351d0594cfed1b2f31958043073c2cca3db3dc9eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117611982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d0105df2285e40ebc46ded1d60069428dec9d3c1cb377c8a1211c5cc9cbcec`
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
# Tue, 21 Apr 2026 22:28:42 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:28:42 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:28:42 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:28:42 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:28:42 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:28:42 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:28:44 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 21 Apr 2026 22:28:44 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 21 Apr 2026 22:28:44 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:28:44 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:28:44 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:29:05 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 21 Apr 2026 22:29:06 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 21 Apr 2026 22:29:06 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 21 Apr 2026 22:29:06 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:29:06 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 21 Apr 2026 22:29:06 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 21 Apr 2026 22:29:06 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 21 Apr 2026 22:29:06 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 21 Apr 2026 22:29:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 22:29:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 22:29:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 21 Apr 2026 22:29:06 GMT
CMD ["rabbitmq-server"]
# Tue, 21 Apr 2026 23:01:45 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 21 Apr 2026 23:01:54 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 21 Apr 2026 23:01:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c171dc1cf147b58bda4d6aefc7d38a060a0f7cc395176cae593ece5139146bf8`  
		Last Modified: Tue, 21 Apr 2026 22:29:31 GMT  
		Size: 46.3 MB (46301267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0645306274c9dc9de33781a7b8aaab70d67cc4ded3a2c072cd7546d1745d7d1`  
		Last Modified: Tue, 21 Apr 2026 22:29:29 GMT  
		Size: 9.0 MB (8990285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27db247fa09cd17131021d6e59be0ac46f9b04551c5e1f8779ef283d4ba3372`  
		Last Modified: Tue, 21 Apr 2026 22:29:28 GMT  
		Size: 9.7 KB (9680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a7deaeeda94fd2bf52fcf64cfcac18a89c28f6176ab94e4858416dd267e6ca`  
		Last Modified: Tue, 21 Apr 2026 22:29:30 GMT  
		Size: 28.0 MB (27975739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421241908f37e6f536baf2bfcbb8ef5f4abec0840a34b7121d60c466db357632`  
		Last Modified: Tue, 21 Apr 2026 22:29:30 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238588bf6890953892814293887395bdbd151a5cd320257afc71c11f1a4bc4b6`  
		Last Modified: Tue, 21 Apr 2026 22:29:30 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e929c425694cdcc1edea7520dc58b68c31f26f696f3e797490838459abbdb71`  
		Last Modified: Tue, 21 Apr 2026 22:29:31 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f468dd216d8cd1ae4f2239693428b4964cffdeda1edfda3e635f988f17dfe4a5`  
		Last Modified: Tue, 21 Apr 2026 22:29:32 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f034b133258ad6aaf41de06b5fa9263f19d51dea8d9034fe4c56433528318e`  
		Last Modified: Tue, 21 Apr 2026 23:02:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a274461c03c1d101ce241660eef7760b4ea8a7631257468a12c9589d614ff1`  
		Last Modified: Tue, 21 Apr 2026 23:02:02 GMT  
		Size: 4.6 MB (4600010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8e803163b7411ae8990acacdd175489f3b015244787ed6f7d6ba64c28ac94988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec7221fd4c6d79625014f7a2e2544637d269b9dda66f8124b0537344a1b2b7a`

```dockerfile
```

-	Layers:
	-	`sha256:44fa98476ce1c7139495f664c70fa780d056500aa185a9955d4588dda7e5ca28`  
		Last Modified: Tue, 21 Apr 2026 23:02:02 GMT  
		Size: 2.5 MB (2486697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e700b28ee71ab2c47b8b24b9457d0affd88db4997bd6fa89914b108586d726f`  
		Last Modified: Tue, 21 Apr 2026 23:02:01 GMT  
		Size: 16.3 KB (16269 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:20d5c3c1c91817f5a201a12dc3b163dd7262466516acb682c74706ae9dbf92ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95380616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eac7e723312b248cb89632526ef5a9d141a6d95684e90fc41d2c1ad1c64b56d`
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
# Tue, 21 Apr 2026 22:29:00 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:29:00 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:29:00 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:29:00 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:29:00 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:29:00 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:29:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 21 Apr 2026 22:29:02 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 21 Apr 2026 22:29:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:29:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:29:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:29:25 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 21 Apr 2026 22:29:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 21 Apr 2026 22:29:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 21 Apr 2026 22:29:26 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:29:26 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 21 Apr 2026 22:29:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 21 Apr 2026 22:29:26 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 21 Apr 2026 22:29:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 21 Apr 2026 22:29:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 22:29:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 22:29:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 21 Apr 2026 22:29:26 GMT
CMD ["rabbitmq-server"]
# Tue, 21 Apr 2026 23:00:25 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 21 Apr 2026 23:00:25 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 21 Apr 2026 23:00:25 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d8b99658a9baf70be8a1e78a92c994747e174dac2df3c4ff12de37d17582b4`  
		Last Modified: Tue, 21 Apr 2026 22:29:51 GMT  
		Size: 33.3 MB (33324894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a5d13bfb5bbc06c67896959304f81587f0245dd561da2fb90d8e4770cf97b9`  
		Last Modified: Tue, 21 Apr 2026 22:29:50 GMT  
		Size: 7.3 MB (7306832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b235c395e375e871735c94363963c74c3ba5c2b3e32ceb686038ad470349f4a`  
		Last Modified: Tue, 21 Apr 2026 22:29:49 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecd741e02b7ff782183bcade1d6616c9af779d10149903ee0d3736198447045`  
		Last Modified: Tue, 21 Apr 2026 22:29:51 GMT  
		Size: 27.9 MB (27877413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f639fe1a552f6b7f106e3cc542fbd1074d5ca5ba57512da521a69b08b567040d`  
		Last Modified: Tue, 21 Apr 2026 22:29:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc61ce57318bc3c317a1c4f368b2510e02e69d7d126ad809ea48271b4588b6`  
		Last Modified: Tue, 21 Apr 2026 22:29:51 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2579bcf08b981b7674b6e1d647d2533699394a47eab0916b3b57ce9af663aa5`  
		Last Modified: Tue, 21 Apr 2026 22:29:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4812bbacdc9dda71a144a5ba3ed40240b186327887ce7111389b702d2270d0e1`  
		Last Modified: Tue, 21 Apr 2026 22:29:52 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d4ea6ad841e2990a97ad97e7978f3aa66757fb9d585ff00cbc384d80598259`  
		Last Modified: Tue, 21 Apr 2026 23:00:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4540d9e93381821502438fff9bcca8b5f311807eeffdc5123c3d1f08f9760cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fad61792f2c02473e372adfd1e79c04e9248ebf0e6e4d2b5bc2e3751c6b04f9`

```dockerfile
```

-	Layers:
	-	`sha256:77c3514d89afc310f078364d9d9c61123e8a5e46a453e43f698b25cac9354944`  
		Last Modified: Tue, 21 Apr 2026 23:00:42 GMT  
		Size: 2.5 MB (2487497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ca8d139074cee27faf02ff0a4bbe3c5e73d1bf6f475cfe67f7f57138852c79`  
		Last Modified: Tue, 21 Apr 2026 23:00:42 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:1e0044cfd9318cd94ff7d3a9272b8e138d08f8ebb3765ac225891f7fde8ff027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115234997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d0b18a1e1cb8d61bcb9f0aaf0d17b38ded57de340c46f64efb98603895147b`
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
# Tue, 21 Apr 2026 22:28:30 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:28:30 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:28:30 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:28:31 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:28:31 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:28:31 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:28:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 21 Apr 2026 22:28:32 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 21 Apr 2026 22:28:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:28:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:28:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:28:51 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 21 Apr 2026 22:28:52 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 21 Apr 2026 22:28:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 21 Apr 2026 22:28:52 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:28:52 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 21 Apr 2026 22:28:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 21 Apr 2026 22:28:52 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 21 Apr 2026 22:28:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 21 Apr 2026 22:28:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 22:28:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 22:28:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 21 Apr 2026 22:28:52 GMT
CMD ["rabbitmq-server"]
# Tue, 21 Apr 2026 23:01:58 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 21 Apr 2026 23:02:12 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 21 Apr 2026 23:02:12 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4db75c9047a5f9ebae711f1ea719e3c32ce2c695bce49b025222e16e693a85`  
		Last Modified: Tue, 21 Apr 2026 22:29:19 GMT  
		Size: 44.4 MB (44388040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269ba9377f0012d75b8a1c9bc755672e634f2374e055cc14d7cddec8b5fefaa1`  
		Last Modified: Tue, 21 Apr 2026 22:29:17 GMT  
		Size: 9.7 MB (9714852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223ecd91a81360a47997625e971e89307a7089c50eeccfe72c5a11fa2f894674`  
		Last Modified: Tue, 21 Apr 2026 22:29:16 GMT  
		Size: 9.7 KB (9666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862249dbed6a740acba77c37779fd664ca639627af175523ec05067efb967624`  
		Last Modified: Tue, 21 Apr 2026 22:29:18 GMT  
		Size: 27.9 MB (27885094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7337f8bf12f46562ce6b7b3d8e8c543fb83d92580f2f60ddd76618ae7d8f8d26`  
		Last Modified: Tue, 21 Apr 2026 22:29:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2e0973715d8f4e21527f65ded0f11cc43e7826bdda2d8dd07b42e7c78a804c`  
		Last Modified: Tue, 21 Apr 2026 22:29:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e5b87eb65e9a6324928fbaefa3c9ef39a8211cd6516154f91259d810564de2`  
		Last Modified: Tue, 21 Apr 2026 22:29:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988e5cdfe767c149952f3df1d28b138e81c5ac09e62cf6342643cc00fd21001f`  
		Last Modified: Tue, 21 Apr 2026 22:29:20 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da63ad1868541febd5b294d7b086bf6b77b9e52b0fbbd2b349e0a8e3b701aa30`  
		Last Modified: Tue, 21 Apr 2026 23:02:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5350c6128612cd4aa98320fd844236e70f63bec4b9d869ec01399a46ad816ff`  
		Last Modified: Tue, 21 Apr 2026 23:02:19 GMT  
		Size: 4.4 MB (4359540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:44fe535a2caa3229b425cdc2eaaa1e4be4f267ac61e5fa910263c4010e8722cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b841e8f63c7ba221dd0ecd569a26ffa9acef8ff6469e7fcf7db0e0a6800c3ed4`

```dockerfile
```

-	Layers:
	-	`sha256:1fe06828277228ed58e0993ddebe595ee4bb2d96cbf8f962d243b909714c62f1`  
		Last Modified: Tue, 21 Apr 2026 23:02:19 GMT  
		Size: 2.5 MB (2487757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2ea808b8c28467098cf39fe034e43e55f2eab6f38586878011c9f8c58c79f78`  
		Last Modified: Tue, 21 Apr 2026 23:02:19 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:c9e35668af31212306ef0a73b3cd0e952d47d3e0aaaaf4b0c173710d60242fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111399267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae05f7303814da5426d79e863ebb9015a1823bfeb0e7ed7ed53f113592881bd8`
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
# Tue, 21 Apr 2026 22:29:58 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:29:58 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:29:58 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:29:59 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:29:59 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:29:59 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:30:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 21 Apr 2026 22:30:02 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 21 Apr 2026 22:30:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:30:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:30:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:30:40 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 21 Apr 2026 22:30:42 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 21 Apr 2026 22:30:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 21 Apr 2026 22:30:42 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:30:42 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 21 Apr 2026 22:30:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 21 Apr 2026 22:30:42 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 21 Apr 2026 22:30:43 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 21 Apr 2026 22:30:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 22:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 22:30:43 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 21 Apr 2026 22:30:43 GMT
CMD ["rabbitmq-server"]
# Tue, 21 Apr 2026 23:00:31 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 21 Apr 2026 23:00:32 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 21 Apr 2026 23:00:32 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc816157179a8bfcdae99f55c6f2d26139173bfb43af906ce2614c5cb69d7af`  
		Last Modified: Tue, 21 Apr 2026 22:31:38 GMT  
		Size: 39.5 MB (39538683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be564f6d9c95fc723dd0c54ad71feb32c81b5fbdb3a23cdffb66f66f7f1e364`  
		Last Modified: Tue, 21 Apr 2026 22:31:36 GMT  
		Size: 9.6 MB (9599875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966a412fe6a56a14ba7ab222c6bd45dba446e6968f80fe31dbad889db191ac4`  
		Last Modified: Tue, 21 Apr 2026 22:31:35 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90111e59841c510b93cada7f71f7ec4cb037f93eb688d76c044e7dffd9979ba6`  
		Last Modified: Tue, 21 Apr 2026 22:31:38 GMT  
		Size: 27.9 MB (27934807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51ad2339e466c4a8f9cfdce769445a157d0c1d85fc3ca2c43afde5e66f4681b`  
		Last Modified: Tue, 21 Apr 2026 22:31:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecffb4a2bbe5b842e07759a86ef977051518609a1eaec776096a047e684f8f46`  
		Last Modified: Tue, 21 Apr 2026 22:31:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4145fc800b0b1dea337198c7eddd28a0f0e46e7af4efb850c2e1e4a1da5ac905`  
		Last Modified: Tue, 21 Apr 2026 22:31:38 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fdcc3350f611b1e17e5cc84a336065e374af5ee3badb37bef88035359a9279`  
		Last Modified: Tue, 21 Apr 2026 22:31:39 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffac01cbfdef62e3b03f03be7d2efbf2bf021d3a7e5d860caa86f0a21e044f`  
		Last Modified: Tue, 21 Apr 2026 23:00:47 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f487a9c637ab60a095416b3a065ca69ba0a1234fa51432efde04fcaa3ff0b0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d35907adde25eaf817d7b83f917ca6c0c941e69e07e9a0081b2ca9a050a6125`

```dockerfile
```

-	Layers:
	-	`sha256:b02895b47385f440dffdcf1162373b7142fe5e17b2dcfc17329b48d4eb5a0c66`  
		Last Modified: Tue, 21 Apr 2026 23:00:49 GMT  
		Size: 2.5 MB (2491150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d61ef80db610c4bb7d275e6452a4225ae2bfbf0871847341ff0fdade353e8d`  
		Last Modified: Tue, 21 Apr 2026 23:00:46 GMT  
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
$ docker pull rabbitmq@sha256:bcf490b0325b24df759b249b2c5a28962483fc4350d9eeb64de453c26388e67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105125472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd967902958690848c83d69537be706562fdfe094749393fc54803efa34e7a52`
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
# Tue, 21 Apr 2026 22:30:12 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 21 Apr 2026 22:30:12 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 21 Apr 2026 22:30:12 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 21 Apr 2026 22:30:12 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 21 Apr 2026 22:30:12 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:30:12 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:30:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 21 Apr 2026 22:30:13 GMT
ENV RABBITMQ_VERSION=4.2.5
# Tue, 21 Apr 2026 22:30:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 21 Apr 2026 22:30:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 21 Apr 2026 22:30:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 22:30:30 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 21 Apr 2026 22:30:32 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 21 Apr 2026 22:30:32 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 21 Apr 2026 22:30:32 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 21 Apr 2026 22:30:32 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 21 Apr 2026 22:30:32 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 21 Apr 2026 22:30:32 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 21 Apr 2026 22:30:32 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 21 Apr 2026 22:30:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 22:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 22:30:32 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 21 Apr 2026 22:30:32 GMT
CMD ["rabbitmq-server"]
# Tue, 21 Apr 2026 23:00:17 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 21 Apr 2026 23:00:17 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-x86_64-unknown-linux-gnu'; digest='dce127b1bf19255e2706665decb7073f14fdddbc76cb62791d427020946b1a40' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.29.0/rabbitmqadmin-2.29.0-aarch64-unknown-linux-gnu'; digest='4181fad3d3ed05691e474fcebb248f5ac834bbc39ce3551987bc2362824b0156' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 21 Apr 2026 23:00:17 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c2666a1d2aa18d763e8dc55b83ba0f73dda534eab3587dd92c26908224c456`  
		Last Modified: Tue, 21 Apr 2026 22:31:12 GMT  
		Size: 38.6 MB (38622900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11a71c768d8705d5299267f1851a7a1cda6566a3eb3fc7f3ffec2b5fb6abcbb`  
		Last Modified: Tue, 21 Apr 2026 22:31:11 GMT  
		Size: 8.6 MB (8621456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167fd5cbf420d982f8f71d3a8f1f5cf2d9e7ab49d0b408d8e7c81775ac5e7d34`  
		Last Modified: Tue, 21 Apr 2026 22:31:11 GMT  
		Size: 9.8 KB (9796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c73a02edd9a2bef59621db8182c75d27423998cf6152075f0e0ea470792725`  
		Last Modified: Tue, 21 Apr 2026 22:31:12 GMT  
		Size: 28.0 MB (27957117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391cf436f88e75d1fae86c51be885f66327362945790ea3cd131ee1e7af1254c`  
		Last Modified: Tue, 21 Apr 2026 22:31:12 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc32b9e5c5aa80b4d7043547f764ebf76ddd932d95ebd8d5f4010aff29c60d0`  
		Last Modified: Tue, 21 Apr 2026 22:31:12 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d76fdc62b200119c66c4d20187af7f40a936af1bceb9d4388b0de4a08782aa`  
		Last Modified: Tue, 21 Apr 2026 22:31:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59f0af0d20ba9144b1d862bd54b463a5dec348fd4ea4edd83ca75058a8625da`  
		Last Modified: Tue, 21 Apr 2026 22:31:13 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb474c0e3f9b0fc004dc77247bf6805fba9a15d0149bfab4e8d23cb6c5bb30a`  
		Last Modified: Tue, 21 Apr 2026 23:00:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:981e934db1f169a4308be00df833f1b233817429a7c503af7bb13a7b9bd51f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2505071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2d13a82e0770d962ec1d6cc6d272a9fd202fc389bf61b90db017a72c68541a`

```dockerfile
```

-	Layers:
	-	`sha256:0e088efa35576fbb149f21c2d9745d2f83bdb882d65eb30dce3d982b74a2a0c6`  
		Last Modified: Tue, 21 Apr 2026 23:00:38 GMT  
		Size: 2.5 MB (2488807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcf2fa7f6284ad00c29dba02b8ea0dcd77e62b38b88d51975ded9103feac77e`  
		Last Modified: Tue, 21 Apr 2026 23:00:38 GMT  
		Size: 16.3 KB (16264 bytes)  
		MIME: application/vnd.in-toto+json
