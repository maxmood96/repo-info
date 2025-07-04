## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:677f08fc624ebdd1e11a62cdd192e091d815f239230b339a902b1f337707699c
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
$ docker pull rabbitmq@sha256:a30bfa17f922a71340c04ff390296d7d2198da5825e3c41e6178cd795e9a97d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115329815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83ead07939667681a604706fae3b33c9ea34bc31044db704009f0118b3a115b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Jul 2025 17:05:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_VERSION=4.1.2
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Jul 2025 17:05:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Jul 2025 17:05:34 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bc06b492f274e8b69c5fd9bd9c28834efa18cc27e6ff7594e168375a6c4625`  
		Last Modified: Thu, 03 Jul 2025 23:16:05 GMT  
		Size: 46.2 MB (46249416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5443e20a68a7e5d3b5aec06c74e0fb13575fd7b55898e535d9f2c6329f12b6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:42 GMT  
		Size: 8.2 MB (8173842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4a02cfe92867723bb39ea1f2fa5d55962dbb90090c2fb2216cb0821f0e56a0`  
		Last Modified: Thu, 03 Jul 2025 23:15:40 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a50da602dc1b0093ee24fd2e1097984dbb6054a5feb5ff1564cbfc311c5a743`  
		Last Modified: Thu, 03 Jul 2025 23:15:57 GMT  
		Size: 31.2 MB (31176960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df65927f37a86720c429966fd9881fc7eca66950b2ecbc469e2b8e3665cf0a90`  
		Last Modified: Thu, 03 Jul 2025 23:15:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07387d31093537ff7442164b280db47ef569876af91ddcbed6383627295d9bb`  
		Last Modified: Thu, 03 Jul 2025 23:15:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649069e803080509d8edf0f484b81f931e6defd9ac379fed8393b5fd13a49200`  
		Last Modified: Thu, 03 Jul 2025 23:15:43 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11385cfddca7f450bba14d7191f5fdb43fd673a3437307a4e26578339203608`  
		Last Modified: Thu, 03 Jul 2025 23:15:44 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b886e2d10c8b64b83498976605452b35fb1940d37363bbae55a514dfdf77f8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18837163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a12ca2dca02f46eb8f9700f8b513dabf8bc2fcf1da7bf9315a520a4d913c96`

```dockerfile
```

