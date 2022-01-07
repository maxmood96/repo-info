## `rabbitmq:management`

```console
$ docker pull rabbitmq@sha256:821c31bdb35240822e9a7b95eb57e2aaa9590dc367b0598b58efd15fb037fc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `rabbitmq:management` - linux; amd64

```console
$ docker pull rabbitmq@sha256:65a21ca413bc6db799a8c138757ad4b554d360ce92c26cc990f550d5cfb9e2a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108806214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd125ba2410e2264ebed833a6e6f5f050f77ea78f0f62dc3ce54ea058a62c9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*; 	gosu nobody true
# Fri, 07 Jan 2022 03:45:15 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Fri, 07 Jan 2022 03:45:16 GMT
ENV OPENSSL_VERSION=1.1.1m
# Fri, 07 Jan 2022 03:45:16 GMT
ENV OPENSSL_SOURCE_SHA256=f89199be8b23ca45fc7cb9f1d8d3ee67312318286ad030f5316aca6462db6c96
# Fri, 07 Jan 2022 03:45:16 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Fri, 07 Jan 2022 03:45:16 GMT
ENV OTP_VERSION=24.2
# Fri, 07 Jan 2022 03:45:16 GMT
ENV OTP_SOURCE_SHA256=af0f1928dcd16cd5746feeca8325811865578bf1a110a443d353ea3e509e6d41
# Fri, 07 Jan 2022 03:49:13 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		autoconf 		ca-certificates 		dpkg-dev 		gcc 		g++ 		gnupg 		libncurses5-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum --check --strict -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	debMultiarch="$(dpkg-architecture --query DEB_HOST_MULTIARCH)"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		--libdir="lib/$debMultiarch" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	ldconfig; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --progress dot:giga --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum --check --strict -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; export CFLAGS; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Fri, 07 Jan 2022 03:49:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 07 Jan 2022 03:49:14 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Fri, 07 Jan 2022 03:49:14 GMT
ENV RABBITMQ_VERSION=3.9.12
# Fri, 07 Jan 2022 03:49:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 07 Jan 2022 03:49:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 07 Jan 2022 03:49:15 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RABBITMQ_LOGS=-
# Fri, 07 Jan 2022 03:49:37 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Fri, 07 Jan 2022 03:49:39 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Fri, 07 Jan 2022 03:49:40 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Fri, 07 Jan 2022 03:49:40 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 07 Jan 2022 03:49:40 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 07 Jan 2022 03:49:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 07 Jan 2022 03:49:41 GMT
COPY --chown=rabbitmq:rabbitmqfile:2b942f4756de24f6094cd4bd8e85adc37054221a296429e1c867c9e0f4b5dba8 in /etc/rabbitmq/conf.d/ 
# Fri, 07 Jan 2022 03:49:41 GMT
COPY file:d7e54a3570407a262351dfa2e082aa1713b74883d564d1616d93787afcf4b8c0 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:49:41 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Fri, 07 Jan 2022 03:49:41 GMT
CMD ["rabbitmq-server"]
# Fri, 07 Jan 2022 03:49:56 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version
# Fri, 07 Jan 2022 03:49:56 GMT
EXPOSE 15671 15672
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8128e02f0caaa72e1ce3dd11da8a199fe9e3cc3100ebeaff24bbba78b9d0ad9b`  
		Last Modified: Fri, 07 Jan 2022 03:51:17 GMT  
		Size: 870.0 KB (870017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190ad14731bd4c869cf0fb0310addbefdd64bb9eaea36cb165bef33a1f9cee41`  
		Last Modified: Fri, 07 Jan 2022 03:51:23 GMT  
		Size: 50.9 MB (50929771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77793ffcdff3300a23c6e877dfe074ddbf0d825895040055f29ce5271a32de74`  
		Last Modified: Fri, 07 Jan 2022 03:51:17 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ded75d28575dc16f77c2e174f127ac656fadc52fab7c2982b48809665b59037`  
		Last Modified: Fri, 07 Jan 2022 03:51:16 GMT  
		Size: 16.8 MB (16791777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fe6cea12ab0db786cfe404b213f6fac38e53314eaf224d53ce2a482c7cdb8a`  
		Last Modified: Fri, 07 Jan 2022 03:51:14 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec228f486d8ed615eb06dc61e1bd12674c9c3a61339f84860dd00f22c2f6d6b6`  
		Last Modified: Fri, 07 Jan 2022 03:51:14 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e93459f9f248b77af07273a9d750611d9acf4ac90f020be94ca77761009b496`  
		Last Modified: Fri, 07 Jan 2022 03:51:14 GMT  
		Size: 443.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a076196fb8bdedf2310b3de785050adb1c684107c454f3ae52336711328e2cb`  
		Last Modified: Fri, 07 Jan 2022 03:51:14 GMT  
		Size: 832.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975e2d61b91eb32fb86497b294899d23a775f7ed250c6a39661daeb34cb9b804`  
		Last Modified: Fri, 07 Jan 2022 03:51:40 GMT  
		Size: 11.6 MB (11644490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:management` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:8e3611596420beeee16a079cc2414162b74fc59314bcd21ad308f8230d67945f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93939282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9541208e17f065f7af4be52fa7088dc850d6c0eb9c4a65cd653b1b528f1c7c70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:25 GMT
ADD file:ac83e0dc7e48a0dc1805c0fd7b71b8eb119b3eeafd1fdcab93e11fbc9c0bcda0 in / 
# Fri, 07 Jan 2022 02:26:26 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*; 	gosu nobody true
# Fri, 07 Jan 2022 04:21:58 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Fri, 07 Jan 2022 04:21:58 GMT
ENV OPENSSL_VERSION=1.1.1m
# Fri, 07 Jan 2022 04:21:59 GMT
ENV OPENSSL_SOURCE_SHA256=f89199be8b23ca45fc7cb9f1d8d3ee67312318286ad030f5316aca6462db6c96
# Fri, 07 Jan 2022 04:21:59 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Fri, 07 Jan 2022 04:21:59 GMT
ENV OTP_VERSION=24.2
# Fri, 07 Jan 2022 04:22:00 GMT
ENV OTP_SOURCE_SHA256=af0f1928dcd16cd5746feeca8325811865578bf1a110a443d353ea3e509e6d41
# Fri, 07 Jan 2022 04:26:59 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		autoconf 		ca-certificates 		dpkg-dev 		gcc 		g++ 		gnupg 		libncurses5-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum --check --strict -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	debMultiarch="$(dpkg-architecture --query DEB_HOST_MULTIARCH)"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		--libdir="lib/$debMultiarch" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	ldconfig; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --progress dot:giga --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum --check --strict -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; export CFLAGS; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Fri, 07 Jan 2022 04:27:00 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 07 Jan 2022 04:27:02 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Fri, 07 Jan 2022 04:27:02 GMT
ENV RABBITMQ_VERSION=3.9.12
# Fri, 07 Jan 2022 04:27:03 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 07 Jan 2022 04:27:03 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 07 Jan 2022 04:27:04 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RABBITMQ_LOGS=-
# Fri, 07 Jan 2022 04:27:50 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Fri, 07 Jan 2022 04:27:55 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Fri, 07 Jan 2022 04:27:57 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Fri, 07 Jan 2022 04:27:57 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 07 Jan 2022 04:27:58 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 07 Jan 2022 04:27:58 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 07 Jan 2022 04:27:58 GMT
COPY --chown=rabbitmq:rabbitmqfile:2b942f4756de24f6094cd4bd8e85adc37054221a296429e1c867c9e0f4b5dba8 in /etc/rabbitmq/conf.d/ 
# Fri, 07 Jan 2022 04:27:59 GMT
COPY file:d7e54a3570407a262351dfa2e082aa1713b74883d564d1616d93787afcf4b8c0 in /usr/local/bin/ 
# Fri, 07 Jan 2022 04:27:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 04:28:00 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Fri, 07 Jan 2022 04:28:00 GMT
CMD ["rabbitmq-server"]
# Fri, 07 Jan 2022 04:28:36 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version
# Fri, 07 Jan 2022 04:28:37 GMT
EXPOSE 15671 15672
```

-	Layers:
	-	`sha256:9b8080fa0945580f29aa3abed4664f8ab849229eca04510b5d259a9e29616064`  
		Last Modified: Fri, 07 Jan 2022 02:30:39 GMT  
		Size: 24.1 MB (24064434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96edaa244ff6fb8ddcf21526e0cd83e89e9a53908502fc14377baebca4291b25`  
		Last Modified: Fri, 07 Jan 2022 04:32:57 GMT  
		Size: 838.9 KB (838905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907ae0ad7647062dbf8d6b7b893b3e075ee3d026eb68c1d81303f004c5765b6b`  
		Last Modified: Fri, 07 Jan 2022 04:33:17 GMT  
		Size: 41.7 MB (41718354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ceb922d5780f666e3738a85d2add6506aa3b9890504cfb80b41ab56f96ccd5b`  
		Last Modified: Fri, 07 Jan 2022 04:32:57 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e42dae8a9914a337d766a1094c3d0aed271bbe5265a44fe1802bf0d23c26c4`  
		Last Modified: Fri, 07 Jan 2022 04:33:02 GMT  
		Size: 16.8 MB (16792785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4185845b1c9a6f29c29da453e463660f09c63bcff6d465fa6a20ac1a73b3d83`  
		Last Modified: Fri, 07 Jan 2022 04:32:55 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a8c80b8105a550bc0bf12aae14a1c9a51207567839ae1419baff7d2d1aa42`  
		Last Modified: Fri, 07 Jan 2022 04:32:55 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efae33faf71b2e00ff827caa00acda72f6717730536f9d9803ecbad52a2a11e7`  
		Last Modified: Fri, 07 Jan 2022 04:32:55 GMT  
		Size: 443.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea541ce2884f83eba85a768516bdb4e95d6638b7d540f6d2ba6a417ae0705cb`  
		Last Modified: Fri, 07 Jan 2022 04:32:55 GMT  
		Size: 833.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0811f1fb4947f35ed02e2c192d3253c1a29ccef07966752b2937cc239de375`  
		Last Modified: Fri, 07 Jan 2022 04:33:45 GMT  
		Size: 10.5 MB (10521078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:management` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:da6a771102ba728d18a6d63a61508f7fcb33435ce2f2f6b60b7e91876830eabe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98971980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2685727968f5e63cd7db948a86b00d165184df6e79072b7d351121e60bafeaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:02:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*; 	gosu nobody true
# Fri, 07 Jan 2022 03:02:42 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Fri, 07 Jan 2022 03:02:43 GMT
ENV OPENSSL_VERSION=1.1.1m
# Fri, 07 Jan 2022 03:02:44 GMT
ENV OPENSSL_SOURCE_SHA256=f89199be8b23ca45fc7cb9f1d8d3ee67312318286ad030f5316aca6462db6c96
# Fri, 07 Jan 2022 03:02:45 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Fri, 07 Jan 2022 03:02:46 GMT
ENV OTP_VERSION=24.2
# Fri, 07 Jan 2022 03:02:47 GMT
ENV OTP_SOURCE_SHA256=af0f1928dcd16cd5746feeca8325811865578bf1a110a443d353ea3e509e6d41
# Fri, 07 Jan 2022 03:05:11 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		autoconf 		ca-certificates 		dpkg-dev 		gcc 		g++ 		gnupg 		libncurses5-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum --check --strict -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	debMultiarch="$(dpkg-architecture --query DEB_HOST_MULTIARCH)"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		--libdir="lib/$debMultiarch" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	ldconfig; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --progress dot:giga --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum --check --strict -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; export CFLAGS; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Fri, 07 Jan 2022 03:05:11 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 07 Jan 2022 03:05:12 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Fri, 07 Jan 2022 03:05:13 GMT
ENV RABBITMQ_VERSION=3.9.12
# Fri, 07 Jan 2022 03:05:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 07 Jan 2022 03:05:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 07 Jan 2022 03:05:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RABBITMQ_LOGS=-
# Fri, 07 Jan 2022 03:05:38 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Fri, 07 Jan 2022 03:05:39 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Fri, 07 Jan 2022 03:05:40 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Fri, 07 Jan 2022 03:05:41 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 07 Jan 2022 03:05:42 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 07 Jan 2022 03:05:43 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 07 Jan 2022 03:05:45 GMT
COPY --chown=rabbitmq:rabbitmqfile:2b942f4756de24f6094cd4bd8e85adc37054221a296429e1c867c9e0f4b5dba8 in /etc/rabbitmq/conf.d/ 
# Fri, 07 Jan 2022 03:05:46 GMT
COPY file:d7e54a3570407a262351dfa2e082aa1713b74883d564d1616d93787afcf4b8c0 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:05:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:05:47 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Fri, 07 Jan 2022 03:05:48 GMT
CMD ["rabbitmq-server"]
# Fri, 07 Jan 2022 03:06:17 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version
# Fri, 07 Jan 2022 03:06:17 GMT
EXPOSE 15671 15672
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248076cfac7c4575d978fca1d09ccaf38392b10cc4d239910c9b04ddb66ffef7`  
		Last Modified: Fri, 07 Jan 2022 03:08:32 GMT  
		Size: 699.0 KB (699034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4064e75cc0e5120f63a42a32aac87507b1561226d4ce5c90bc796791c74b68`  
		Last Modified: Fri, 07 Jan 2022 03:08:37 GMT  
		Size: 42.7 MB (42697093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818b9fdf6a838e24217b2095d0a504297c26130955b1b5c72b2c0f7807739a1`  
		Last Modified: Fri, 07 Jan 2022 03:08:31 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea846c04d0e36380879b09ca96045034b486fd7b7104c368720743812d0e4175`  
		Last Modified: Fri, 07 Jan 2022 03:08:31 GMT  
		Size: 16.8 MB (16791979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c489c3d853330e131f553ac251ac93199062a03c8b766e0d35f18d1135e0b7`  
		Last Modified: Fri, 07 Jan 2022 03:08:29 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23b8a5caf3cec30574cb5ed45e788f7624243b3ce47d2cff42d2945274a9132`  
		Last Modified: Fri, 07 Jan 2022 03:08:29 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985f12611006f4aecd433b83950da5839c66584817d6da7a28db58408de1b5ed`  
		Last Modified: Fri, 07 Jan 2022 03:08:29 GMT  
		Size: 442.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7620bfa2ffd754331fad02a296ad76bed5d4e92f216aa2be5a5b5fca64ebc3`  
		Last Modified: Fri, 07 Jan 2022 03:08:29 GMT  
		Size: 833.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552bd4a8fb90176cf4237aae87685662599b8813dfe06210375620c6d3ac5824`  
		Last Modified: Fri, 07 Jan 2022 03:08:57 GMT  
		Size: 11.6 MB (11609179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:management` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:a54f9c0975447d77b909417731aca7f53ff82c9f6cabcb60f80ddba95a407b86
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107767285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60339249e197e2c4d0760fb4df86f54743af987134166470743f78c3956e0e93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*; 	gosu nobody true
# Fri, 07 Jan 2022 03:57:20 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Fri, 07 Jan 2022 03:57:21 GMT
ENV OPENSSL_VERSION=1.1.1m
# Fri, 07 Jan 2022 03:57:22 GMT
ENV OPENSSL_SOURCE_SHA256=f89199be8b23ca45fc7cb9f1d8d3ee67312318286ad030f5316aca6462db6c96
# Fri, 07 Jan 2022 03:57:26 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Fri, 07 Jan 2022 03:57:29 GMT
ENV OTP_VERSION=24.2
# Fri, 07 Jan 2022 03:57:30 GMT
ENV OTP_SOURCE_SHA256=af0f1928dcd16cd5746feeca8325811865578bf1a110a443d353ea3e509e6d41
# Fri, 07 Jan 2022 04:02:53 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		autoconf 		ca-certificates 		dpkg-dev 		gcc 		g++ 		gnupg 		libncurses5-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum --check --strict -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	debMultiarch="$(dpkg-architecture --query DEB_HOST_MULTIARCH)"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		--libdir="lib/$debMultiarch" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	ldconfig; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --progress dot:giga --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum --check --strict -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; export CFLAGS; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Fri, 07 Jan 2022 04:02:58 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 07 Jan 2022 04:03:05 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Fri, 07 Jan 2022 04:03:06 GMT
ENV RABBITMQ_VERSION=3.9.12
# Fri, 07 Jan 2022 04:03:08 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 07 Jan 2022 04:03:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 07 Jan 2022 04:03:12 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RABBITMQ_LOGS=-
# Fri, 07 Jan 2022 04:04:26 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Fri, 07 Jan 2022 04:04:34 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Fri, 07 Jan 2022 04:04:39 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Fri, 07 Jan 2022 04:04:41 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 07 Jan 2022 04:04:44 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 07 Jan 2022 04:04:49 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 07 Jan 2022 04:04:51 GMT
COPY --chown=rabbitmq:rabbitmqfile:2b942f4756de24f6094cd4bd8e85adc37054221a296429e1c867c9e0f4b5dba8 in /etc/rabbitmq/conf.d/ 
# Fri, 07 Jan 2022 04:04:52 GMT
COPY file:d7e54a3570407a262351dfa2e082aa1713b74883d564d1616d93787afcf4b8c0 in /usr/local/bin/ 
# Fri, 07 Jan 2022 04:04:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 04:04:57 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Fri, 07 Jan 2022 04:04:59 GMT
CMD ["rabbitmq-server"]
# Fri, 07 Jan 2022 04:05:50 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version
# Fri, 07 Jan 2022 04:05:54 GMT
EXPOSE 15671 15672
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5ef770a5d3eac321151f101e2737cabeee58b3e0a9e16d48d6bfc84314de89`  
		Last Modified: Fri, 07 Jan 2022 04:10:07 GMT  
		Size: 822.2 KB (822243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9084b18ae20194dc749044ad5e7a29670625f1976b472aba6eb1fe8fc12652`  
		Last Modified: Fri, 07 Jan 2022 04:10:14 GMT  
		Size: 44.3 MB (44268892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a25f140f495516861df912b7e006ff923ba5770aa2cc2f1f598edd79fc98d97`  
		Last Modified: Fri, 07 Jan 2022 04:10:07 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f822e3b368cb984af36744212031abc9c97ddb208d23d4c4e20ac9b602ec53`  
		Last Modified: Fri, 07 Jan 2022 04:10:07 GMT  
		Size: 16.8 MB (16792878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb82f6ada94759dbe65e1f5bff613f2ed497b5a0c6755ae79dd979004600e2`  
		Last Modified: Fri, 07 Jan 2022 04:10:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663fd3368df42799cf3c71bcc34c2a533d555ad186fa698695b0f7a79ef3b01a`  
		Last Modified: Fri, 07 Jan 2022 04:10:04 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c0bf463bf444062c233f2533cedc1cf4ec62baf2b7e492d239f79eafe64520`  
		Last Modified: Fri, 07 Jan 2022 04:10:04 GMT  
		Size: 441.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958246cf608c58ec71849211dc0e46489e327a911490b85f8f98ddfd30c2c42`  
		Last Modified: Fri, 07 Jan 2022 04:10:04 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29930b8f38a433ade07a5490b0d0fcb8c9c9a162be434eedffab3bbce27e5aad`  
		Last Modified: Fri, 07 Jan 2022 04:10:37 GMT  
		Size: 12.6 MB (12592644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:management` - linux; riscv64

```console
$ docker pull rabbitmq@sha256:48bd3c6a853af44bfa0a45b4bbe7230963cdfea09e86e214baaf31af06bc8a40
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95218042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b48dc4b1544a58654b7eefafd35cb7e9c7490daff49fe1f85b05d13edc627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:16:06 GMT
ADD file:8c67f745313efae2d5d96d237357fdd8bd6ea54c3f198c07010bf1bce663d48c in / 
# Fri, 07 Jan 2022 02:16:08 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*; 	gosu nobody true
# Fri, 07 Jan 2022 04:09:56 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Fri, 07 Jan 2022 04:09:56 GMT
ENV OPENSSL_VERSION=1.1.1m
# Fri, 07 Jan 2022 04:09:57 GMT
ENV OPENSSL_SOURCE_SHA256=f89199be8b23ca45fc7cb9f1d8d3ee67312318286ad030f5316aca6462db6c96
# Fri, 07 Jan 2022 04:09:57 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Fri, 07 Jan 2022 04:09:58 GMT
ENV OTP_VERSION=24.2
# Fri, 07 Jan 2022 04:09:58 GMT
ENV OTP_SOURCE_SHA256=af0f1928dcd16cd5746feeca8325811865578bf1a110a443d353ea3e509e6d41
# Fri, 07 Jan 2022 04:36:23 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		autoconf 		ca-certificates 		dpkg-dev 		gcc 		g++ 		gnupg 		libncurses5-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum --check --strict -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	debMultiarch="$(dpkg-architecture --query DEB_HOST_MULTIARCH)"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		--libdir="lib/$debMultiarch" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	ldconfig; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --progress dot:giga --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum --check --strict -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; export CFLAGS; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Fri, 07 Jan 2022 04:36:24 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 07 Jan 2022 04:36:27 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Fri, 07 Jan 2022 04:36:27 GMT
ENV RABBITMQ_VERSION=3.9.12
# Fri, 07 Jan 2022 04:36:28 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 07 Jan 2022 04:36:28 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 07 Jan 2022 04:36:29 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RABBITMQ_LOGS=-
# Fri, 07 Jan 2022 04:38:05 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Fri, 07 Jan 2022 04:38:15 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Fri, 07 Jan 2022 04:38:18 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Fri, 07 Jan 2022 04:38:18 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 07 Jan 2022 04:38:19 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 07 Jan 2022 04:38:19 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 07 Jan 2022 04:38:20 GMT
COPY --chown=rabbitmq:rabbitmqfile:2b942f4756de24f6094cd4bd8e85adc37054221a296429e1c867c9e0f4b5dba8 in /etc/rabbitmq/conf.d/ 
# Fri, 07 Jan 2022 04:38:21 GMT
COPY file:d7e54a3570407a262351dfa2e082aa1713b74883d564d1616d93787afcf4b8c0 in /usr/local/bin/ 
# Fri, 07 Jan 2022 04:38:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 04:38:22 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Fri, 07 Jan 2022 04:38:22 GMT
CMD ["rabbitmq-server"]
# Fri, 07 Jan 2022 04:41:25 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version
# Fri, 07 Jan 2022 04:41:26 GMT
EXPOSE 15671 15672
```

-	Layers:
	-	`sha256:8c703baf60b6c639070fea2dcfc339570983cdb4555d172e28f82e765410e364`  
		Last Modified: Fri, 07 Jan 2022 02:34:37 GMT  
		Size: 24.2 MB (24226982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e26f8dbae331e177c25ff11d88ec25fc4cf830481be14bfb097d4346b52580`  
		Last Modified: Fri, 07 Jan 2022 04:57:53 GMT  
		Size: 931.6 KB (931650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854f4a5816a569f84457fd9b8af8b54fbe29a82abcd6c7b13bee59590722826b`  
		Last Modified: Fri, 07 Jan 2022 04:58:43 GMT  
		Size: 43.0 MB (43044023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9de099141ea0dcf147495a67f1012fd2efabf8de23141ac526ec57a62f97fa`  
		Last Modified: Fri, 07 Jan 2022 04:57:52 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4021d10bbb20aa7cb306e96684401dbd71b1e1b7bf21dd2dae90b63553f0a2cf`  
		Last Modified: Fri, 07 Jan 2022 04:58:04 GMT  
		Size: 16.8 MB (16793390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b12329d20e6979faeb8e28e195bae74204d94892522c24a8a03b38b699fc49`  
		Last Modified: Fri, 07 Jan 2022 04:57:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330f6a2fba9afbb2dbb53caeb1010caa0fd00e2f01e467c5a130f95a193ecce0`  
		Last Modified: Fri, 07 Jan 2022 04:57:49 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e80d1c4c0253e69c132d904a868a0b9b3448b7846f76bf079468611d76c1454`  
		Last Modified: Fri, 07 Jan 2022 04:57:49 GMT  
		Size: 442.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1afe0eb4765babcf7e8308c389737a45bdcf26b241a935d3d2bd0c35d9b1928`  
		Last Modified: Fri, 07 Jan 2022 04:57:49 GMT  
		Size: 837.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a526ae81664d19f1bdb2879138e50901c741d5a6464ae8f21790de4da2309ca3`  
		Last Modified: Fri, 07 Jan 2022 05:01:02 GMT  
		Size: 10.2 MB (10218349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:management` - linux; s390x

```console
$ docker pull rabbitmq@sha256:baf4449dae4fe0c2a317ea167dfd0a73cce33f123e2390099d8f5fe3d5395e00
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98233291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4984659cbbb51336beb37416fa0cb7084a3610a10ede0b6b9ef9c4afa1effa4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/*; 	gosu nobody true
# Fri, 07 Jan 2022 02:40:27 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Fri, 07 Jan 2022 02:40:28 GMT
ENV OPENSSL_VERSION=1.1.1m
# Fri, 07 Jan 2022 02:40:28 GMT
ENV OPENSSL_SOURCE_SHA256=f89199be8b23ca45fc7cb9f1d8d3ee67312318286ad030f5316aca6462db6c96
# Fri, 07 Jan 2022 02:40:28 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Fri, 07 Jan 2022 02:40:28 GMT
ENV OTP_VERSION=24.2
# Fri, 07 Jan 2022 02:40:28 GMT
ENV OTP_SOURCE_SHA256=af0f1928dcd16cd5746feeca8325811865578bf1a110a443d353ea3e509e6d41
# Fri, 07 Jan 2022 02:42:43 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		autoconf 		ca-certificates 		dpkg-dev 		gcc 		g++ 		gnupg 		libncurses5-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum --check --strict -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	debMultiarch="$(dpkg-architecture --query DEB_HOST_MULTIARCH)"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		--libdir="lib/$debMultiarch" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	ldconfig; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --progress dot:giga --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum --check --strict -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; export CFLAGS; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Fri, 07 Jan 2022 02:42:44 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 07 Jan 2022 02:42:45 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Fri, 07 Jan 2022 02:42:45 GMT
ENV RABBITMQ_VERSION=3.9.12
# Fri, 07 Jan 2022 02:42:45 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 07 Jan 2022 02:42:45 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 07 Jan 2022 02:42:45 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RABBITMQ_LOGS=-
# Fri, 07 Jan 2022 02:43:00 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Fri, 07 Jan 2022 02:43:02 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Fri, 07 Jan 2022 02:43:02 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Fri, 07 Jan 2022 02:43:02 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 07 Jan 2022 02:43:02 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 07 Jan 2022 02:43:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 07 Jan 2022 02:43:03 GMT
COPY --chown=rabbitmq:rabbitmqfile:2b942f4756de24f6094cd4bd8e85adc37054221a296429e1c867c9e0f4b5dba8 in /etc/rabbitmq/conf.d/ 
# Fri, 07 Jan 2022 02:43:03 GMT
COPY file:d7e54a3570407a262351dfa2e082aa1713b74883d564d1616d93787afcf4b8c0 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:43:03 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Fri, 07 Jan 2022 02:43:03 GMT
CMD ["rabbitmq-server"]
# Fri, 07 Jan 2022 02:43:21 GMT
RUN set eux; 	rabbitmq-plugins enable --offline rabbitmq_management; 	rm -f /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	cp /plugins/rabbitmq_management-*/priv/www/cli/rabbitmqadmin /usr/local/bin/rabbitmqadmin; 	[ -s /usr/local/bin/rabbitmqadmin ]; 	chmod +x /usr/local/bin/rabbitmqadmin; 	apt-get update; 	apt-get install -y --no-install-recommends python3; 	rm -rf /var/lib/apt/lists/*; 	rabbitmqadmin --version
# Fri, 07 Jan 2022 02:43:22 GMT
EXPOSE 15671 15672
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea125c9093dd5866ad65d4d638e53a84ac6bd937ec48e65f1a0b1993ece6e20`  
		Last Modified: Fri, 07 Jan 2022 02:45:21 GMT  
		Size: 861.6 KB (861575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df26b8a5ddcd79cfde80c07cc41e3a89532fd70f370385ff1d56172514fb5d7`  
		Last Modified: Fri, 07 Jan 2022 02:45:26 GMT  
		Size: 42.2 MB (42192914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daac3b28a74174c5852dfa29b70174e15950e398eaf17f15057fa3d72c861f38`  
		Last Modified: Fri, 07 Jan 2022 02:45:21 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee7a15d1177df5d0029ebad6c62e768109a2539a9e0851b06484f4c2e5362f9`  
		Last Modified: Fri, 07 Jan 2022 02:45:21 GMT  
		Size: 16.8 MB (16791512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e027406ffad2db95eb245d83ccc4a6e97ed1ba48cc8b3c7a165b9ad5e76a2d9e`  
		Last Modified: Fri, 07 Jan 2022 02:45:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1bbe5969c6d8c127542d623d33198db73384869e89671cdf76c618967ae467`  
		Last Modified: Fri, 07 Jan 2022 02:45:19 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504d1c2a73702eb3fe153f09261295975d112f3a17b10fdaf5a9de9f03a1ff12`  
		Last Modified: Fri, 07 Jan 2022 02:45:19 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facda8920abbd105a508ab6b919a0cd333427789a1b820e97bdd68acabb74240`  
		Last Modified: Fri, 07 Jan 2022 02:45:19 GMT  
		Size: 833.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea489cccc654fbfcd77728e918d2a0d983730a0461969f920148136191d1b841`  
		Last Modified: Fri, 07 Jan 2022 02:45:38 GMT  
		Size: 11.3 MB (11262555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
