## `rabbitmq:management`

```console
$ docker pull rabbitmq@sha256:c5239ad28348b428cd59cce5a3cf3f0166790e599570d9420577c54bbc4c4ee9
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

### `rabbitmq:management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:fe15b288c836eb2798de27a7d3cc1d73e69ddd39cd69b5ae07fd72785f569fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127617467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81a52923fd34540b7b326a1e934d23e49f759dde3c36be23c87476a460b7757`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2184782314d53602ba6da50cbb41eb697c5eead0e79d0b26fa74bf380a934fc9`  
		Last Modified: Tue, 15 Apr 2025 22:06:51 GMT  
		Size: 46.2 MB (46237718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf9f0651be8b6bc71268f60f9f96f0cd2cccf95ba9ed2a694301fac498dd858`  
		Last Modified: Tue, 15 Apr 2025 22:06:50 GMT  
		Size: 8.2 MB (8171067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729adb9ccc7b8f870c124e0035862d9d146b4a8ecd0b9ed4cdf49c01a4d7d35f`  
		Last Modified: Tue, 15 Apr 2025 22:06:49 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9f58dfcce58bbf8ea219e7d308b9b7f56ca9df8538807318e13a1ffa896035`  
		Last Modified: Tue, 15 Apr 2025 22:06:51 GMT  
		Size: 31.0 MB (31016572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5274cc533cb4578e882a4a9b8220012006f1880f915aac341aebadaa59fd0e2`  
		Last Modified: Tue, 15 Apr 2025 22:06:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ecf8c0e621299baaf68a704562b3870b8c6d3122becb8f1b46141d76815393`  
		Last Modified: Tue, 15 Apr 2025 22:06:51 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d1c4875ae85de1e3f775624df30db4cba1ab8d7cc06dfa6300074e12802ba3`  
		Last Modified: Tue, 15 Apr 2025 22:06:51 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7d7a8292b2f512e12896ec5bec692d01072599fd2c3f619e0fbd2dc4f8ff54`  
		Last Modified: Tue, 15 Apr 2025 22:06:52 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7436722fb1936ab6777ed1ceace9293faf3c22340324205e457673ecc256033e`  
		Last Modified: Tue, 15 Apr 2025 22:26:26 GMT  
		Size: 12.5 MB (12463221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c42c34965ba02d8be305deec5effcf0a818837b1d914f0b97a4a8833f77b3867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2961398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae5358e69162600f4e705c83bc61fded9b14d8a449e8479bbba2a6f03e72cf0`

```dockerfile
```

-	Layers:
	-	`sha256:2b58d68f297051749f8bf43cc0df4ea3c26cd5b9f9022f00cce72807a7f67873`  
		Last Modified: Tue, 15 Apr 2025 22:26:26 GMT  
		Size: 2.9 MB (2949997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44fd73be10210aa039f2d5da55715a372676a6664d11473cf1e27e73295ac8c7`  
		Last Modified: Tue, 15 Apr 2025 22:26:25 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:9bdea1aa7f2b4c1bf4f535d156b2f954aec7065ed3c8c16ec4797d352ea7db29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109193804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407a4ca0d05e78e7ce7fd2471dabe2d9a0fb683ccc177e73aa75cd7866cca11f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:57 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:57 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:47:00 GMT
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
# Tue, 08 Apr 2025 10:47:00 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:34560582cc6246fb88c88648a1db5ef09d8b65d143991211ba2abe7378aee811`  
		Last Modified: Tue, 08 Apr 2025 11:53:53 GMT  
		Size: 26.8 MB (26837532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515984ceb12a9a39425504dea956ee1b4729f0d9cd78a402ef0bdcb714f0cc27`  
		Last Modified: Wed, 09 Apr 2025 11:56:57 GMT  
		Size: 33.3 MB (33279765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f09ea589fddfcb77cf5b02d0e97b04cae8d823b355fd25d45fd92a2899cfe9`  
		Last Modified: Wed, 09 Apr 2025 11:56:56 GMT  
		Size: 6.7 MB (6670896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd854963ba559fb4c63731891c807b83d5c95698ed0552a8b19121369143b86`  
		Last Modified: Wed, 09 Apr 2025 11:56:56 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4e942981f93b88624738444d3428a37431f351cb98f8c0d386e8362afd28e`  
		Last Modified: Tue, 15 Apr 2025 22:15:58 GMT  
		Size: 30.9 MB (30918697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e64a311d33e8fecb768e246b7021e28294d38b438782d934da90d50f1beee3`  
		Last Modified: Tue, 15 Apr 2025 22:15:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710a54be637aef1fac7c071301a845857a05596ca548734c6d56035ad28b1b7e`  
		Last Modified: Tue, 15 Apr 2025 22:15:57 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe26fa5c9a033dfb7a97b03941255c8012da8f7f602521940c25784ebf2d949`  
		Last Modified: Tue, 15 Apr 2025 22:15:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09207725b8856f708c23717f47d0b4808a2d07cdeba6afd935e2a70ec3f6d0`  
		Last Modified: Tue, 15 Apr 2025 22:15:58 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce86105f23afc17af266b688242edffd5d10896e853ccdab04cea9f2086316ca`  
		Last Modified: Tue, 15 Apr 2025 22:43:00 GMT  
		Size: 11.5 MB (11475630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8b496908cd78a2b2f6dae91fa02540a72b22ab800a5cf8c9bbf5e10aa4414c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2962434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff6e57876ebfdc06e188a2edf021b26a8b3766beb6ab796a9c106fb345ee92f`

```dockerfile
```

-	Layers:
	-	`sha256:dbd4ba898e9934c3ecb4711d61bcfcc6e70455387b7d1eb8a81cd28b25e66a3c`  
		Last Modified: Tue, 15 Apr 2025 22:43:00 GMT  
		Size: 3.0 MB (2950957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb54d91dfa14fc6673215cf8806b3438fb7bb25e488b4d45fbf56b955283bc5f`  
		Last Modified: Tue, 15 Apr 2025 22:43:00 GMT  
		Size: 11.5 KB (11477 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:c3f72108f1d0c37c1ffd1a71474976005e8c4f0852bf0da8bda4d4eca2203024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125388468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb916f79b125e78af9429e7e9930387ba71819badb76073ca1052adbad54ff1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401d670900d6f6041c5f1a99140e46299a511acb459251e41877d2f964fb2a76`  
		Last Modified: Wed, 09 Apr 2025 08:58:14 GMT  
		Size: 44.3 MB (44331780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a91c6dc822dd3c7f00888ab6177a92546e93bae0a1673423e2a2d559d378d8`  
		Last Modified: Wed, 09 Apr 2025 08:58:13 GMT  
		Size: 8.9 MB (8943314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aca869fceae569ad48849ca0b55e0b465148a326f73e18c6069ee9515f4c860`  
		Last Modified: Wed, 09 Apr 2025 08:58:13 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882ce4d913a5532c53cb95ec7df2bd4a12e47f347cdf37483724a6556db6652c`  
		Last Modified: Tue, 15 Apr 2025 22:19:24 GMT  
		Size: 30.9 MB (30924912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc27ac031da95d7842209c0c9310a556d28145bb2f1bae123cfc8bc573e8c91c`  
		Last Modified: Tue, 15 Apr 2025 22:19:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd7c8121aa36386de8037ed159bdb9abf3a4d131bcac7a50049dd58d1ea8fe0`  
		Last Modified: Tue, 15 Apr 2025 22:19:23 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb61f60440c242d9102ea3f7feac3a0776a6d3a58c5837e9cafbaa763297a100`  
		Last Modified: Tue, 15 Apr 2025 22:19:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81aa05c6440f4fe5a48993696855f8f74a73952a7e1ab0612cc8501a5fce934`  
		Last Modified: Tue, 15 Apr 2025 22:19:24 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c488117e309a6ba986634fa981171936677cb7a59c8d00d2ea63cac163a56ad2`  
		Last Modified: Tue, 15 Apr 2025 22:31:52 GMT  
		Size: 12.3 MB (12330342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9e088829878017a8eac99b999eaea7e5ff2a3c0977785805ffe23618cabfef2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2962614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4512fbc32ad5dab5a4618a0565eedbd84ea724c2b9abe4c7dc9af2bee0354b3`

```dockerfile
```

-	Layers:
	-	`sha256:5818a2b5d0c6f895e5fb00aad542eba75906c4b2e9cd433e964cb658359652da`  
		Last Modified: Tue, 15 Apr 2025 22:31:51 GMT  
		Size: 3.0 MB (2951109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2024b8d4e5d4eed92ff5a1552b82a2fa4780c1cca81c472171fbc07d67c2eb1`  
		Last Modified: Tue, 15 Apr 2025 22:31:51 GMT  
		Size: 11.5 KB (11505 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:6011fccf74da83ea281d519aae5aafa26e4003f8e55a4964a3ef4b6b406ab49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126470769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fa474f9efce4460b96ba7b5df9dc1a1635e78df6eba74fddc9514acacf09bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fdefc1d6971b6a384fa76723ab8c1c8205915e8b0d76afe67bbd874152750c`  
		Last Modified: Wed, 09 Apr 2025 06:24:27 GMT  
		Size: 39.5 MB (39481227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd669b11ad0ea6ab17f1e0bfc2d0df89d9a90ba7d1150121314c634cd6348e7`  
		Last Modified: Wed, 09 Apr 2025 06:24:26 GMT  
		Size: 8.7 MB (8699433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a174956a08a4856b2e1fa7b3ce7b99d72df0d69ebff46082af94800f4c59765a`  
		Last Modified: Wed, 09 Apr 2025 06:24:25 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df4a52b1a5f53e044101ea84c89b55a426b966928cecde8d52ee4370a7f6e0e`  
		Last Modified: Tue, 15 Apr 2025 22:11:21 GMT  
		Size: 31.0 MB (30974328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4275e35853a3fcdae091aef242a78f1491018641eb0a158a993fdc2feaad9131`  
		Last Modified: Tue, 15 Apr 2025 22:11:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20b56bc8821c3d0271301959016e01a289b509e7198dd491b5696d31c861381`  
		Last Modified: Tue, 15 Apr 2025 22:11:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148344d07478e8d0d3be0f84cd29bc9904cada23348dfba63fc800ab9cff43c8`  
		Last Modified: Tue, 15 Apr 2025 22:11:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5eef38efcc6f56f90c471f6efd1805609f198436ed8ce83ccc51dd6aab0f3c`  
		Last Modified: Tue, 15 Apr 2025 22:11:20 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a610656a2c5cedbf908ddc39d170101a0dcde2b850151a97f43f7d764deed109`  
		Last Modified: Tue, 15 Apr 2025 22:39:15 GMT  
		Size: 13.0 MB (12963769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:88651831415922e7133fa65702722725da4fc00dc9d6c3fbab0e743c5be457a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c2960ab13c79d44de10ebfee00c599218a32807c7f652a391e73825acb9956`

```dockerfile
```

-	Layers:
	-	`sha256:6278d581115d2504465179b20a87bb53e73e75f3d0ad15a670d9d391e8926525`  
		Last Modified: Tue, 15 Apr 2025 22:39:14 GMT  
		Size: 3.0 MB (2954626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ace4a7161fc88951e7191e64503f4fa8f71b34c67b50dfa3df7f1b95ff6a3c`  
		Last Modified: Tue, 15 Apr 2025 22:39:14 GMT  
		Size: 11.4 KB (11445 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:8e1b96e2e6fa55a52e89018e6cfaf8f7398652c405b9c8254ef0fae40449439b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119127251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bb2f2742f612eb31924587a4576f12543965bc173e7df689ddd1aa5e3e1873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 11:16:50 GMT
ARG RELEASE
# Tue, 08 Apr 2025 11:16:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 11:16:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 11:16:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 11:17:29 GMT
ADD file:ef7c97f5dd8d665aae899afe52c54f7acaf71fa51e9d7f26e13ed6073141c666 in / 
# Tue, 08 Apr 2025 11:17:31 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:ba2f284f7444fb0b78fa804d74c44dee4b397610267539e4a6e9c41ae41e06a1`  
		Last Modified: Tue, 08 Apr 2025 11:54:06 GMT  
		Size: 30.9 MB (30943202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cdbd868cc1adc61328d67614839fa18450a921df3252989bd14ec77ec87008`  
		Last Modified: Wed, 09 Apr 2025 07:14:19 GMT  
		Size: 35.1 MB (35128410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8c6de69198d0d40e4ba20190ce9009e900d7e1eb1af51c0d3a540a62a207bf`  
		Last Modified: Wed, 09 Apr 2025 07:14:15 GMT  
		Size: 9.8 MB (9789666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cb4ca09dc366fa63314e988f583aaf21a9b21db831297d8186593ff9595d29`  
		Last Modified: Wed, 09 Apr 2025 07:14:12 GMT  
		Size: 9.5 KB (9473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006bc319611428e7a11bfd0a0b9348e561666ec950fad039b820ef10ee14da33`  
		Last Modified: Tue, 15 Apr 2025 22:09:30 GMT  
		Size: 30.9 MB (30928350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0f625112680bb993a8cc6659c38e207774c086222d1c82b9b6e32d9ae11ca9`  
		Last Modified: Tue, 15 Apr 2025 22:09:25 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68d5ab49bcaf3302dc8edf02b7c4703b9fb960f613daa05ffeeb8debe41673`  
		Last Modified: Tue, 15 Apr 2025 22:09:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6adf6baf052188b321b4b6ab6ba0d5af8ca5875d979ef1910dcc2c930f0231`  
		Last Modified: Tue, 15 Apr 2025 22:09:25 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6deb30df57639abb0d80bd23a7e92a1a9d02e34e3c1a44fe09cb468a4262ac8d`  
		Last Modified: Tue, 15 Apr 2025 22:09:26 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac9c1f869ea021d3fdd7c2b320512251869a8c2dd729b8a634f4a5dec797457`  
		Last Modified: Tue, 15 Apr 2025 22:39:05 GMT  
		Size: 12.3 MB (12326402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:187ec265ce002a54c170443d8c7d2b9df2749a6793f4712139ce929769e31cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2954073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c35919644b58c02f2e848222757ef106801b047b58126af9442f4ea0098ec`

```dockerfile
```

-	Layers:
	-	`sha256:35d2c05ee37aad0896ca450f65fccce7538ef87ad2f134bbe3ab1ddc8e403f06`  
		Last Modified: Tue, 15 Apr 2025 22:39:03 GMT  
		Size: 2.9 MB (2942628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f2b7642fdf2c4e45128bbaab29a5913bc45edd05b12a231c4c2055fb181f29`  
		Last Modified: Tue, 15 Apr 2025 22:39:02 GMT  
		Size: 11.4 KB (11445 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:fb6a1110f648d984f8b8d747eabdcf98b9039d6787725a5fcb18b5c46ea9b9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119758640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052aaf06a31f578bec6bc7a46d1aeeb916df108b9539af03b88ca98d540e6202`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:29 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:29 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:30 GMT
ADD file:8f287f40ca940c9bd87c8706751f5f1c5bbd0a83fd75f7d938832b226fdb936d in / 
# Tue, 08 Apr 2025 10:46:30 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 15 Apr 2025 17:26:54 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_VERSION=4.1.0
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 15 Apr 2025 17:26:54 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 15 Apr 2025 17:26:54 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 15 Apr 2025 17:26:54 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 15 Apr 2025 17:26:54 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 15 Apr 2025 17:26:54 GMT
CMD ["rabbitmq-server"]
# Tue, 15 Apr 2025 17:26:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Tue, 15 Apr 2025 17:26:54 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:e5722f32c6281fa87f1e5f7ebe307864b50aa95a116496a205ce47478bc9b52c`  
		Last Modified: Tue, 08 Apr 2025 11:54:12 GMT  
		Size: 30.0 MB (29956206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d629cd92050f0ccf0802a7b0ca01547593128930d4c31efad28afefdf10b4203`  
		Last Modified: Wed, 09 Apr 2025 06:51:07 GMT  
		Size: 38.6 MB (38561141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c64f602e81ea3007f9260ba3c62875426f533e648e281a41ce75d453c12dbd`  
		Last Modified: Wed, 09 Apr 2025 06:51:06 GMT  
		Size: 7.6 MB (7551996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ee2e1181522c291c6e8a6b113e379953ad50990c68e51916cf71be7604147a`  
		Last Modified: Wed, 09 Apr 2025 06:51:05 GMT  
		Size: 9.6 KB (9609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab64f0c662fc9ff58c6776f9b1a0e7f62cc7f3d82d2ed43a3bc8c283f8c186b4`  
		Last Modified: Tue, 15 Apr 2025 22:10:53 GMT  
		Size: 31.0 MB (30998957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a205c685f2981867d1ed6b362161eefc55a6f81c4eaf2ec0b0e728f0a643434`  
		Last Modified: Tue, 15 Apr 2025 22:10:52 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b8f8ec27436dbcd657dcc5499a4d68b8e4affcfc06c7f846799f4f2359a664`  
		Last Modified: Tue, 15 Apr 2025 22:10:52 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68bf68e763ff59dca66e3c2199310985504377831efa2ccb872da3f8a393fb`  
		Last Modified: Tue, 15 Apr 2025 22:10:52 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468374354a6bc8678b2a08a557a946670409e9c62f0a62a234493e446f29e730`  
		Last Modified: Tue, 15 Apr 2025 22:10:53 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d041e2f571c4eec0d2ce60c1f0cd171a89cbb1bb0f8cebe6bdfe9376dc16a9e`  
		Last Modified: Tue, 15 Apr 2025 22:38:49 GMT  
		Size: 12.7 MB (12678984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fa0bf8c198fa078517651c411c3fffa4c46eb382357fcd5ef8dbf816c1869471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2963458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a023be4bd7ff493bcd419ed41c33c7c83942a9142fd602b9d71ca59dc02e554`

```dockerfile
```

-	Layers:
	-	`sha256:043c98c33deaa975bc89c3dcd43f1c449107b688c2369a820822b26cb9cccab9`  
		Last Modified: Tue, 15 Apr 2025 22:38:48 GMT  
		Size: 3.0 MB (2952057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4c7af0b3c93d5e6df4c1a14417edc7403ad10874d413d5e0deb38788e35098`  
		Last Modified: Tue, 15 Apr 2025 22:38:48 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.in-toto+json
