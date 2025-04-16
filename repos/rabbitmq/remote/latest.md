## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:f15e0e32d7d6122ff96eaedfa60d0b6e81c5f987e00e329a58a0b9519f45daa6
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
$ docker pull rabbitmq@sha256:53c8cd85929a07abbcd56714652e57121657059d180f3084e54606d099321522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115154246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f66def88625f25c05ca46c11cfdeea740553c1c42ef8a8f041ca23c9817be1`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b669f2cbe1165535947097af027a15f52b0427c7654f5e4e785a09cfe653912f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18193684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0458b496b431f40c3fb5afeb43f2aeba6e5065fe2ece9023d62bfac828f92f29`

```dockerfile
```

-	Layers:
	-	`sha256:8de73872e8cee63e540232ae0fa0459f5c58a39698d9b78a2667be0234ed4c37`  
		Last Modified: Tue, 15 Apr 2025 22:06:50 GMT  
		Size: 2.4 MB (2366876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927c2afb641f8cd59706e4a829da66b074552977fd1aa187f6263e0ba8bb7876`  
		Last Modified: Tue, 15 Apr 2025 22:06:50 GMT  
		Size: 5.2 MB (5202998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0a51bb1ffe9b2e8217cfac23bb1708b42a2bc602fce37a65e4cecf657af064`  
		Last Modified: Tue, 15 Apr 2025 22:06:50 GMT  
		Size: 5.4 MB (5359243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe380ad9627cf6b4e50c70e4627fd2df3f6d79134972602712a728f18b6bcee`  
		Last Modified: Tue, 15 Apr 2025 22:06:50 GMT  
		Size: 5.2 MB (5204740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb16aa6ac423bd0499899c15434b165a9ea1e5142a37a8b9f32fd445b8cccf9f`  
		Last Modified: Tue, 15 Apr 2025 22:06:51 GMT  
		Size: 59.8 KB (59827 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:b5a36756aaf549bfe2191b33a9d96ce7eb9da3272c1af503ed851cfe7e02d6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97718174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80504106a31f08a98a49c12c92512b1132985c91863269c31b84ed9894ada837`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e97c1dd983d3a0e6141facf848be4ee354e9b0de4d3584eb068d75e8b8b54eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17655929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506f32926c0ed6384c290c59ee25d53c35875371668a37e4329f0f1593799cfb`

```dockerfile
```

-	Layers:
	-	`sha256:9b454bb2d5190570eebaa8a265e5c10114a0503c972f590518d839ce22692f20`  
		Last Modified: Tue, 15 Apr 2025 22:15:57 GMT  
		Size: 2.4 MB (2367680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe75eb067526abc361153ab75eb9f2d3cc8ca545eb2bb363330de93b1c9eabd`  
		Last Modified: Tue, 15 Apr 2025 22:15:57 GMT  
		Size: 5.0 MB (5024263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bdc5714d644845f3fa7d466c9a2b3b05ee168fde77aba9d11fc73991dccdb84`  
		Last Modified: Tue, 15 Apr 2025 22:15:57 GMT  
		Size: 5.2 MB (5177961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c53915cdf062b23c8e9a76f186d2200bbf255360b9f6f1608fbf0355e8c9c9b`  
		Last Modified: Tue, 15 Apr 2025 22:15:57 GMT  
		Size: 5.0 MB (5026005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a54753fd52ff60ea58daab4edfa8fbbc543d46633517af22e093a953a0a246`  
		Last Modified: Tue, 15 Apr 2025 22:15:58 GMT  
		Size: 60.0 KB (60020 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:00eb75263b9b8d6c9986ec82ef6f319aba3899898d3c29760373a42fb33d92ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113058126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a606739a9be22893a5430c5022f56c27bc438ee0c130cb8fb2448491114ec31`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b8e1239ee5f607f4eedd4486fe8a903dc4dc884f84c766c756b64690698d1143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18253792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a9f21072f8493f5d0ec2dea0235d4a563bd93ab23901d9cadcf478e3d7c63c`

```dockerfile
```

-	Layers:
	-	`sha256:158326da1a9576c885e22253af486945fe26995ff4cc2b72b02a1c317f1acf08`  
		Last Modified: Tue, 15 Apr 2025 22:19:23 GMT  
		Size: 2.4 MB (2367936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c79ec28e308649e5650e11468782541179c27a91a1910f6bdefed3b30e2ba39a`  
		Last Modified: Tue, 15 Apr 2025 22:19:23 GMT  
		Size: 5.2 MB (5222595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0518ff460c68abbe1a10e95defea3eac5a906bb03204457ce499b67d3e95e0`  
		Last Modified: Tue, 15 Apr 2025 22:19:23 GMT  
		Size: 5.4 MB (5378858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cf53731ece8f5ad26f1c3e5e524f5e8d0ddbc871dd139a4e0cc226b9f9a4d8`  
		Last Modified: Tue, 15 Apr 2025 22:19:23 GMT  
		Size: 5.2 MB (5224337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67af783807682b69d65688a3bcc150bbd23885446595698ddb226ced0ed5b4c0`  
		Last Modified: Tue, 15 Apr 2025 22:19:24 GMT  
		Size: 60.1 KB (60066 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:6f37acaea3494f3b9be11bd5bc7f774b5b42b60c41362aaf3576b3c3589ec980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113507000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4293912a535c0f45c8b53f23d4f94fc7791cde4bbb6b5dff199632de2f4337`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cc0dd68bec8e6afeeb8e5ab68816964f001ff6d604689a986cfd51c467f51f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18110264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6f1b80afd09de051866343758ec11453616ac697346eee0b796a5d9e5cf463`

```dockerfile
```

-	Layers:
	-	`sha256:c354dcc63df7caef846687d5846c4a21130ae7732f2e19e6351700e80cd5c12d`  
		Last Modified: Tue, 15 Apr 2025 22:11:20 GMT  
		Size: 2.4 MB (2371231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3829fa0878a900c8ddfa7d9a2a847f453cbe6e98303fe1e8a6388a9b8338ab70`  
		Last Modified: Tue, 15 Apr 2025 22:11:20 GMT  
		Size: 5.2 MB (5173709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3379ce7540370641412d779f774928b3cf8205c78f132801ca634cb783faa55`  
		Last Modified: Tue, 15 Apr 2025 22:11:20 GMT  
		Size: 5.3 MB (5329984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae474bd2261065ac6d8c946d463e9d2f71af53e3562644083f921215c1290b6`  
		Last Modified: Tue, 15 Apr 2025 22:11:20 GMT  
		Size: 5.2 MB (5175451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5770dae2c5b304de4a82dae5ea82f735ed9e28e248aba098ed70db4a20429ce`  
		Last Modified: Tue, 15 Apr 2025 22:11:21 GMT  
		Size: 59.9 KB (59889 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:f18370fc6757b2c94788c2b8b0be974872920c7fb5ccbd38616c655ce07174df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde5b16a5a43c10c13f022a0eef0a8424a58318251eb45544ac1f0be371aa189`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:698147c675d83d4f16bcce7681a08378c81cf70ce993aef567dff8d851e649da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18083874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35741052d8103174714bd39025d0f4743578da318db202e7fe879373d9e26506`

```dockerfile
```

-	Layers:
	-	`sha256:5df5b32ca73dde09f7b5a4acc49c32ddd21d91f8e6b22874fddf7f1cfbc4330e`  
		Last Modified: Tue, 15 Apr 2025 22:09:25 GMT  
		Size: 2.4 MB (2359441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856590e32f4c843e50dae8c9d07ce685e9aa1bf9c1a7c9c0b0b4800131b4994a`  
		Last Modified: Tue, 15 Apr 2025 22:09:26 GMT  
		Size: 5.2 MB (5169702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89cb5d3e8d1215cc96c43463976481a9a265ee01a20ee7217a6f668ce75df078`  
		Last Modified: Tue, 15 Apr 2025 22:09:26 GMT  
		Size: 5.3 MB (5323398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66fc720accc6d2441dce3c3f391790e79b26d20447a63bea3de7739d1c8bd4c3`  
		Last Modified: Tue, 15 Apr 2025 22:09:26 GMT  
		Size: 5.2 MB (5171444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db888d36e456b246c6ad28d351db5ae39a33b10230c22b07a67af266157f198`  
		Last Modified: Tue, 15 Apr 2025 22:09:26 GMT  
		Size: 59.9 KB (59889 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:499bcb397d8a9738a5876b3c9cf59795e7e944017a190924921ac6449471d389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107079656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02dd51864030461e4b8ef4ae9218a29ca3d55d60f91349066c078e75ceb40553`
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

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:61ed3a8261fe8215581c4cbc233c604fc128677d5f5691c95d06903467720304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17740227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b668620e2356101202bad73b53a61fa245d865b9060363d2d171e8e59d99099f`

```dockerfile
```

-	Layers:
	-	`sha256:0dc2ef5067487a89e41f382642d521dc9d5f73c0e1a789a98f16c6d07d12f891`  
		Last Modified: Tue, 15 Apr 2025 22:10:52 GMT  
		Size: 2.4 MB (2368988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3699e413e1a9cb248216c502caef82b97683b298e08ab9c5d5a086bd0a4e6262`  
		Last Modified: Tue, 15 Apr 2025 22:10:52 GMT  
		Size: 5.1 MB (5051575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a718f5841a735c3df5bd8fd1693f5e779c9425f7c4185bd28614fb4fabcc7dc0`  
		Last Modified: Tue, 15 Apr 2025 22:10:52 GMT  
		Size: 5.2 MB (5206520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45b1d62dea755c46eee21568129bd60844c35275ba6a2f7aa813c9ac9131175`  
		Last Modified: Tue, 15 Apr 2025 22:10:52 GMT  
		Size: 5.1 MB (5053317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1867e9430e01784474bb1d0a1a24b712e11c2bc2973eb05b0434eb4dadc5c91`  
		Last Modified: Tue, 15 Apr 2025 22:10:53 GMT  
		Size: 59.8 KB (59827 bytes)  
		MIME: application/vnd.in-toto+json
