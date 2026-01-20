## `rabbitmq:management`

```console
$ docker pull rabbitmq@sha256:de1b5b16bc8d425ab8db9df9ccf74ebb78e83771dc2fd80398616ada4645c4ad
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
$ docker pull rabbitmq@sha256:f84316066d2acfaffe6c5bd58168e5d9664f46fac66ab1491cf9f7ca73a33e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117762718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2c960398c28e7fa8f164ca60eca5e926efe921db2a3c96420e7e5622579d6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 21:52:50 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Jan 2026 21:52:50 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Jan 2026 21:52:50 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Jan 2026 21:52:50 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Jan 2026 21:52:50 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:52:50 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:52:51 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 16 Jan 2026 21:52:51 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 16 Jan 2026 21:52:51 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 21:52:51 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 21:52:51 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:53:13 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 16 Jan 2026 21:53:14 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Jan 2026 21:53:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Jan 2026 21:53:14 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:53:14 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Jan 2026 21:53:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Jan 2026 21:53:14 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 16 Jan 2026 21:53:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Jan 2026 21:53:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Jan 2026 21:53:14 GMT
CMD ["rabbitmq-server"]
# Fri, 16 Jan 2026 22:10:50 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Fri, 16 Jan 2026 22:11:02 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-x86_64-unknown-linux-gnu'; digest='daec0f7b906ea9f79e672b2ef5368db08137df79a7c7d9f9b3c4f0f66acb453e' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-aarch64-unknown-linux-gnu'; digest='e0bdff91823be7f760c7b030c0c24802204eda7ad21a95b907ed36be8503cb76' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Fri, 16 Jan 2026 22:11:02 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b605fd694c0f9e1210db78973a942ba6cd044602c15f6aa9b7f3699b82ae2c29`  
		Last Modified: Fri, 16 Jan 2026 22:06:13 GMT  
		Size: 46.3 MB (46261530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cb76db81cbf242b56cccf18b061e5c5dd7827d612e8fb5a4475419b49a31a1`  
		Last Modified: Fri, 16 Jan 2026 21:53:37 GMT  
		Size: 9.0 MB (8994550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27ae1443e864d36b9fdf3140bef80a2be8c122422c854ed81d282a0d4b56d4c`  
		Last Modified: Fri, 16 Jan 2026 21:53:47 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f813129d9f1c0864ef0ec262a511e1c982daa0a5a0dfc47543886f411d2f327`  
		Last Modified: Fri, 16 Jan 2026 21:53:49 GMT  
		Size: 27.9 MB (27881766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7f643d70ad201f4fa1998e8a617c4d8dea77e5ff4a53031b2d1961690abf44`  
		Last Modified: Fri, 16 Jan 2026 21:53:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c457f28e544f0a3d6c769f4f7046b527a87749279ad17d1ffaaadf743faf4e23`  
		Last Modified: Fri, 16 Jan 2026 21:53:47 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e6f9d46769ec9f59708df6bf5a8c8433b3b385a8bd52b972f3136b12080428`  
		Last Modified: Fri, 16 Jan 2026 21:53:47 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2cb4101ff3969a1cbed4bb2de7d22cf9c6de37c039511f004c322054aa91e`  
		Last Modified: Fri, 16 Jan 2026 21:53:47 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded6a69a96ac73dd2711bec89fabaf27a425974d69a31325c47824fcde653c8e`  
		Last Modified: Fri, 16 Jan 2026 22:11:25 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35332e1fcae4c36c413c1ab203350201e4b576bd8747a6ff708fe444556ac7a3`  
		Last Modified: Fri, 16 Jan 2026 22:11:25 GMT  
		Size: 4.9 MB (4887171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8cea17077e9ca508dc5d5cc35ddc3f0f622e118b492efb60e44b45137e303f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7b902468df5f9d20ae218fd0012de649bbe0b7c055c83d008ea2bd0ab5d56`

```dockerfile
```

-	Layers:
	-	`sha256:37421075ec13261f45227cbdbfec96869ebf6cf9129f48e6800f50a6b0bc7a2a`  
		Last Modified: Sat, 17 Jan 2026 01:52:36 GMT  
		Size: 2.5 MB (2486661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0667a6e7424a7bd6e389a2db9c4cc17c5078aef712c4ed227398ec2924a958`  
		Last Modified: Fri, 16 Jan 2026 22:11:10 GMT  
		Size: 16.3 KB (16269 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:89a1b55300694ee88dceceb1379f3d0e9837fcde95fe7575026a39cb35aa4e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95251811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2b14474320a063da1e27bc312bfcf0e7f6134e4caadd28867e38bf4e3be3bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:59 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:02 GMT
ADD file:9e6534a5b837dcbcc4b9596878a4feeb07210fb34c7385aeee0217ff03c2460e in / 
# Tue, 13 Jan 2026 05:40:03 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 21:50:03 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Jan 2026 21:50:03 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Jan 2026 21:50:03 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Jan 2026 21:50:03 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Jan 2026 21:50:03 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:50:03 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:50:05 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 16 Jan 2026 21:50:05 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 16 Jan 2026 21:50:05 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 21:50:05 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 21:50:05 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:50:25 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 16 Jan 2026 21:50:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Jan 2026 21:50:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Jan 2026 21:50:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:50:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Jan 2026 21:50:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Jan 2026 21:50:26 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 16 Jan 2026 21:50:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Jan 2026 21:50:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:50:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:50:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Jan 2026 21:50:26 GMT
CMD ["rabbitmq-server"]
# Fri, 16 Jan 2026 22:12:21 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Fri, 16 Jan 2026 22:12:21 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-x86_64-unknown-linux-gnu'; digest='daec0f7b906ea9f79e672b2ef5368db08137df79a7c7d9f9b3c4f0f66acb453e' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-aarch64-unknown-linux-gnu'; digest='e0bdff91823be7f760c7b030c0c24802204eda7ad21a95b907ed36be8503cb76' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Fri, 16 Jan 2026 22:12:21 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:a56277e49d30e9a430d5cefad3038f88470a8681e48b806fff292791ed54f1fc`  
		Last Modified: Tue, 13 Jan 2026 10:01:35 GMT  
		Size: 26.9 MB (26853837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aacf64db9b7ea5837aa94fb2d54502cc4c160bec1798aa85a6c256c7796bf76`  
		Last Modified: Fri, 16 Jan 2026 21:51:01 GMT  
		Size: 33.3 MB (33295227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3a5aec936f0dd11fbbb4f72e83213a9c763bbec9c3325f2d53743407950ebe`  
		Last Modified: Fri, 16 Jan 2026 21:50:58 GMT  
		Size: 7.3 MB (7309046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d0d87ed085b8c97c580b18f9d5dce61c5096b78a564499674e265b5ac0fed5`  
		Last Modified: Fri, 16 Jan 2026 21:50:58 GMT  
		Size: 9.7 KB (9748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dc65bd5a1033c4ed45aaa712c408ca56815034c1fc8796f3cdd23a4c557dd6`  
		Last Modified: Fri, 16 Jan 2026 21:51:00 GMT  
		Size: 27.8 MB (27781901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17781a89be4ecd4d06d0c33b6d777241843d4f8d652790a76b749712e8384fd8`  
		Last Modified: Fri, 16 Jan 2026 21:51:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e6b4b1b5be823212d6f20f4ec87323cf532d8f8538832c963be13fcecb1680`  
		Last Modified: Fri, 16 Jan 2026 21:50:51 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e4d3b5ca23e8fff5a010b13590f5c35d65bea9080076c1a4d0274faa32abd8`  
		Last Modified: Fri, 16 Jan 2026 21:51:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ede9be6bfd1842ae35855b914d4d7966f3749e37180def8139b8101f240209`  
		Last Modified: Fri, 16 Jan 2026 21:50:57 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1350bbc426929d043acf54a3f2d4991dd9981eaf88679f98b01edd77f21c28e7`  
		Last Modified: Fri, 16 Jan 2026 22:12:29 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8797b2fd90175300fce6394406a79ef6192d559ee77d59ef8be20f463bd9d9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22b8b244bdce72ddae0def0cd8ab0aad6fe59b7f426fa66320e033d72326cab`

```dockerfile
```

-	Layers:
	-	`sha256:f6869b077bc1b56d836083a945443a934aae1dfaf3f6f609810dd1a5748b2e27`  
		Last Modified: Sat, 17 Jan 2026 01:52:41 GMT  
		Size: 2.5 MB (2487461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65eddf61d7d561b2c58aa59941bc45a2fd0828bafdb7d2843a61c09ac9b0fa7e`  
		Last Modified: Fri, 16 Jan 2026 22:12:28 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:4f75a627e61e547484524cb9ffbeb618cb1ad3f2b9255a59b392a4e69747482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115379007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d11163481ea795a6018e0c9d6ba1b5e66338296098ef3bf08800072ef23f0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 21:52:53 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 16 Jan 2026 21:52:53 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 16 Jan 2026 21:52:53 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 16 Jan 2026 21:52:53 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 16 Jan 2026 21:52:53 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:52:53 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:52:55 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 16 Jan 2026 21:52:55 GMT
ENV RABBITMQ_VERSION=4.2.2
# Fri, 16 Jan 2026 21:52:55 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 16 Jan 2026 21:52:55 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 16 Jan 2026 21:52:55 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:53:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 16 Jan 2026 21:53:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 16 Jan 2026 21:53:17 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 16 Jan 2026 21:53:17 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 16 Jan 2026 21:53:17 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 16 Jan 2026 21:53:17 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 16 Jan 2026 21:53:17 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Fri, 16 Jan 2026 21:53:17 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 16 Jan 2026 21:53:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 21:53:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:53:17 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 16 Jan 2026 21:53:17 GMT
CMD ["rabbitmq-server"]
# Fri, 16 Jan 2026 22:12:42 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Fri, 16 Jan 2026 22:12:55 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-x86_64-unknown-linux-gnu'; digest='daec0f7b906ea9f79e672b2ef5368db08137df79a7c7d9f9b3c4f0f66acb453e' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-aarch64-unknown-linux-gnu'; digest='e0bdff91823be7f760c7b030c0c24802204eda7ad21a95b907ed36be8503cb76' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Fri, 16 Jan 2026 22:12:55 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce6e27d23cbf736dd80f243d001e8704845c69b3038726cd32e31dbfb702b8a`  
		Last Modified: Fri, 16 Jan 2026 21:53:55 GMT  
		Size: 44.4 MB (44355386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5040603a13443393f0453a17d0719fe614fddfc0047224e4f6f1bdd3afe93d21`  
		Last Modified: Fri, 16 Jan 2026 21:53:52 GMT  
		Size: 9.7 MB (9716276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f1ccecc0e12310254732c8d4fa537a776f1c15b0e6429b3a2b8ee04dac33b0`  
		Last Modified: Fri, 16 Jan 2026 21:53:53 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3299982cb370d715feb25200458f13d250debd79bdcbe08a45565369c2dd490`  
		Last Modified: Fri, 16 Jan 2026 21:53:56 GMT  
		Size: 27.8 MB (27790880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d522e824b15441a466d400a91b82f361bd9c66b6d07cfb15ba3675a2e8c8e697`  
		Last Modified: Fri, 16 Jan 2026 21:53:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa15e2c65030e8e63344c44c7ea5a8484b4fc5f301d3604001c42d6a8e1acda`  
		Last Modified: Fri, 16 Jan 2026 21:53:50 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3149c5e10ec6ae4f976a53e0462a00c96ac60dff4829796b9e32dd1d1ee64968`  
		Last Modified: Fri, 16 Jan 2026 21:53:42 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3fe40ed3277c366f617b0f605fc21272d21d4172a9d235627882d8665e7c16`  
		Last Modified: Fri, 16 Jan 2026 21:53:50 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc4673deb0c31ce65e347a34bee0e0f3a1399f460ff73ca411c8d0b36608639`  
		Last Modified: Fri, 16 Jan 2026 22:13:18 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1732959aff28ebabb468991dabc98b86f57181dbba81bf9ba669b7d6568745ed`  
		Last Modified: Fri, 16 Jan 2026 22:13:18 GMT  
		Size: 4.6 MB (4640986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:adebec4e10cdf4dbedb5fe350560dbe508eaba692998431aee2d48437a33ad90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806b46e8c69d6576110be587b823a86daa9fa83c968e51a42f230eb9e66df5b6`

```dockerfile
```

-	Layers:
	-	`sha256:89d8c5ddfd09606646c1c76b3ccaf4deb414afd141b00473a5efdfe02d87b397`  
		Last Modified: Sat, 17 Jan 2026 01:52:46 GMT  
		Size: 2.5 MB (2487721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744fcf33d48d3b98f4727feb4cb409af98da99e7729ea5ce51b2fd01e3458bf6`  
		Last Modified: Sat, 17 Jan 2026 01:52:47 GMT  
		Size: 16.4 KB (16387 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:0365bfa50b2483a09a71d8c7203f5447013983d63163e526cda19a76cfb4b3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111267468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781e22c0e2c74984269a1bbf91b5eda8115038ef10a1ca73b799a9009a48bd29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:20:17 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Jan 2026 23:20:17 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Jan 2026 23:20:17 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Jan 2026 23:20:18 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Jan 2026 23:20:18 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:20:18 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Jan 2026 23:20:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 15 Jan 2026 23:20:20 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 15 Jan 2026 23:20:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Jan 2026 23:20:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Jan 2026 23:20:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:21:07 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 15 Jan 2026 23:21:10 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 15 Jan 2026 23:21:11 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 15 Jan 2026 23:21:11 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 15 Jan 2026 23:21:11 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 15 Jan 2026 23:21:11 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 23:21:11 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 15 Jan 2026 23:21:14 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 15 Jan 2026 23:21:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:21:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:21:15 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 15 Jan 2026 23:21:15 GMT
CMD ["rabbitmq-server"]
# Fri, 16 Jan 2026 04:50:03 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Fri, 16 Jan 2026 22:28:59 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-x86_64-unknown-linux-gnu'; digest='daec0f7b906ea9f79e672b2ef5368db08137df79a7c7d9f9b3c4f0f66acb453e' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-aarch64-unknown-linux-gnu'; digest='e0bdff91823be7f760c7b030c0c24802204eda7ad21a95b907ed36be8503cb76' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Fri, 16 Jan 2026 22:28:59 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 07:12:18 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b66004f60715e2b64d2a5b9596535176d35315e17d9cc24e0564aba21e57fa`  
		Last Modified: Thu, 15 Jan 2026 23:22:31 GMT  
		Size: 39.5 MB (39509660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2122401978ab0aaf97b2cf0682999fd386bed109a43efad2f84c13ea3d4a26d`  
		Last Modified: Thu, 15 Jan 2026 23:22:15 GMT  
		Size: 9.6 MB (9598288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5557fd0a5fd75aa541e9086de6f73193fc426c57f71d521ba5e7bbfc7324160d`  
		Last Modified: Thu, 15 Jan 2026 23:22:25 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424f091962fc89adc3f09e98c95e507afeef8b42e1923283e71b3d5b98b1f22a`  
		Last Modified: Thu, 15 Jan 2026 23:22:28 GMT  
		Size: 27.8 MB (27841674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b502aedbb56038589b4e5d6c6dc6f3bf9484ebca1643ceed2f4d4a7ea1a0f943`  
		Last Modified: Thu, 15 Jan 2026 23:22:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40cf2f02dc835b207ed2873d8e16d7a761e9d06590134eaa7b02ccd5357c5aa`  
		Last Modified: Thu, 15 Jan 2026 23:22:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94a1f212d0ee1d1cdb4e2b2d5dafecca5d725cddb1750110458fb842ae56b9d`  
		Last Modified: Thu, 15 Jan 2026 23:22:16 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abd8a705decd3ffafde59dfb5fd4bfb4c50e86f9a7e1a80ec75d6456de521d4`  
		Last Modified: Thu, 15 Jan 2026 23:22:17 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fc5ba0857e0e6764e47029689deafc4decae47544e714ed2a302e9846ccd26`  
		Last Modified: Fri, 16 Jan 2026 04:50:41 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4de5d2528e71bfe2b0bec2931f0b773175701410060c9800f68553383703ce54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e814a40fa704086306d143f898d26d754d5612fab6499e27e5e4d60c81dcdef`

```dockerfile
```

-	Layers:
	-	`sha256:9e84a24df77cedcaa8a6e41b34cdf5d07fa810d24849088c2ce86b22f8bcfbe2`  
		Last Modified: Sat, 17 Jan 2026 01:52:51 GMT  
		Size: 2.5 MB (2491114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f69186c4815696638725d18e8743b6f9821f816efe26e457f41148a1886fc812`  
		Last Modified: Sat, 17 Jan 2026 01:52:52 GMT  
		Size: 16.3 KB (16310 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:e61bc4ab9998382a1cd0fd0ca4b58cb8146923156ed4093d3778b0579250d1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104737340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6c5ca56e760ec467b83faa4c2e6cae546ba2a3fef4ea0c6c175a28dc1469f0`
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
ENV RABBITMQ_VERSION=4.2.2
# Sat, 15 Nov 2025 14:46:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 15 Nov 2025 14:46:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 15 Nov 2025 14:46:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 15:38:33 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 16 Dec 2025 15:38:42 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 16 Dec 2025 15:38:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 16 Dec 2025 15:38:42 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 16 Dec 2025 15:38:42 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 16 Dec 2025 15:38:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 16 Dec 2025 15:38:42 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 16 Dec 2025 15:38:42 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 16 Dec 2025 15:38:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Dec 2025 15:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Dec 2025 15:38:42 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 16 Dec 2025 15:38:42 GMT
CMD ["rabbitmq-server"]
# Wed, 07 Jan 2026 18:56:35 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Wed, 07 Jan 2026 18:56:35 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-x86_64-unknown-linux-gnu'; digest='61a034ed8182edba945d83f82780592b8c520ea4df2fcbcf349fe9263d6c4ce2' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.21.0/rabbitmqadmin-2.21.0-aarch64-unknown-linux-gnu'; digest='ccbf3af417b50c48afb91136ea3acc9eaf7f01f26440dc0f9ed35f9c21c50733' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Wed, 07 Jan 2026 18:56:35 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:4f36e1b0a2cc427e5979b49608ef4e52795313f083fdc941cab616d5ab2b861b`  
		Last Modified: Wed, 14 Jan 2026 11:08:38 GMT  
		Size: 31.0 MB (30952148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606650a61dbbc93efe83db6c01f31098ae14abd4834968121b22948aa3594218`  
		Last Modified: Thu, 15 Jan 2026 04:37:07 GMT  
		Size: 35.1 MB (35148108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894681447bb26bf478bea3393756ebd369dbe3c51970e4acdedc0b1d8f9876e8`  
		Last Modified: Thu, 15 Jan 2026 04:37:06 GMT  
		Size: 10.8 MB (10831054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ace5028ea6ad662e89ea950028a3569eea4433bdf62c87e8ce84d58b6133cc`  
		Last Modified: Thu, 15 Jan 2026 04:37:06 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39f1f7b51f95a401c17ad073b382632b7622fbbc042b29953789e490b7bab9c`  
		Last Modified: Tue, 16 Dec 2025 16:46:59 GMT  
		Size: 27.8 MB (27794303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404b01652dc3d5431a26713b2067eb4215b58cec916b4c5c19beaf296a645e2`  
		Last Modified: Tue, 16 Dec 2025 16:46:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ff99d44501fb6989085f815f7e2482f1d2cbaacf3946630ea286001d8dae9d`  
		Last Modified: Tue, 16 Dec 2025 16:46:41 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb12767cbfa8d91e9bc2beb04faf773ece51bcae49b7b5e66399ba3c10617f97`  
		Last Modified: Tue, 16 Dec 2025 16:46:56 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d05f415a3b881e94f564d76a570281f7a218065fefbc515379dfa567b7846f`  
		Last Modified: Tue, 16 Dec 2025 16:46:56 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92283e4edb85964240467806f3c0f873a1dea0375f4b819b146b2680a89c4824`  
		Last Modified: Wed, 07 Jan 2026 18:57:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:235ef040b30ad151e178cb41f3ae29f854a9a1666007d53313060b8179385a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c17c23f9b60884e876f6cf1c5a9d525c665a5aa5b516a83134cc1e03b06e4e`

```dockerfile
```

-	Layers:
	-	`sha256:eeb64348844f3dbd1422a10c0f279a52069eed70be5075f3332eeeea13e51464`  
		Last Modified: Wed, 07 Jan 2026 19:55:27 GMT  
		Size: 2.5 MB (2479028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9f0a8b37dd0aa533d2cdba053dfeb35fc63db6bbcaccf918e903a688526426`  
		Last Modified: Wed, 07 Jan 2026 19:55:28 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:2b233b7162f76107c2d1a66999614081cb81bfe51e08365b117d835a5adf5fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104990511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b830b50277487cc8f21eb4bccfee1a91bf0cce97a9a5806e0ecba09392b02a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:25:39 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 15 Jan 2026 22:25:39 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 15 Jan 2026 22:25:39 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 15 Jan 2026 22:25:39 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 15 Jan 2026 22:25:39 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:25:39 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 15 Jan 2026 22:25:41 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 15 Jan 2026 22:25:41 GMT
ENV RABBITMQ_VERSION=4.2.2
# Thu, 15 Jan 2026 22:25:41 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 15 Jan 2026 22:25:41 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 15 Jan 2026 22:25:41 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:25:56 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 15 Jan 2026 22:25:57 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 15 Jan 2026 22:25:57 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 15 Jan 2026 22:25:57 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 15 Jan 2026 22:25:57 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 15 Jan 2026 22:25:57 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:25:57 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Thu, 15 Jan 2026 22:25:57 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 15 Jan 2026 22:25:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:25:57 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 15 Jan 2026 22:25:57 GMT
CMD ["rabbitmq-server"]
# Fri, 16 Jan 2026 22:10:05 GMT
RUN set -eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/20-management_agent.disable_metrics_collector.conf # buildkit
# Fri, 16 Jan 2026 22:10:05 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-x86_64-unknown-linux-gnu'; digest='daec0f7b906ea9f79e672b2ef5368db08137df79a7c7d9f9b3c4f0f66acb453e' ;; 		'arm64') url='https://github.com/rabbitmq/rabbitmqadmin-ng/releases/download/v2.22.0/rabbitmqadmin-2.22.0-aarch64-unknown-linux-gnu'; digest='e0bdff91823be7f760c7b030c0c24802204eda7ad21a95b907ed36be8503cb76' ;; 		*) echo "[INFO] rabbitmqadmin is not available on $arch (yet?)"; exit 0 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 		wget -O /usr/local/bin/rabbitmqadmin "$url"; 	echo "$digest */usr/local/bin/rabbitmqadmin" | sha256sum --strict --check -; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		chmod +x /usr/local/bin/rabbitmqadmin; 	rabbitmqadmin --help # buildkit
# Fri, 16 Jan 2026 22:10:05 GMT
EXPOSE map[15671/tcp:{} 15672/tcp:{}]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 07:12:17 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec13ac7aea7104212abef800bfc438cd0de05f42a1dd9163fabc27207a2ff98`  
		Last Modified: Thu, 15 Jan 2026 22:26:45 GMT  
		Size: 38.6 MB (38581121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b13df2dbcf1da99013535f651cb22ff97843ad28ef7aeb91ac111d4d9045dd6`  
		Last Modified: Thu, 15 Jan 2026 22:26:35 GMT  
		Size: 8.6 MB (8623247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7b65a57f61456819bb64b22c0490766aa106c3f7602aceddb79d113e81f181`  
		Last Modified: Thu, 15 Jan 2026 22:26:35 GMT  
		Size: 9.8 KB (9815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9935e026448217f57397e0096ad82e98ef60321342ed487e39d683ba8488ee8`  
		Last Modified: Thu, 15 Jan 2026 22:26:45 GMT  
		Size: 27.9 MB (27865071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8823a503049316c4cc323a7238ff27bf2570f461e1ba1d32a70227eab4eabbe`  
		Last Modified: Thu, 15 Jan 2026 22:26:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d273b657e6a261846ec298dca38c6e378dd9c0858f2815120c5245f4ce4a440`  
		Last Modified: Thu, 15 Jan 2026 22:26:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ef1eb6eb184b9733da2a4e7eb37eb78ad54b4b73724c9a03455aa66f3c01c`  
		Last Modified: Thu, 15 Jan 2026 22:26:43 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896d37a5e749c014869b6fbe8b13803a913716da82a8fac6442d05425c2714fa`  
		Last Modified: Thu, 15 Jan 2026 22:26:43 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bb6b9693a2f6fada5cbcb54f69e90873fe5dacb4fa1586882dc8b8db96702e`  
		Last Modified: Fri, 16 Jan 2026 22:10:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:management` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:af4db1080db61ba5663028b7a6c0605fac1269fde90462840a44bddc540ac59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2505035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2adcc9b132a450b5516a906aeb3a42a3912757c9cc6cc8385e89439ece1d824`

```dockerfile
```

-	Layers:
	-	`sha256:c440c98db6e04b5f8fcd2279a7fa525fbb1c5e79c3aa8392b46b47bedfe6068b`  
		Last Modified: Sat, 17 Jan 2026 01:52:58 GMT  
		Size: 2.5 MB (2488771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0528439087d2b2b5d31be30b64924d6ce14bc26e38e660cf1e38edc4d459c058`  
		Last Modified: Fri, 16 Jan 2026 22:10:17 GMT  
		Size: 16.3 KB (16264 bytes)  
		MIME: application/vnd.in-toto+json
