## `rabbitmq:management`

```console
$ docker pull rabbitmq@sha256:1a92c703abc1bafd1683a500c230da5b5af00c96dacbe9d72ac2a839c3e1b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `rabbitmq:management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:d758d37175c41fbf0ae541f8c1afd97d483970780346355f89c900fa756d1f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115310828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4566dd9cd065927a4700fb206a9b6d1733435301dbbbb8031a6ffa43b16d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 07:12:34 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 02 Mar 2023 07:12:34 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 02 Mar 2023 07:12:35 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 02 Mar 2023 07:12:37 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 02 Mar 2023 07:12:37 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		ldconfig; 	sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 02 Mar 2023 07:12:37 GMT
ENV RABBITMQ_VERSION=3.11.10
# Thu, 02 Mar 2023 07:12:37 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 02 Mar 2023 07:12:37 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 02 Mar 2023 07:12:37 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 23:01:01 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 02 Mar 2023 23:01:02 GMT
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf # buildkit
# Thu, 02 Mar 2023 23:01:03 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 02 Mar 2023 23:01:03 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 02 Mar 2023 23:01:03 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 02 Mar 2023 23:01:03 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 02 Mar 2023 23:01:03 GMT
COPY 10-defaults.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 02 Mar 2023 23:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Mar 2023 23:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 23:01:03 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 02 Mar 2023 23:01:03 GMT
CMD ["rabbitmq-server"]
# Thu, 02 Mar 2023 23:01:19 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 02 Mar 2023 23:01:19 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d91e84cfcc9a9877b50f18e7d9d78b8ebef41354489b8dfe82dda186f6e3c9`  
		Last Modified: Thu, 02 Mar 2023 07:15:42 GMT  
		Size: 424.7 KB (424660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09f83bfdf7347d42050f5a402a1409396d052503b32a4f2058f93b5c2f62eae`  
		Last Modified: Thu, 02 Mar 2023 07:15:42 GMT  
		Size: 10.1 KB (10127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50ba1435db6125cd01ba5740e1899412c8dfa2f8ce8526ea32574742d3a0f41`  
		Last Modified: Thu, 02 Mar 2023 07:15:50 GMT  
		Size: 54.8 MB (54801437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b73a65d6673890e287d0eb722512f7ec23c912e0142fca62d5b6763800624b6`  
		Last Modified: Thu, 02 Mar 2023 07:15:42 GMT  
		Size: 10.9 KB (10882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328b9d3248edeb3ae6e7f9c347bcdb5632c122be218e6ecd89543cca9c8f1997`  
		Last Modified: Thu, 02 Mar 2023 23:03:34 GMT  
		Size: 21.6 MB (21582797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1158a8a532ef3556727faf939c7a9fc489b7be3c4cb969c5a053f3f28fefbd`  
		Last Modified: Thu, 02 Mar 2023 23:03:32 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7875cd2030eccad9ab153676b3987388a37fdb5f2b08ed812dd0c33068c5ae7`  
		Last Modified: Thu, 02 Mar 2023 23:03:32 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab8b1b533639dbdba25abb968a16719e3c2c8bf80b3bf887a3e6c429b3d4544`  
		Last Modified: Thu, 02 Mar 2023 23:03:32 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91a7fea1b48547afb7c4b3521428e993edcbc7d575f08a217392a0fbc12a5f8`  
		Last Modified: Thu, 02 Mar 2023 23:03:32 GMT  
		Size: 831.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cc50f4da3cbb7ad12fbcf199affe23c8ac926dc11c9245481384ad7d2ae2f5`  
		Last Modified: Thu, 02 Mar 2023 23:03:49 GMT  
		Size: 9.9 MB (9901211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:fb2ad3949bed9970b45b5736968dface57793ed2c3dc5b84b21b16cf95ba1461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99186915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a7e22fa524cabd845829fde6d2a4bd24462f58f5f653088620253fcb9875ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:16 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:18 GMT
ADD file:e066e7492699b78467000ed6a4a902a41599ea2d7aa291332c3f76729a1e798e in / 
# Wed, 01 Mar 2023 05:41:18 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 11:16:50 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 02 Mar 2023 11:16:50 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 02 Mar 2023 11:16:50 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 02 Mar 2023 11:16:52 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 02 Mar 2023 11:16:52 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		ldconfig; 	sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 02 Mar 2023 11:16:52 GMT
ENV RABBITMQ_VERSION=3.11.10
# Thu, 02 Mar 2023 11:16:52 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 02 Mar 2023 11:16:52 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 02 Mar 2023 11:16:52 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 22:57:03 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 02 Mar 2023 22:57:04 GMT
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf # buildkit
# Thu, 02 Mar 2023 22:57:04 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 02 Mar 2023 22:57:04 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 02 Mar 2023 22:57:04 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 02 Mar 2023 22:57:04 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 02 Mar 2023 22:57:04 GMT
COPY 10-defaults.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 02 Mar 2023 22:57:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Mar 2023 22:57:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 22:57:04 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 02 Mar 2023 22:57:04 GMT
CMD ["rabbitmq-server"]
# Thu, 02 Mar 2023 22:57:23 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 02 Mar 2023 22:57:23 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:f229fa8347dd45ed1a1495c295e3cef520b6fc0a5929756068638d7d3ef82193`  
		Last Modified: Thu, 02 Mar 2023 11:06:49 GMT  
		Size: 24.6 MB (24586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83641797cd8f98808f5afe0bc34b2ba046c20445ebbbaa171c63e52a62037097`  
		Last Modified: Thu, 02 Mar 2023 11:25:10 GMT  
		Size: 390.6 KB (390587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e57709d792a25d68f56a3dfc6fbd62762b53eeb87ae1c295e4cd7d0a60787d`  
		Last Modified: Thu, 02 Mar 2023 11:25:10 GMT  
		Size: 10.1 KB (10129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979cece76c781382ae70b38eb2fc5b0f3304953e30085ad696fa1599fd9e0375`  
		Last Modified: Thu, 02 Mar 2023 11:25:16 GMT  
		Size: 43.9 MB (43901346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3946c2935160ae80e1f893790f72d113fbd7dcb41b4b1c746d2426119352cca1`  
		Last Modified: Thu, 02 Mar 2023 11:25:10 GMT  
		Size: 10.8 KB (10840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66b71fbe7c1bb5e1747a9e4a8f4f4a8460e38f33873e776ff7f4f11e27b0ed9`  
		Last Modified: Thu, 02 Mar 2023 23:00:58 GMT  
		Size: 21.2 MB (21153538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45af269b93e4c10db3240f5ff421701cd633618e14abf3973b885b3a0efd25a8`  
		Last Modified: Thu, 02 Mar 2023 23:00:55 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f197ae93201ccfc79cdfc8b254f02903b0d6f3fd590f69c5dff638839942f4`  
		Last Modified: Thu, 02 Mar 2023 23:00:56 GMT  
		Size: 105.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f404220cb5482b58dcc4c2d3dfa85a9e292f1a0a7649d5f7117730d57554545`  
		Last Modified: Thu, 02 Mar 2023 23:00:55 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5280ffee3a373ee1a5e3d342c993eec30a7232d2ed0c96c365f02fb0c319d17a`  
		Last Modified: Thu, 02 Mar 2023 23:00:55 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6946536a96fca79fde74224be4f6a696d92eb37bfb9fb26b4edac1a4c02c3e0`  
		Last Modified: Thu, 02 Mar 2023 23:01:16 GMT  
		Size: 9.1 MB (9132316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:f1f79547736783302adbe3b7ed5478708d7471effa6f7ab691e78e7008b5289b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111903192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf773418aea9dda272421862b8042bfd34483574b14121725f3a730e4db40cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:51:11 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 02 Mar 2023 04:51:11 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 02 Mar 2023 04:51:11 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 02 Mar 2023 04:51:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 02 Mar 2023 04:51:13 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		ldconfig; 	sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 02 Mar 2023 04:51:13 GMT
ENV RABBITMQ_VERSION=3.11.10
# Thu, 02 Mar 2023 04:51:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 02 Mar 2023 04:51:13 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 02 Mar 2023 04:51:13 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 23:32:36 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 02 Mar 2023 23:32:37 GMT
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf # buildkit
# Thu, 02 Mar 2023 23:32:38 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 02 Mar 2023 23:32:38 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 02 Mar 2023 23:32:38 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 02 Mar 2023 23:32:38 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 02 Mar 2023 23:32:38 GMT
COPY 10-defaults.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 02 Mar 2023 23:32:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Mar 2023 23:32:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 23:32:38 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 02 Mar 2023 23:32:38 GMT
CMD ["rabbitmq-server"]
# Thu, 02 Mar 2023 23:32:55 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 02 Mar 2023 23:32:55 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321e172a600ea67bbc8d4fec1ab3faa9f8a0bc08635d6fc678f08c23ae3a73f3`  
		Last Modified: Thu, 02 Mar 2023 04:53:51 GMT  
		Size: 409.1 KB (409056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8329b21e376ab3939265d966108efa4c1d44cc9938f9d16cd068d553fc4b2a`  
		Last Modified: Thu, 02 Mar 2023 04:53:51 GMT  
		Size: 10.1 KB (10137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4396ba88f6f6db3e4f4b8994f3993b08b871965193a2a4975abb0709883199d8`  
		Last Modified: Thu, 02 Mar 2023 04:53:56 GMT  
		Size: 52.9 MB (52881241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6739a9b5c0f5a790cf55f98025b316fbf06da7c0ecfd4208e82bb973b69f2c26`  
		Last Modified: Thu, 02 Mar 2023 04:53:50 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9761cb124896944f89248bc928370649bae645492323870fefc14730edf3880`  
		Last Modified: Thu, 02 Mar 2023 23:34:57 GMT  
		Size: 21.4 MB (21398816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0372553c05af99c4931aeb0296454b5d40a229fe45783a1fe811b994c4720001`  
		Last Modified: Thu, 02 Mar 2023 23:34:55 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c4c632e96aeea6cd449c1668e5ea57811dca3d167e14d33faa2b7bcd4a4f9a`  
		Last Modified: Thu, 02 Mar 2023 23:34:55 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6d5ca85a2c6b6fe96fcfe8dcf12591b892c429031c8026b6843d2d9a272200`  
		Last Modified: Thu, 02 Mar 2023 23:34:55 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90b970bdea4e623ca8990550f285f1e343204322a18e425aee08b25f16a692f`  
		Last Modified: Thu, 02 Mar 2023 23:34:55 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907467d73e195d498ea46e9fd9b342ca478fb2e2a2cae04f268fa5193c0ab110`  
		Last Modified: Thu, 02 Mar 2023 23:35:12 GMT  
		Size: 10.0 MB (9996819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:d9915340d4cbbf30dbfc4dc64fb457f149068c3501201aefbd8e357a899460b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114154210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1604cec9749b1fba74a9e40dca6107bc9e9b42804c377eff3bbe39add168c6a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 05:04:24 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 02 Mar 2023 05:04:25 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 02 Mar 2023 05:04:27 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 02 Mar 2023 05:04:30 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 02 Mar 2023 05:04:30 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		ldconfig; 	sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 02 Mar 2023 05:04:30 GMT
ENV RABBITMQ_VERSION=3.11.10
# Thu, 02 Mar 2023 05:04:30 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 02 Mar 2023 05:04:30 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 02 Mar 2023 05:04:30 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 23:10:44 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 02 Mar 2023 23:10:49 GMT
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf # buildkit
# Thu, 02 Mar 2023 23:10:52 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 02 Mar 2023 23:10:52 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 02 Mar 2023 23:10:52 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 02 Mar 2023 23:10:52 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 02 Mar 2023 23:10:54 GMT
COPY 10-defaults.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 02 Mar 2023 23:10:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Mar 2023 23:10:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 23:10:56 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 02 Mar 2023 23:10:56 GMT
CMD ["rabbitmq-server"]
# Thu, 02 Mar 2023 23:11:47 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 02 Mar 2023 23:11:47 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235d66aa259063bf73bb8ed489cdcb4427f944c57e149d28a58780b271441c73`  
		Last Modified: Thu, 02 Mar 2023 05:11:09 GMT  
		Size: 451.0 KB (451042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327b940b879cdaedd8f22daeab3d1d66778e8034c98e5418ffd9c7c3c64148c6`  
		Last Modified: Thu, 02 Mar 2023 05:11:09 GMT  
		Size: 10.1 KB (10139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441fe28e82dab7207814b3ebfe5b9882e326e3f810e2c0634b7d16c86af8541c`  
		Last Modified: Thu, 02 Mar 2023 05:11:19 GMT  
		Size: 48.0 MB (47980467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564182920138a9171149c268a6b8dc96d7d6bd9197e74d8ac8b6f5147aacf1df`  
		Last Modified: Thu, 02 Mar 2023 05:11:09 GMT  
		Size: 10.8 KB (10803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fd145449d79dfafb2b86a61325e0fb57baff4474a44e3632e981c51d5a6ecc`  
		Last Modified: Thu, 02 Mar 2023 23:16:37 GMT  
		Size: 21.7 MB (21720926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0352be42bed8e9eebbaed4dbbc9acf83a51e1a6ad005aca4c83b29c68d95b7c`  
		Last Modified: Thu, 02 Mar 2023 23:16:33 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0916669e314fef5b371c5f7c112302e03553ca786d933a5e6708e63aa6a077d6`  
		Last Modified: Thu, 02 Mar 2023 23:16:33 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e584f176369bbd285bb125e5f3b962fdfb0bc8892e4046d2253029dbfaa80148`  
		Last Modified: Thu, 02 Mar 2023 23:16:33 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f4ef9927d88aef6687461607f3300498c6821d812dd39603248ee4c3609726`  
		Last Modified: Thu, 02 Mar 2023 23:16:33 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2242ffc9cc8a27b0224ba00791d4cad18ef4bd20ee3d1c0847dfdd629de69aaa`  
		Last Modified: Thu, 02 Mar 2023 23:16:58 GMT  
		Size: 10.7 MB (10678737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:d6eecbda9c3debc6dddf3c4dce700a60c065baa089b82aef479b497be3f2c592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103238255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1b4c0df92a17e1265432272d588a714433348cbb6bc658112bbb544cb33401`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 18:16:06 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 02 Mar 2023 18:16:07 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 02 Mar 2023 18:16:08 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 02 Mar 2023 18:16:10 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 02 Mar 2023 18:16:10 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		ldconfig; 	sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 02 Mar 2023 18:16:10 GMT
ENV RABBITMQ_VERSION=3.11.10
# Thu, 02 Mar 2023 18:16:10 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 02 Mar 2023 18:16:10 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 02 Mar 2023 18:16:10 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 23:14:22 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 02 Mar 2023 23:14:23 GMT
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf # buildkit
# Thu, 02 Mar 2023 23:14:23 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 02 Mar 2023 23:14:23 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 02 Mar 2023 23:14:23 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 02 Mar 2023 23:14:23 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 02 Mar 2023 23:14:23 GMT
COPY 10-defaults.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 02 Mar 2023 23:14:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Mar 2023 23:14:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 23:14:23 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 02 Mar 2023 23:14:23 GMT
CMD ["rabbitmq-server"]
# Thu, 02 Mar 2023 23:14:41 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version # buildkit
# Thu, 02 Mar 2023 23:14:41 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b3ad8923d90140ecab3885bd4bf659071fb8b8f677847d40e7ad3c423a663c`  
		Last Modified: Thu, 02 Mar 2023 18:20:10 GMT  
		Size: 425.8 KB (425778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4c65e5b1327c26a2acaad1cd86747db6daec7b8ad68b8024660d3ae195f652`  
		Last Modified: Thu, 02 Mar 2023 18:20:10 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619a5bcc32aa89705e0d773e12337897e91f748288813a03f49873af585ba074`  
		Last Modified: Thu, 02 Mar 2023 18:20:15 GMT  
		Size: 44.7 MB (44690910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3ac05f3c02c60afe84e851ff8654d8cbeffadc348507609de13aad94934253`  
		Last Modified: Thu, 02 Mar 2023 18:20:09 GMT  
		Size: 10.9 KB (10896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d8eab85f5b8166b36c96681474b1aefa8d65b6d9004904046af72862f1feba`  
		Last Modified: Thu, 02 Mar 2023 23:17:53 GMT  
		Size: 21.3 MB (21273870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd28327e7d96858f196d641286528a6b986318877f8b62ac82564153c069ea72`  
		Last Modified: Thu, 02 Mar 2023 23:17:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df94306f52f92c2d4f765185531e15e4a1cd4a0e4e6884fa9d35852b1291b17`  
		Last Modified: Thu, 02 Mar 2023 23:17:51 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ddfdd778397fdc05543fc24f3b47eb8f2d88086a6c2cdb690edbbb6e84483d`  
		Last Modified: Thu, 02 Mar 2023 23:17:51 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ee78a267e4dd1cbb09caf2fe31c38eaf06d7c5aa1b69f005ee401f580cfd13`  
		Last Modified: Thu, 02 Mar 2023 23:17:51 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb01f4c6678e204042d1afeb248277a3f0dceb0a68d8092e408417aad13ac48`  
		Last Modified: Thu, 02 Mar 2023 23:18:06 GMT  
		Size: 9.8 MB (9808561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
