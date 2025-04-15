## `rabbitmq:4-management`

```console
$ docker pull rabbitmq@sha256:c907d1c4b6449faf4bc168473eda35624e25265306b49ebe39e6c3a52be4423d
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
$ docker pull rabbitmq@sha256:8d684780806fec89cc99727a013feb6d181d63f941872d732209596e537bafd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117492408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b4d4395c6bdd2799dad5bf52317cd3c46286b1847e5d3a575984fcee6385a6`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
ENV RABBITMQ_VERSION=4.0.9
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21975ae9ac1dc254a649f593ad16e80d045305b2be9e195a8368edf91f69435`  
		Last Modified: Mon, 14 Apr 2025 23:06:16 GMT  
		Size: 46.2 MB (46237888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06a456387d6e6500ce45d376015b584da957ed18eef662a430ea7b239b18c16`  
		Last Modified: Mon, 14 Apr 2025 23:06:16 GMT  
		Size: 8.2 MB (8171076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380b616fd0aa7df5f9bb58c79f324a66d38b0220ae8f324e9bd2c60770acdc20`  
		Last Modified: Mon, 14 Apr 2025 23:06:16 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac5bc2e9c416d2c8b32dd7268092a6f5644a7895f559dcf4e7b07845d55cfb5`  
		Last Modified: Mon, 14 Apr 2025 23:06:17 GMT  
		Size: 20.9 MB (20891393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cf0213efd320c947f86fd3e4fd4e7dc48eaf2658cdcf553cc5423796b8e13a`  
		Last Modified: Mon, 14 Apr 2025 23:06:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2ba3e3a09bf3da356d65240804ead8a5fbfd454fde3370e4e9e09bab28b197`  
		Last Modified: Mon, 14 Apr 2025 23:06:17 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2640c31c5352fc38cd47f02ba400679aaecace617009aab3a4a5400e55d66645`  
		Last Modified: Mon, 14 Apr 2025 23:06:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8379c1e3ebd5a03bd543d02a4b239761db8ac1267f81922a2df3e105d79bc3e6`  
		Last Modified: Mon, 14 Apr 2025 23:06:18 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1357315dc372701d8889541280eb8ac3e597a4e033e151485073bb91c2c7b5f`  
		Last Modified: Tue, 15 Apr 2025 00:05:34 GMT  
		Size: 12.5 MB (12463163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4790a8585ef8e69ee0d553c7709eaa66adbc05a3104c36a7cf826ea7b73303fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfb2e06b20b536c0b92c3725173c2e78260faec7e12581d1d2de3dc8d1d703f`

```dockerfile
```

-	Layers:
	-	`sha256:3f8036bcb8a8a8a574766f1af2a51acbb6c8b6ec79af452845a8abf192e1700d`  
		Last Modified: Tue, 15 Apr 2025 00:05:34 GMT  
		Size: 2.9 MB (2947571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0414d7f9073e50c8750f5f566551664c661a5d4681f75c2187d0c51fd9f8fa15`  
		Last Modified: Tue, 15 Apr 2025 00:05:34 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:06bf145789b9c554ee7b968fa244d00bd46698ffd1612644824755945d4d09a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99068736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31572347522e95cbcca20e9ce9bb1208e770e1f0bf88c24fe284545a2cb6f812`
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
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
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
ENV RABBITMQ_VERSION=4.0.9
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
	-	`sha256:91b06012d8ec59c917dedd79d01361ad8412716a3fbbb8457c64d36b405009b4`  
		Last Modified: Mon, 14 Apr 2025 23:12:15 GMT  
		Size: 20.8 MB (20793677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb6a752d6ff039a0bee0612752fe91012f5306aa400da45c0688d58a9a630ec`  
		Last Modified: Mon, 14 Apr 2025 23:12:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649b2fd5d5b471a3de4b9e8cd8e3c016ef97f180ccd9b78e7b9c41ad06dd9298`  
		Last Modified: Mon, 14 Apr 2025 23:12:13 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda00de671d78e84d787ab2f1efd1e59ff606d11738345fe4d1d99db14188f38`  
		Last Modified: Mon, 14 Apr 2025 23:12:13 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06dff205afffd94e21b202f12123bc221d70cd3c60ed51c375cc5f320fe3070`  
		Last Modified: Mon, 14 Apr 2025 23:12:14 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782dbd21321d68058e1cdbbbbee7c71bee2880ac944760dc5b00b785038e2fe`  
		Last Modified: Tue, 15 Apr 2025 00:05:02 GMT  
		Size: 11.5 MB (11475585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:9474566f6d9203ec5afc02486770d64acba0f55906864ace91d47794b654f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba78fb88ee739291538530258d1952b4c45d90744c631ac04cb4b66714e88d08`

```dockerfile
```

-	Layers:
	-	`sha256:9303b923004fd09bab0f1601130c20ebec0c8fd835faacf7c0ff839b239cbe77`  
		Last Modified: Tue, 15 Apr 2025 00:05:01 GMT  
		Size: 2.9 MB (2948531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:497161b48d468c6a3614768abc661ba1cbe047dc866163b66718cd68858d5e58`  
		Last Modified: Tue, 15 Apr 2025 00:05:01 GMT  
		Size: 11.5 KB (11477 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:ffb11b588a3c4bc0049f86e2a78b626f123bcc03e3cef2d3b2d45c54d820670b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115263570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d72a8eb7d3f4f33aee00a2f21fab4b6914d83bbed2dd9d41ca1f625b20f78e6`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
ENV RABBITMQ_VERSION=4.0.9
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
	-	`sha256:72ce2bb81c9ac183f3f6a07dd16d478159959d0bc79e8c0e6ab03ebee765d599`  
		Last Modified: Mon, 14 Apr 2025 23:18:06 GMT  
		Size: 20.8 MB (20800076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecb3ce9ab19b9813bc6d79c448898ff024d86d6482d6eb9a57dfde3739f0293`  
		Last Modified: Mon, 14 Apr 2025 23:18:05 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727b24a0ed66da7d364fb9f99a723ea1c8f57ecdf6888eb4af1d3a9b1201d69`  
		Last Modified: Mon, 14 Apr 2025 23:18:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b48c97e3dd8a5ac41751227bdb7ca7651b3738bd35f13da0931c3a4aa3fa43`  
		Last Modified: Mon, 14 Apr 2025 23:18:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc9120e00c49e2372bc9dcb89d7a5132b8327d090bf7015ed9496d3bda90469`  
		Last Modified: Mon, 14 Apr 2025 23:18:06 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d49d91e89f3f1f916392dbfae65f09b7d153bf8299c8212d630c194ce0c993`  
		Last Modified: Tue, 15 Apr 2025 00:07:40 GMT  
		Size: 12.3 MB (12330280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4a3eae64c5784f2cf157f94e2e9696615ed9933a8bf1e1fdae6d48a8207715bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f29fe0a0a44c4aaadb607f6ef96bc526f9b35c48635132be2b07f7850dd5691`

```dockerfile
```

-	Layers:
	-	`sha256:7d4fa071542b6528420425a6e7cce5060099c1ba82b52f93c95f91d534208ade`  
		Last Modified: Tue, 15 Apr 2025 00:07:39 GMT  
		Size: 2.9 MB (2948683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2594740ea35b03a611f759b626dcc18da89292b5fce9a6912451f02128ec16f3`  
		Last Modified: Tue, 15 Apr 2025 00:07:38 GMT  
		Size: 11.5 KB (11504 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:c3b865f704ecc51e8432f6e8aa8f07a0a6a6c250da815fcb6ee5e82c52bb4000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116345618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061d29080a456aa6388bce0fba93d82cd4c4a30091ff750e8598e39b69e21f35`
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
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
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
ENV RABBITMQ_VERSION=4.0.9
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
	-	`sha256:614db0f2b1bdf5d9a64cda99e13206816d9ef31b19642acfe22938e4f15492bd`  
		Last Modified: Mon, 14 Apr 2025 23:16:54 GMT  
		Size: 20.8 MB (20849293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e7a3d5f1fdc3bc73841dc53f37d5c0b8336056bc8fe13887358c5ee3f6a146`  
		Last Modified: Mon, 14 Apr 2025 23:16:53 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46828df43b565443a869e478a8e0f5327ab5567705f43230e3dba52174b0504d`  
		Last Modified: Mon, 14 Apr 2025 23:16:53 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850ebd7ae3b5d99533931a5e12b7dd1ce7d2b8004140399ecdc58ebb5fa7a989`  
		Last Modified: Mon, 14 Apr 2025 23:16:53 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdccddb6475fa8247b4ccac077ecf5774d5db33eb062ec10278860dd394f858`  
		Last Modified: Mon, 14 Apr 2025 23:16:54 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d69b6f3d3980c1da221dd586f8364ac6b66608610b66b7d26eb1e2a8cbb7f`  
		Last Modified: Tue, 15 Apr 2025 00:05:50 GMT  
		Size: 13.0 MB (12963653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f785261fe03f642ad86682e248e550878a85e1de1679f5ed2ca0449a802c908e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2963645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb112fa66b106d455f2ff3ca4774064f311cebdb287dbd599185916878769ab`

```dockerfile
```

-	Layers:
	-	`sha256:f5264a7826be8505cbc380d53016b422ba46b2ff203c218eb80a11a058bf7484`  
		Last Modified: Tue, 15 Apr 2025 00:05:49 GMT  
		Size: 3.0 MB (2952200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c953ae80a79375d2550122bee0019ed04720753e130699402a29a03827c7180`  
		Last Modified: Tue, 15 Apr 2025 00:05:49 GMT  
		Size: 11.4 KB (11445 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:e869bb25914c33c1f5f0a4e0652aafe0c33502a617428c1486d387b5881a3813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109000027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647b161444179fd93e6f39f76b00f9384bed10d9726b8d43825d81f6ceae9eaf`
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
ADD file:ef7c97f5dd8d665aae899afe52c54f7acaf71fa51e9d7f26e13ed6073141c666 in / 
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
ENV RABBITMQ_VERSION=4.0.8
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
	-	`sha256:564d832896e4832fd832c03d9cf3be98c6bedff6b0873dcac5c6280d70b221f6`  
		Last Modified: Wed, 09 Apr 2025 07:25:08 GMT  
		Size: 20.8 MB (20801135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9b7854620cf30550a1a57bd9b2af1bd03a89c650ad2783fb402216673d25d6`  
		Last Modified: Wed, 09 Apr 2025 07:25:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d97a6b30ca6ff16a54fff33ece2128114b420d2b17cf347b6966b72133c99`  
		Last Modified: Wed, 09 Apr 2025 07:25:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992b501933ca4de8d2c6533c35989174e2281f535dddd3a4f125204b0e0332ce`  
		Last Modified: Wed, 09 Apr 2025 07:25:04 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b553f0589fc849647e3184eb599c6e9a61a4cd33194e82829c8d07bb4ebc088e`  
		Last Modified: Wed, 09 Apr 2025 07:25:05 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942ed29d0059d7ae6793f6e3a7e2bbdd5f873b409939f64d82e23607d3c1ab63`  
		Last Modified: Wed, 09 Apr 2025 09:39:25 GMT  
		Size: 12.3 MB (12326395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1c213daa46bcf84870be5ca477e907f764cd68fd8bef45db49341c403369f466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2951647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f56dc94e2503867771afbedf559eef3bc6482d7dd070a55d22999cb01fdebb9`

```dockerfile
```

-	Layers:
	-	`sha256:bec5d3167141eb8a55513ddec68a4c1f0b1bc73d4a811a90bc72091598829721`  
		Last Modified: Wed, 09 Apr 2025 09:39:23 GMT  
		Size: 2.9 MB (2940202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f96aa3dab63cac453f5b4bac4521c5f9c19dc842e04230e7e30f8473f87afa`  
		Last Modified: Wed, 09 Apr 2025 09:39:23 GMT  
		Size: 11.4 KB (11445 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:4-management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:fce87c4be1e4724a7cb7d3f33362bb0e4523a506d10539eaae8d2d44c875c83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109633688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc711ac01313361a40c906720cbec857d2ec05489236f252d196491110a614e`
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
ADD file:8f287f40ca940c9bd87c8706751f5f1c5bbd0a83fd75f7d938832b226fdb936d in / 
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
ENV RABBITMQ_VERSION=4.0.9
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
	-	`sha256:e81dcc8170ab7d2af2e0521d908b7d529ec32938c79372767e9cb2999b8cfcc6`  
		Last Modified: Mon, 14 Apr 2025 23:48:39 GMT  
		Size: 20.9 MB (20874040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6e332b97cfeb2bbb62ec06ff5c2758a86a4b6cabed9433695ab47153445476`  
		Last Modified: Mon, 14 Apr 2025 23:48:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58a6511b0fb48f73696db6ed6a49d4507984e2f00e80a31f7bee7cb2ca230a0`  
		Last Modified: Mon, 14 Apr 2025 23:48:37 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9753de4eea42b6da671c7f1ed9963c3d3834c8e32cdaffcac5f1f59a34d1d34c`  
		Last Modified: Mon, 14 Apr 2025 23:48:37 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ad6967365064ea0927b991f66711c18c8b7afae77bff03d1ddca6239c2e0d7`  
		Last Modified: Mon, 14 Apr 2025 23:48:38 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8103c76a7646443a2a58ec4d18bd8e9634c70e96ec2215866631947c2f3e2852`  
		Last Modified: Tue, 15 Apr 2025 00:05:45 GMT  
		Size: 12.7 MB (12678950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:4-management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3e52d467cf419310a5251e0377ed0dfeeb2cee9beba3f82f98548edbc9e7f2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2961032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2451ef46b5ef223a9943698eabe5fbd59363cf8303db42bf9e1424070b17f808`

```dockerfile
```

-	Layers:
	-	`sha256:8001d60c88c7b529fb9ed63a51453123e8b275b2c3bfed8ead988d78736887f9`  
		Last Modified: Tue, 15 Apr 2025 00:05:45 GMT  
		Size: 2.9 MB (2949631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d2116342cdb418194c56948bb5cf1cea78be88854f7c2f94720ff4d6935461`  
		Last Modified: Tue, 15 Apr 2025 00:05:44 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.in-toto+json
