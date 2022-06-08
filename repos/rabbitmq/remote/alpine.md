## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:5cbb3d0bffdbcd163c5c997e2ae777b70619accd7847c5770e00f500923926c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:9dc905f9515d8192f5a2bdaa6786d961c08bb498b6fed17deb2dca1c0aa8f2c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67648382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175a090938663edc213b681dbfaeb819adc88693c07e62790c531b591cfd17c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 21:58:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		bash 		procps
# Wed, 25 May 2022 21:58:13 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Wed, 25 May 2022 21:58:13 GMT
ENV OPENSSL_VERSION=1.1.1o
# Wed, 25 May 2022 21:58:13 GMT
ENV OPENSSL_SOURCE_SHA256=9384a2b0570dd80358841464677115df785edb941c71211f75076d72fe6b438f
# Wed, 25 May 2022 21:58:13 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Wed, 08 Jun 2022 18:52:36 GMT
ENV OTP_VERSION=24.3.4.1
# Wed, 08 Jun 2022 18:52:36 GMT
ENV OTP_SOURCE_SHA256=f5c502dfab713a83f73eabf79fb6d83ac85d53386a571f55c2297e165a8145de
# Wed, 08 Jun 2022 18:55:19 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		dpkg-dev dpkg 		g++ 		gcc 		gnupg 		libc-dev 		linux-headers 		make 		ncurses-dev 	; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		mkdir /usr/local/src; 		wget --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum -c -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum -c -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	export CFLAGS='-g -O2'; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 	apk del --no-network .build-deps; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Wed, 08 Jun 2022 18:55:19 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 08 Jun 2022 18:55:20 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Wed, 08 Jun 2022 18:55:20 GMT
ENV RABBITMQ_VERSION=3.10.5
# Wed, 08 Jun 2022 18:55:20 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 08 Jun 2022 18:55:20 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 08 Jun 2022 18:55:20 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 18:55:28 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Wed, 08 Jun 2022 18:55:30 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Wed, 08 Jun 2022 18:55:31 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Wed, 08 Jun 2022 18:55:31 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 08 Jun 2022 18:55:31 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 08 Jun 2022 18:55:31 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 08 Jun 2022 18:55:31 GMT
COPY --chown=rabbitmq:rabbitmqfile:1010d75e6e011d4f35a78624739f459bbc98829ae9696991358350d1bd6a12ac in /etc/rabbitmq/conf.d/ 
# Wed, 08 Jun 2022 18:55:31 GMT
COPY file:0667537cb067f2e42e0e1d5c1def14391eaf4bfe791bc7f23fd95a83eff81025 in /usr/local/bin/ 
# Wed, 08 Jun 2022 18:55:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Jun 2022 18:55:31 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Wed, 08 Jun 2022 18:55:31 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e9c1b278dc7da8fb7f38b20166c9ad9e2693ec5dfeea9b3dcb73a98b66d5fa`  
		Last Modified: Wed, 25 May 2022 22:02:59 GMT  
		Size: 1.1 MB (1053733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ceecb7d73a36031d324359c3a0facc616689714779ceee9b3ae6a4ed5c74cd`  
		Last Modified: Wed, 08 Jun 2022 18:59:13 GMT  
		Size: 47.0 MB (46951374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7979ecf45fb2f998ea2504692e2ee309caa8cee04b7653c8d0bc032381cb79b`  
		Last Modified: Wed, 08 Jun 2022 18:59:07 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31ca819b707c53cf2dcd236719f38ac2a02a0df442f9bc83fd9ec7ae87372c8`  
		Last Modified: Wed, 08 Jun 2022 18:59:06 GMT  
		Size: 16.8 MB (16841175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e28856ad8da74563c5903266cf901fd67924a94fd9724c177f718f6346dc9c`  
		Last Modified: Wed, 08 Jun 2022 18:59:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c878cb08dcf62e178cdda6cd6721f90547ed7a29dbc19e5ec9e4abc26e295b97`  
		Last Modified: Wed, 08 Jun 2022 18:59:05 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c566278dd7f15cc8ef9ae0c5cccfced52e0e92adb1c638f378001d729e544f81`  
		Last Modified: Wed, 08 Jun 2022 18:59:05 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f286425086d3c854a254df640c84303ed2c66a2c724025544afd76afb2b5536`  
		Last Modified: Wed, 08 Jun 2022 18:59:05 GMT  
		Size: 836.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:718ea00adcf7e26a8343644b5949a552901486fc720a54ebafca42993f5ff6cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59029002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7161adc846eb983ffea82aa4371186365363d56953fa936ec5b485fdf5966c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 May 2022 19:49:32 GMT
ADD file:f7cee617575b5e5a7672d298a519bb8d8b5098efb90aa2a5d7b0510003457d52 in / 
# Mon, 23 May 2022 19:49:33 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 23:37:51 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		bash 		procps
# Wed, 25 May 2022 23:37:51 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Wed, 25 May 2022 23:37:51 GMT
ENV OPENSSL_VERSION=1.1.1o
# Wed, 25 May 2022 23:37:52 GMT
ENV OPENSSL_SOURCE_SHA256=9384a2b0570dd80358841464677115df785edb941c71211f75076d72fe6b438f
# Wed, 25 May 2022 23:37:52 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Wed, 08 Jun 2022 18:55:49 GMT
ENV OTP_VERSION=24.3.4.1
# Wed, 08 Jun 2022 18:55:50 GMT
ENV OTP_SOURCE_SHA256=f5c502dfab713a83f73eabf79fb6d83ac85d53386a571f55c2297e165a8145de
# Wed, 08 Jun 2022 19:00:04 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		dpkg-dev dpkg 		g++ 		gcc 		gnupg 		libc-dev 		linux-headers 		make 		ncurses-dev 	; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		mkdir /usr/local/src; 		wget --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum -c -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum -c -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	export CFLAGS='-g -O2'; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 	apk del --no-network .build-deps; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Wed, 08 Jun 2022 19:00:05 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 08 Jun 2022 19:00:07 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Wed, 08 Jun 2022 19:00:07 GMT
ENV RABBITMQ_VERSION=3.10.5
# Wed, 08 Jun 2022 19:00:08 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 08 Jun 2022 19:00:08 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 08 Jun 2022 19:00:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 19:00:34 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Wed, 08 Jun 2022 19:00:40 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Wed, 08 Jun 2022 19:00:41 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Wed, 08 Jun 2022 19:00:42 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 08 Jun 2022 19:00:42 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 08 Jun 2022 19:00:42 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 08 Jun 2022 19:00:43 GMT
COPY --chown=rabbitmq:rabbitmqfile:1010d75e6e011d4f35a78624739f459bbc98829ae9696991358350d1bd6a12ac in /etc/rabbitmq/conf.d/ 
# Wed, 08 Jun 2022 19:00:43 GMT
COPY file:0667537cb067f2e42e0e1d5c1def14391eaf4bfe791bc7f23fd95a83eff81025 in /usr/local/bin/ 
# Wed, 08 Jun 2022 19:00:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Jun 2022 19:00:44 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Wed, 08 Jun 2022 19:00:45 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:79a25ccaf940855872635c06e7614d9b27dd38ffb5a8adfdb9274dfdc0ea0d87`  
		Last Modified: Mon, 23 May 2022 19:08:47 GMT  
		Size: 2.6 MB (2606142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9427f3a70802471f61f062a8efd9d91c6de6f2d38daf6a77b1b8a05ef3355ff0`  
		Last Modified: Wed, 25 May 2022 23:47:09 GMT  
		Size: 1.0 MB (1009314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4001552052abec6d05cab1edb4798105984433c6e61fdbb036be7f24a0ac8e`  
		Last Modified: Wed, 08 Jun 2022 19:05:29 GMT  
		Size: 38.6 MB (38570027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c420c16c7d901b8f03551dd31b23aafaa28dc9b6d986c7d55981c92838075682`  
		Last Modified: Wed, 08 Jun 2022 19:05:11 GMT  
		Size: 1.5 KB (1486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643affbf2f78a7bdf9ea02ac4a3a15f8904f845c17236ac0225ba828ca9c6694`  
		Last Modified: Wed, 08 Jun 2022 19:05:15 GMT  
		Size: 16.8 MB (16840314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4304dcf2e5a5d289c65bb9b2c78f1b50e821f1a873a5043dd8ad0040e916e8d0`  
		Last Modified: Wed, 08 Jun 2022 19:05:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63474764afb9b8018e3124a96dcdee844d51d57f71cc7092db36349af4cd4ff`  
		Last Modified: Wed, 08 Jun 2022 19:05:09 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca258f81e3f65bf417fa0bea03d733f38b4ede1a5797e54d2672dbb4110def3d`  
		Last Modified: Wed, 08 Jun 2022 19:05:09 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad928d395b80bd252031ed8868d235da51960fba8747eb48f5a6cee5a8a0ca4d`  
		Last Modified: Wed, 08 Jun 2022 19:05:09 GMT  
		Size: 833.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:9c08ac5afe33a4398a4653a4b5a1f9bde340feb7ca7bbeef8ee182c69773892d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58322220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e711e90c74c02448dc89a160327e3670d9778f57a6fadbe9ef7aa9f4eee458b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 May 2022 18:57:46 GMT
ADD file:72698cc08524b911ebaacf992490707e5a951ddd2fe6edb3fb598e9dc7155049 in / 
# Mon, 23 May 2022 18:57:47 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 01:21:57 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		bash 		procps
# Thu, 26 May 2022 01:21:58 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Thu, 26 May 2022 01:21:58 GMT
ENV OPENSSL_VERSION=1.1.1o
# Thu, 26 May 2022 01:21:58 GMT
ENV OPENSSL_SOURCE_SHA256=9384a2b0570dd80358841464677115df785edb941c71211f75076d72fe6b438f
# Thu, 26 May 2022 01:21:59 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Thu, 26 May 2022 01:21:59 GMT
ENV OTP_VERSION=24.3.4
# Thu, 26 May 2022 01:22:00 GMT
ENV OTP_SOURCE_SHA256=76fcca5ba6f11eb9caac32bf053badc46b5d66f867150eef077f4f0d7944ecd7
# Thu, 26 May 2022 01:26:03 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		dpkg-dev dpkg 		g++ 		gcc 		gnupg 		libc-dev 		linux-headers 		make 		ncurses-dev 	; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		mkdir /usr/local/src; 		wget --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum -c -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum -c -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	export CFLAGS='-g -O2'; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 	apk del --no-network .build-deps; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Thu, 26 May 2022 01:26:04 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 26 May 2022 01:26:06 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Fri, 03 Jun 2022 00:26:07 GMT
ENV RABBITMQ_VERSION=3.10.5
# Fri, 03 Jun 2022 00:26:07 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 03 Jun 2022 00:26:07 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 03 Jun 2022 00:26:08 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jun 2022 00:26:25 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Fri, 03 Jun 2022 00:26:30 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Fri, 03 Jun 2022 00:26:31 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Fri, 03 Jun 2022 00:26:31 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 03 Jun 2022 00:26:32 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 03 Jun 2022 00:26:32 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 03 Jun 2022 00:26:33 GMT
COPY --chown=rabbitmq:rabbitmqfile:1010d75e6e011d4f35a78624739f459bbc98829ae9696991358350d1bd6a12ac in /etc/rabbitmq/conf.d/ 
# Fri, 03 Jun 2022 00:26:33 GMT
COPY file:0667537cb067f2e42e0e1d5c1def14391eaf4bfe791bc7f23fd95a83eff81025 in /usr/local/bin/ 
# Fri, 03 Jun 2022 00:26:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Jun 2022 00:26:34 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Fri, 03 Jun 2022 00:26:34 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:6366ba92f08e2418e90171f1e34bd86ecd50fdc95953b3f33b8943c143518eca`  
		Last Modified: Mon, 23 May 2022 18:59:17 GMT  
		Size: 2.4 MB (2411648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0275d8669ccf8e2e20a5edbe9bd4001de952c3b299028326f97ae970797e3c`  
		Last Modified: Thu, 26 May 2022 01:32:17 GMT  
		Size: 920.6 KB (920608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ac179f79cfd4ba8a0a4d1ce7281a50758279c0ade68f07a44f0073777f96ed`  
		Last Modified: Thu, 26 May 2022 01:32:35 GMT  
		Size: 38.1 MB (38146517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d066bacc38b3aa54dea13c2514820bf819a92b1a2a5e606bfc0b562a0baa40de`  
		Last Modified: Thu, 26 May 2022 01:32:17 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cda32d69e7b447191412e606d4dc49e059af70517b554f213bfec56b81a723`  
		Last Modified: Fri, 03 Jun 2022 00:36:03 GMT  
		Size: 16.8 MB (16840234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc6cd24d67e948e8b548e9a75d4d56576be72c1751d265787180aa61218041f`  
		Last Modified: Fri, 03 Jun 2022 00:35:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b8a95503e5524a9a6d3a69fa2d0734db1ff73a7d7370841d6c0f167ecb3565`  
		Last Modified: Fri, 03 Jun 2022 00:35:56 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b440772441fc3ccadf570751c1e566b7d95b512e3bdabcd14a0ecbe815ad0e7`  
		Last Modified: Fri, 03 Jun 2022 00:35:56 GMT  
		Size: 502.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54c14491932fab24760bb91a664fb97022e327a2aad2e29576d267993b479da`  
		Last Modified: Fri, 03 Jun 2022 00:35:57 GMT  
		Size: 838.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:552f7a49845050385e35f55f4019f38ab11375957b4d319f84a3ca9fa4afd94a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59895755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d13579ce26e3074a0372766974d0f98d9a767fc8ede17093ccac5dee39d9872`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 23:31:29 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		bash 		procps
# Wed, 25 May 2022 23:31:29 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Wed, 25 May 2022 23:31:30 GMT
ENV OPENSSL_VERSION=1.1.1o
# Wed, 25 May 2022 23:31:31 GMT
ENV OPENSSL_SOURCE_SHA256=9384a2b0570dd80358841464677115df785edb941c71211f75076d72fe6b438f
# Wed, 25 May 2022 23:31:32 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Wed, 08 Jun 2022 18:59:36 GMT
ENV OTP_VERSION=24.3.4.1
# Wed, 08 Jun 2022 18:59:37 GMT
ENV OTP_SOURCE_SHA256=f5c502dfab713a83f73eabf79fb6d83ac85d53386a571f55c2297e165a8145de
# Wed, 08 Jun 2022 19:02:12 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		dpkg-dev dpkg 		g++ 		gcc 		gnupg 		libc-dev 		linux-headers 		make 		ncurses-dev 	; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		mkdir /usr/local/src; 		wget --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum -c -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum -c -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	export CFLAGS='-g -O2'; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 	apk del --no-network .build-deps; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Wed, 08 Jun 2022 19:02:13 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 08 Jun 2022 19:02:14 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Wed, 08 Jun 2022 19:02:15 GMT
ENV RABBITMQ_VERSION=3.10.5
# Wed, 08 Jun 2022 19:02:16 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 08 Jun 2022 19:02:17 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 08 Jun 2022 19:02:18 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 19:02:25 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Wed, 08 Jun 2022 19:02:27 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Wed, 08 Jun 2022 19:02:28 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Wed, 08 Jun 2022 19:02:29 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 08 Jun 2022 19:02:30 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 08 Jun 2022 19:02:31 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 08 Jun 2022 19:02:33 GMT
COPY --chown=rabbitmq:rabbitmqfile:1010d75e6e011d4f35a78624739f459bbc98829ae9696991358350d1bd6a12ac in /etc/rabbitmq/conf.d/ 
# Wed, 08 Jun 2022 19:02:34 GMT
COPY file:0667537cb067f2e42e0e1d5c1def14391eaf4bfe791bc7f23fd95a83eff81025 in /usr/local/bin/ 
# Wed, 08 Jun 2022 19:02:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Jun 2022 19:02:35 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Wed, 08 Jun 2022 19:02:36 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cf3ff4d16125cf33e94ad3c00ac687c62d5b81dece608da4ebe05aa756715d`  
		Last Modified: Wed, 25 May 2022 23:39:48 GMT  
		Size: 1.1 MB (1078745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0bf26627f5eba93ef7526894ba8fd26b323937010c015affa4e5346988abd2`  
		Last Modified: Wed, 08 Jun 2022 19:08:09 GMT  
		Size: 39.3 MB (39279392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e0b8db2386baae8410d82ce64a24339129dad8c0e7e9a66120247a5784531b`  
		Last Modified: Wed, 08 Jun 2022 19:08:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134f74233774b559552f0ccb01bde8f1e9fbedb3684b35a3802cc9b0b3203c5b`  
		Last Modified: Wed, 08 Jun 2022 19:08:03 GMT  
		Size: 16.8 MB (16840019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05678c8a1b19e5fb466c01d6a37862eb7b72318dc36f01b0e54f3568085c85d`  
		Last Modified: Wed, 08 Jun 2022 19:08:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a2e4b487280e175ea86a2d6fbd1923493ce9789d046fb56678f47aefd17b5c`  
		Last Modified: Wed, 08 Jun 2022 19:08:01 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53df09aaaa00178d090119d3d37b6de3ae1add23aa9be681e13233b95b8cfc8`  
		Last Modified: Wed, 08 Jun 2022 19:08:02 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c7f153e611fdaf21caf73d945557c04301ef34ac9d40ef0074801ed0d67c24`  
		Last Modified: Wed, 08 Jun 2022 19:08:02 GMT  
		Size: 833.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:0638063ff3bdfb0a7ae60a8360886d412f2df49cec660f71b47d0270e69f5e96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60562500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3a349b78afdbf958ce29e063d640c4ec79a5998df89be23ea9fef7979f9863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 May 2022 19:38:20 GMT
ADD file:1750ccfabfe93636015070d51a6e824cbd738056223421c69d8aaabc38041b18 in / 
# Mon, 23 May 2022 19:38:20 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 22:04:24 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		bash 		procps
# Wed, 25 May 2022 22:04:25 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Wed, 25 May 2022 22:04:26 GMT
ENV OPENSSL_VERSION=1.1.1o
# Wed, 25 May 2022 22:04:27 GMT
ENV OPENSSL_SOURCE_SHA256=9384a2b0570dd80358841464677115df785edb941c71211f75076d72fe6b438f
# Wed, 25 May 2022 22:04:28 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Wed, 08 Jun 2022 18:50:48 GMT
ENV OTP_VERSION=24.3.4.1
# Wed, 08 Jun 2022 18:50:49 GMT
ENV OTP_SOURCE_SHA256=f5c502dfab713a83f73eabf79fb6d83ac85d53386a571f55c2297e165a8145de
# Wed, 08 Jun 2022 18:53:29 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		dpkg-dev dpkg 		g++ 		gcc 		gnupg 		libc-dev 		linux-headers 		make 		ncurses-dev 	; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		mkdir /usr/local/src; 		wget --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum -c -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum -c -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	export CFLAGS='-g -O2'; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 	apk del --no-network .build-deps; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Wed, 08 Jun 2022 18:53:29 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 08 Jun 2022 18:53:30 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Wed, 08 Jun 2022 18:53:31 GMT
ENV RABBITMQ_VERSION=3.10.5
# Wed, 08 Jun 2022 18:53:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 08 Jun 2022 18:53:33 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 08 Jun 2022 18:53:34 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 18:53:43 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Wed, 08 Jun 2022 18:53:44 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Wed, 08 Jun 2022 18:53:45 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Wed, 08 Jun 2022 18:53:46 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 08 Jun 2022 18:53:47 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 08 Jun 2022 18:53:48 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 08 Jun 2022 18:53:50 GMT
COPY --chown=rabbitmq:rabbitmqfile:1010d75e6e011d4f35a78624739f459bbc98829ae9696991358350d1bd6a12ac in /etc/rabbitmq/conf.d/ 
# Wed, 08 Jun 2022 18:53:51 GMT
COPY file:0667537cb067f2e42e0e1d5c1def14391eaf4bfe791bc7f23fd95a83eff81025 in /usr/local/bin/ 
# Wed, 08 Jun 2022 18:53:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Jun 2022 18:53:52 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Wed, 08 Jun 2022 18:53:53 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:bb638a3869eed698f88775c7a48f36f8e22e7c6bbaa98fa1d5678966b619b859`  
		Last Modified: Mon, 23 May 2022 19:09:25 GMT  
		Size: 2.8 MB (2801887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603a81f33b481e5dbd0cf309172cc60e91179f774688a6526b01a2122187c693`  
		Last Modified: Wed, 25 May 2022 22:10:10 GMT  
		Size: 1.1 MB (1108703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e09dc3ea2c4709f3362e6a6fd3e8712e25c3fc22176ae3c92910c4cc8556b8a`  
		Last Modified: Wed, 08 Jun 2022 18:56:10 GMT  
		Size: 39.8 MB (39808792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c952547b895245f174955fea2a7ca1d56c0e780788d9244f64814b301a7479c`  
		Last Modified: Wed, 08 Jun 2022 18:56:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19f8af97b7145047b90b2314c6981b03860e169c51437792de91296e4acf6d8`  
		Last Modified: Wed, 08 Jun 2022 18:56:03 GMT  
		Size: 16.8 MB (16839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49b99ef61e1d37498ef42fab136d2cedcafe450aba6482f3263096d94e45f3e`  
		Last Modified: Wed, 08 Jun 2022 18:56:00 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6178b43a2db2223ce77e20f02a1227e156ecbaef1a64d74f507c039b5338571b`  
		Last Modified: Wed, 08 Jun 2022 18:56:00 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68596cd838ecefc6000733b2efdb2d2d55b7e4d58017ea488321e28eb6cc1e9`  
		Last Modified: Wed, 08 Jun 2022 18:56:00 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195c855b0c2a0f5c27159d06eee65550e9507eb7734e1ac204186f0e47a0d12d`  
		Last Modified: Wed, 08 Jun 2022 18:56:00 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:d77b0833e3669fbc339388262e7df1e09c4a5bd05095c1b1ab9d3dd79397286f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60918160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dded4819fc93ca16e047e9049f675fa4083fb26af869d92f18e04005a9e975`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 May 2022 19:16:51 GMT
ADD file:6a5450c8a7cee3ceda59e7cb350c54df4139b0f7b7cf49c8b31bb9c01646c3cd in / 
# Mon, 23 May 2022 19:16:53 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 00:02:27 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		bash 		procps
# Thu, 26 May 2022 00:02:36 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Thu, 26 May 2022 00:02:40 GMT
ENV OPENSSL_VERSION=1.1.1o
# Thu, 26 May 2022 00:02:46 GMT
ENV OPENSSL_SOURCE_SHA256=9384a2b0570dd80358841464677115df785edb941c71211f75076d72fe6b438f
# Thu, 26 May 2022 00:02:56 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Thu, 26 May 2022 00:03:05 GMT
ENV OTP_VERSION=24.3.4
# Thu, 26 May 2022 00:03:12 GMT
ENV OTP_SOURCE_SHA256=76fcca5ba6f11eb9caac32bf053badc46b5d66f867150eef077f4f0d7944ecd7
# Thu, 26 May 2022 00:06:57 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		dpkg-dev dpkg 		g++ 		gcc 		gnupg 		libc-dev 		linux-headers 		make 		ncurses-dev 	; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		mkdir /usr/local/src; 		wget --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum -c -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum -c -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	export CFLAGS='-g -O2'; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 	apk del --no-network .build-deps; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Thu, 26 May 2022 00:07:05 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 26 May 2022 00:07:16 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Thu, 02 Jun 2022 22:39:11 GMT
ENV RABBITMQ_VERSION=3.10.5
# Thu, 02 Jun 2022 22:39:13 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 02 Jun 2022 22:39:15 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 02 Jun 2022 22:39:16 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Jun 2022 22:39:35 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Thu, 02 Jun 2022 22:39:41 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Thu, 02 Jun 2022 22:39:47 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Thu, 02 Jun 2022 22:39:48 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 02 Jun 2022 22:39:50 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 02 Jun 2022 22:39:53 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 02 Jun 2022 22:39:54 GMT
COPY --chown=rabbitmq:rabbitmqfile:1010d75e6e011d4f35a78624739f459bbc98829ae9696991358350d1bd6a12ac in /etc/rabbitmq/conf.d/ 
# Thu, 02 Jun 2022 22:39:55 GMT
COPY file:0667537cb067f2e42e0e1d5c1def14391eaf4bfe791bc7f23fd95a83eff81025 in /usr/local/bin/ 
# Thu, 02 Jun 2022 22:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Jun 2022 22:39:58 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Thu, 02 Jun 2022 22:39:59 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:d3deabf2a506ef6f5fa7c2a68bf27047574cef9908b30a97ff2d01ae539b089a`  
		Last Modified: Mon, 23 May 2022 19:09:13 GMT  
		Size: 2.8 MB (2789745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3751639409b417c4afb9085a495323144fd242e88c176b859eb6e068ee06d6`  
		Last Modified: Thu, 26 May 2022 00:17:06 GMT  
		Size: 1.2 MB (1180435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9a2ffec7163739473cacc8f6c748f238544bc573aeb2a52f733267719b7bc4`  
		Last Modified: Thu, 26 May 2022 00:17:11 GMT  
		Size: 40.1 MB (40104511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fb0fd9aadd34d00689d38bcd47f8736155ec34179b6dba4132a6da6ad4271c`  
		Last Modified: Thu, 26 May 2022 00:17:05 GMT  
		Size: 1.5 KB (1492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6014356610a6536920aaa6e62476777fc856fa8260843c757b62170ea465f4a0`  
		Last Modified: Thu, 02 Jun 2022 22:51:15 GMT  
		Size: 16.8 MB (16840254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e028f2729de6f30a2a622e1766fcf92eb3a8faf94f81a7b4b5163ef80604f8cd`  
		Last Modified: Thu, 02 Jun 2022 22:51:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fcc90b6e536dbc1664bc389ae8ef53003f91cedad1875fccffeb0ac08f1b061`  
		Last Modified: Thu, 02 Jun 2022 22:51:13 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8baf275d1a017e9c8a8aede736f259eabf4c272cba542ca89debbc7c40d5fa`  
		Last Modified: Thu, 02 Jun 2022 22:51:13 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aafa9287358604082251f792fd9f41a59c04075622dc59459eff92502b42b59`  
		Last Modified: Thu, 02 Jun 2022 22:51:13 GMT  
		Size: 837.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:6ad45730dc78f2a97fdb7617fc9dbd9b8275cf2579045f3fdb1dc5a2d14a4021
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59093786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d876daf806ff7f1b340b5b1f7424213f4a6fbcee0f42ef17dd3676a3450c0e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 23 May 2022 19:41:59 GMT
ADD file:e1852d8ef555a0d3ef6d0b74a898720c82bb9f491430b06a0dd0499497ce118e in / 
# Mon, 23 May 2022 19:42:10 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 23:14:41 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		bash 		procps
# Wed, 25 May 2022 23:14:41 GMT
ARG PGP_KEYSERVER=keyserver.ubuntu.com
# Wed, 25 May 2022 23:14:42 GMT
ENV OPENSSL_VERSION=1.1.1o
# Wed, 25 May 2022 23:14:42 GMT
ENV OPENSSL_SOURCE_SHA256=9384a2b0570dd80358841464677115df785edb941c71211f75076d72fe6b438f
# Wed, 25 May 2022 23:14:43 GMT
ENV OPENSSL_PGP_KEY_IDS=0x8657ABB260F056B1E5190839D9C4D26D0E604491 0x5B2545DAB21995F4088CEFAA36CEE4DEB00CFE33 0xED230BEC4D4F2518B9D7DF41F0DB4D21C1D35231 0xC1F33DD8CE1D4CC613AF14DA9195C48241FBF7DD 0x7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C 0xE5E52560DD91C556DDBDA5D02064C53641C25E5D
# Wed, 08 Jun 2022 18:55:28 GMT
ENV OTP_VERSION=24.3.4.1
# Wed, 08 Jun 2022 18:55:29 GMT
ENV OTP_SOURCE_SHA256=f5c502dfab713a83f73eabf79fb6d83ac85d53386a571f55c2297e165a8145de
# Wed, 08 Jun 2022 18:58:50 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		dpkg-dev dpkg 		g++ 		gcc 		gnupg 		libc-dev 		linux-headers 		make 		ncurses-dev 	; 		OPENSSL_SOURCE_URL="https://www.openssl.org/source/openssl-$OPENSSL_VERSION.tar.gz"; 	OPENSSL_PATH="/usr/local/src/openssl-$OPENSSL_VERSION"; 	OPENSSL_CONFIG_DIR=/usr/local/etc/ssl; 		mkdir /usr/local/src; 		wget --output-document "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_SOURCE_URL.asc"; 	wget --output-document "$OPENSSL_PATH.tar.gz" "$OPENSSL_SOURCE_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $OPENSSL_PGP_KEY_IDS; do 		gpg --batch --keyserver "$PGP_KEYSERVER" --recv-keys "$key"; 	done; 	gpg --batch --verify "$OPENSSL_PATH.tar.gz.asc" "$OPENSSL_PATH.tar.gz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	echo "$OPENSSL_SOURCE_SHA256 *$OPENSSL_PATH.tar.gz" | sha256sum -c -; 	mkdir -p "$OPENSSL_PATH"; 	tar --extract --file "$OPENSSL_PATH.tar.gz" --directory "$OPENSSL_PATH" --strip-components 1; 		cd "$OPENSSL_PATH"; 	MACHINE="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" 	RELEASE="4.x.y-z" 	SYSTEM='Linux' 	BUILD='???' 	./config 		--openssldir="$OPENSSL_CONFIG_DIR" 		-Wl,-rpath=/usr/local/lib 	; 	make -j "$(getconf _NPROCESSORS_ONLN)"; 	make install_sw install_ssldirs; 	cd ..; 	rm -rf "$OPENSSL_PATH"*; 	rmdir "$OPENSSL_CONFIG_DIR/certs" "$OPENSSL_CONFIG_DIR/private"; 	ln -sf /etc/ssl/certs /etc/ssl/private "$OPENSSL_CONFIG_DIR"; 	openssl version; 		OTP_SOURCE_URL="https://github.com/erlang/otp/releases/download/OTP-$OTP_VERSION/otp_src_$OTP_VERSION.tar.gz"; 	OTP_PATH="/usr/local/src/otp-$OTP_VERSION"; 		mkdir -p "$OTP_PATH"; 	wget --output-document "$OTP_PATH.tar.gz" "$OTP_SOURCE_URL"; 	echo "$OTP_SOURCE_SHA256 *$OTP_PATH.tar.gz" | sha256sum -c -; 	tar --extract --file "$OTP_PATH.tar.gz" --directory "$OTP_PATH" --strip-components 1; 		cd "$OTP_PATH"; 	export ERL_TOP="$OTP_PATH"; 	./otp_build autoconf; 	export CFLAGS='-g -O2'; 	export CFLAGS="$CFLAGS -Wl,-rpath=/usr/local/lib"; 	hostArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)"; 	buildArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	dpkgArch="$(dpkg --print-architecture)"; dpkgArch="${dpkgArch##*-}"; 	jitFlag=; 	case "$dpkgArch" in 		amd64) jitFlag='--enable-jit' ;; 	esac; 	./configure 		--host="$hostArch" 		--build="$buildArch" 		--disable-dynamic-ssl-lib 		--disable-hipe 		--disable-sctp 		--disable-silent-rules 		--enable-clock-gettime 		--enable-hybrid-heap 		--enable-kernel-poll 		--enable-shared-zlib 		--enable-smp-support 		--enable-threads 		--with-microstate-accounting=extra 		--without-common_test 		--without-debugger 		--without-dialyzer 		--without-diameter 		--without-edoc 		--without-erl_docgen 		--without-et 		--without-eunit 		--without-ftp 		--without-hipe 		--without-jinterface 		--without-megaco 		--without-observer 		--without-odbc 		--without-reltool 		--without-ssh 		--without-tftp 		--without-wx 		$jitFlag 	; 	make -j "$(getconf _NPROCESSORS_ONLN)" GEN_OPT_FLGS="-O2 -fno-strict-aliasing"; 	make install; 	cd ..; 	rm -rf 		"$OTP_PATH"* 		/usr/local/lib/erlang/lib/*/examples 		/usr/local/lib/erlang/lib/*/src 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 	apk del --no-network .build-deps; 		openssl version; 	erl -noshell -eval 'io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'
# Wed, 08 Jun 2022 18:58:54 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 08 Jun 2022 18:58:56 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie
# Wed, 08 Jun 2022 18:58:56 GMT
ENV RABBITMQ_VERSION=3.10.5
# Wed, 08 Jun 2022 18:58:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 08 Jun 2022 18:58:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 08 Jun 2022 18:58:58 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jun 2022 18:59:23 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"
# Wed, 08 Jun 2022 18:59:36 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN set -eux; 	su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus; 	echo 'management_agent.disable_metrics_collector = true' > /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf; 	chown rabbitmq:rabbitmq /etc/rabbitmq/conf.d/management_agent.disable_metrics_collector.conf
# Wed, 08 Jun 2022 18:59:38 GMT
# ARGS: PGP_KEYSERVER=keyserver.ubuntu.com
RUN ln -sf /opt/rabbitmq/plugins /plugins
# Wed, 08 Jun 2022 18:59:38 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 08 Jun 2022 18:59:39 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 08 Jun 2022 18:59:39 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 08 Jun 2022 18:59:40 GMT
COPY --chown=rabbitmq:rabbitmqfile:1010d75e6e011d4f35a78624739f459bbc98829ae9696991358350d1bd6a12ac in /etc/rabbitmq/conf.d/ 
# Wed, 08 Jun 2022 18:59:40 GMT
COPY file:0667537cb067f2e42e0e1d5c1def14391eaf4bfe791bc7f23fd95a83eff81025 in /usr/local/bin/ 
# Wed, 08 Jun 2022 18:59:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Jun 2022 18:59:42 GMT
EXPOSE 15691 15692 25672 4369 5671 5672
# Wed, 08 Jun 2022 18:59:42 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:af1ac1a73384e058591d04d19bc05a06781cc32d52d4593b468d6cb95eda9858`  
		Last Modified: Mon, 23 May 2022 19:43:36 GMT  
		Size: 2.6 MB (2580494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0342018e218e55e0bf9b04ef353fd0059bd009a8fa3707245b2ce8b60e68c97`  
		Last Modified: Wed, 25 May 2022 23:21:59 GMT  
		Size: 1.1 MB (1100505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c9d60769f0ac8a7b06b819d2f56f1a2e547e111b3aa58884eb5cbcab8d1a5b`  
		Last Modified: Wed, 08 Jun 2022 19:08:06 GMT  
		Size: 38.6 MB (38569248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abb4598dbcb0a1a136acdc3ce12d8600b1df2a97fc7d4497fd3ae9944a2b368`  
		Last Modified: Wed, 08 Jun 2022 19:08:01 GMT  
		Size: 1.5 KB (1489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06893405b23b4c16a5b7b6b67d2dd6cb8208ee2cbb0bc4bd05292b9d565b9cd`  
		Last Modified: Wed, 08 Jun 2022 19:08:01 GMT  
		Size: 16.8 MB (16840327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365432f7fcb9d01e313609f6ba032a7e3953bc350117158f5ecb08b5ea3614e6`  
		Last Modified: Wed, 08 Jun 2022 19:08:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f2073c389a690a4610d5b26e8d55e5024d0d095033fd8265b2f77b07742c8a`  
		Last Modified: Wed, 08 Jun 2022 19:08:00 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b77a3f99612c947b940a4f1ff69ccf223191cef65c9f551abf8b9723568fe1`  
		Last Modified: Wed, 08 Jun 2022 19:08:00 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e435ba9e45dc2eb44be821f77628b22023ecf26518f6625d9c0ed94acaefc48d`  
		Last Modified: Wed, 08 Jun 2022 19:08:00 GMT  
		Size: 833.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
