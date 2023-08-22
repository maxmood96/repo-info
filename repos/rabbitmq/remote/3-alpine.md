## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:7abf73ecd8d3c6514225e39ec16d066e07af656e6a549c3248f6e56db56e2b17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:3-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:17fb3237822db85cce3381f476dc006a95297a1a89273b5213c585b31e0f6a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74755325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4df33df4019789c04e0062c94689c515c68a9b2a1deb6a041c26344bc2c6854`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_VERSION=3.12.3
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 17 Aug 2023 23:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 23:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 17 Aug 2023 23:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77895582007450c6e436dbf161b4c0c4bc7bc41147d321aecc8a694118c01ade`  
		Last Modified: Mon, 21 Aug 2023 20:00:28 GMT  
		Size: 430.3 KB (430263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6e57c1d4c38d4d43acd6eea47e8ab222e85cb1edb8e6001e9182ffeb2d78ad`  
		Last Modified: Mon, 21 Aug 2023 20:00:27 GMT  
		Size: 10.1 KB (10146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d2885758715dbf284ae9eefd7e73bb4c8470b0150509ae9c0f40069091974`  
		Last Modified: Mon, 21 Aug 2023 20:00:30 GMT  
		Size: 50.9 MB (50916982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b3622bfc809414edcdd38e0bdbf8786e8e557fe73d03ecf2fabdc19379fc2a`  
		Last Modified: Mon, 21 Aug 2023 20:00:28 GMT  
		Size: 2.3 MB (2296121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878aee99bd6ac4d2e87210425b1050844badd2b17455251463e24ab2160f7682`  
		Last Modified: Mon, 21 Aug 2023 20:00:30 GMT  
		Size: 17.7 MB (17698451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5c37df992eee7990ef7ff31d1e8bb3216ee8b78751d8bdf7f7ff813e749f3e`  
		Last Modified: Mon, 21 Aug 2023 20:00:29 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e17b17ee53cab84978694d57f4b17fb719e5accc499196e82617da6cd5dbfad`  
		Last Modified: Mon, 21 Aug 2023 20:00:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260d242f5b7f5a8f420494a56855f3ef4e2aea678897261de962d2348171f716`  
		Last Modified: Mon, 21 Aug 2023 20:00:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99453e4f48e595c53b4468be3117cc30293357493b0eac3ac9cc620901443c`  
		Last Modified: Mon, 21 Aug 2023 20:00:30 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e509db916e46adb9209a3979dceafd3904a443c8a8cf1b16e0c1f82a6e050724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.5 KB (760542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de613ac1f852283cc57df4df5b595c9e65d2614f406ac0610b5715dc7491f258`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b1d8c91a8f99111ee8a854ef44ab239c2746e9fa85881150b0ddd1d31439e`  
		Last Modified: Mon, 21 Aug 2023 20:00:28 GMT  
		Size: 701.5 KB (701508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ccb5cf4284f5507fb9f5324f3db040f69c9e4461b20400c236f178c6b37d72`  
		Last Modified: Mon, 21 Aug 2023 20:00:28 GMT  
		Size: 59.0 KB (59034 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:050bcc25cb0c0cd87ef2cd3ecf470274f824e2e31723ae651ee051898892c78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64008802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fd31fcb5bd9ca15534febfd8b8ebbd9cc0989d9f1004304e48249ffc87ddb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Mon, 17 Jul 2023 17:37:26 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Mon, 17 Jul 2023 17:37:26 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Mon, 17 Jul 2023 17:37:26 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Mon, 17 Jul 2023 17:37:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Mon, 17 Jul 2023 17:37:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Mon, 17 Jul 2023 17:37:26 GMT
ENV RABBITMQ_VERSION=3.12.2
# Mon, 17 Jul 2023 17:37:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Mon, 17 Jul 2023 17:37:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Mon, 17 Jul 2023 17:37:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Jul 2023 17:37:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Mon, 17 Jul 2023 17:37:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Mon, 17 Jul 2023 17:37:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Mon, 17 Jul 2023 17:37:26 GMT
ENV HOME=/var/lib/rabbitmq
# Mon, 17 Jul 2023 17:37:26 GMT
VOLUME [/var/lib/rabbitmq]
# Mon, 17 Jul 2023 17:37:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 17 Jul 2023 17:37:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Mon, 17 Jul 2023 17:37:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jul 2023 17:37:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Jul 2023 17:37:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Mon, 17 Jul 2023 17:37:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5781bdd6b98f88b6a42e80aac18988828ca6f4df1adb961b82d0699fb035bc7`  
		Last Modified: Mon, 31 Jul 2023 22:30:31 GMT  
		Size: 407.4 KB (407409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce953f5bfeb468181877dd524ff1bee270ca2582c893ddc7083c71409cdbff6`  
		Last Modified: Mon, 31 Jul 2023 22:30:31 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede374d943a6cbc1f22ea9824bf905b3e367de5c7e5f781313f6724ce2784600`  
		Last Modified: Mon, 31 Jul 2023 22:35:03 GMT  
		Size: 41.4 MB (41374967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22718ecc4d67b3ebc36448e9bea6010ffb253fce8fc30a412ba33c27a1fcd1e4`  
		Last Modified: Mon, 31 Jul 2023 22:34:58 GMT  
		Size: 1.4 MB (1404252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0338c6cb990390cb932e57c97bdaaa051d3342edfb71740e3d1a3b83ad58ed0d`  
		Last Modified: Mon, 31 Jul 2023 22:34:59 GMT  
		Size: 17.7 MB (17666934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29a73a52f8e3b50715b13ccfe7eb8fceae460272af9b349a58fdc06fc898830`  
		Last Modified: Mon, 31 Jul 2023 22:34:56 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac57dcc0b9c845c62e03592520de3cdf698472ee5d606f4f999a088f454d0a1`  
		Last Modified: Mon, 31 Jul 2023 22:34:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79da68e53abb17d7a7e9e7f3db59c9d54f98f641d195f3a4bb37fe22584d8589`  
		Last Modified: Mon, 31 Jul 2023 22:34:56 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce1e3281dd8973973247e9d24635df5e95b27daf8bd32d9a6099d5fc4fbe2c6`  
		Last Modified: Mon, 31 Jul 2023 22:34:56 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:2aefcd9104e569f99a844f3f283ba0b9b1f979cc00acefde51fa66d7fcb2402d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63104850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c071f2ac490053e73f68cc4c233126689cc5946073b57bbdfc1791720eb994e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_VERSION=3.12.3
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 17 Aug 2023 23:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 23:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 17 Aug 2023 23:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a7d6afd79205115eb6352e8cdc69b32b83c16b38117d824a45a709cfb7c88`  
		Last Modified: Wed, 09 Aug 2023 01:12:53 GMT  
		Size: 390.0 KB (389991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed440a1b3d9ccc752805ebd2f70b123778714929fba871514c035a75a88883e`  
		Last Modified: Wed, 09 Aug 2023 01:12:52 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18bc4bdbf70f86c361da5414bdeec5a836df0457df5abdd53a11a47e7398729`  
		Last Modified: Wed, 09 Aug 2023 03:10:08 GMT  
		Size: 40.8 MB (40806738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d36c591a33dca0bff9fde8ee9d459ee300a86dbc4cf00e24b08f87582a39f8`  
		Last Modified: Wed, 09 Aug 2023 03:10:04 GMT  
		Size: 1.3 MB (1298577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f6cc6117f57b8a3473debe59a97e8fa95d0c705f94d592be514662290790c3`  
		Last Modified: Mon, 21 Aug 2023 19:51:45 GMT  
		Size: 17.7 MB (17698182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e87e4d26efa3ddcad170445a3142b84c7e5cca710f4405d271de4ee248eb72c`  
		Last Modified: Mon, 21 Aug 2023 19:51:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cea2dbd1869f25bee004d88f82ba7e95a28f896e96578ed053a6ae79250922`  
		Last Modified: Mon, 21 Aug 2023 19:51:43 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae668a2ca8a310c5eb18ede049ae05b732b0baee903d131d0171d2c08261c45`  
		Last Modified: Mon, 21 Aug 2023 19:51:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1835b28c111366d4a8e4fce03f011e857f4fd58e2afb7d26d21ffed367e2c31c`  
		Last Modified: Mon, 21 Aug 2023 19:51:44 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:23694f2d3e4e5242cac5441db8cebd22b8e0e2bf810dc0b0f3868265ddffe9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.5 KB (756471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94561b16bce91ea605be54d43bdc1b4c4b629fac6085be3dfb41d1304b157b74`

```dockerfile
```

-	Layers:
	-	`sha256:c053672efe9c58ecf374c6e73f88f69c80b1e66db0979699ee8e8cb8f0953f09`  
		Last Modified: Mon, 21 Aug 2023 19:51:44 GMT  
		Size: 697.4 KB (697431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e676aca5a74ce350277536339c6f80e8507599787c5c9a0278638539e6b8011`  
		Last Modified: Mon, 21 Aug 2023 19:51:43 GMT  
		Size: 59.0 KB (59040 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:e367e7e7ff1dc343b4291158926731a674f8fd3c45af3ce5edca9d86a89403b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71804538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55db9986023902d1574d7f69feae6ef54709b53f453365e048a8a6b4baeeacbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_VERSION=3.12.3
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 17 Aug 2023 23:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 23:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 17 Aug 2023 23:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667f55f8875b6436bbfba6fc0cb1d76fd37b98f19217e63a4db031998ba82538`  
		Last Modified: Wed, 09 Aug 2023 10:35:58 GMT  
		Size: 409.3 KB (409331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d831351cd1ccd83812fbe61759255cbafccb9d7e3903aca96af13d5eeee0d3dc`  
		Last Modified: Wed, 09 Aug 2023 10:35:57 GMT  
		Size: 10.1 KB (10125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7737dca9b00e34927c9805d71ccc09e8eca763cfb841ec8bdecad0c520ea240`  
		Last Modified: Wed, 09 Aug 2023 14:09:39 GMT  
		Size: 48.0 MB (47985821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d3862c01fb1de5dadbfae7cff1bd335880156e96bff67d22de633085ffdb90`  
		Last Modified: Wed, 09 Aug 2023 14:09:37 GMT  
		Size: 2.4 MB (2368265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b12fea0fd56b0fc5a4106d1c8b4354bb72041072b99575d4a78ecf7ac07efe`  
		Last Modified: Mon, 21 Aug 2023 23:38:35 GMT  
		Size: 17.7 MB (17698489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab736ed513740652e98724ff0a3e7e8ce7d24558f1be4c9729fcae2f9a8fafa`  
		Last Modified: Mon, 21 Aug 2023 23:38:34 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1879f857f6f0bc886a10d32f58d12b2cdb0e81b7f2ddbf1ef59888141df529`  
		Last Modified: Mon, 21 Aug 2023 23:38:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488e10cf02f941031cd15c4165f520905108506e905f61b6ccd50d62e6d48807`  
		Last Modified: Mon, 21 Aug 2023 23:38:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8effa34c735f50006ae8fb7af4fec66f7c61580bfc5753abc2970cad1eb1a0`  
		Last Modified: Mon, 21 Aug 2023 23:38:35 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:5f173adcad3af18a2d68d126d9346a32b2748236fb5929f252d3db8037c32419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.4 KB (760408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a2f37b6f53871c24f3ce1c5ac37ad4addefcb7870c154995c46a374011bfa6`

```dockerfile
```

-	Layers:
	-	`sha256:883021c9d277b33a74428f472c8e7a1b554f72f853f6af45aa059eb5a151fa9e`  
		Last Modified: Mon, 21 Aug 2023 23:38:34 GMT  
		Size: 701.5 KB (701530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2591cefaee4da84ed9c3438c7a13d562ba7d153eabe6057d46a16603b5181891`  
		Last Modified: Mon, 21 Aug 2023 23:38:34 GMT  
		Size: 58.9 KB (58878 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:3b9944633b684618ebe8637d6e8a6162332e66be99b3861cb602d416fb3ea76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65986452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c302508773d047830e218898353cb8acf29fcf76e0f79bb28aa8e322893faa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_VERSION=3.12.3
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 17 Aug 2023 23:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 23:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 17 Aug 2023 23:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea54736fc4404623ac03bfd9bc8c330425bffb1a1a0cedbabf114f16988083a9`  
		Last Modified: Mon, 21 Aug 2023 20:00:26 GMT  
		Size: 445.2 KB (445173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a23d8631627d9d08be957f8059b0d19679b5116149b643531ebcaba3f173a45`  
		Last Modified: Mon, 21 Aug 2023 20:00:26 GMT  
		Size: 10.1 KB (10148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692a353daf4d4e486a3fd8b6a817101ced4e28c07d4668d4d75323152e7abd57`  
		Last Modified: Mon, 21 Aug 2023 20:00:30 GMT  
		Size: 43.2 MB (43195832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7e0c3b0b1f2852bd8888deb379019da6f8af45b770dfaaa27fd5ecc3257b4d`  
		Last Modified: Mon, 21 Aug 2023 20:00:27 GMT  
		Size: 1.4 MB (1400179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f86a06d01a746530ec3a0f8f8c61775c671c90238e0fb5b60a8d65697a98846`  
		Last Modified: Mon, 21 Aug 2023 20:00:29 GMT  
		Size: 17.7 MB (17698228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37aee4dc71fbc8a83eb5358dca5b34d354f013b88aef91c7cbb009ea13ed43c5`  
		Last Modified: Mon, 21 Aug 2023 20:00:27 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2d28bfa54d26cccf277998f6e88785e9aa22de01e8e72d32eb29e1e4a71662`  
		Last Modified: Mon, 21 Aug 2023 20:00:28 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d3aeae13b8e1cf2389853878e4a4f726a5064941a7440d43c884840df7574e`  
		Last Modified: Mon, 21 Aug 2023 20:00:29 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dcc2ee5a1e426aaa4826fe7782034beac56fa570b26c386b8386912fd0774b`  
		Last Modified: Mon, 21 Aug 2023 20:00:29 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:51146aca8fd81585ed1d488a1a3c3d2c2502393d3ff69f54d4f29c57b5e995b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 KB (58764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8d45e1675c1af46b7c446e88c6262c3e68a0f95e502a7da6444cfe491d1e87`

```dockerfile
```

-	Layers:
	-	`sha256:8980f51b91c4b4c11e8139fb7cc135273d4b3456e980b905a6fd2ea8ba1d09f6`  
		Last Modified: Mon, 21 Aug 2023 20:00:26 GMT  
		Size: 58.8 KB (58764 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:7b99fea972c6c510c2700e59c5c2b6ce4da1ec98884cfb217593cd64621e88d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67122941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c90fae074248e922f6808f9e8be30445959a0d7e37bc3f07173eedc408bede`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_VERSION=3.12.3
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 17 Aug 2023 23:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 23:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 17 Aug 2023 23:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad30f2c2ea24300733758f57c86de1345309abc331440d30489541dfbf8d4f23`  
		Last Modified: Wed, 09 Aug 2023 08:48:18 GMT  
		Size: 473.3 KB (473277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f90d3f6f00cd150a918e39ec2061008175f9d189baf332a55e51779087eeed7`  
		Last Modified: Wed, 09 Aug 2023 08:48:18 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bfa1e4b201d96a10f379dba964ef3084cc033150e2545ae9fdd76ed768ab4c`  
		Last Modified: Wed, 09 Aug 2023 14:29:26 GMT  
		Size: 44.1 MB (44073653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccdec895322602b4abcd26bf973fbda07dd963f3d2e2bd9250a633a8927459c`  
		Last Modified: Wed, 09 Aug 2023 14:29:23 GMT  
		Size: 1.5 MB (1519688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf3ef03853e2761ee55f9ef4eaa05091e9656b5138a1bb92fe2562608d48915`  
		Last Modified: Mon, 21 Aug 2023 23:33:48 GMT  
		Size: 17.7 MB (17698175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7a9179ae44f229dd8065ff2f702e35abe9b6059ffb13b80c3d54e79109ebdd`  
		Last Modified: Mon, 21 Aug 2023 23:33:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0c05007f80a0c9e358eacc18b94f2a05ed7ba17f95bd79deeb76c4572775e4`  
		Last Modified: Mon, 21 Aug 2023 23:33:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6e308d3f155950c99692cbce778bef0790630849b69164d60f2d0c97d146c7`  
		Last Modified: Mon, 21 Aug 2023 23:33:46 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc4563c8e922dbe44473cacad886e07649627860c7e59d9abc48d03fec5c565`  
		Last Modified: Mon, 21 Aug 2023 23:33:47 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cda9cb7970557ae5486707c8348415db02876d2bbea76658b0923aef19fea97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.9 KB (754899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56936aaa387998ce1363d6ad58a316b040647aa4d806d7935e066fc444d60914`

```dockerfile
```

-	Layers:
	-	`sha256:897cce821a373ecccab376c8b413e31f5b6bc3714401228df37131c6316f6e04`  
		Last Modified: Mon, 21 Aug 2023 23:33:46 GMT  
		Size: 696.0 KB (695977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89d832bbe564ed19d47f4c05754ee2bfef64b029598db0c800da5c92c342ea59`  
		Last Modified: Mon, 21 Aug 2023 23:33:46 GMT  
		Size: 58.9 KB (58922 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:303cfa90cfc33c2ffd2e8e2fbfda959ce817cf2bf65c7d33008293cef65be70c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64339862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b9c4b2cec6da7d0285eed569b181f58acd06815c1beadba98560a9aa5f2379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_VERSION=3.12.3
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 17 Aug 2023 23:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 23:05:26 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 17 Aug 2023 23:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 17 Aug 2023 23:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 23:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Aug 2023 23:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Aug 2023 23:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 17 Aug 2023 23:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8bd020b2175f142a2a3f9429c4296358dd43a44cfbb01e663569dfff85d137`  
		Last Modified: Wed, 09 Aug 2023 08:59:07 GMT  
		Size: 427.9 KB (427887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2594681521d2f9a47261aed70f074eed34684452c91f97b6340181613a7e3e`  
		Last Modified: Wed, 09 Aug 2023 08:59:07 GMT  
		Size: 10.1 KB (10148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1a63d9af94d59864fccb2432620087cb92b8e56f111cb6e0bc18171256903`  
		Last Modified: Wed, 09 Aug 2023 11:46:15 GMT  
		Size: 41.5 MB (41492657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b21249d925567afeda76c04bb02003e65914ed85bc2ad4e69ce9484df44c47`  
		Last Modified: Wed, 09 Aug 2023 11:46:13 GMT  
		Size: 1.5 MB (1495030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff52337ae303f7e6397937e65f70566b2830ce64982fe0587ff9f08bfea643d`  
		Last Modified: Mon, 21 Aug 2023 22:47:45 GMT  
		Size: 17.7 MB (17698200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3355b4ade12689af9452976d8c01c67e997a7fb58d9105e44ba1ebae1b919`  
		Last Modified: Mon, 21 Aug 2023 22:47:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b3bfa4d61349ea2a76b5e89900b151736048bcf27e572dd49a657d65c1d1ad`  
		Last Modified: Mon, 21 Aug 2023 22:47:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be963587c3079eed3e86cd23b8a68a30bd05613157ca3d4dccb431b8ae1c0b34`  
		Last Modified: Mon, 21 Aug 2023 22:47:44 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c956c61cc7878cba9cae9224812377e094947cbc510bfe64597bb365f9fbb26`  
		Last Modified: Mon, 21 Aug 2023 22:47:45 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:41b8af83615a22f338e9700863c7a84ef1a863763782af03060e8348343e9b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.8 KB (754778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa37b252f4264f68d6b226195c866ac60f8dc3374ad2d88ebccf7f8ca1e61c5c`

```dockerfile
```

-	Layers:
	-	`sha256:9b1fd369ad20faf9e30f0999e35fe7e24f95edf7dc062bf961d2472bbcf11a09`  
		Last Modified: Mon, 21 Aug 2023 22:47:44 GMT  
		Size: 695.9 KB (695910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb5efe28ff2b9ca335427cf047e2416809e7b5db41d53a24dcca9505efaafb4`  
		Last Modified: Mon, 21 Aug 2023 22:47:44 GMT  
		Size: 58.9 KB (58868 bytes)  
		MIME: application/vnd.in-toto+json
