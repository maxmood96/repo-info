## `rabbitmq:management`

```console
$ docker pull rabbitmq@sha256:aeee1db0ff9fdb1347f3585242c14ed10877b56c22eeaa113b21208ef3dd3edf
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
$ docker pull rabbitmq@sha256:e6b9a7b9293b17d884e414aa7aba7382ad85ee10a04feb0d00c2187bbc529893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117481485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e474d7d441704e878e4249148d4893b08c0c658096ed0b163502616c3c38593`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:20:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 17 Mar 2026 02:20:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 17 Mar 2026 02:20:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 17 Mar 2026 02:20:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 17 Mar 2026 02:20:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:20:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 17 Mar 2026 02:20:35 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 17 Mar 2026 02:20:35 GMT
ENV RABBITMQ_VERSION=4.2.4
# Tue, 17 Mar 2026 02:20:35 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 17 Mar 2026 02:20:35 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 17 Mar 2026 02:20:35 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:20:57 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 02:20:58 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 02:20:58 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 02:20:58 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 02:20:58 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 02:20:58 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:58 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 02:20:58 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 02:20:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:20:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:58 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 02:20:58 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 03:20:11 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 03:20:21 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-gnu'; digest='291d8ce7fa85a374cc613a9ddff0bbce0b65ac50d1e44e0386ab960677be20c5' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-gnu'; digest='da3acbe998ec06bc9dfe41bd7b5c49365b60366f03d6481badfcf1a430221b1b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 03:20:21 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b9cad85b872564b008f27ffa402e1f6b6b618fe12ba32269243879ed7f2430`  
		Last Modified: Tue, 17 Mar 2026 02:21:21 GMT  
		Size: 46.3 MB (46276950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1daa1e08f9e9ec845d621f5c502360b655af01001d2587d05de7372ef7189ba`  
		Last Modified: Tue, 17 Mar 2026 02:21:20 GMT  
		Size: 9.0 MB (8985479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fab35df390606980f874b94d3304492aa72ba675f8e139a7847d62e0c539a4`  
		Last Modified: Tue, 17 Mar 2026 02:21:19 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badcee8df0c24cb919594dd1a91739f88b742a8293da88166f17bfc53f18501c`  
		Last Modified: Tue, 17 Mar 2026 02:21:21 GMT  
		Size: 28.0 MB (27961473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291a8daff2845dba5c667279854bc12ae6a749da09d31b4c228e830c95c8b586`  
		Last Modified: Tue, 17 Mar 2026 02:21:20 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b767f150c9f1f716eeeba7b9e9f40a0dd9335de6f5bd68a4360fa3f7de9bc11`  
		Last Modified: Tue, 17 Mar 2026 02:21:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfdf8a5bb483ba17abcccf0113c5aa626bb100892802062ad0bfbf9b4f07ee8`  
		Last Modified: Tue, 17 Mar 2026 02:21:21 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c022413d08eb2c7e8d2e3418b5daf6429a602f38648f701af94291f46b6f`  
		Last Modified: Tue, 17 Mar 2026 02:21:22 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372f55fba8a4a2176ea36cb174dfc6e2ac65aa3ace83aa7136c693081aac7146`  
		Last Modified: Tue, 17 Mar 2026 03:20:28 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2c1ffc44ce9643ac7cb495dbc16da61cf1ac948844a935ef808a689d3b9759`  
		Last Modified: Tue, 17 Mar 2026 03:20:28 GMT  
		Size: 4.5 MB (4513895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9497fa9d757c7c3c5fe5197cec7ddaa093e6d35e166d1868886ec00114a343ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4896df7f5fb2cbdfdb8564e36a3b5a0a5ba9c879e626b91776b7d2245d29c0`

```dockerfile
```

-	Layers:
	-	`sha256:1a17cb3a8acdbbaad7dd92bc1fe2b1b3419fe137622eabb96ad3ec4e26ce091e`  
		Last Modified: Tue, 17 Mar 2026 03:20:28 GMT  
		Size: 2.5 MB (2486689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e315c9bdcf0e30fec1d6625dc2567cb39ec811f685eae56d33b39d73298cec29`  
		Last Modified: Tue, 17 Mar 2026 03:20:28 GMT  
		Size: 16.3 KB (16269 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:fe6d06270636dae1f3562a5d27e5bb0d3fc55965e082bd49edb252f2b3201c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95348208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4655472a1031fb4163a0c33bd9f949be798f2a9a28f8c8f691a656ef5e5f20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:10 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:10 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:14 GMT
ADD file:834191023ea63b612bd409fecc858bd572114f2ce02aca5944385eae5eaf48f8 in / 
# Mon, 23 Feb 2026 17:19:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:20:21 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 17 Mar 2026 01:20:21 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 17 Mar 2026 01:20:21 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 17 Mar 2026 01:20:21 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 17 Mar 2026 01:20:21 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:20:21 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 17 Mar 2026 01:20:22 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 17 Mar 2026 01:20:22 GMT
ENV RABBITMQ_VERSION=4.2.4
# Tue, 17 Mar 2026 01:20:22 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 17 Mar 2026 01:20:22 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 17 Mar 2026 01:20:22 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:20:48 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 01:20:49 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 01:20:49 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 01:20:49 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 01:20:49 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 01:20:49 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 01:20:49 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 01:20:49 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 01:20:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:20:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:20:49 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 01:20:49 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 02:37:22 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 02:37:22 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-gnu'; digest='291d8ce7fa85a374cc613a9ddff0bbce0b65ac50d1e44e0386ab960677be20c5' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-gnu'; digest='da3acbe998ec06bc9dfe41bd7b5c49365b60366f03d6481badfcf1a430221b1b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 02:37:22 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:51c4cbb22341ed2a12c82974973354e1be3db5c9041bb5fbe2640ced2f41020b`  
		Last Modified: Mon, 23 Feb 2026 17:51:31 GMT  
		Size: 26.9 MB (26859311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab4f0ec897e555784db19d1e62617444a3a5ffd85323c5190b5d4a8e0d07c93`  
		Last Modified: Tue, 17 Mar 2026 01:21:13 GMT  
		Size: 33.3 MB (33314034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c5dc0988c7a75a268e8647f078608145c00ddeba57c53ec9038123c8c06889`  
		Last Modified: Tue, 17 Mar 2026 01:21:12 GMT  
		Size: 7.3 MB (7301129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ee9c93026459ee826be15b6ae4f062777e1fbf8c5e858e601d999ce9e74197`  
		Last Modified: Tue, 17 Mar 2026 01:21:12 GMT  
		Size: 9.8 KB (9751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93d092829ff3e7398e25bb0c5911738ce48e6f96e068702564865cca83f25ee`  
		Last Modified: Tue, 17 Mar 2026 01:21:13 GMT  
		Size: 27.9 MB (27861931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab95e956e50408061050bbd00758c8dc9de0cadf739aa45a58e54bdcc9e859ea`  
		Last Modified: Tue, 17 Mar 2026 01:21:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ccf8898a94103fc0bbe98714cddfdc40c8620f50c3968940d46f28e99d84b9`  
		Last Modified: Tue, 17 Mar 2026 01:21:13 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906259a0762b6421875709e0aabd52cb0037c3be30f18b986edbdd6e6fa683b`  
		Last Modified: Tue, 17 Mar 2026 01:21:14 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6300e16f47f685dc36a893c824cf0e0d037a339279bbe4d96e55b96b489353d4`  
		Last Modified: Tue, 17 Mar 2026 01:21:14 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda77097861b6c9f62e843d238b0a39eb9e799623d67778cb8eca59bd91ee90a`  
		Last Modified: Tue, 17 Mar 2026 02:37:29 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:515efd3b4d22f7cc077219fb539a0f1c584eb88fae183283168033d10a4208d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f16e085c1817ca78fad4722e9eadb977d1a0ead786ac648de610b6c1e27610`

```dockerfile
```

-	Layers:
	-	`sha256:e1321ae926466623aa5074b11cca8cc657881460bc128ad4d3075ede599ca051`  
		Last Modified: Tue, 17 Mar 2026 02:37:29 GMT  
		Size: 2.5 MB (2487489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab06121c316f3521c4930ad7ffc5508a58484ac0ff5214e6aaa79ebfe51f8c9`  
		Last Modified: Tue, 17 Mar 2026 02:37:29 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:46d84795232d9f43a1c7007504b8b884992b64d0cefa961b07f6066f5692e099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115121426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb4d759d812ed67eaca27402ce17d1480bafe0aab7c0055cbd59260dbe7d0ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:51 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 17 Mar 2026 02:25:51 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 17 Mar 2026 02:25:51 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 17 Mar 2026 02:25:52 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 17 Mar 2026 02:25:52 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:25:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 17 Mar 2026 02:25:53 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 17 Mar 2026 02:25:53 GMT
ENV RABBITMQ_VERSION=4.2.4
# Tue, 17 Mar 2026 02:25:53 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 17 Mar 2026 02:25:53 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 17 Mar 2026 02:25:53 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:26:17 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 02:26:17 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 02:26:18 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 02:26:18 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 02:26:18 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 02:26:18 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:26:18 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 02:26:18 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 02:26:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:26:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:26:18 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 02:26:18 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 03:21:59 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 03:22:14 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-gnu'; digest='291d8ce7fa85a374cc613a9ddff0bbce0b65ac50d1e44e0386ab960677be20c5' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-gnu'; digest='da3acbe998ec06bc9dfe41bd7b5c49365b60366f03d6481badfcf1a430221b1b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 03:22:14 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f3db3697de07996a7128110a1dac244314228de7f8986d6940f26a2d6a824f`  
		Last Modified: Tue, 17 Mar 2026 02:26:44 GMT  
		Size: 44.4 MB (44382441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2258f0689be0eaec6f2668cae6b0304adf5814ad95eca24c6ac7ad3419386c`  
		Last Modified: Tue, 17 Mar 2026 02:26:43 GMT  
		Size: 9.7 MB (9708937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccddcc6e9c7004345e89b8cddb9b12a632f54092a79c57667dc432c0246a37da`  
		Last Modified: Tue, 17 Mar 2026 02:26:42 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99391c1b8c9b44a887273aa75d4a39672137bb8ad6d1c23f9a25aa3ccf90d954`  
		Last Modified: Tue, 17 Mar 2026 02:26:44 GMT  
		Size: 27.9 MB (27871973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da327a3d622183f011c22630530406c46f03cc820578a74f61b7d8f9a95f7c0`  
		Last Modified: Tue, 17 Mar 2026 02:26:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad27ddbf31de33a5cf480147f7e4739be0150ef51b942f7594a5d612aaaabab`  
		Last Modified: Tue, 17 Mar 2026 02:26:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba96bd0b2749350a6e2fc4adaf8588bf06bbc8a20b06ed412fad1894721655`  
		Last Modified: Tue, 17 Mar 2026 02:26:45 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aad0f93da889961304baaa7ed42d2b07fdef68e37f11526ddaf1fc0880936e`  
		Last Modified: Tue, 17 Mar 2026 02:26:45 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3b9ffdeb761cf83f5224229edfee414bfb809e655916c59164b7946ad2d78c`  
		Last Modified: Tue, 17 Mar 2026 03:22:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85880fe15e54a1470308fc08c9eb7937d22d07a297849c0a693dc2bc8152069c`  
		Last Modified: Tue, 17 Mar 2026 03:22:22 GMT  
		Size: 4.3 MB (4276676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:93afd7063e0e2e2d0b53d0a4c2588befd43000c78517d3cacf5bdca2a68deba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69aed35274ee9d1e8f255b1d5594d9473d92f3ca0a158f3d77147a005f1abf4a`

```dockerfile
```

-	Layers:
	-	`sha256:2b31d381778bc8d4477a60531483f5e2bd98a32d5785e3f6ee529ca54e7a793b`  
		Last Modified: Tue, 17 Mar 2026 03:22:22 GMT  
		Size: 2.5 MB (2487749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc3c9a4e0c35f1a1476a9f6b57e6dcc4c1bad984c5ba96fab8ea791cfa37a4e`  
		Last Modified: Tue, 17 Mar 2026 03:22:22 GMT  
		Size: 16.4 KB (16387 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:ace380d0e8f42cd4c077f99f574e3d0d8428f8010451a69f90741d759c2d0c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111356504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0c3c52af98776e084b74f3f822e32a3de276bc6f809ead82ae2a028a4e478f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:27:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 17 Mar 2026 09:27:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 17 Mar 2026 09:27:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 17 Mar 2026 09:27:58 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 17 Mar 2026 09:27:58 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 09:27:58 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 17 Mar 2026 09:28:00 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 17 Mar 2026 09:28:00 GMT
ENV RABBITMQ_VERSION=4.2.4
# Tue, 17 Mar 2026 09:28:00 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 17 Mar 2026 09:28:00 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 17 Mar 2026 09:28:00 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 09:29:02 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 09:29:04 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 09:29:05 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 09:29:05 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 09:29:05 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 09:29:05 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 09:29:05 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 09:29:05 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 09:29:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 09:29:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 09:29:06 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 09:29:06 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 17:01:49 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 17:01:49 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-gnu'; digest='291d8ce7fa85a374cc613a9ddff0bbce0b65ac50d1e44e0386ab960677be20c5' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-gnu'; digest='da3acbe998ec06bc9dfe41bd7b5c49365b60366f03d6481badfcf1a430221b1b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 17:01:49 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8f5803074ec873396a7e60bb55e5ae65da74bfe8192d888d59dbd1cb8d6d5f`  
		Last Modified: Tue, 17 Mar 2026 09:29:57 GMT  
		Size: 39.5 MB (39521363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6d6fde3ad503e5a8c0217d2bd787cacf0b5599dc437112c545a1df39efd40e`  
		Last Modified: Tue, 17 Mar 2026 09:29:56 GMT  
		Size: 9.6 MB (9591889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88163c891ad819e5573954f87eea11e6a4fb99defbeea1e19fa75bf3b178061b`  
		Last Modified: Tue, 17 Mar 2026 09:29:55 GMT  
		Size: 9.7 KB (9669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105a1245d7a5b728f5164d0f9fb282b853d6988edb57b43739f9d2e4fae02680`  
		Last Modified: Tue, 17 Mar 2026 09:29:57 GMT  
		Size: 27.9 MB (27921471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b27374dada9516718ab6bd552d160f620976067734d5cf3fb2f0605792bc6`  
		Last Modified: Tue, 17 Mar 2026 09:29:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040fc55cf788a73b470050329bfcc0f23249c9aff4078a1b02dbfdc2d3100081`  
		Last Modified: Tue, 17 Mar 2026 09:29:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e161ed19d1bea08343519e1c034796c882673d8659aa4086aadc9e7d13e9fa`  
		Last Modified: Tue, 17 Mar 2026 09:29:58 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06093cc4ca0eb806bc1f48d406e66c8362708ba227302c2e067c7bf4a32abdfe`  
		Last Modified: Tue, 17 Mar 2026 09:29:58 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136c10151c6d08d42ca7c2419ab1d6960d8d7b202ec45085e1c9b4b0a5c49c02`  
		Last Modified: Tue, 17 Mar 2026 17:02:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4c807b9e56de9a6dfb3d3dff5374cd6d4c24e4b15b14ba6c231fe39b8c9244e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12eecc432072ccd8ced101a231e9631af4cb79c736adbcda39ed6dc424f30be`

```dockerfile
```

-	Layers:
	-	`sha256:4d0f32c9cd9e866fd5b7f79740d0d029e3af209e2ff6ef45a6ac479511483097`  
		Last Modified: Tue, 17 Mar 2026 17:02:07 GMT  
		Size: 2.5 MB (2491142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad65cd5cd68927d108e5c0561a452f09149fe65c00f88fc2826fc28e72ae5ef8`  
		Last Modified: Tue, 17 Mar 2026 17:02:07 GMT  
		Size: 16.3 KB (16310 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:167eae568420ed66631f3a32dc6f241fac19f2ec94eeaa023b53934293087aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104843729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ada2cdd2838f24f826a72fbab1916fe3f15cf01e81aed1627fa9cd9ea1ae2e`
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
# Fri, 13 Mar 2026 21:05:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 13 Mar 2026 21:05:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 13 Mar 2026 21:05:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 13 Mar 2026 21:05:33 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 13 Mar 2026 21:05:33 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 21:05:33 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 13 Mar 2026 21:05:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 13 Mar 2026 21:05:36 GMT
ENV RABBITMQ_VERSION=4.2.4
# Fri, 13 Mar 2026 21:05:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 13 Mar 2026 21:05:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 13 Mar 2026 21:05:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 21:07:55 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 13 Mar 2026 21:08:04 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 13 Mar 2026 21:08:04 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 13 Mar 2026 21:08:04 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Mar 2026 21:08:04 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Mar 2026 21:08:04 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 13 Mar 2026 21:08:04 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 13 Mar 2026 21:08:04 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 13 Mar 2026 21:08:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 21:08:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 21:08:05 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 13 Mar 2026 21:08:05 GMT
CMD ["rabbitmq-server"]
# Sat, 14 Mar 2026 07:37:14 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Sat, 14 Mar 2026 07:37:15 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-gnu'; digest='291d8ce7fa85a374cc613a9ddff0bbce0b65ac50d1e44e0386ab960677be20c5' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-gnu'; digest='da3acbe998ec06bc9dfe41bd7b5c49365b60366f03d6481badfcf1a430221b1b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Sat, 14 Mar 2026 07:37:15 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f2683d5e2cbe038b4f1178e139d507e705e0a3a566f8b9c89bf3484f426119af`  
		Last Modified: Tue, 10 Feb 2026 17:42:05 GMT  
		Size: 31.0 MB (30954431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14b0fd98874c5ea9440b6f4041f5d9f924f068fcad019fd46e77e82fe333b68`  
		Last Modified: Fri, 13 Mar 2026 21:14:38 GMT  
		Size: 35.2 MB (35174557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5567215dcaafcf4f3d7a09bf170dbc905e931df84c13cb7ba3e7660d2be8c402`  
		Last Modified: Fri, 13 Mar 2026 21:14:31 GMT  
		Size: 10.8 MB (10828919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9699bf3b517ee4792ac34fb8bc46f03210de86ef089dee25ce234bdae4a0e`  
		Last Modified: Fri, 13 Mar 2026 21:14:25 GMT  
		Size: 9.7 KB (9703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c7ccf54945740572f89944882b141cc9476f7e27915505d32d523d79065937`  
		Last Modified: Fri, 13 Mar 2026 21:14:37 GMT  
		Size: 27.9 MB (27874063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a2b97141ec7a68f6744637af21f40add0d7478ef1f3c0b7fd5f24e1f349ee4`  
		Last Modified: Fri, 13 Mar 2026 21:14:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a22b6899574ab1e99e7fe13b7734fa186540090dea63b85f278e656bf8aa5e`  
		Last Modified: Fri, 13 Mar 2026 21:14:32 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1363c4b2705ce407ac4612ea6a535f30e773b63c50ccc1da5d35b5a8f655f7e3`  
		Last Modified: Fri, 13 Mar 2026 21:14:33 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847652964e681cc6bfdce07a52e58825f14324fc8535dfa46400adf6e86fccf0`  
		Last Modified: Fri, 13 Mar 2026 21:14:34 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd49df6324539a39c34b6e078571ffa5ccaace1d10cc2ad7a33deba7dc05a853`  
		Last Modified: Sat, 14 Mar 2026 07:38:33 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:41edc5eb6e54e873cbb0da3ece79d65234edcc1d2cba87235aa7d4b963ab8472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2bd9e93f5669aa99997944c712d3268b73d7a70ba434b590fb4957546bc97b`

```dockerfile
```

-	Layers:
	-	`sha256:8c5f629e4376b473cbec55b41c86ef05eb22dba3eb7205bf2f2a5c13f329fd3f`  
		Last Modified: Sat, 14 Mar 2026 07:38:33 GMT  
		Size: 2.5 MB (2479040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b653d4ee1de2dfb2aaced7d7fea48a7a78e0376007833f013ab70d8c68b8fc3`  
		Last Modified: Sat, 14 Mar 2026 07:38:32 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:bbfb2c5cb236050cb872cfa4e88623d09059974282eee1425fe08a96cf3b3426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105096915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38dba8416a0e3f9396d4a0bfcd07392574e1694210dd127b8d534ddc2303c39f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:45 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:46 GMT
ADD file:36da4c002083f47f3a54f9afaf09c1e01e856a8f55618e96eb26304b47eb72b6 in / 
# Mon, 23 Feb 2026 17:19:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:43:18 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 17 Mar 2026 02:43:18 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 17 Mar 2026 02:43:18 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 17 Mar 2026 02:43:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 17 Mar 2026 02:43:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:43:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 17 Mar 2026 02:43:24 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 17 Mar 2026 02:43:24 GMT
ENV RABBITMQ_VERSION=4.2.4
# Tue, 17 Mar 2026 02:43:24 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 17 Mar 2026 02:43:24 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 17 Mar 2026 02:43:24 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:44:15 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 17 Mar 2026 02:44:17 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 17 Mar 2026 02:44:18 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 17 Mar 2026 02:44:18 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 17 Mar 2026 02:44:18 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 17 Mar 2026 02:44:18 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:44:18 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 17 Mar 2026 02:44:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 17 Mar 2026 02:44:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:44:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:44:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 17 Mar 2026 02:44:19 GMT
CMD ["rabbitmq-server"]
# Tue, 17 Mar 2026 09:19:48 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Tue, 17 Mar 2026 09:19:51 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-x86_64-unknown-linux-gnu'; digest='291d8ce7fa85a374cc613a9ddff0bbce0b65ac50d1e44e0386ab960677be20c5' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.27.0/rabbitmqadmin-2.27.0-aarch64-unknown-linux-gnu'; digest='da3acbe998ec06bc9dfe41bd7b5c49365b60366f03d6481badfcf1a430221b1b' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Tue, 17 Mar 2026 09:19:51 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:07785e1e3448bfcdd4a7c917fe2208c68391368db6b314a3bd60d0c083944c3b`  
		Last Modified: Mon, 23 Feb 2026 17:51:53 GMT  
		Size: 29.9 MB (29910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa3fa571cd02e4397d34d2224f2145e29e6ba0579359032acb762b78e3e747`  
		Last Modified: Tue, 17 Mar 2026 02:45:19 GMT  
		Size: 38.6 MB (38616185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e53b515f3f3ab57294a4a934ed54ef67828f3b8d255f6da24df846b98752f9`  
		Last Modified: Tue, 17 Mar 2026 02:45:17 GMT  
		Size: 8.6 MB (8613451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1b77d335e4a04b3e41d63fc4b157b097b0959fdd121ad7969a7c7a8da6d694`  
		Last Modified: Tue, 17 Mar 2026 02:45:16 GMT  
		Size: 9.9 KB (9855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e1476f99edb35fd2fa9dd794b3f994defb20d46c23ef7dcd770fe676ccf9c1`  
		Last Modified: Tue, 17 Mar 2026 02:45:18 GMT  
		Size: 27.9 MB (27944981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9c7a0fd179a259f6a0b03383958296a2f958bee4f169ee7fe8dc7b011b407a`  
		Last Modified: Tue, 17 Mar 2026 02:45:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df942ba2dc575e79d20e334a7273ba27947c6ebdf1593c380472605013424ac7`  
		Last Modified: Tue, 17 Mar 2026 02:45:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ca1229a6cc68dad82a0f0b8975a1e93762e8dfa6cd2a11df20e5b389dc4f6`  
		Last Modified: Tue, 17 Mar 2026 02:45:19 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2724a6080af7a0d59e685e0103887a9fb79fc2d21bfe17842e75654ea857dd7f`  
		Last Modified: Tue, 17 Mar 2026 02:45:20 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592030dd94b9d8b6ce5928e02596c8b0ace8c4bdd33ec1f299f285c0ec5f7903`  
		Last Modified: Tue, 17 Mar 2026 09:21:59 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2fb2129a0211be305fb2260607e7eba6be4215ec2214111ec617c613829e268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2505063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62bebb46dca67fd349fddabbdcf603843e426444681d5cf13def0a0b3b14eaf`

```dockerfile
```

-	Layers:
	-	`sha256:875596bf41a34868bdd41f97f9846646bc8715920d720842027a98b9ef8291e0`  
		Last Modified: Tue, 17 Mar 2026 09:21:58 GMT  
		Size: 2.5 MB (2488799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61e3732be0a67d27e61eb93745484532e47d6b641e85f69822a5ae2290921245`  
		Last Modified: Tue, 17 Mar 2026 09:21:58 GMT  
		Size: 16.3 KB (16264 bytes)  
		MIME: application/vnd.in-toto+json
