## `rabbitmq:4-management`

```console
$ docker pull rabbitmq@sha256:e24c4f044b5fe04c02ba9791d6a0cd324a7ab8efbfb73821985f57f4ba36ffb2
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
$ docker pull rabbitmq@sha256:ead0bc61315912c89bc3be129c85a18f86ecf72fa9f7a155ec0ba0285d65a7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117476873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bb315154062c4e4628ba3f26fc7cb66c1b8036ac958b041bd333ba843eaf69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 19:13:07 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:13:07 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:13:07 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:13:07 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:13:07 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:13:07 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:13:08 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Feb 2026 19:13:08 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:13:08 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:13:08 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:13:08 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:13:27 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:13:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:13:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:13:28 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:13:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:13:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:13:28 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:13:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:13:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:13:29 GMT
CMD ["rabbitmq-server"]
# Mon, 09 Mar 2026 18:34:54 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Mon, 09 Mar 2026 18:35:06 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-gnu'; digest='291d8ce7fa85a374cc613a9ddff0bbce0b65ac50d1e44e0386ab960677be20c5' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-gnu'; digest='da3acbe998ec06bc9dfe41bd7b5c49365b60366f03d6481badfcf1a430221b1b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Mon, 09 Mar 2026 18:35:06 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737b809c13c293a6a0f4095ef499bd1b306e3077a20b750e96da93689da0fc8`  
		Last Modified: Fri, 20 Feb 2026 19:13:53 GMT  
		Size: 46.3 MB (46277609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5fc766253d41e6f7612eb33b058a6cc1c0204d0200ac663c4f1535f48a6c54`  
		Last Modified: Fri, 20 Feb 2026 19:13:51 GMT  
		Size: 9.0 MB (8985488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968a6189d29ce9d72ab06f87d5c1ab68470e2ce8586437636987804e83d4025b`  
		Last Modified: Fri, 20 Feb 2026 19:13:51 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766dfd181eececccf12ef38210bf56f5431666e24fc0e708ae02567f80c72498`  
		Last Modified: Fri, 20 Feb 2026 19:13:52 GMT  
		Size: 28.0 MB (27961525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eef02324233a0f3bc96e7bab4cbadb6e8c82888f2e0d0dd8cedd1697f53ad77`  
		Last Modified: Fri, 20 Feb 2026 19:13:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfa4b1dd3e3bcf696a093e335e67997c2da38cd06691efbed5eb1d4ff0107d2`  
		Last Modified: Fri, 20 Feb 2026 19:13:53 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e45bf90ea563b568cf92d25f16175d2ad06c1b90deb97409997719e8bce6443`  
		Last Modified: Fri, 20 Feb 2026 19:13:53 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0a1ce0c420d497245f93346d0d18dd6d2e13832040eec67ed3ce08adfa678d`  
		Last Modified: Fri, 20 Feb 2026 19:13:54 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec444487e8766fb5810ece85b7d6f05a3b2f21e5b5c9d1cdee9824f1f993761`  
		Last Modified: Mon, 09 Mar 2026 18:35:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f959a50a37c495453ccbc852ec87640c382688a1143fa509406aaf2417613f`  
		Last Modified: Mon, 09 Mar 2026 18:35:14 GMT  
		Size: 4.5 MB (4512915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c4531b280309520587b1d9d467d54d72af146948b98b48145af833e11ed4a652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59af29530c77d97840c2a7bee7942d897adc6ac0b1bd6ce3bde5bf8c1bdae23d`

```dockerfile
```

-	Layers:
	-	`sha256:6bc3d3d3a67ea19da663cb0efe6942e48995519df9a39bf6c6ad9d994b71006c`  
		Last Modified: Mon, 09 Mar 2026 18:35:14 GMT  
		Size: 2.5 MB (2486673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c16f1a954df1eb3e8cd28dc8c30f5fcc2ff8b5a046a5cb9944820779718dab3c`  
		Last Modified: Mon, 09 Mar 2026 18:35:14 GMT  
		Size: 16.3 KB (16269 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:fae94225610b8db05b67f1c421f54de76698352032a6d01b23471e3fe75cc4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95342928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb05b21cb774feb835451b4d6451a4fd482c6180c728bcdd49c6560e4e421993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:51:23 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:51:27 GMT
ADD file:9633092e110ed5475e9e31841bcc6e288ca09c116e102d75694089f384f549b3 in / 
# Tue, 10 Feb 2026 16:51:28 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 19:12:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:12:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:12:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:12:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:12:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:12:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:12:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Feb 2026 19:12:30 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:12:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:12:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:12:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:12:51 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:12:52 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:12:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:12:52 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:12:52 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:12:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:12:52 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:12:52 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:12:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:12:52 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:12:52 GMT
CMD ["rabbitmq-server"]
# Mon, 09 Mar 2026 18:52:47 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Mon, 09 Mar 2026 18:52:47 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-gnu'; digest='291d8ce7fa85a374cc613a9ddff0bbce0b65ac50d1e44e0386ab960677be20c5' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-gnu'; digest='da3acbe998ec06bc9dfe41bd7b5c49365b60366f03d6481badfcf1a430221b1b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Mon, 09 Mar 2026 18:52:47 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:dd135084b7c993802b7c1ba97d192c201727ddf710812c361d5441cb729f5c20`  
		Last Modified: Tue, 10 Feb 2026 17:41:49 GMT  
		Size: 26.9 MB (26855457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14e8fa411c4d8defbabbcdd26ba222a584a7e47c02f3256539f1a31eced6ea`  
		Last Modified: Fri, 20 Feb 2026 19:13:16 GMT  
		Size: 33.3 MB (33312611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bb21477220271c9c9da20d18b4f1aa4a5870683b70fdf41da61d5f1c49ecec`  
		Last Modified: Fri, 20 Feb 2026 19:13:15 GMT  
		Size: 7.3 MB (7301108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c4da6636adf340aac9eb860cc4d5887b04f1b851236d05f4ea2a300e418542`  
		Last Modified: Fri, 20 Feb 2026 19:13:15 GMT  
		Size: 9.8 KB (9766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b6d3400e4f4fb8be85d948e1fb7014f0b2bc47b68f67250a6d96b2ee38925`  
		Last Modified: Fri, 20 Feb 2026 19:13:16 GMT  
		Size: 27.9 MB (27861932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b5a382db4ea338fb49510952c7abd0f22ffaf0d6e6db114c184d63b9469733`  
		Last Modified: Fri, 20 Feb 2026 19:13:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a765d5cdec1f679eed8ac4ab57fc25771ccab9fd4fc98e84d8c666f73fd3d312`  
		Last Modified: Fri, 20 Feb 2026 19:13:17 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fb34f176fc26fa1e3848b5af21833541e259dcafc62c328ba16bb14c5c123`  
		Last Modified: Fri, 20 Feb 2026 19:13:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42789cd514fab2b4279b94105712dbfac6a371f0fb1bb749f6c7fe6cd433b9c9`  
		Last Modified: Fri, 20 Feb 2026 19:13:18 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ead6daaedb66453dc19d813a3388f39ea88405763287e39348dcd6472258445`  
		Last Modified: Mon, 09 Mar 2026 18:52:55 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6481334695d308ad2d3391a1c58c4230e5f5d76b345b6041aa05440f9051931c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae32b2e0027cea037a25f6405776328ff38aa1460df25e382de8aba47e4ddda`

```dockerfile
```

-	Layers:
	-	`sha256:aea3c2043c6653921ddf074739978ef3c42a10c7b332a74cf03ba883d48ecb61`  
		Last Modified: Mon, 09 Mar 2026 18:52:55 GMT  
		Size: 2.5 MB (2487473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d6ad5a0184f4da755f73734e714265e9cb5cae8797e3a664a7b5f9a9da65d9`  
		Last Modified: Mon, 09 Mar 2026 18:52:55 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:841164a65b40c2af2621415fb6a2afc6187ad5ef97ef4d75db3df38d999d8d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115118404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40708241e06cc425d50f7be602bd948cc53ab5b5dcd30617961d95f45f388fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 19:14:10 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:14:10 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:14:10 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:14:10 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:14:10 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:14:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:14:11 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Feb 2026 19:14:11 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:14:11 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:14:11 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:14:11 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:14:33 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:14:33 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:14:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:14:34 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:14:34 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:14:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:14:34 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:14:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:14:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:14:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:14:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:14:34 GMT
CMD ["rabbitmq-server"]
# Mon, 09 Mar 2026 18:36:17 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Mon, 09 Mar 2026 18:36:31 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-gnu'; digest='291d8ce7fa85a374cc613a9ddff0bbce0b65ac50d1e44e0386ab960677be20c5' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-gnu'; digest='da3acbe998ec06bc9dfe41bd7b5c49365b60366f03d6481badfcf1a430221b1b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Mon, 09 Mar 2026 18:36:31 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a50fda65c75d013e550609da44745b2ad2a0407cff6694d10b3e71176ce7f33`  
		Last Modified: Fri, 20 Feb 2026 19:15:00 GMT  
		Size: 44.4 MB (44384350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef903154297c4db746eefd3570aba4960159a8fe38754887918499378fc9eeb0`  
		Last Modified: Fri, 20 Feb 2026 19:14:58 GMT  
		Size: 9.7 MB (9708957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f93e7064210c1a23654b906dc7bfb2d6fd6a9a68b7ff0cc899e3a0c2d99c346`  
		Last Modified: Fri, 20 Feb 2026 19:14:58 GMT  
		Size: 9.6 KB (9639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6e93d6160af8d35d69f012a43cd61fde86dd78d0ac18ea0be1ea11ed89707a`  
		Last Modified: Fri, 20 Feb 2026 19:14:59 GMT  
		Size: 27.9 MB (27872040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcca2a756547a1fec4ed53c2af56ece868a723c332502dcb4797192944471a`  
		Last Modified: Fri, 20 Feb 2026 19:14:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea74ed3e57ee18c16469a40f3ae5281a28a90e6cab66c185cd510944351a59d5`  
		Last Modified: Fri, 20 Feb 2026 19:15:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cba482cea90298b1716c2b22dae9e78b0a41b0ddc34bf8411d26417578a936`  
		Last Modified: Fri, 20 Feb 2026 19:15:00 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6159d45eace0b4aba908d93a385f5200da9d9da4913144101883b261ad03b9`  
		Last Modified: Fri, 20 Feb 2026 19:15:01 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904d8832bc51e2f558b758403f7124e6691f1a945b3f877c4eff0525969fa77c`  
		Last Modified: Mon, 09 Mar 2026 18:36:38 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf25fcbded3882b6893f82f4abbeaf45799ed0929d0a7016556edb7055556b1`  
		Last Modified: Mon, 09 Mar 2026 18:36:38 GMT  
		Size: 4.3 MB (4276269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ff0bf2a55abb64efe1abcf88f38082a0474462a7dc91001c88e8fa876d92c4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70928dd3c8c3463c379dfb1bd65c149eccd9adc22f8013ad02b2bffe09d090a8`

```dockerfile
```

-	Layers:
	-	`sha256:18bb13853e48ab6db000be8c3d59efaffdcfb0af7acac89e617bbb07c811089d`  
		Last Modified: Mon, 09 Mar 2026 18:36:38 GMT  
		Size: 2.5 MB (2487733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee4fbea2acd9709fccd365f51b8988eb2f397fd12cd50537841c35ec50db6c50`  
		Last Modified: Mon, 09 Mar 2026 18:36:38 GMT  
		Size: 16.4 KB (16387 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:d656ef3b1b79919b2be196c349c5a536010d59d95b58739b5b0430bdef4c256c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111353099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe362dff440c5b7a3614647396f1cdeb63fe18488b07df1d306c5549a441e21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 19:15:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:15:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:15:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:15:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:15:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:15:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:15:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Feb 2026 19:15:52 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:15:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:15:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:15:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:16:33 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:16:36 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:16:39 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:16:39 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:16:39 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:16:39 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:16:39 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:16:41 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:16:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:16:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:16:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:16:42 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Feb 2026 20:09:32 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 25 Feb 2026 05:25:38 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.26.0/rabbitmqadmin-2.26.0-x86_64-unknown-linux-gnu'; digest='66b56f0aa975142035d58ff5c652dfbf466b2bb848fc8183d72f5eb304aa308c' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.26.0/rabbitmqadmin-2.26.0-aarch64-unknown-linux-gnu'; digest='af39eb11a8c4b8dd4ebd1d0a4e50c27aa100b516f9c42cc1e63aad700da8d923' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 25 Feb 2026 05:25:38 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b9ba7fd5441568fb847e1b3e915439a5731cba018544b167e2144120385479`  
		Last Modified: Fri, 20 Feb 2026 19:17:42 GMT  
		Size: 39.5 MB (39521005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3f2a41135e0f2e9bb938ce5d5782d597047132b5c87d7bc5f7370fb2ac9af5`  
		Last Modified: Fri, 20 Feb 2026 19:17:40 GMT  
		Size: 9.6 MB (9591827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8213887204d5dee7c482b684651ceddfb69bf755936ad743d316e30ba6b653`  
		Last Modified: Fri, 20 Feb 2026 19:17:39 GMT  
		Size: 9.6 KB (9646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5009e80d851c20fe0acc0009260737dfc0b092970bfff38f1a32afc4d0eab568`  
		Last Modified: Fri, 20 Feb 2026 19:17:41 GMT  
		Size: 27.9 MB (27921660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4450967b7ef4616ac8f32e75cccf579a145eca633d6d9a7239b827dda6ea1e`  
		Last Modified: Fri, 20 Feb 2026 19:17:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c903c558096ef330a2bd3028c36025c89c032d0f226cdc14fc055aff9030cb00`  
		Last Modified: Fri, 20 Feb 2026 19:17:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77375774fd8a3ab93520a89fc77271452709dc210495ccbae1233e21eb91118f`  
		Last Modified: Fri, 20 Feb 2026 19:17:42 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe81ed0d83edaffebeb1f4f33e26bb559ae9767a42c953fa3184f2eec12b2728`  
		Last Modified: Fri, 20 Feb 2026 19:17:43 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3598d8500d706ba8d8b6ddcb7d0dc692cbace58b874adc4b64680ba11542de59`  
		Last Modified: Fri, 20 Feb 2026 20:09:52 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:00f181e4c5b0c13f6d9c004d8e19eb9e7b45cc86d593cc1503e5d1d6ff4bf831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6527c8d08c5cbe94f75cf2eafbb60a2a551054c588f3722fe18c48d38d20658e`

```dockerfile
```

-	Layers:
	-	`sha256:917765b1cf200a7cbf74a336fa07e87d840bf6a8d06b45dbc6e575b64b340039`  
		Last Modified: Wed, 25 Feb 2026 05:26:00 GMT  
		Size: 2.5 MB (2491126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09a6930ba2a45982f3a366630b1b35219c8d6d80a549dcddb338b7a6ddda2d6c`  
		Last Modified: Wed, 25 Feb 2026 05:25:59 GMT  
		Size: 16.3 KB (16310 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:c06b27b214a9a9941904687d45cd0a3b7d0adf49361454ea5705ff345cdb18f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104843996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38cd9ca010d688c1af9814a07bcfe19fbf7cc29a9c602aadb799a4e3cfed7a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 17:33:09 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:33:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:33:10 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 17:33:55 GMT
ADD file:b4821892707dbb5cc8e8eb3b4e757edc2d124db81fcdedfc3b244dcb5c1fa6c0 in / 
# Tue, 10 Feb 2026 17:34:00 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 20:10:56 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 20:10:56 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 20:10:56 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 20:10:57 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 20:10:57 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 20:10:57 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 20:11:00 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Feb 2026 20:11:00 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 20:11:00 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 20:11:00 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 20:11:00 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 20:13:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 20:13:24 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 20:13:24 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 20:13:24 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 20:13:24 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 20:13:24 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 20:13:24 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 20:13:25 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 20:13:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 20:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 20:13:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 20:13:25 GMT
CMD ["rabbitmq-server"]
# Fri, 20 Feb 2026 23:06:13 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Fri, 27 Feb 2026 16:14:56 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.26.0/rabbitmqadmin-2.26.0-x86_64-unknown-linux-gnu'; digest='66b56f0aa975142035d58ff5c652dfbf466b2bb848fc8183d72f5eb304aa308c' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.26.0/rabbitmqadmin-2.26.0-aarch64-unknown-linux-gnu'; digest='af39eb11a8c4b8dd4ebd1d0a4e50c27aa100b516f9c42cc1e63aad700da8d923' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Fri, 27 Feb 2026 16:14:56 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f2683d5e2cbe038b4f1178e139d507e705e0a3a566f8b9c89bf3484f426119af`  
		Last Modified: Tue, 10 Feb 2026 17:42:05 GMT  
		Size: 31.0 MB (30954431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e859433849962fa0c87ef35b20b509699f99c5d50bb8ace353a37cea36f455a`  
		Last Modified: Fri, 20 Feb 2026 20:19:50 GMT  
		Size: 35.2 MB (35174774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc270860c2e13dd83ca6cc9b6adc11fc5196cdfb87f331f0fa69286104fad8bf`  
		Last Modified: Fri, 20 Feb 2026 20:19:43 GMT  
		Size: 10.8 MB (10828936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1307e8a106243bd8e4e1a4604db25b8bbc88c0d8599b45109a6f057d53695647`  
		Last Modified: Fri, 20 Feb 2026 20:19:36 GMT  
		Size: 9.7 KB (9700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570b21c1a56b01530a66057fc75d5ea47590baf06fb63c7cb8e264d55b18deac`  
		Last Modified: Fri, 20 Feb 2026 20:19:49 GMT  
		Size: 27.9 MB (27874102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46a75cc1a5dd37f6ea9035cbf95927efaceb6d7aa287811b29554ef1b2806b`  
		Last Modified: Fri, 20 Feb 2026 20:19:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb8d35cb35d13d2bfdad6485b6ad76b73e04effa61632496ba60207e7f89df7`  
		Last Modified: Fri, 20 Feb 2026 20:19:43 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b65c74b583701c50179a73a2f653e2cdb324705cb07cd12c37ff8a642913064`  
		Last Modified: Fri, 20 Feb 2026 20:19:45 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b386d8ae9eaca90e5aa1bf935f1c6cbc35e18dc2742ec407114a4edfddd1466`  
		Last Modified: Fri, 20 Feb 2026 20:19:45 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a44596fd78c2b8eb053386b1f0e9d7ae95c5af00753a5168e771ecfdff23f25`  
		Last Modified: Fri, 20 Feb 2026 23:07:36 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e0b7e11e0362a65a22bf0de9058a9eb1489b244dfdc047d129cb40bf1bf8f0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11e9a17a01963ecaf97f37be87e0f9e367e5e0feb933df37285666e82423468`

```dockerfile
```

-	Layers:
	-	`sha256:a620e5caaf3eecc16f2ef200f9e7ea1494f115d7c403efba8a8afde30f8af390`  
		Last Modified: Fri, 27 Feb 2026 16:16:16 GMT  
		Size: 2.5 MB (2479040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e328162d26980597a3f28b64e78e9736f71b4e89b78c746c49af43bdd25e66ef`  
		Last Modified: Fri, 27 Feb 2026 16:16:15 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:89419caf2c88a0d99ca9b4829813a0a819fa647341e8d848714084de7d88e533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105095192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9738ac67c3396d81342ef13bd8b7126373551bdf7faa6ceca2f2eaaf82560`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 19:18:36 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 20 Feb 2026 19:18:36 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 20 Feb 2026 19:18:36 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 20 Feb 2026 19:18:37 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 20 Feb 2026 19:18:37 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:18:37 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:18:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 20 Feb 2026 19:18:40 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 20 Feb 2026 19:18:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 20 Feb 2026 19:18:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 20 Feb 2026 19:18:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Feb 2026 19:19:12 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 20 Feb 2026 19:19:14 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 20 Feb 2026 19:19:15 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 20 Feb 2026 19:19:15 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 20 Feb 2026 19:19:15 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 20 Feb 2026 19:19:15 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Feb 2026 19:19:15 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 20 Feb 2026 19:19:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 20 Feb 2026 19:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Feb 2026 19:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Feb 2026 19:19:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 20 Feb 2026 19:19:16 GMT
CMD ["rabbitmq-server"]
# Mon, 09 Mar 2026 19:05:50 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Mon, 09 Mar 2026 19:05:50 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-gnu'; digest='291d8ce7fa85a374cc613a9ddff0bbce0b65ac50d1e44e0386ab960677be20c5' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-gnu'; digest='da3acbe998ec06bc9dfe41bd7b5c49365b60366f03d6481badfcf1a430221b1b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Mon, 09 Mar 2026 19:05:50 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c53d1a9b415b405482edb8bb9d563937505c703d6a10916fed03979ad8b950b`  
		Last Modified: Fri, 20 Feb 2026 19:20:12 GMT  
		Size: 38.6 MB (38615127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15528794eaf6ce4cdc78df1abd9fbfc5f7f3d1fb58c6313b7115622e75210d49`  
		Last Modified: Fri, 20 Feb 2026 19:20:11 GMT  
		Size: 8.6 MB (8613477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7ba8b125733a79f6c15415ebc35cfbebcfe215df0a502f799061b77a446bc2`  
		Last Modified: Fri, 20 Feb 2026 19:20:11 GMT  
		Size: 9.8 KB (9801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ace4667f8ebb3596b5ac7ead95903b2d927d2b7685d7a2c9a5b1601347b98b`  
		Last Modified: Fri, 20 Feb 2026 19:20:12 GMT  
		Size: 27.9 MB (27944944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c75cf7f9190c873e2c2959dbb621ddd41763500b0351ffc04d31cdabbddbfb9`  
		Last Modified: Fri, 20 Feb 2026 19:20:12 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e530a7e40867c28a417868e7a780347d93ec2368733eecaed3c7eb4bc60679`  
		Last Modified: Fri, 20 Feb 2026 19:20:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf29599f010ee92ef8ea8d46414ded6c1fd863f9f6ebc971d6f418b75be68a8`  
		Last Modified: Fri, 20 Feb 2026 19:20:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487123714141016f4dcac1d5e789cefb712a61bdec3dbcd833a8cb853de9d1a7`  
		Last Modified: Fri, 20 Feb 2026 19:20:13 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dd1dafdde0962cebba72e18d7dc2ebadf62cde402e7c6f2ab1255709f6061f`  
		Last Modified: Mon, 09 Mar 2026 19:06:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7f23f570119f36adc5270e9d0f947c67fd62ace065c0470b81cfeeb6167f68cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2505046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2e02002c6273e2d487e5244455a205b1808c71f2d6266f2c8812d8737659b8`

```dockerfile
```

-	Layers:
	-	`sha256:6adeb1e07626aee22ea5f243e56a0bf41d25a11cbbf70a8cb195b35757515b5f`  
		Last Modified: Mon, 09 Mar 2026 19:06:03 GMT  
		Size: 2.5 MB (2488783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151efcbac0642495acf885c19fa46fb8179ad2e39cb2bb9717f0a2832be2998f`  
		Last Modified: Mon, 09 Mar 2026 19:06:03 GMT  
		Size: 16.3 KB (16263 bytes)  
		MIME: application/vnd.in-toto+json
