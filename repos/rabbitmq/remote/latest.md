## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:a709c42b26d9303ec33994dceacfbfe11ee325dc6e16f70c7704a5f500c694be
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
$ docker pull rabbitmq@sha256:98b33c5f7a2d6220dbf76d09ee4ea1d69501774a39c420c463747a3ba0125a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104680114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a5e820097fb0deaebb8e561644c5690ac238fb9fc5ee93446bde75331ebdf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 26 Aug 2024 05:05:19 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Aug 2024 05:05:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 26 Aug 2024 05:05:19 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01f81de54074b0b4640234d5ade71ea9be048ef35cc4396eceb0115adca9d02`  
		Last Modified: Mon, 26 Aug 2024 23:02:25 GMT  
		Size: 46.0 MB (46016280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a58f223d10283223b765fa378d0488111c1ec00b1d1c970223ee5387d2ff79`  
		Last Modified: Mon, 26 Aug 2024 23:02:24 GMT  
		Size: 7.5 MB (7483837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa819df00ade3b9974f70b5190a7079ffe153dbe84dad8c11ee9ea1452e904a9`  
		Last Modified: Mon, 26 Aug 2024 23:02:24 GMT  
		Size: 10.7 KB (10749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e59daf96e17798237afe1b06386a339a9f0897a67df7bea2ff32f107ccbf1c`  
		Last Modified: Mon, 26 Aug 2024 23:02:24 GMT  
		Size: 21.6 MB (21631479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c504ac8adb337b92e22687bcd00b3dd4a7248ad45b2f0f63809ded6ae5460d1c`  
		Last Modified: Mon, 26 Aug 2024 23:02:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081e86dd22bfecdecc1bb682e157d80a1a526f2c8c1061c8f420937e3cd44022`  
		Last Modified: Mon, 26 Aug 2024 23:02:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb614a522a4f88edbf48cbaea120fe908051ea5affb422961e8d28e6dfa6fcac`  
		Last Modified: Mon, 26 Aug 2024 23:02:25 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff646133387d64052deb46ac3b9c3655d1abac4a8c42c6c8d9998c62bce7c17`  
		Last Modified: Mon, 26 Aug 2024 23:02:25 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:62c13900eb670097369c6cda99431b00e7d047be3e741ccf57e24e2872c2393f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18702952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306613f403721824132ff1642c6a154ca90ea30eb16ecbd4e78f48db31145bcb`

```dockerfile
```

-	Layers:
	-	`sha256:bd7dad1b8e649ad71259fd54453f586a9aa91c4590f4251e2e6c19998dc349c3`  
		Last Modified: Mon, 26 Aug 2024 23:02:24 GMT  
		Size: 2.9 MB (2919768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b31fb03ef3a7c7712e5403376a8eb0a18c44c4fa550f41c5d91cacf7436ec06`  
		Last Modified: Mon, 26 Aug 2024 23:02:24 GMT  
		Size: 5.2 MB (5192868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6ac444981ed30f49a41d4f03875dfc403a470c0a6785a2f335a13168b12c44`  
		Last Modified: Mon, 26 Aug 2024 23:02:24 GMT  
		Size: 5.3 MB (5332955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd52e4fc0d57848a3a02658ca9d7c264b26e9873e11c0260076a93c1b8f6fe38`  
		Last Modified: Mon, 26 Aug 2024 23:02:24 GMT  
		Size: 5.2 MB (5194390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07c40ba8d7dc3656a3d33eabba6b7b3a302d9c8eddefbdf690eb93d9b73d254`  
		Last Modified: Mon, 26 Aug 2024 23:02:25 GMT  
		Size: 63.0 KB (62971 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:d79fe7884e27f05761922502eb0f0852be3837db9518e5f0adae1bac05149c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87781938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f092a2145f8175747661be57a5fda99adc608a7c1a4fc2cde18538c1233c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:06 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:09 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 13 Aug 2024 09:28:09 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Sep 2024 23:00:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_VERSION=3.13.7
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Sep 2024 23:00:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 23:00:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Sep 2024 23:00:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f6fe61417ce419fef49e041c7a72ab306333edf1ac9f55a140962ba63026af8c`  
		Last Modified: Tue, 13 Aug 2024 10:45:02 GMT  
		Size: 26.6 MB (26639952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9f0c62e7f2b8e3fdd9d0655d551aba6705e009f6d47074ba0ab98dd7b45067`  
		Last Modified: Fri, 06 Sep 2024 22:20:16 GMT  
		Size: 33.5 MB (33505318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfb6b16f5445dbbfdefb97ee6205ec68219d418220a62255d292b67fefcb48e`  
		Last Modified: Fri, 06 Sep 2024 22:20:15 GMT  
		Size: 6.1 MB (6078166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb3ffe657953f192462141ceb8af57f514d3a1ee694bf16f6ba441f39f3bf2`  
		Last Modified: Fri, 06 Sep 2024 22:20:14 GMT  
		Size: 10.7 KB (10689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae5e07e1049261ee8124aed782904aa09b1a8dfd17843d519c36524d0f3786f`  
		Last Modified: Fri, 06 Sep 2024 22:20:15 GMT  
		Size: 21.5 MB (21546066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4117f49dd665941a8218d194f77de9587195f7b726f1b559d3f31b36cb9016a`  
		Last Modified: Fri, 06 Sep 2024 22:20:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1011b745223741465fb0a361bfb896ddcc33aae934b5dcc025532b748dd73e`  
		Last Modified: Fri, 06 Sep 2024 22:20:16 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d639a9f8196c5026514225d981d23c011078bc48a5e207b3b941a933e82df2e2`  
		Last Modified: Fri, 06 Sep 2024 22:20:16 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2451556e3c72e88f95ff7647887d36a5828113e6063cd6df857b169666200e86`  
		Last Modified: Fri, 06 Sep 2024 22:20:17 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:473caa862c6f1a1b95cad4ddc483e0b09d6222f5ea23c8e1f147e31d424e2228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18163360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99b2ddb46cd3564db318b8b3305992c6be9aed7ed8b3ea7cb100186987439b`

```dockerfile
```

-	Layers:
	-	`sha256:abcdee78702c5ab89ec2e3ec05e24d86812def93268ca17c7769e6a23d026293`  
		Last Modified: Fri, 06 Sep 2024 22:20:15 GMT  
		Size: 2.9 MB (2922686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9c08284cd881a869d7ec0aafe65722684e70559ab0a878bd27a14c98e63916`  
		Last Modified: Fri, 06 Sep 2024 22:20:15 GMT  
		Size: 5.0 MB (5013333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beb4e964bfa338b03d5077f1fbe4167d8c446d3964aebc04fa5a25f372b0232e`  
		Last Modified: Fri, 06 Sep 2024 22:20:15 GMT  
		Size: 5.2 MB (5151295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee57527903154593a87325a86a72fcdc42053b1d8f4bf67216e394e85d27b184`  
		Last Modified: Fri, 06 Sep 2024 22:20:15 GMT  
		Size: 5.0 MB (5014855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49772a24c8a841bb8a9d1a3274de9f46e433ee5379b53090812b8a901067a1e8`  
		Last Modified: Fri, 06 Sep 2024 22:20:16 GMT  
		Size: 61.2 KB (61191 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:2e6f90e34507f46502ced09eb568434a6526639f3ea5622b17c5ad5e22843b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100141722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919316c593c451e8249d672e7f6136321fbde364f4605ca3dd9d1b7fdf0d2a2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Sep 2024 23:00:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_VERSION=3.13.7
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Sep 2024 23:00:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 23:00:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Sep 2024 23:00:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208cb6e5cd8666040170efdc9f3493966f9db83bd36a75b2fb62332767871e0`  
		Last Modified: Fri, 06 Sep 2024 22:51:56 GMT  
		Size: 44.1 MB (44094743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bb9b223a1857689973883ad517254420a10928ee8d809ed0bb361f5cb7496b`  
		Last Modified: Fri, 06 Sep 2024 22:51:55 GMT  
		Size: 7.1 MB (7135016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b057ef1289c3ebc80d93eee0d2ad47bd5683860029a4ac27b6a82020c8efc0`  
		Last Modified: Fri, 06 Sep 2024 22:51:54 GMT  
		Size: 10.7 KB (10742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a9c0fa6a13f14efedc19240105146753cfaec4b835957b744ae5895017d6`  
		Last Modified: Fri, 06 Sep 2024 22:51:55 GMT  
		Size: 21.5 MB (21540789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c5e426c3c5a1ee0567ab6796724a6440ac2334c04503d8f3dd570133d1a0b`  
		Last Modified: Fri, 06 Sep 2024 22:51:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811761d316234208fe96147db15d1bcf0071d996ff32d17dc596277a4864aa4f`  
		Last Modified: Fri, 06 Sep 2024 22:51:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb41b67a5e527a1d1fff6919af1b66cac0c716f7487d70605f84bd57add4c82`  
		Last Modified: Fri, 06 Sep 2024 22:51:56 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1f88a54d8e83c8c0538b9ada9e5dd347194774fc4deb88f9d2f110b92e9a2c`  
		Last Modified: Fri, 06 Sep 2024 22:51:56 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:55169f1e0508b666331f2571a5e09e9767a6e8b484e028861be485af0a0c69ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18696715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729521d1859804fded8a578e60ba47c875477bc163e5282b8abe421f4e9a3ebb`

```dockerfile
```

-	Layers:
	-	`sha256:fdd0835137cf76f346cbf81d3a3d91a546c3d7d9e58e9f66936dc5464db7cb66`  
		Last Modified: Fri, 06 Sep 2024 22:51:55 GMT  
		Size: 2.9 MB (2921934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63245001c2740b5e21e1f20d2bec972d5fd344e147f3dfd4351d109298493b1f`  
		Last Modified: Fri, 06 Sep 2024 22:51:55 GMT  
		Size: 5.2 MB (5190613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cd6110d3113c8f24ec025e4b7fc5c4c4c7148fee7857644d2c616da7115cc2`  
		Last Modified: Fri, 06 Sep 2024 22:51:55 GMT  
		Size: 5.3 MB (5330728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9146b1065f5a1800db017e9563b89dc456fb3a8cc7ae3997469b132da6f71917`  
		Last Modified: Fri, 06 Sep 2024 22:51:55 GMT  
		Size: 5.2 MB (5192135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c95f02b14246ef17849ae6caf4f0abad9a4c73d33d7f0b331f3435a10e7026`  
		Last Modified: Fri, 06 Sep 2024 22:51:56 GMT  
		Size: 61.3 KB (61305 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:72de2221ccaf8ac311ff9710e4f384e13180f6bedf930115700b2ed9e056e65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103531047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b071a21ae9ea3fc1718220c88835f47a8e4069af2389c74c0b486fc6daefb98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Sep 2024 23:00:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_VERSION=3.13.7
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Sep 2024 23:00:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 23:00:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Sep 2024 23:00:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a70f4bb767cb8840eb80cca7b9e3cf304b5920e6e4e1efdc81661e41b2d0486`  
		Last Modified: Fri, 06 Sep 2024 22:25:47 GMT  
		Size: 39.6 MB (39613222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29148e6de42540f6d1c59c7397251d7ebe5a16c86f74868643b26526810576b`  
		Last Modified: Fri, 06 Sep 2024 22:25:44 GMT  
		Size: 7.9 MB (7870431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a5d5253bd2d5b8345ad873b9a1203592721b8b1a15139b7d0d3753a19354a9`  
		Last Modified: Fri, 06 Sep 2024 22:25:44 GMT  
		Size: 10.7 KB (10660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657aaa7abde74af1d52a465fd4d1fd95eec3cb339377bedda4834817e582921`  
		Last Modified: Fri, 06 Sep 2024 22:25:45 GMT  
		Size: 21.6 MB (21570801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60803a4a022e7242b6d7e0a2048494ce36d73b506b8131dab18c7a0fc836c4`  
		Last Modified: Fri, 06 Sep 2024 22:25:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304ea1984d3a3a7fd64b5ad87455a5f0406bbc2be3d0e77668cee8711abd26eb`  
		Last Modified: Fri, 06 Sep 2024 22:25:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ce556957f620fe7063aed16947c2a2cb9fe3cbf85826542b8097e1b9649db9`  
		Last Modified: Fri, 06 Sep 2024 22:25:46 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5829cc081a07b8dd6fcd27e91ce5d33a03e132e4ba7cf47b0052f1db3e70944c`  
		Last Modified: Fri, 06 Sep 2024 22:25:46 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f57f0a4400bac7f9c01fc35eb0f6b7ce10816491663e59fbf8e07185c3a4c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18594793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa427e54c29946460e80edc0edbc39cd5f117eece57b87d3f553d6e419b14f7d`

```dockerfile
```

-	Layers:
	-	`sha256:bcccb1ea8644bc0dea62e0807b4de95adb83e8b55218bef735364ca9e71792ed`  
		Last Modified: Fri, 06 Sep 2024 22:25:44 GMT  
		Size: 2.9 MB (2925419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d815c2fd3d9e652383d6fff0e6710ac09ce24bef02a837a874d21f2a397e9f5b`  
		Last Modified: Fri, 06 Sep 2024 22:25:44 GMT  
		Size: 5.2 MB (5155923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eba720f661c530e50f89eacd9170ad2edd8f1f8531094e7f9991ccb46d4434`  
		Last Modified: Fri, 06 Sep 2024 22:25:44 GMT  
		Size: 5.3 MB (5294946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cca4b2d569b14fb200c5b217e2a4378f9850d22f1e741f11b2f5d2cadec78ee`  
		Last Modified: Fri, 06 Sep 2024 22:25:45 GMT  
		Size: 5.2 MB (5157445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fc79856ad5674ad4009fc4b00d1b3259cdeacfb3a6d1c018cb3a0a95e5f231`  
		Last Modified: Fri, 06 Sep 2024 22:25:45 GMT  
		Size: 61.1 KB (61060 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:fd8b0dd1eb8bcbba07b292453656cde86fdb124549e40acdf070c0babd3e5049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90311816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddaecad3c5b555ac3b4560c48de55a90b114aff74c03cb3c8b1a8292b32e749d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Aug 2024 09:46:18 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:46:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:46:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:46:50 GMT
ADD file:65730ebc4f5c87ad2819baf4578dff86ef70bfa877e40377f92374ad73967fb8 in / 
# Tue, 13 Aug 2024 09:46:52 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Mon, 26 Aug 2024 05:05:19 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_VERSION=3.13.7
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 26 Aug 2024 05:05:19 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Aug 2024 05:05:19 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 26 Aug 2024 05:05:19 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 26 Aug 2024 05:05:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 26 Aug 2024 05:05:19 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 05:05:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 05:05:19 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 26 Aug 2024 05:05:19 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:871720a2bca8bf3798ea402af23e433011d55654d989b8049f476bb064f81b9a`  
		Last Modified: Tue, 13 Aug 2024 10:45:14 GMT  
		Size: 27.0 MB (27039180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c23d5ce60948d36cd18e87e1c7ad8fe04ddf218ded847281f825a092e229c20`  
		Last Modified: Sat, 24 Aug 2024 03:07:43 GMT  
		Size: 34.5 MB (34491950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a39624180d1a07329fb0f56cf6c9708574a4a9cbffb5ed9042ce1241656302`  
		Last Modified: Sat, 24 Aug 2024 03:07:38 GMT  
		Size: 7.2 MB (7213432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466a08a698cd6360636c958cae96d2305db59de1e485824bb98b0b8103b4a804`  
		Last Modified: Sat, 24 Aug 2024 03:07:36 GMT  
		Size: 10.7 KB (10705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba5593d8a7a6bdadfe2a65cf80af1344c117da9ce1d296e52502170889d278f`  
		Last Modified: Mon, 26 Aug 2024 23:05:11 GMT  
		Size: 21.6 MB (21554801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78007db2fa1c257145038d1dd85f6c957788dc4529875b5ca370d4dade492a9c`  
		Last Modified: Mon, 26 Aug 2024 23:05:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1405bf47d0c15ebefd7f8e7440cd34c41321c250abdd77516d294340ec186fbf`  
		Last Modified: Mon, 26 Aug 2024 23:05:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4b47d5042c3f03aab74d9cb0a013efb349586556859b05ea393d5ac613b581`  
		Last Modified: Mon, 26 Aug 2024 23:05:08 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a11776eac0f80fe2bdfc76562ced023ae3b2ebefe8a107a97d489642dae6eda`  
		Last Modified: Mon, 26 Aug 2024 23:05:09 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:03f94b9195fe0da8246e3cd7315f18cd3e9d6d08d4b49e2ad0d5a39326ca1a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18552403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80438060f9a60a006238fc7ef1ee5f50bec4e24a3a423c11e3f9d630522018f1`

```dockerfile
```

-	Layers:
	-	`sha256:3e0d8da10f1c5864a7ccb120ed4547189df4d9b821e77d97101c978f9c9d3454`  
		Last Modified: Mon, 26 Aug 2024 23:05:08 GMT  
		Size: 2.9 MB (2912693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b024a07d2a7c1602dedf577842a91abbb0f698f25cadd181ebd328a77885113`  
		Last Modified: Mon, 26 Aug 2024 23:05:09 GMT  
		Size: 5.1 MB (5145737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:312b4ee8cbd19d18107c7dc6bb43a955ce5f609941d4fb111dd2334b742385e0`  
		Last Modified: Mon, 26 Aug 2024 23:05:09 GMT  
		Size: 5.3 MB (5283687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db054e66920ad6e11171b09e2c9755b16e4f0f3e07fb7fcf299de175a9081d38`  
		Last Modified: Mon, 26 Aug 2024 23:05:09 GMT  
		Size: 5.1 MB (5147259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4183a1435f239d656d84374012db4c77b15e4564e5530be40da7d1bc7f33a99`  
		Last Modified: Mon, 26 Aug 2024 23:05:09 GMT  
		Size: 63.0 KB (63027 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:b8c325d5ea31f122e152651d884a7120d6dd2396a42677896d4d554cba3792bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94397736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4424e3af6e5f476c130869acb1cc0c6b7c9ed3ad3179d647fbeac9befb8bdef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 05 Sep 2024 23:00:29 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_VERSION=3.13.7
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 05 Sep 2024 23:00:29 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 23:00:29 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 05 Sep 2024 23:00:29 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 05 Sep 2024 23:00:29 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 05 Sep 2024 23:00:29 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 23:00:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 23:00:29 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 05 Sep 2024 23:00:29 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e280dadf5b2aeff3eee5ef7e055d95037f9fdf834a26d90fa2a2127a91d7cf49`  
		Last Modified: Tue, 13 Aug 2024 10:45:20 GMT  
		Size: 28.0 MB (28001322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1116d7d5f92ba7361ac4d981692ccb139a04db99583ac7d67efa1c4eabfb4f5e`  
		Last Modified: Fri, 06 Sep 2024 22:25:00 GMT  
		Size: 38.2 MB (38247399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e740c02a0168b9035993553e837b685f76a0aea447949ce95539a90055837`  
		Last Modified: Fri, 06 Sep 2024 22:24:59 GMT  
		Size: 6.5 MB (6536567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce443b5f5058c7d0bd21a3a0014b485c9ced8fcbab6e881f705fc7a3388f4cd3`  
		Last Modified: Fri, 06 Sep 2024 22:24:59 GMT  
		Size: 10.7 KB (10746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d91db04c001b6811b2d6031f1f52337d2afd552821faeb4f5c637fb9873604`  
		Last Modified: Fri, 06 Sep 2024 22:25:00 GMT  
		Size: 21.6 MB (21599952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da98719828cc7aa2bf0e8b843edf5d42c65d8b0006ee8500d60a2a8a4fa6d055`  
		Last Modified: Fri, 06 Sep 2024 22:25:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb195e6c0a3388bfd1e7adeb91050063364132c6b2bd024fa4ad29a6eb3e9200`  
		Last Modified: Fri, 06 Sep 2024 22:25:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f4eb13a1eb8b65ad01b0db6e65c4f248ff43ce7b6459bf6a2947ce728da188`  
		Last Modified: Fri, 06 Sep 2024 22:25:00 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c82423983b308bca547efb0573d26abbbde9f4f5dd3c200b830716b43d15ea`  
		Last Modified: Fri, 06 Sep 2024 22:25:01 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:73d230a1c85ff808d80eaa8aade2e815f1232e14335c2429629d81ddfbb01bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3672d32cbc2acbbc45fa45fbe5fc639654330d3d443ccee4d04fb264e264f6c`

```dockerfile
```

-	Layers:
	-	`sha256:d6ab2e4089f6779e9ef45f8ba243f97e59eae33b9733738e1828cd2659d678d3`  
		Last Modified: Fri, 06 Sep 2024 22:24:59 GMT  
		Size: 2.9 MB (2923269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:835ec43fb0fe562a3f69278c49abd7bf67da2184c970d2c1e3a45dbbcbf44ba3`  
		Last Modified: Fri, 06 Sep 2024 22:24:59 GMT  
		Size: 5.0 MB (5036603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3e990385cdba95d7759d4a3a2b3ecdde50599834c8c79bc29c368519e5fe5f8`  
		Last Modified: Fri, 06 Sep 2024 22:24:59 GMT  
		Size: 5.2 MB (5175606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c424949f6ff1f496fd119c4882a8891b8bb92e5b360864e7ad14119403856d`  
		Last Modified: Fri, 06 Sep 2024 22:24:59 GMT  
		Size: 5.0 MB (5038125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d60489f0ec7e4e888a273ed87c4f3700488f3954ce930330c31a8725fc05e1`  
		Last Modified: Fri, 06 Sep 2024 22:25:00 GMT  
		Size: 61.0 KB (61004 bytes)  
		MIME: application/vnd.in-toto+json