-	Layers:
	-	`sha256:dded6e93bfe0a6b98a4a87428928d5cc27506488ce9bcbd4d852ce519cb7b456`  
		Last Modified: Fri, 04 Jul 2025 00:52:37 GMT  
		Size: 2.5 MB (2483894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a1d9e391aaa2309de95a4c828bd9e8f524011b1d21ca1e013a56f8c5cdb23d`  
		Last Modified: Fri, 04 Jul 2025 00:52:38 GMT  
		Size: 5.4 MB (5378375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03983f9cb31639969e49b8ad45e4982f04acfce489bcde04225210463f2a5cd9`  
		Last Modified: Fri, 04 Jul 2025 00:52:39 GMT  
		Size: 5.5 MB (5534936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5ef6728aade0d867871bc0baf929f9f17df19e8bd1b68cf5fb706679349f79d`  
		Last Modified: Fri, 04 Jul 2025 00:52:40 GMT  
		Size: 5.4 MB (5380117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fec5afb6092607bbe562635a02d7cf586b4d06de4dd24b5c0c50de7811410038`  
		Last Modified: Fri, 04 Jul 2025 00:52:41 GMT  
		Size: 59.8 KB (59841 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:329c4ecac3a2b83569cf0120bdb4a96582fd0d7ec1e2298f44e6abb4d2de9e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97884907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6fade8a3fb01a4708eac314fcd5b65acbcdb6fe8845928417f7af837aa98c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 19 Jun 2025 23:17:29 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:17:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:17:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:17:29 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:17:32 GMT
ADD file:88b7ca184cec1707b10b6b543ddfa7abfcacc2605cdd5919877294ff5290aa3e in / 
# Thu, 19 Jun 2025 23:17:33 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Jul 2025 17:05:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_VERSION=4.1.2
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Jul 2025 17:05:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Jul 2025 17:05:34 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:149362fdfa6e6a5d9f009b896da3be3172c395ba2287b57d4969f3f46e573055`  
		Last Modified: Fri, 20 Jun 2025 10:02:42 GMT  
		Size: 26.8 MB (26844462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c736e9b1c519b4a1ede7879077a44f09cb5e7f8776f3559d3790c9c5f430142d`  
		Last Modified: Wed, 02 Jul 2025 10:38:24 GMT  
		Size: 33.3 MB (33280390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f64fd76ded544fa3c2bdc0f21265c80670999b8b1cb39046fcb4bbb37f62e14`  
		Last Modified: Wed, 02 Jul 2025 10:38:08 GMT  
		Size: 6.7 MB (6670174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f8f66c1e903468e9285698254742d63355dc49c02e1c039bf75d775c711bdc`  
		Last Modified: Wed, 02 Jul 2025 10:38:06 GMT  
		Size: 9.5 KB (9515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495bb2a9db8df2c7fadfcfa35d91a3a18851eff0e22bb465d170d7c6798bc422`  
		Last Modified: Fri, 04 Jul 2025 05:12:37 GMT  
		Size: 31.1 MB (31078617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0923fa64d0073a2ada4a63a71fe98e8387056785845f6d147c08b847fbfff44d`  
		Last Modified: Fri, 04 Jul 2025 05:12:33 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d20cc1edd02ad8382412bac536505ec1fe6ac98c57390ff527514249f639a0`  
		Last Modified: Fri, 04 Jul 2025 05:12:33 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40430a57ee5496d1374328b78b221a871c8a97e4421ef28025d7788cee9ad6`  
		Last Modified: Fri, 04 Jul 2025 05:12:32 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682232e26147e27d58be473e6058277a4dfc1b5bf47b784ad97ae66266d31e2d`  
		Last Modified: Fri, 04 Jul 2025 05:12:33 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:db50154e5cde7c00a4dfcbbc3cf417e8a923a020509e621323502eeaf2a21a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18291949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bd69e04b7432ad0af1b7408a47491dfd6450fe5e78a6baea2631416c0972ff`

```dockerfile
```

-	Layers:
	-	`sha256:27f1b036b51211cb345160bc375e58d81c5268f245daf2acb6b102a524ab9315`  
		Last Modified: Fri, 04 Jul 2025 06:52:48 GMT  
		Size: 2.5 MB (2484698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57010eb167794995c169154920e827dbdc729a11d9455b7cbf9d9bc9f17395cc`  
		Last Modified: Fri, 04 Jul 2025 06:52:49 GMT  
		Size: 5.2 MB (5197155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5973a0c4c2537456d2181bbb742cddbbd1d5ab61eafc523249f29723ca2f0f`  
		Last Modified: Fri, 04 Jul 2025 06:52:50 GMT  
		Size: 5.4 MB (5351165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9763d3e110a69ed214e6806405c14cd389f6f98b1d63b075b3e01a8a942693`  
		Last Modified: Fri, 04 Jul 2025 06:52:51 GMT  
		Size: 5.2 MB (5198897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ac15be0e5259e6ca7f9c76d43e1da78ae06ea00e38f1c0056badb0c3d913b20`  
		Last Modified: Fri, 04 Jul 2025 06:52:51 GMT  
		Size: 60.0 KB (60034 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:ee541bfa357d8f6779e02fcaa6573ff0f8f5a3507120815e11afb07e3b916110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113244298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2244e5b3dbd2c30e05159381555bb3aa7d55df2f2ce35cdb4c408ffc8de24306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Jul 2025 17:05:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_VERSION=4.1.2
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Jul 2025 17:05:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Jul 2025 17:05:34 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e0fa44061449a8370e1b175883a34ced482668229715359eeddddc8500885`  
		Last Modified: Wed, 02 Jul 2025 06:19:03 GMT  
		Size: 44.3 MB (44339886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fa53e092b9644ac160698c515ba7c07ee8835279bda3e44479fb81630c7670`  
		Last Modified: Wed, 02 Jul 2025 06:18:58 GMT  
		Size: 9.0 MB (8950472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a355ea2c474923a8bacb7c0afea23225644f43a846ea2d7f1b4b826c48b38e15`  
		Last Modified: Wed, 02 Jul 2025 06:18:57 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656c75960d709abf04baa406ab850fdf9d3b37c69bcbc249e037692b1a98f3ff`  
		Last Modified: Fri, 04 Jul 2025 07:59:07 GMT  
		Size: 31.1 MB (31086747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28f0b8dd720ea08dd6a1f1fed81f4d37790ba71579ab18b2fec38241d4a6a85`  
		Last Modified: Fri, 04 Jul 2025 07:59:05 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c6e6ddd60c728ee2c54b7515079b667e94f93ef438b8080e2f15853239ae9d`  
		Last Modified: Fri, 04 Jul 2025 07:59:05 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6b59115c24faf4dfd8b83801df90789569c6fb7ad59c3c0af6ae03e3627e0`  
		Last Modified: Fri, 04 Jul 2025 07:59:05 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f1dc297a5d34104ff59ff119597dce383f2e4decf6972b6b4fea349f73f26c`  
		Last Modified: Fri, 04 Jul 2025 07:59:05 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:a282df761fa94696c1a3f16e2c6785d64a5a14859eb95bfa1421ea43f9c33152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18896143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8207318186efbd66ef89ac197650ca877628801ffc746c490bd8dd168d4efc56`

```dockerfile
```

-	Layers:
	-	`sha256:2b0582c421e2329810a9d3b1f79629682e8e239ce33ab0e8d7b018cb08e77801`  
		Last Modified: Fri, 04 Jul 2025 09:53:02 GMT  
		Size: 2.5 MB (2484954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a930aec2f6dbf16278ad52ea302741ad305f1be1f379c70248a9e61f5c5dfbb`  
		Last Modified: Fri, 04 Jul 2025 09:53:04 GMT  
		Size: 5.4 MB (5397596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd11f4fe0b15118889284a52b7e5f42bdc2b3b6028d384292e44484c9712d8a7`  
		Last Modified: Fri, 04 Jul 2025 09:53:05 GMT  
		Size: 5.6 MB (5554175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832b7f8032e8cb012ce45308ce894f30d951060c5905f1196c24e9c160c299ec`  
		Last Modified: Fri, 04 Jul 2025 09:53:07 GMT  
		Size: 5.4 MB (5399338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e8781239bc02f2b856010aa9a4e0682a105c670dde906c7e04dc1dc0c5b82c`  
		Last Modified: Fri, 04 Jul 2025 09:53:07 GMT  
		Size: 60.1 KB (60080 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:49bc750671130be8ef099155478ce422db97b53dcaf3d6e7671c217a68a75eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113651075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382b1bb28b5ba010aaccb97d2037cbe2ff9fe5185eb68f2a9471e773d1933547`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 19 Jun 2025 23:18:14 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:18:18 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Thu, 19 Jun 2025 23:18:18 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Jul 2025 17:05:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_VERSION=4.1.2
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Jul 2025 17:05:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Jul 2025 17:05:34 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d2bba74425982e030400de843abdc2bc27acc4e91613999d98c6e54703f50f`  
		Last Modified: Wed, 02 Jul 2025 04:28:46 GMT  
		Size: 39.5 MB (39481375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8208f10bd1177a1c6da08eabf611e427734bfff1d2618bc65da75152bfc9a`  
		Last Modified: Wed, 02 Jul 2025 04:28:44 GMT  
		Size: 8.7 MB (8700492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd7c951189bf5fb8d8e1ac62c5fd815f9adbf9b80f0dcdb7ae67c80c719fc99`  
		Last Modified: Wed, 02 Jul 2025 04:28:43 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a9d86eb2b7323125655264c4b7e9311a9b41a0762932402e124b82eacf1248`  
		Last Modified: Fri, 04 Jul 2025 06:41:03 GMT  
		Size: 31.1 MB (31136565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffc0a7ec173352f57ce3d89f738eb15b195331ba4ea0b1afaff2ab9453f145c`  
		Last Modified: Fri, 04 Jul 2025 06:41:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5370f0309044b1121a45d8c276b1db6cbbbf3bea6532593ba242cb0ba962b6f0`  
		Last Modified: Fri, 04 Jul 2025 06:41:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5b694b27c700f347d9d25872f5886aecd8298321573b716ed9143fd16a20cf`  
		Last Modified: Fri, 04 Jul 2025 06:41:01 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75e8e2512069f33101aa99740a4ecf5ffe3bc059dfdb32acd81255491859731`  
		Last Modified: Fri, 04 Jul 2025 06:41:01 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8442d905a255fe334e570388861fe591141c30f4c95bed072269c1dfad18d729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18751534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaa7f4e7f3d2ae4cb06941aa9a7e4d88424a2412f1186bf898134fb991f83af`

```dockerfile
```

-	Layers:
	-	`sha256:8c4534b1b17b310584769bb805846ebb726c64d65c53c5580982c5d0f5c807f9`  
		Last Modified: Fri, 04 Jul 2025 09:53:16 GMT  
		Size: 2.5 MB (2488347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9e8e9644eddd17fc13e7e78899bb387055cd5c878548c448e79b967dfd288e`  
		Last Modified: Fri, 04 Jul 2025 09:53:17 GMT  
		Size: 5.3 MB (5348317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:805fd7c62a269ddc3161449d63f19dc5d3016d87f1f938031a57b618aeb2daf4`  
		Last Modified: Fri, 04 Jul 2025 09:53:18 GMT  
		Size: 5.5 MB (5504908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f69046a37558447b4b8a8ee9e4c274c7d3216f89706e0b32fe5cc13fc78d6d3`  
		Last Modified: Fri, 04 Jul 2025 09:53:19 GMT  
		Size: 5.4 MB (5350059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ef1478bb25c5d6c3d47ae07009e56cc4deec7f3adb2bfcd94383ed4fb8cfb5`  
		Last Modified: Fri, 04 Jul 2025 09:53:20 GMT  
		Size: 59.9 KB (59903 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:a66c0d09c7ade5081506561d2730270923e8737b6ae515a3fd7a2b3845979f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106913805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5779f39c3a3e11b7089b2c71861222160a266575714d2bd054c04f9939751232`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 20 Jun 2025 01:33:34 GMT
ARG RELEASE
# Fri, 20 Jun 2025 01:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 01:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 01:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Jun 2025 01:34:22 GMT
ADD file:202c5a7a84e813495c089800398f2ba18952221717db2c10e042ce4179ee6fc0 in / 
# Fri, 20 Jun 2025 01:34:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 01 Jul 2025 17:33:36 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_VERSION=4.1.1
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 01 Jul 2025 17:33:36 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 17:33:36 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 01 Jul 2025 17:33:36 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 01 Jul 2025 17:33:36 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 01 Jul 2025 17:33:36 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Jul 2025 17:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 17:33:36 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 01 Jul 2025 17:33:36 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4ccdff8fdb11e14b8e0dab6804aeebce5855635c68b20f199dcf0efcd9b4c462`  
		Last Modified: Wed, 02 Jul 2025 01:17:14 GMT  
		Size: 31.0 MB (30951024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be7b0af61fef4d20c27e5839f79ff2c94c421e8c21e282402605fd4b2b03de3`  
		Last Modified: Wed, 02 Jul 2025 05:09:00 GMT  
		Size: 35.1 MB (35134643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d80a6edacf1ca483e6d85d047d781a5b4a7ca5aa09b84850b831ec4b592821f`  
		Last Modified: Wed, 02 Jul 2025 05:08:59 GMT  
		Size: 9.8 MB (9791868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e674410975d4fc5258001f16f83318dd839e53b9a88a5f156e5e45ee1e71bd32`  
		Last Modified: Wed, 02 Jul 2025 05:08:58 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7c2dbe70f9ef222239b1b5168a85ef4d5de79912566ff5651af50b8f229cf7`  
		Last Modified: Wed, 02 Jul 2025 05:09:00 GMT  
		Size: 31.0 MB (31025026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a25e3b914679ef67a8f941699ebc3bf411c6029b310702e43c38c92e4c9d1e4`  
		Last Modified: Wed, 02 Jul 2025 05:08:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e374e096a6dc56be6b64f9316a6613bf6b4c770abd825287837dc9dc6feb04`  
		Last Modified: Wed, 02 Jul 2025 05:08:58 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae730b64496e237ef246ac08f38be9f6933d5e2b49e52852eb11f08da90b34cd`  
		Last Modified: Wed, 02 Jul 2025 05:08:58 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a728ac62c2feefe3249dab9861332ac5b3baaf399e8ae387e9be6aaf1f6aa89e`  
		Last Modified: Wed, 02 Jul 2025 05:08:58 GMT  
		Size: 838.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:35c659ae27a258ec3f56f2f54c57f27789de9ac0855a8487c89e2bc173a8d524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18720165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d9df5e12b903303fdec397fbffe647fc0db373bc0a2ed33286a15f40237a26`

```dockerfile
```

-	Layers:
	-	`sha256:ff06039908cfa4e353e2436017f663a19162f9089916e616a1b2bbb60d7e127b`  
		Last Modified: Wed, 02 Jul 2025 06:53:47 GMT  
		Size: 2.5 MB (2476262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13bd01feecf04a48b6720c331480027d56387778d9cb69250069097e2d25c8f4`  
		Last Modified: Wed, 02 Jul 2025 06:53:48 GMT  
		Size: 5.3 MB (5342750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ea6e3954f023fad5452d9b3b80158dcd11f0f66176ca7cfec378264ed39423`  
		Last Modified: Wed, 02 Jul 2025 06:53:48 GMT  
		Size: 5.5 MB (5496758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa85b80c60a97b5380a451e463d84cd2d044ca8418159aade3365cba828be689`  
		Last Modified: Wed, 02 Jul 2025 06:53:49 GMT  
		Size: 5.3 MB (5344492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868fd95ee5d2700105f8bf795999f78ed781296875160fc540e70eebdfc7da87`  
		Last Modified: Wed, 02 Jul 2025 06:53:50 GMT  
		Size: 59.9 KB (59903 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:b545c9034e39e6a4cf13f2fbdb3ce09705d600c24d87d7cbe8e835bf2b78b2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107211205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95190e0389ea58c2a878090660502f61d26a7e8b3b833a6119232ec8dd8a06b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 19 Jun 2025 23:17:26 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:17:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:17:28 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Thu, 19 Jun 2025 23:17:28 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 03 Jul 2025 17:05:34 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_VERSION=4.1.2
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 03 Jul 2025 17:05:34 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Jul 2025 17:05:34 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 03 Jul 2025 17:05:34 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 03 Jul 2025 17:05:34 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 03 Jul 2025 17:05:34 GMT
COPY --chown=rabbitmq:rabbitmq 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 17:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 17:05:34 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 03 Jul 2025 17:05:34 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5b72d3e7cf8f0af964ffde32769ff62f24fc508e6db80a191b6562b72fb374`  
		Last Modified: Wed, 02 Jul 2025 05:01:50 GMT  
		Size: 38.6 MB (38559145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f66466a0fec1837e1ae38d931dc3065f44da594ffd27bcd12fc8335f672fc9`  
		Last Modified: Wed, 02 Jul 2025 05:01:49 GMT  
		Size: 7.6 MB (7555955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c95780ec97cce14471b543fe504613ca7e538a1bcd02edb09a16237c08c41b`  
		Last Modified: Wed, 02 Jul 2025 05:01:48 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7830ab2035d2433b0de4d5a99b0a9cd6628acabc583822860f8946ae1234762`  
		Last Modified: Fri, 04 Jul 2025 04:34:50 GMT  
		Size: 31.2 MB (31159094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1405f45de67fed5c016e1dab08d8df02184687ddc69c37be5ee725557b41cb67`  
		Last Modified: Fri, 04 Jul 2025 04:34:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb4ec712c1933162f34b8e6098f45241943b7c63639de62670fc48209049e56`  
		Last Modified: Fri, 04 Jul 2025 04:34:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a0a1c0c034a40acf5d99b16771dcfabfc3bcc5b1814a93dd038e763d99b04e`  
		Last Modified: Fri, 04 Jul 2025 04:34:35 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d4bb6a0edada4220f1712bc2df3ebcd0aa9687c3ce656245ebf66556064e6`  
		Last Modified: Fri, 04 Jul 2025 04:34:36 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ef0db55f743a5d51ab8277117443dbde2d940b962c979d421df497e882616810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18377314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7e833620f72f9c4c65336e3af026fafb2301e18076aeea64d650788eabefd8`

```dockerfile
```

-	Layers:
	-	`sha256:c284dd94791d00d0c595413fe64f67830d2ed9ff8beb380e39b2155b78ccb805`  
		Last Modified: Fri, 04 Jul 2025 06:53:23 GMT  
		Size: 2.5 MB (2486006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6425fa72d3845dbd7892fe984ad4977775c041bc1483da9b213b22f22b049c`  
		Last Modified: Fri, 04 Jul 2025 06:53:24 GMT  
		Size: 5.2 MB (5224822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d393a9d420ef9eec401e260dd3bbbf18d2cc648c3a2e38f4c7cbc8101a90a82`  
		Last Modified: Fri, 04 Jul 2025 06:53:25 GMT  
		Size: 5.4 MB (5380081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8347bf1eb17d114ed3f90c374d7f72a11aa90e54d3c91bb7aed8d9596cc645`  
		Last Modified: Fri, 04 Jul 2025 06:53:26 GMT  
		Size: 5.2 MB (5226564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3fe360f4fce187073370aff6e9f43a968f1f9bd12bdddc4e0e1b5f8ff86a680`  
		Last Modified: Fri, 04 Jul 2025 06:53:27 GMT  
		Size: 59.8 KB (59841 bytes)  
		MIME: application/vnd.in-toto+json
