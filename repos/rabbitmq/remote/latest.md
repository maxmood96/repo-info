## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:bb4e60e71e7dab9d9b6a4a680871047d21a501947dae59faffa089e61281cb7b
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
$ docker pull rabbitmq@sha256:87995b48ae9a6ee81f32398a3881c295f19303686e7a90832268056d467f2f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107252938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4093a263704995d3fed660f1c0350c80375ed1a5b9e51a767f2bce3c91d39c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f73d79d4de92263be08d3e094d6830c76f5260248afe0abb7a30d43ae6daeff`  
		Last Modified: Thu, 19 Dec 2024 21:37:26 GMT  
		Size: 48.4 MB (48397770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0246a10015b388fb964da0eded106db452088dcd292c2394c2648a669e41e2`  
		Last Modified: Thu, 19 Dec 2024 21:37:26 GMT  
		Size: 8.2 MB (8169293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c2200eb82ccc75c0d43122afc7a1528cc2c8211fa7ff089579236d4197dfcf`  
		Last Modified: Thu, 19 Dec 2024 21:37:26 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f071906ce3b479d069aefa43f58e6626104155e887f415894e768cc2ee8fe949`  
		Last Modified: Thu, 19 Dec 2024 21:37:26 GMT  
		Size: 20.9 MB (20922718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34563e7910a729f0ba1474c453a5ceeece0c169fb28a4cec16aa69bf918ada4`  
		Last Modified: Thu, 19 Dec 2024 21:37:26 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5461254c53b94cf5e9a7d78bc711584ecb67da0dcd46f2bb79f2133919eef507`  
		Last Modified: Thu, 19 Dec 2024 21:37:27 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042417f0b6e9e78d7d60ca28ee5eb655a6b99c25768c44a824c76d5154a916fc`  
		Last Modified: Thu, 19 Dec 2024 21:37:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410649ab8bd0fa85dbf788b9e74a4d6065a05b3fda07e9d9addbf3ce51672151`  
		Last Modified: Thu, 19 Dec 2024 21:37:27 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e22900e4ab036e9359175ca867690fae3edd5061ab430ef370e7bb7811ba6784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18194936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb99fe4b4d574ec70bf26d7e30ea87391bd000bd5e9e331e64e783feac1905e9`

```dockerfile
```

-	Layers:
	-	`sha256:664f0e8d5002775a51201fa99af43b2a54e77b138553711d50483875b6fa30e4`  
		Last Modified: Thu, 19 Dec 2024 21:37:26 GMT  
		Size: 2.4 MB (2364681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d63db754f159e76a0717d00b29d1c6065a4b7f583f6a6f849bfae0ea93cf9c1`  
		Last Modified: Thu, 19 Dec 2024 21:37:26 GMT  
		Size: 5.2 MB (5204082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64a8e0f3e57ebfef44e2d20abf11b5498db72a0eecc86db5c80b91bd18273b2f`  
		Last Modified: Thu, 19 Dec 2024 21:37:26 GMT  
		Size: 5.4 MB (5360622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a495671b3791387c8a97b5c8ca1338829c827f738a5f1c40175b73ee3084cf7`  
		Last Modified: Thu, 19 Dec 2024 21:37:26 GMT  
		Size: 5.2 MB (5205824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73597e9263846e38855d98c21c1132161ef3057a306257fdc1a6f9a48eb6b7af`  
		Last Modified: Thu, 19 Dec 2024 21:37:26 GMT  
		Size: 59.7 KB (59727 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:02b390ccd2b19affe3b3ff8b94f41584be8d33134fbbbf02e075f345aea7a5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89819855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b1efc980f8bdc31cdcb136bd130321fb0e1bc3d57e7ea6ea6f234eaf79f533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:50 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:53 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Tue, 19 Nov 2024 16:18:53 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddbe0fa0ca64bcd247be40bee928e934c0900148f9c757cb0e8d29f68579d49`  
		Last Modified: Wed, 29 Jan 2025 00:34:07 GMT  
		Size: 35.4 MB (35445401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a564914538c5bc366150ddf7111a42ebd75e9f9d96245d825e5c6fb93bbe47`  
		Last Modified: Wed, 29 Jan 2025 00:34:06 GMT  
		Size: 6.7 MB (6668105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d131e21e20cd8eca791b4d665fe37142b67723f37fb3ca13794d5061b0fbd772`  
		Last Modified: Wed, 29 Jan 2025 00:34:06 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258de73350d024bc2b39ae8a393c21cd6d7600a68d1d763db77ea49b5d599670`  
		Last Modified: Wed, 29 Jan 2025 00:40:15 GMT  
		Size: 20.8 MB (20825439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd637b134fa4730f6ce8481e138a3c14ca4f05f246914b2776fd477a007910b7`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcc398e4d560a6ecf9ca416d3851979f0bea8ba12b745ec7a3253323beb6efb`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e7c0bd91f2aa75079134abeae4a083cb5493352d2f38f86a6e4a8ae5e02ebd`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9423f0e5ba2568439a898c9678b6def69b948887eed29b3b57b34685afb120e`  
		Last Modified: Wed, 29 Jan 2025 00:40:15 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6c59b486ef826497438c525e66cc5b2233830cc602ba7e79969fad5d287e3eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17657664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3448460299638d79fb0f5d4a82853c7387b5ae83736c1c5f3de131658a9686d`

```dockerfile
```

-	Layers:
	-	`sha256:a18b16f4c8a9d3b3cf7ba54197cd1edc9a34efde15c457d4e8c31e8467ab601b`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 2.4 MB (2365507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446c7ec6f0e3a618c2208cd6170ac7e82f666b19950328dbcd2a65185e573dfb`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 5.0 MB (5025395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d921fad037a7c717662d076b38e2cee835b744eb7ff3216c9663d21e971d6baf`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 5.2 MB (5179690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0aa6fee9407b4f2d1eae95c3ba8582d3b981016ef466d664ba05087d30e76e`  
		Last Modified: Wed, 29 Jan 2025 00:40:14 GMT  
		Size: 5.0 MB (5027137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c05019b8803aa35c09b84b1a9b1541c97d05e1d20653672ff44515aed85577`  
		Last Modified: Wed, 29 Jan 2025 00:40:15 GMT  
		Size: 59.9 KB (59935 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:46be2c2715ea415550db3278ec0c07685376e10a4e8f140747ad3a5bbd9822fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105164474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675f67710353445fd483701431ca62e52b87e255326cadeb2dc2a283bc551402`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52299e8730d11af6eb71f33b5c16790dae4bb4959ed39906fc96caca2c82e821`  
		Last Modified: Wed, 29 Jan 2025 00:46:47 GMT  
		Size: 46.5 MB (46493171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfe2da4ebaba3053af2ca724275efde70b702f3b62906aba3a2c688da09b33b`  
		Last Modified: Wed, 29 Jan 2025 00:46:46 GMT  
		Size: 8.9 MB (8934957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905d928b7e4fd4f2d74836057463713dfb2fce6b1efd79e739f9fd039604882d`  
		Last Modified: Wed, 29 Jan 2025 00:46:45 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aba1b68919f476c74a7d8ad55c183c400dfe5a6fc94cd76d399ee3a8523fa8`  
		Last Modified: Wed, 29 Jan 2025 00:55:02 GMT  
		Size: 20.8 MB (20832468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa93f18d41f04fbbdff3047160e6948cfedb7c93d79efb336f7b2a0f84d1d5b2`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264553379a3a76a701874b9a3231cb63a56a4e0ea2f8cacf0655edd979f04c79`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835f34527f4da6765945ef2c4e2b06fedf08622089ed3c2fbe767d2e1b0abc72`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df14d10b2d576101d93c7f96027ab614362557e3e0c61ac1b220b71fdeb96af2`  
		Last Modified: Wed, 29 Jan 2025 00:55:02 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2b7905f27dc1c363e2376ab26439ca41567cb6bf76ed311fd52b0caa276bf909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18255527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aecd608c0ea7d0eb72e38f1017e62bd588172294d8092dc55d81d60b1b5699d5`

```dockerfile
```

-	Layers:
	-	`sha256:fdeb79a53d0dd76c61ec76368e8df3a1e9c98b0e953ba6e5347fd855d9127463`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 2.4 MB (2365763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e10b7302c3fbc7af2be59aa77fb721f056a763c784386d4863a869191bf5ed62`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 5.2 MB (5223727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16045ef83d48c3c4f2d7057d6b3481e8dc13e6e7408a3122161e484aa6543ea8`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 5.4 MB (5380587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48b5ec1d8f2c1544862fe3339a9d34414c7936751f932865e680049f06b4cf31`  
		Last Modified: Wed, 29 Jan 2025 00:55:01 GMT  
		Size: 5.2 MB (5225469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee90d1a2022b026166ff0086ed9ee0e32bd036e290c8a6f195589420f7df145`  
		Last Modified: Wed, 29 Jan 2025 00:55:02 GMT  
		Size: 60.0 KB (59981 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:de4de2b2a04469564ba519a1601c7eb4381a62fb4fecbe5216b73c2ad20b9ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105603936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f499bfc473347ddd60b8fc0d9a9f8e8cf5727819036d59ece88ab9decce323a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35aaa542f56f99732fa6a5ce5ca4b3980f55c461636cc332d4792017c9f15431`  
		Last Modified: Wed, 11 Dec 2024 22:38:19 GMT  
		Size: 41.6 MB (41633236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e85aabb1a869502abef25c5e467f417a1d8aeca7a26ed9ade9d7d914d39d0`  
		Last Modified: Wed, 11 Dec 2024 22:38:18 GMT  
		Size: 8.7 MB (8689219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4feb9952ffad20211d81b56be0c2dfe81e14bbc20c685d956302a993a2036a8e`  
		Last Modified: Wed, 11 Dec 2024 22:38:17 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d8c0db02760df7e7427352e3769f4acec7213799ac17d7979849196c912681`  
		Last Modified: Thu, 19 Dec 2024 23:00:53 GMT  
		Size: 20.9 MB (20881471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18e4b681be35f870af16521790af278cc37bbe4c9f9425994d68efd85a8f6cb`  
		Last Modified: Thu, 19 Dec 2024 23:00:52 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c0b8102ce18af9182874d5332d4b1fb25aa6297df8a9512aceae383f84eb83`  
		Last Modified: Thu, 19 Dec 2024 23:00:52 GMT  
		Size: 106.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b972d35869fefd573ab645af244d7120e0f8db1bc870beb7e40c8fb96a3e83e7`  
		Last Modified: Thu, 19 Dec 2024 23:00:52 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682e8d0d901ad67960cb815110986cdcaf16f6bd2bfc60b4cb568fe4f072a08c`  
		Last Modified: Thu, 19 Dec 2024 23:00:53 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:389b2a19c1326df83c8c4551fcb672caf41a3fb5ebead48893d340c660e0a268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18111517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e036b5772d87122a767c59ced70a2b9da0fac43ff3f1b8a442ac1dbba592323`

```dockerfile
```

-	Layers:
	-	`sha256:1370ca4b5f4a5433e86fcbc27e0bd84df7c944b648282b58910d0b3a78c579c3`  
		Last Modified: Thu, 19 Dec 2024 23:00:52 GMT  
		Size: 2.4 MB (2369036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f9c1a35d9165c34c49832110915d8c5f999a3249e00782cb69d40334c20bfc`  
		Last Modified: Thu, 19 Dec 2024 23:00:52 GMT  
		Size: 5.2 MB (5174793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a7d197d973307488c81e1d908fb38fdb83f7377ea964e015c39e1021d7e32d`  
		Last Modified: Thu, 19 Dec 2024 23:00:52 GMT  
		Size: 5.3 MB (5331363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d40f3e2a7cc31db9cc577fecf52889b836a27c549f604e3f24e30e59831299`  
		Last Modified: Thu, 19 Dec 2024 23:00:52 GMT  
		Size: 5.2 MB (5176535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b0b594d271cb6bfc6b27e4f5e7a2b8e8c8ee8c3a67f541ef3bcb54ed67e3ee2`  
		Last Modified: Thu, 19 Dec 2024 23:00:53 GMT  
		Size: 59.8 KB (59790 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:34b9bdfd8cfec232eea3731a95440dba94e5d990d64a3f81a963d5822584d631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98891082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff85d501ee59d0d4ba5d115b0a450183e92fd555d15a0626acff262e9be592b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:33:48 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:33:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:33:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:33:49 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:34:25 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Tue, 19 Nov 2024 16:34:27 GMT
CMD ["/bin/bash"]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 16 Dec 2024 06:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_VERSION=4.0.5
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 16 Dec 2024 06:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 06:05:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 16 Dec 2024 06:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 16 Dec 2024 06:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 16 Dec 2024 06:05:26 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 06:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Dec 2024 06:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 16 Dec 2024 06:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fed26cd19175c1e49674a896fa0e40e2a6cde8a62490a87d18503bad9af8b27`  
		Last Modified: Thu, 12 Dec 2024 00:03:32 GMT  
		Size: 37.3 MB (37281928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f4f308364cbd96a45afc7705a79e92182bd81c84a010c5d5c46a55ce56cdf8`  
		Last Modified: Thu, 12 Dec 2024 00:03:27 GMT  
		Size: 9.8 MB (9783482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439dbee123c9e270fb2ada75c33aea9a0e8a826582867b63f144367c3f10227b`  
		Last Modified: Thu, 12 Dec 2024 00:03:25 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa331686d65c78de6fb8ce0cdec237d217de57f571eb842bf70e8b52eb35ba3b`  
		Last Modified: Thu, 19 Dec 2024 23:02:52 GMT  
		Size: 20.8 MB (20833581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c79f500c923d4260e9200a4b4d827085373c8a1156e850c38444ffef98f318`  
		Last Modified: Thu, 19 Dec 2024 23:02:49 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a09a57d730cd88d3b765f653578dcbbe29128ea57d4e23cc1fde2c835dded1`  
		Last Modified: Thu, 19 Dec 2024 23:02:49 GMT  
		Size: 105.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ddf57d756586dffa50a4d9f56d535455893d352e7ccbc5b4d8aecd88e7618`  
		Last Modified: Thu, 19 Dec 2024 23:02:49 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f588e9aca5019a2fe84be9bbc09fa92b26e3d24946eec317b267a85c2e9925`  
		Last Modified: Thu, 19 Dec 2024 23:02:50 GMT  
		Size: 836.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:936b5cc9469fa7b36b029f84c0b3b0e13c2cbd7a5ea2cf0836e50fb8d5fd799c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18071858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd7187e3d3caff9119ae5eaae511bdb0783d8e869866b8222338047a317246d`

```dockerfile
```

-	Layers:
	-	`sha256:4cd585f3979628a43709db6ace26ffd4637730a4c6df2989ad97c8156487f773`  
		Last Modified: Thu, 19 Dec 2024 23:02:49 GMT  
		Size: 2.4 MB (2357250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98c140b89215e6c6eff5e33f7dc13a8f2fec30380cc4c168f2d05533eaf4dca3`  
		Last Modified: Thu, 19 Dec 2024 23:02:50 GMT  
		Size: 5.2 MB (5166360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa5a9b70343323674ec73cc704e1cab1c3256b3bd5f2b320a6a266f19d78e10b`  
		Last Modified: Thu, 19 Dec 2024 23:02:50 GMT  
		Size: 5.3 MB (5320359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50a727a52edabe0bbe1458008a750396a2f98f3236760798db490d5554c277cd`  
		Last Modified: Thu, 19 Dec 2024 23:02:50 GMT  
		Size: 5.2 MB (5168102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d1290395a1ff48b77236a90c4060a12bbf76f79528d979ddb38a8f29906baed`  
		Last Modified: Thu, 19 Dec 2024 23:02:50 GMT  
		Size: 59.8 KB (59787 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:803d546d4b0d6bf0e98c54c7b37d64215ec990f69defcb5360b9bcbc28788c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99211250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba49da1c1788d95e6f1e892acf0101096e0d37fee52f2f63b8c846bf3e7d611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:14 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:16 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Tue, 19 Nov 2024 16:18:16 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 28 Jan 2025 21:27:16 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_VERSION=4.0.5
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 28 Jan 2025 21:27:16 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 21:27:16 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 28 Jan 2025 21:27:16 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 28 Jan 2025 21:27:16 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 28 Jan 2025 21:27:16 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 21:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 21:27:16 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 28 Jan 2025 21:27:16 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965e29136c0040e37abbc80a6accd48640ce74eb7aeda66ce0aa16698c5c0cd8`  
		Last Modified: Wed, 29 Jan 2025 00:50:24 GMT  
		Size: 40.7 MB (40729114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13f00b9fcaef34a53fe78c034076f777ddcb89aa23fc24922cc58a8c87fa107`  
		Last Modified: Wed, 29 Jan 2025 00:50:23 GMT  
		Size: 7.5 MB (7546466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e68b5fa2a4586323b16f1cae2f3664d3c85773ea6450673bc81d2d406ced6b`  
		Last Modified: Wed, 29 Jan 2025 00:50:23 GMT  
		Size: 9.6 KB (9599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457003a14ccc5aa75e3b453b94bddb97ad4183ce291732ed864985dcda0e2c75`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 20.9 MB (20903492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f362644e0dbafb92e06907290b574a88ba542bf1c5562fd4f65ffa03b151c14b`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6e270ae5cceda2c7a574e6f0e52d9a7d61dd5cfd131a7195af0c4fa8cd2814`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc2b19646336d401b4a3d081627ea905f312682605ea652e1702c12a90bbc72`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1e513c9481efcef38d62171303f14904cde1561459c51d3205ca024b9d3291`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:48d5b5e7b5585483a0d18fd87796c70cf45f4f8b7d7ab3b662d9127bcec42051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17741962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa202eef118d0bf11b949d4488468c47ed563a50fed674510ba9e4ac49137f2b`

```dockerfile
```

-	Layers:
	-	`sha256:5110b033d5d3dd01e0b3873295d515afea420969a69e15ad62002d8dafe0304e`  
		Last Modified: Wed, 29 Jan 2025 01:01:46 GMT  
		Size: 2.4 MB (2366815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ddbd2d6f5b17f8287c2a215a7385cbb3599489baf6c9b1589ebdf9409a28e70`  
		Last Modified: Wed, 29 Jan 2025 01:01:46 GMT  
		Size: 5.1 MB (5052707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682c9774b6e8caaac16205dc71bba4447ded11200fdca7d22d108bc8ea4285d0`  
		Last Modified: Wed, 29 Jan 2025 01:01:46 GMT  
		Size: 5.2 MB (5208249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abaa6becb3ba11d319805a2db5bceb55c9aa9786e2810ecc2ce68cdddecacebb`  
		Last Modified: Wed, 29 Jan 2025 01:01:46 GMT  
		Size: 5.1 MB (5054449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b20b5ff80574525ce70fb4e9632b231f7fbb3bc8e7285a5fbf9efa1433304e6c`  
		Last Modified: Wed, 29 Jan 2025 01:01:47 GMT  
		Size: 59.7 KB (59742 bytes)  
		MIME: application/vnd.in-toto+json
