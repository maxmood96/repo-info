## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:9ccaa287bf8457b69b1bb0b138aa05c7313b369e966ab463df57d1d09822be7c
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
$ docker pull rabbitmq@sha256:b063d376aa39cd852d16d81477283468835a146be7faae5cc8309f7ff66c6127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112837290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1e628858900fbf4861cc07170ffe2408fd45bda517bd45a7ba8b75c5734373`
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
# Tue, 02 Dec 2025 01:21:19 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 01:21:19 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 01:21:19 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 01:21:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 01:21:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:21:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:21:20 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 01:21:20 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 01:21:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 01:21:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 01:21:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:21:40 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 01:21:41 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 01:21:41 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 01:21:41 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:21:41 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 01:21:41 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 01:21:41 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 01:21:41 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 01:21:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:21:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:21:41 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 01:21:41 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297c96417da90d50f7195cbe9c4ced29e6ee418bf6bf253a6aa3538244479d1d`  
		Last Modified: Tue, 02 Dec 2025 01:22:33 GMT  
		Size: 46.3 MB (46261495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c461b3cd1d0cde92687c8788e05f6d47aa079bfd46b16e4ef84ecfd9df6000`  
		Last Modified: Tue, 02 Dec 2025 01:22:30 GMT  
		Size: 9.0 MB (8994539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d529325e910b8d9cc361581b270d2ea184c0b26a82a80125e2f6514c7da9ec6`  
		Last Modified: Tue, 02 Dec 2025 01:22:28 GMT  
		Size: 9.7 KB (9686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20bfc22a4ab0e8db8a0d0e8a64493c409d74f680a83a7e1b566f833f278bb0`  
		Last Modified: Tue, 02 Dec 2025 01:22:32 GMT  
		Size: 27.8 MB (27845135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945e0aae58bcc3808cab1f54ff4d608ea724369a35e2fe525c94aa9bcb0fcefe`  
		Last Modified: Tue, 02 Dec 2025 01:22:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db132cf1165e381eb27193654202a7104350a39ebee1fb0225b947609dcf8ca`  
		Last Modified: Tue, 02 Dec 2025 01:22:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98667767aaf6d8db5d537363c15e47d56518d6cdec6fdb90d6739a81994fe90`  
		Last Modified: Tue, 02 Dec 2025 01:22:30 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b7bcfad26cdce70a32ad9fefef544cad65bd89067a24003f7590dff8bba0c`  
		Last Modified: Tue, 02 Dec 2025 01:22:29 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8997152efded0175b1bf2ea7861f53af2457a69b292f345b07addaa062338438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18841458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb408e43832e5a13ff12e947225b37631bce927758285118d9a0cadf83c7011`

```dockerfile
```

-	Layers:
	-	`sha256:0d1a9cec19676cd26288574b26ca575941c2f7c3595282825b95ca92284f753f`  
		Last Modified: Tue, 02 Dec 2025 04:54:31 GMT  
		Size: 2.5 MB (2487854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:536f38788e1dd00202f4efe56c52a42fbb69c463f6d7330f224504f2604bea9f`  
		Last Modified: Tue, 02 Dec 2025 04:54:32 GMT  
		Size: 5.4 MB (5378389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd9d6fcd8fdf6f72588104a5c92cb7dbb6c98d90b93326944cc280a9afff5984`  
		Last Modified: Tue, 02 Dec 2025 04:54:33 GMT  
		Size: 5.5 MB (5534998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6a91b9d9c85baa1428cf1733bb97dc1e3d1ea537da797680e04cea1c0db07d`  
		Last Modified: Tue, 02 Dec 2025 04:54:35 GMT  
		Size: 5.4 MB (5380131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25bdfa8c3b6c01ff2d4c70480c3712355d71a33b67a645de240781409cfd08f0`  
		Last Modified: Tue, 02 Dec 2025 04:54:35 GMT  
		Size: 60.1 KB (60086 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:2ffb017f9ae3469af70146669cd7f686441431008ad15549296e0979c91f7457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95214465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dd18bcdc64a52cef5eaa39f7c1083a663e1ede7b1031a99bb635bb2e2e1552`
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
# Tue, 02 Dec 2025 01:27:05 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 01:27:05 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 01:27:05 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 01:27:05 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 01:27:05 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:27:05 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:27:07 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 01:27:07 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 01:27:07 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 01:27:07 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 01:27:07 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:27:27 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 01:27:28 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 01:27:28 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 01:27:28 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 01:27:28 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 01:27:28 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 01:27:28 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 01:27:28 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 01:27:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:27:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:27:28 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 01:27:28 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6cdc0abf996c3192bfbda4018d34c282871d4be33fb369176002cb2199673adf`  
		Last Modified: Fri, 17 Oct 2025 08:06:35 GMT  
		Size: 26.9 MB (26852672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcbb09a93ae3d36610f50b0d55638ba7cd8d288f03e9f9fb07bc577a6b9202f`  
		Last Modified: Tue, 02 Dec 2025 01:28:16 GMT  
		Size: 33.3 MB (33294623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972413af07fee6d7ce719743984c40d3beea2e9eac546ce6e32e95a8f2e6c0b7`  
		Last Modified: Tue, 02 Dec 2025 01:28:13 GMT  
		Size: 7.3 MB (7309012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f9f1ff31f62672af050b316504f6cb18bc5142a1d2187bc26339a73c6d70c`  
		Last Modified: Tue, 02 Dec 2025 01:28:13 GMT  
		Size: 9.7 KB (9745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b424e2b1be04e61d88ab6efbed28a8a6e61da846608246eec78117f3e573daa6`  
		Last Modified: Tue, 02 Dec 2025 01:28:16 GMT  
		Size: 27.7 MB (27746665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05df82fba182ef125498b7db959ad897530cd6b10c1b9103b63729ccc95cd2`  
		Last Modified: Tue, 02 Dec 2025 01:28:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5e779ab2d3d2e4c6f0a2b341586bfd3da51a3fe56ed78866503d5832441dca`  
		Last Modified: Tue, 02 Dec 2025 01:28:13 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f6cb5b7c68f560d54efefcc1ec09cd022f174784cbda42afe89ba3f4cf8e2b`  
		Last Modified: Tue, 02 Dec 2025 01:28:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f3024ab6c39c58df2d436833c2c85445f7dc9e3395178021fc55883928aabc`  
		Last Modified: Tue, 02 Dec 2025 01:28:13 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e29cd1533edd918ea23068014f223592d0940cc7b0f764fba0ddcff2abceb204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18296238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ffdcdc4731db9480b978fcca89fde58f6f68982d8f1dd132ff7ef2c4aa88ca`

```dockerfile
```

-	Layers:
	-	`sha256:1a8479dc8caa2dc1442624d367e5dac98db53e119ea8ce8e8f8935232b2fac15`  
		Last Modified: Tue, 02 Dec 2025 04:54:43 GMT  
		Size: 2.5 MB (2488654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f45b21697017dd2da0c780843c3250be20bbebf0891a72a1b9c342f89eebf5dd`  
		Last Modified: Tue, 02 Dec 2025 04:54:45 GMT  
		Size: 5.2 MB (5197169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2377d278f78d239d3105318ddcbafdeef97296f4f35fb5af113b1709fc963f0b`  
		Last Modified: Tue, 02 Dec 2025 04:54:46 GMT  
		Size: 5.4 MB (5351223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f728f1c21ad0759d99711d409c186dca828a1649c5c118969668a35bccf59a8d`  
		Last Modified: Tue, 02 Dec 2025 04:54:48 GMT  
		Size: 5.2 MB (5198911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5cfef2a8826a10c03ec78fd4de8c6791f7f9a124ac4b25698a6c300b3059ea`  
		Last Modified: Tue, 02 Dec 2025 04:54:49 GMT  
		Size: 60.3 KB (60281 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:d52e74bb1575be8e4c14414fdb921bcbd26807f7f536702b213c0733678f1fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110699201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc89072ebda01417916226431954951e0143e254524b88327609152be379615a`
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
# Tue, 02 Dec 2025 02:37:43 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 02:37:43 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 02:37:43 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 02:37:43 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 02:37:43 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:37:43 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 02:37:44 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 02:37:44 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 02:37:44 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 02:37:44 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 02:37:44 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:38:08 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 02:38:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 02:38:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 02:38:09 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 02:38:09 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 02:38:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 02:38:09 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 02:38:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 02:38:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:38:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:38:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 02:38:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3afdb63c5614cb30959a5dcdbb2d8ccaa5bdbe716d2b07b0c9eae8304d0501d`  
		Last Modified: Tue, 02 Dec 2025 02:38:50 GMT  
		Size: 44.4 MB (44354990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8df9eebd7ff9da8ef0770fd7cd9b22eb896887f7266f40b3ec4aebc9a904ea`  
		Last Modified: Tue, 02 Dec 2025 02:38:44 GMT  
		Size: 9.7 MB (9716266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7a24377ed613718ed53ca963349737a3ba829196cb0178565d239ed16151e7`  
		Last Modified: Tue, 02 Dec 2025 02:38:42 GMT  
		Size: 9.6 KB (9631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d263a9a640dc44d265c7493973e826b0f9aa37444f9ca481045372b932163a86`  
		Last Modified: Tue, 02 Dec 2025 02:38:46 GMT  
		Size: 27.8 MB (27754608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a819fed2da63aa7b14e5cb80ffccbd3a83a02b5c333598d014cf38daae4b5c`  
		Last Modified: Tue, 02 Dec 2025 02:38:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6672119e073740d5c38e061fbcd0df2b2182a28531e3574518e00927a1f262`  
		Last Modified: Tue, 02 Dec 2025 02:38:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04114ef47a2ee62e03a7a947f456b98386327c295444cefc34c58f384afd0160`  
		Last Modified: Tue, 02 Dec 2025 02:38:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b271d0933f5decae8524e1f356b542f4e9c5a9634e5c77f03931287d21a5356e`  
		Last Modified: Tue, 02 Dec 2025 02:38:42 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:858fd4d6e55f889bf110781ace32f40fde934e09fa7ec0b3fe4c433d622a4805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18900438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b011046ea619ed8a49bdb764dbf25264e21a74f360a6fc16b27d04fb7c9dd060`

```dockerfile
```

-	Layers:
	-	`sha256:f64da7e0ed57f111f622a2dab8ad0ffa40bab2b479cd671d77e9a3b0c96b837f`  
		Last Modified: Tue, 02 Dec 2025 04:54:57 GMT  
		Size: 2.5 MB (2488914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1804dba6a688c9c89ac84acc99705a7bcad410c15879afb1cfbf998c75ad7913`  
		Last Modified: Tue, 02 Dec 2025 04:54:59 GMT  
		Size: 5.4 MB (5397610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d7d057c8aad1f77f25d2c68d78345e95c49a5a3980701731a9837f86068cfe`  
		Last Modified: Tue, 02 Dec 2025 04:55:00 GMT  
		Size: 5.6 MB (5554237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:351e8926a6228b416c64e370ca30157960ddd8f44b87896c4da546404b3cefa6`  
		Last Modified: Tue, 02 Dec 2025 04:55:02 GMT  
		Size: 5.4 MB (5399352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43662fab72eb0cc8d3091c0d8cf2cd46f291a97eef55b97a3638e2a648d224b2`  
		Last Modified: Tue, 02 Dec 2025 04:55:03 GMT  
		Size: 60.3 KB (60325 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:ca27f2f34a9911816418646941f06a6e21a07d291780f477e4950cb78267305e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111229721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a720c7bcd4f7513b7452acc80df59a9a456aae4e1ec1d856b700da618ce6e257`
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
# Tue, 02 Dec 2025 03:12:23 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 03:12:23 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 03:12:23 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 03:12:24 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 03:12:24 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 03:12:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 03:12:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 03:12:26 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 03:12:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 03:12:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 03:12:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 03:13:06 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 03:13:08 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 03:13:08 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 03:13:08 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 03:13:08 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 03:13:08 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 03:13:08 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 03:13:09 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 03:13:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 03:13:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 03:13:10 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 03:13:10 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea549b601bd9bbaa82330f9116fc3ceb9c4dba7e4c063bd565a810a615f4f96`  
		Last Modified: Tue, 02 Dec 2025 03:14:21 GMT  
		Size: 39.5 MB (39509735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f63d8706fa52525678f46287b8a6b2ac8dc7f755dc72edba93c29a36e16bbc7`  
		Last Modified: Tue, 02 Dec 2025 03:14:16 GMT  
		Size: 9.6 MB (9598278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4572881d52c81f77be9d663c9856c5ecb3a0250ea8c6f4fa2ac927bf2841f79`  
		Last Modified: Tue, 02 Dec 2025 03:14:16 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20bde7fdcd19692e5aee79aa87cdcb9d4b2ac1d12b9aa70b66665fd80ffb7a0`  
		Last Modified: Tue, 02 Dec 2025 03:14:18 GMT  
		Size: 27.8 MB (27805901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8063e8655c58127e320e5037ace9cde1b04e4bf5cd966f93ba4838f1ffc87673`  
		Last Modified: Tue, 02 Dec 2025 03:14:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61f545957012633f7eecc07269c725d428e0413447b6d83b67da13abcb962bf`  
		Last Modified: Tue, 02 Dec 2025 03:14:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef3a4ca803235ada228b878498bce8db3df0708508263941d7d35bc82e4448`  
		Last Modified: Tue, 02 Dec 2025 03:14:16 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c18afbe6bc95cf82491578703fdd071a330ec6c8c4397d183ff191726447a7`  
		Last Modified: Tue, 02 Dec 2025 03:14:16 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0afbbd87052561801036e2321f4cca30d94bf56f02d9771c9ad255b1583a168e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18755829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd1c3b3c729930b9be175570895c619f5106b092782f162fb00f618a4935596`

```dockerfile
```

-	Layers:
	-	`sha256:c8353552fc3fc25904e4608ab4fbff226394abbf89aab443f40ba74f1d1e08ed`  
		Last Modified: Tue, 02 Dec 2025 04:55:10 GMT  
		Size: 2.5 MB (2492307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64ada59339ff60713ef6de91cd0ba0602b2f9af28b34a89de95ca6c643fda66`  
		Last Modified: Tue, 02 Dec 2025 04:55:16 GMT  
		Size: 5.3 MB (5348331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d81079a5acebf669cff919586c4a1e420cbcabe46bbd2937f346eb498d974a58`  
		Last Modified: Tue, 02 Dec 2025 04:55:17 GMT  
		Size: 5.5 MB (5504970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:648e82895f6b022b079a805f512a75433077f739e000cef97cbb5d315dfde4bf`  
		Last Modified: Tue, 02 Dec 2025 04:55:20 GMT  
		Size: 5.4 MB (5350073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2a9debeb8d2997a368c1d2e9881156cbf180af6a291938743ec5479d41aed2`  
		Last Modified: Tue, 02 Dec 2025 04:55:20 GMT  
		Size: 60.1 KB (60148 bytes)  
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
$ docker pull rabbitmq@sha256:d1653ae438d96467e27ba1ae8d9b246b1d54e48c8b4f92b90899bbf9754fd0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104952373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069d3b1b8cb0649f0c9b637550561c983ebf1654c658d92bf4564a1c0e49818b`
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
# Tue, 02 Dec 2025 02:55:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 02 Dec 2025 02:55:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 02 Dec 2025 02:55:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 02 Dec 2025 02:55:27 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 02 Dec 2025 02:55:27 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:55:27 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 02 Dec 2025 02:55:31 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 02 Dec 2025 02:55:31 GMT
ENV RABBITMQ_VERSION=4.2.1
# Tue, 02 Dec 2025 02:55:31 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 02 Dec 2025 02:55:31 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 02 Dec 2025 02:55:31 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:56:39 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 02 Dec 2025 02:56:42 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 02 Dec 2025 02:56:42 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 02 Dec 2025 02:56:42 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 02 Dec 2025 02:56:42 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 02 Dec 2025 02:56:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 02:56:42 GMT
ENV RUNNING_UNDER_SYSTEMD=true
# Tue, 02 Dec 2025 02:56:43 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 02 Dec 2025 02:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:56:44 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 02 Dec 2025 02:56:44 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d2e3d12d22d90577285a238b422dc65ad975a458243adb4fb052caacbd304e`  
		Last Modified: Tue, 02 Dec 2025 02:58:11 GMT  
		Size: 38.6 MB (38581074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dab20848a4fa1330cd1eaa855f221b737f64780b20bdee11ba9146c43ddd173`  
		Last Modified: Tue, 02 Dec 2025 02:58:08 GMT  
		Size: 8.6 MB (8623266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46657e3856ac9150d16476348636b8c7d72106e19f984e34cc1de5d498703dad`  
		Last Modified: Tue, 02 Dec 2025 02:58:06 GMT  
		Size: 9.8 KB (9840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e28e47472202c104e392b63def6d03f8a5681a7166905c25077187c32763f4`  
		Last Modified: Tue, 02 Dec 2025 02:58:10 GMT  
		Size: 27.8 MB (27828838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d5210e1c37de29dfd6d5414fc81128136d66dcfa078b791854fd3d9dd6ef5f`  
		Last Modified: Tue, 02 Dec 2025 02:58:07 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ce6f2af9f813e2aab270aef04e76ce61b46fb5f8ef487f5211c97d503ee68d`  
		Last Modified: Tue, 02 Dec 2025 02:58:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4425f70c705284762ecfefaf0ab94d26d0226206ed9220f4966708479cf20e1`  
		Last Modified: Tue, 02 Dec 2025 02:58:07 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c339aadb0f2846088d566f1f724fa55ae16cead72d05f77454d3d8abafeb0130`  
		Last Modified: Tue, 02 Dec 2025 02:58:07 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ee224f427e0196f22660f9fb82f98186ae7a23169084e9564a88439b96a2e5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18381605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbb2f9c5c62596c5842bc556da363d07c1f50d0b08ede20c01eaf7b2c88d773`

```dockerfile
```

-	Layers:
	-	`sha256:b9ec516e60a5d31c52fdc544f5dfae003bd01ab17143f98fb81f727744017e34`  
		Last Modified: Tue, 02 Dec 2025 04:55:36 GMT  
		Size: 2.5 MB (2489964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b066c657812e3c3dd58df08be016e1a1f9c3276a0b5db1d29f21aa32be18b59`  
		Last Modified: Tue, 02 Dec 2025 04:55:37 GMT  
		Size: 5.2 MB (5224836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ffeceacff64b1b9d65ab6c648700fddd67fd1ceaef328753c40e5bca1f4ab52`  
		Last Modified: Tue, 02 Dec 2025 04:55:39 GMT  
		Size: 5.4 MB (5380141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b827cdf1a17652fcab03b51b4334f04935a149952c1b4f582322770243fa4131`  
		Last Modified: Tue, 02 Dec 2025 04:55:41 GMT  
		Size: 5.2 MB (5226578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d07647dfe9d54fe557c8e5c101a037c0b5749274cd697fa3f198272f9dc21711`  
		Last Modified: Tue, 02 Dec 2025 04:55:45 GMT  
		Size: 60.1 KB (60086 bytes)  
		MIME: application/vnd.in-toto+json
