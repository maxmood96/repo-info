<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `jruby`

-	[`jruby:9`](#jruby9)
-	[`jruby:9.1`](#jruby91)
-	[`jruby:9.1.17`](#jruby9117)
-	[`jruby:9.1.17.0`](#jruby91170)
-	[`jruby:9.1.17.0-jdk`](#jruby91170-jdk)
-	[`jruby:9.1.17.0-jre`](#jruby91170-jre)
-	[`jruby:9.1.17-jdk`](#jruby9117-jdk)
-	[`jruby:9.1.17-jre`](#jruby9117-jre)
-	[`jruby:9.1-jdk`](#jruby91-jdk)
-	[`jruby:9.1-jre`](#jruby91-jre)
-	[`jruby:9.2`](#jruby92)
-	[`jruby:9.2.11`](#jruby9211)
-	[`jruby:9.2.11.1`](#jruby92111)
-	[`jruby:9.2.11.1-jdk`](#jruby92111-jdk)
-	[`jruby:9.2.11.1-jdk11`](#jruby92111-jdk11)
-	[`jruby:9.2.11.1-jdk14`](#jruby92111-jdk14)
-	[`jruby:9.2.11.1-jdk8`](#jruby92111-jdk8)
-	[`jruby:9.2.11.1-jre`](#jruby92111-jre)
-	[`jruby:9.2.11.1-jre11`](#jruby92111-jre11)
-	[`jruby:9.2.11.1-jre8`](#jruby92111-jre8)
-	[`jruby:9.2.11.1-onbuild`](#jruby92111-onbuild)
-	[`jruby:9.2.11-jdk`](#jruby9211-jdk)
-	[`jruby:9.2.11-jdk11`](#jruby9211-jdk11)
-	[`jruby:9.2.11-jdk14`](#jruby9211-jdk14)
-	[`jruby:9.2.11-jdk8`](#jruby9211-jdk8)
-	[`jruby:9.2.11-jre`](#jruby9211-jre)
-	[`jruby:9.2.11-jre11`](#jruby9211-jre11)
-	[`jruby:9.2.11-jre8`](#jruby9211-jre8)
-	[`jruby:9.2.11-onbuild`](#jruby9211-onbuild)
-	[`jruby:9.2-jdk`](#jruby92-jdk)
-	[`jruby:9.2-jdk11`](#jruby92-jdk11)
-	[`jruby:9.2-jdk14`](#jruby92-jdk14)
-	[`jruby:9.2-jdk8`](#jruby92-jdk8)
-	[`jruby:9.2-jre`](#jruby92-jre)
-	[`jruby:9.2-jre11`](#jruby92-jre11)
-	[`jruby:9.2-jre8`](#jruby92-jre8)
-	[`jruby:9.2-onbuild`](#jruby92-onbuild)
-	[`jruby:9-jdk`](#jruby9-jdk)
-	[`jruby:9-jdk8`](#jruby9-jdk8)
-	[`jruby:9-onbuild`](#jruby9-onbuild)
-	[`jruby:latest`](#jrubylatest)

## `jruby:9`

```console
$ docker pull jruby@sha256:53aeba4995166458e27da7b7cb9a941d04800dbb07a5cf3dbd300a727ece360a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9` - linux; amd64

```console
$ docker pull jruby@sha256:f484fee535baea7090a345804ef2d0515de1f3f3c1a17bf1a3a2c27b7e0b138a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148297275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e2fe825882aec44030dae787cfeb39ad250c74e08884716f364e2d5b13d151`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:00:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:00:41 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:00:43 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:09 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2933ef99f22bd61cff7611367805e2a5c1d0449fd74bc4f8b88ddedb4f885f38`  
		Last Modified: Thu, 23 Apr 2020 22:03:02 GMT  
		Size: 25.6 MB (25613208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3152da64902c815ca796efc45ee49884cd09e8018dc099c2ffac5f347a842acf`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564523b13c01741b66dd8e2d8a417966ee277a114aa303083ca037af551e2577`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 1.0 MB (1014148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d571dc0ff4cb7e9531a6e57788455ed5e2172e4c66ac0a7fd0c5a4c28e697ce`  
		Last Modified: Thu, 23 Apr 2020 22:02:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.1`

```console
$ docker pull jruby@sha256:320372d0ce92b2c3eecbf13551312d34dcb60559c7f017dc933ec99ea4012b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.1` - linux; amd64

```console
$ docker pull jruby@sha256:651cae8ef89666f582931003555ed0428fc7e470a1fe92e8c94ec15ad931c1bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143962112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72ba4440cbbad95422460bbaa5d1e603e7080434a98c4c2406dfdbf6cb5001a`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:01:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:01:56 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:10 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:12 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5117ff7c484487bd3d6feb444d23d3c0c7e6db60e139ac2ef553c3d1eccacbb`  
		Last Modified: Thu, 23 Apr 2020 22:03:20 GMT  
		Size: 21.5 MB (21498771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c7eb5ceaa772ded117aa5bc613b06e0416743c473a00fd51fc6499595901d1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c0b0bd6c24cc8da70b9c035475fc1df82551265c9feca827a093e8f0401ba4`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 793.4 KB (793423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53406cd922d4d3b5ef0f1884241c3398785b1153cf842159f4bb2af4abd17de1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.1.17`

```console
$ docker pull jruby@sha256:320372d0ce92b2c3eecbf13551312d34dcb60559c7f017dc933ec99ea4012b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.1.17` - linux; amd64

```console
$ docker pull jruby@sha256:651cae8ef89666f582931003555ed0428fc7e470a1fe92e8c94ec15ad931c1bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143962112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72ba4440cbbad95422460bbaa5d1e603e7080434a98c4c2406dfdbf6cb5001a`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:01:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:01:56 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:10 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:12 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5117ff7c484487bd3d6feb444d23d3c0c7e6db60e139ac2ef553c3d1eccacbb`  
		Last Modified: Thu, 23 Apr 2020 22:03:20 GMT  
		Size: 21.5 MB (21498771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c7eb5ceaa772ded117aa5bc613b06e0416743c473a00fd51fc6499595901d1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c0b0bd6c24cc8da70b9c035475fc1df82551265c9feca827a093e8f0401ba4`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 793.4 KB (793423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53406cd922d4d3b5ef0f1884241c3398785b1153cf842159f4bb2af4abd17de1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.1.17.0`

```console
$ docker pull jruby@sha256:320372d0ce92b2c3eecbf13551312d34dcb60559c7f017dc933ec99ea4012b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.1.17.0` - linux; amd64

```console
$ docker pull jruby@sha256:651cae8ef89666f582931003555ed0428fc7e470a1fe92e8c94ec15ad931c1bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143962112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72ba4440cbbad95422460bbaa5d1e603e7080434a98c4c2406dfdbf6cb5001a`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:01:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:01:56 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:10 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:12 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5117ff7c484487bd3d6feb444d23d3c0c7e6db60e139ac2ef553c3d1eccacbb`  
		Last Modified: Thu, 23 Apr 2020 22:03:20 GMT  
		Size: 21.5 MB (21498771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c7eb5ceaa772ded117aa5bc613b06e0416743c473a00fd51fc6499595901d1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c0b0bd6c24cc8da70b9c035475fc1df82551265c9feca827a093e8f0401ba4`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 793.4 KB (793423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53406cd922d4d3b5ef0f1884241c3398785b1153cf842159f4bb2af4abd17de1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.1.17.0-jdk`

```console
$ docker pull jruby@sha256:262f98bbb5c6c0d2fd60ce64dfacbd14083d0d7c88871a785faf92706560bdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.1.17.0-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:25d6574f72528441666ab18dcc6edb1e6e4af1d24af677e21ee83d80f7074d03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259698050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e66f4773434ca6fc4b01027a88f5abbd7d270eec567d1f4f2cd8e8f35373309`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:02:18 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:02:19 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:02:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:02:21 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:35 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:37 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43793d1d9f4d9d9ce6fc8f97d1d68687625c7b4e57aa09d6adf5ebb266895e8b`  
		Last Modified: Thu, 23 Apr 2020 22:03:29 GMT  
		Size: 21.5 MB (21498902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e948832c9ef2ca707f145a7ad519664e307e2d25834d5692b2cf148a7eb319d6`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979ef030f5ad7106895b56d6747491a2b3844292a750cb82b4545f017477b7b9`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 793.4 KB (793413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb050cae0f3a8591dad3d18ff7d1a479a5c083d0935dee3f7717f4c7ac43fd`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.1.17.0-jre`

```console
$ docker pull jruby@sha256:320372d0ce92b2c3eecbf13551312d34dcb60559c7f017dc933ec99ea4012b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.1.17.0-jre` - linux; amd64

```console
$ docker pull jruby@sha256:651cae8ef89666f582931003555ed0428fc7e470a1fe92e8c94ec15ad931c1bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143962112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72ba4440cbbad95422460bbaa5d1e603e7080434a98c4c2406dfdbf6cb5001a`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:01:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:01:56 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:10 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:12 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5117ff7c484487bd3d6feb444d23d3c0c7e6db60e139ac2ef553c3d1eccacbb`  
		Last Modified: Thu, 23 Apr 2020 22:03:20 GMT  
		Size: 21.5 MB (21498771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c7eb5ceaa772ded117aa5bc613b06e0416743c473a00fd51fc6499595901d1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c0b0bd6c24cc8da70b9c035475fc1df82551265c9feca827a093e8f0401ba4`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 793.4 KB (793423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53406cd922d4d3b5ef0f1884241c3398785b1153cf842159f4bb2af4abd17de1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.1.17-jdk`

```console
$ docker pull jruby@sha256:262f98bbb5c6c0d2fd60ce64dfacbd14083d0d7c88871a785faf92706560bdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.1.17-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:25d6574f72528441666ab18dcc6edb1e6e4af1d24af677e21ee83d80f7074d03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259698050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e66f4773434ca6fc4b01027a88f5abbd7d270eec567d1f4f2cd8e8f35373309`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:02:18 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:02:19 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:02:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:02:21 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:35 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:37 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43793d1d9f4d9d9ce6fc8f97d1d68687625c7b4e57aa09d6adf5ebb266895e8b`  
		Last Modified: Thu, 23 Apr 2020 22:03:29 GMT  
		Size: 21.5 MB (21498902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e948832c9ef2ca707f145a7ad519664e307e2d25834d5692b2cf148a7eb319d6`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979ef030f5ad7106895b56d6747491a2b3844292a750cb82b4545f017477b7b9`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 793.4 KB (793413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb050cae0f3a8591dad3d18ff7d1a479a5c083d0935dee3f7717f4c7ac43fd`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.1.17-jre`

```console
$ docker pull jruby@sha256:320372d0ce92b2c3eecbf13551312d34dcb60559c7f017dc933ec99ea4012b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.1.17-jre` - linux; amd64

```console
$ docker pull jruby@sha256:651cae8ef89666f582931003555ed0428fc7e470a1fe92e8c94ec15ad931c1bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143962112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72ba4440cbbad95422460bbaa5d1e603e7080434a98c4c2406dfdbf6cb5001a`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:01:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:01:56 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:10 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:12 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5117ff7c484487bd3d6feb444d23d3c0c7e6db60e139ac2ef553c3d1eccacbb`  
		Last Modified: Thu, 23 Apr 2020 22:03:20 GMT  
		Size: 21.5 MB (21498771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c7eb5ceaa772ded117aa5bc613b06e0416743c473a00fd51fc6499595901d1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c0b0bd6c24cc8da70b9c035475fc1df82551265c9feca827a093e8f0401ba4`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 793.4 KB (793423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53406cd922d4d3b5ef0f1884241c3398785b1153cf842159f4bb2af4abd17de1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.1-jdk`

```console
$ docker pull jruby@sha256:262f98bbb5c6c0d2fd60ce64dfacbd14083d0d7c88871a785faf92706560bdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.1-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:25d6574f72528441666ab18dcc6edb1e6e4af1d24af677e21ee83d80f7074d03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259698050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e66f4773434ca6fc4b01027a88f5abbd7d270eec567d1f4f2cd8e8f35373309`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:02:18 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:02:19 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:02:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:02:21 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:35 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:37 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43793d1d9f4d9d9ce6fc8f97d1d68687625c7b4e57aa09d6adf5ebb266895e8b`  
		Last Modified: Thu, 23 Apr 2020 22:03:29 GMT  
		Size: 21.5 MB (21498902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e948832c9ef2ca707f145a7ad519664e307e2d25834d5692b2cf148a7eb319d6`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979ef030f5ad7106895b56d6747491a2b3844292a750cb82b4545f017477b7b9`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 793.4 KB (793413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb050cae0f3a8591dad3d18ff7d1a479a5c083d0935dee3f7717f4c7ac43fd`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.1-jre`

```console
$ docker pull jruby@sha256:320372d0ce92b2c3eecbf13551312d34dcb60559c7f017dc933ec99ea4012b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.1-jre` - linux; amd64

```console
$ docker pull jruby@sha256:651cae8ef89666f582931003555ed0428fc7e470a1fe92e8c94ec15ad931c1bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143962112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72ba4440cbbad95422460bbaa5d1e603e7080434a98c4c2406dfdbf6cb5001a`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:01:54 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:01:56 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:01:56 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:57 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:10 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:11 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:12 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5117ff7c484487bd3d6feb444d23d3c0c7e6db60e139ac2ef553c3d1eccacbb`  
		Last Modified: Thu, 23 Apr 2020 22:03:20 GMT  
		Size: 21.5 MB (21498771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c7eb5ceaa772ded117aa5bc613b06e0416743c473a00fd51fc6499595901d1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c0b0bd6c24cc8da70b9c035475fc1df82551265c9feca827a093e8f0401ba4`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 793.4 KB (793423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53406cd922d4d3b5ef0f1884241c3398785b1153cf842159f4bb2af4abd17de1`  
		Last Modified: Thu, 23 Apr 2020 22:03:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2`

```console
$ docker pull jruby@sha256:53aeba4995166458e27da7b7cb9a941d04800dbb07a5cf3dbd300a727ece360a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2` - linux; amd64

```console
$ docker pull jruby@sha256:f484fee535baea7090a345804ef2d0515de1f3f3c1a17bf1a3a2c27b7e0b138a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148297275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e2fe825882aec44030dae787cfeb39ad250c74e08884716f364e2d5b13d151`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:00:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:00:41 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:00:43 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:09 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2933ef99f22bd61cff7611367805e2a5c1d0449fd74bc4f8b88ddedb4f885f38`  
		Last Modified: Thu, 23 Apr 2020 22:03:02 GMT  
		Size: 25.6 MB (25613208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3152da64902c815ca796efc45ee49884cd09e8018dc099c2ffac5f347a842acf`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564523b13c01741b66dd8e2d8a417966ee277a114aa303083ca037af551e2577`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 1.0 MB (1014148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d571dc0ff4cb7e9531a6e57788455ed5e2172e4c66ac0a7fd0c5a4c28e697ce`  
		Last Modified: Thu, 23 Apr 2020 22:02:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.11`

```console
$ docker pull jruby@sha256:53aeba4995166458e27da7b7cb9a941d04800dbb07a5cf3dbd300a727ece360a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2.11` - linux; amd64

```console
$ docker pull jruby@sha256:f484fee535baea7090a345804ef2d0515de1f3f3c1a17bf1a3a2c27b7e0b138a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148297275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e2fe825882aec44030dae787cfeb39ad250c74e08884716f364e2d5b13d151`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:00:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:00:41 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:00:43 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:09 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2933ef99f22bd61cff7611367805e2a5c1d0449fd74bc4f8b88ddedb4f885f38`  
		Last Modified: Thu, 23 Apr 2020 22:03:02 GMT  
		Size: 25.6 MB (25613208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3152da64902c815ca796efc45ee49884cd09e8018dc099c2ffac5f347a842acf`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564523b13c01741b66dd8e2d8a417966ee277a114aa303083ca037af551e2577`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 1.0 MB (1014148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d571dc0ff4cb7e9531a6e57788455ed5e2172e4c66ac0a7fd0c5a4c28e697ce`  
		Last Modified: Thu, 23 Apr 2020 22:02:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.11.1`

```console
$ docker pull jruby@sha256:53aeba4995166458e27da7b7cb9a941d04800dbb07a5cf3dbd300a727ece360a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2.11.1` - linux; amd64

```console
$ docker pull jruby@sha256:f484fee535baea7090a345804ef2d0515de1f3f3c1a17bf1a3a2c27b7e0b138a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148297275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e2fe825882aec44030dae787cfeb39ad250c74e08884716f364e2d5b13d151`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:00:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:00:41 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:00:43 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:09 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2933ef99f22bd61cff7611367805e2a5c1d0449fd74bc4f8b88ddedb4f885f38`  
		Last Modified: Thu, 23 Apr 2020 22:03:02 GMT  
		Size: 25.6 MB (25613208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3152da64902c815ca796efc45ee49884cd09e8018dc099c2ffac5f347a842acf`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564523b13c01741b66dd8e2d8a417966ee277a114aa303083ca037af551e2577`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 1.0 MB (1014148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d571dc0ff4cb7e9531a6e57788455ed5e2172e4c66ac0a7fd0c5a4c28e697ce`  
		Last Modified: Thu, 23 Apr 2020 22:02:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.11.1-jdk`

```console
$ docker pull jruby@sha256:a548e0afb764874c48897a8f94d1748065d632d3fc64c644bf65d5097a057e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2.11.1-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:13d74469d921aacdc14cc4b0d65becb6d6b6bc75b9cb9ee36d901cd745ed26d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (264033247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9251c44dda39f2f6c433bea04c05f174558591193d4b795c51c475c0d0daf50`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:01:26 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:01:26 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:01:29 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:01:29 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:30 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:47 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:47 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:48 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87b9a02d7bee0864f14805ea9d392e8afadff24c367495f285e353b48f6053d`  
		Last Modified: Thu, 23 Apr 2020 22:03:12 GMT  
		Size: 25.6 MB (25613328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bdcd0555968fb3667c3ad364dc50a426ff8a34e163f8d32a4cd1e2575c7adb`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12e57d99d30fc5d4bf15c03c28c531eae0b82553121bfdecbef5289133c9b01`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 1.0 MB (1014183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32e402adb8fd8bdbc4908927ccbbf0e47d645d8ed9e741a0b74c6aa7c9f47c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.11.1-jdk11`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2.11.1-jdk14`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2.11.1-jdk8`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2.11.1-jre`

```console
$ docker pull jruby@sha256:53aeba4995166458e27da7b7cb9a941d04800dbb07a5cf3dbd300a727ece360a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2.11.1-jre` - linux; amd64

```console
$ docker pull jruby@sha256:f484fee535baea7090a345804ef2d0515de1f3f3c1a17bf1a3a2c27b7e0b138a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148297275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e2fe825882aec44030dae787cfeb39ad250c74e08884716f364e2d5b13d151`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:00:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:00:41 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:00:43 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:09 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2933ef99f22bd61cff7611367805e2a5c1d0449fd74bc4f8b88ddedb4f885f38`  
		Last Modified: Thu, 23 Apr 2020 22:03:02 GMT  
		Size: 25.6 MB (25613208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3152da64902c815ca796efc45ee49884cd09e8018dc099c2ffac5f347a842acf`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564523b13c01741b66dd8e2d8a417966ee277a114aa303083ca037af551e2577`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 1.0 MB (1014148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d571dc0ff4cb7e9531a6e57788455ed5e2172e4c66ac0a7fd0c5a4c28e697ce`  
		Last Modified: Thu, 23 Apr 2020 22:02:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.11.1-jre11`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2.11.1-jre8`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2.11.1-onbuild`

```console
$ docker pull jruby@sha256:82f0b7bddd96a9b5dba2bff7b2001823971648f6a07863505f6bc8c2dc5174f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2.11.1-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:10b5f6cbbb11db37f0a3e2fdf699419a1a8bcfd63bb6247c611e6b4cd8bca4d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259698183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efc3fec949511460565f634830426fb3dd701d243f4f403ed90ff751f119ef2`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:02:18 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:02:19 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:02:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:02:21 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:35 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:37 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:37 GMT
CMD ["irb"]
# Thu, 23 Apr 2020 22:02:44 GMT
RUN mkdir -p /usr/src/app
# Thu, 23 Apr 2020 22:02:44 GMT
WORKDIR /usr/src/app
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD RUN bundle install --system
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43793d1d9f4d9d9ce6fc8f97d1d68687625c7b4e57aa09d6adf5ebb266895e8b`  
		Last Modified: Thu, 23 Apr 2020 22:03:29 GMT  
		Size: 21.5 MB (21498902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e948832c9ef2ca707f145a7ad519664e307e2d25834d5692b2cf148a7eb319d6`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979ef030f5ad7106895b56d6747491a2b3844292a750cb82b4545f017477b7b9`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 793.4 KB (793413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb050cae0f3a8591dad3d18ff7d1a479a5c083d0935dee3f7717f4c7ac43fd`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141cab285713ee04a1409f4c15fad7c902718666bdb1481f11e70ed142e09e73`  
		Last Modified: Thu, 23 Apr 2020 22:03:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.11-jdk`

```console
$ docker pull jruby@sha256:a548e0afb764874c48897a8f94d1748065d632d3fc64c644bf65d5097a057e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2.11-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:13d74469d921aacdc14cc4b0d65becb6d6b6bc75b9cb9ee36d901cd745ed26d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (264033247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9251c44dda39f2f6c433bea04c05f174558591193d4b795c51c475c0d0daf50`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:01:26 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:01:26 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:01:29 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:01:29 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:30 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:47 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:47 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:48 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87b9a02d7bee0864f14805ea9d392e8afadff24c367495f285e353b48f6053d`  
		Last Modified: Thu, 23 Apr 2020 22:03:12 GMT  
		Size: 25.6 MB (25613328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bdcd0555968fb3667c3ad364dc50a426ff8a34e163f8d32a4cd1e2575c7adb`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12e57d99d30fc5d4bf15c03c28c531eae0b82553121bfdecbef5289133c9b01`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 1.0 MB (1014183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32e402adb8fd8bdbc4908927ccbbf0e47d645d8ed9e741a0b74c6aa7c9f47c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.11-jdk11`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2.11-jdk14`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2.11-jdk8`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2.11-jre`

```console
$ docker pull jruby@sha256:53aeba4995166458e27da7b7cb9a941d04800dbb07a5cf3dbd300a727ece360a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2.11-jre` - linux; amd64

```console
$ docker pull jruby@sha256:f484fee535baea7090a345804ef2d0515de1f3f3c1a17bf1a3a2c27b7e0b138a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148297275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e2fe825882aec44030dae787cfeb39ad250c74e08884716f364e2d5b13d151`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:00:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:00:41 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:00:43 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:09 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2933ef99f22bd61cff7611367805e2a5c1d0449fd74bc4f8b88ddedb4f885f38`  
		Last Modified: Thu, 23 Apr 2020 22:03:02 GMT  
		Size: 25.6 MB (25613208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3152da64902c815ca796efc45ee49884cd09e8018dc099c2ffac5f347a842acf`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564523b13c01741b66dd8e2d8a417966ee277a114aa303083ca037af551e2577`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 1.0 MB (1014148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d571dc0ff4cb7e9531a6e57788455ed5e2172e4c66ac0a7fd0c5a4c28e697ce`  
		Last Modified: Thu, 23 Apr 2020 22:02:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.11-jre11`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2.11-jre8`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2.11-onbuild`

```console
$ docker pull jruby@sha256:82f0b7bddd96a9b5dba2bff7b2001823971648f6a07863505f6bc8c2dc5174f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2.11-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:10b5f6cbbb11db37f0a3e2fdf699419a1a8bcfd63bb6247c611e6b4cd8bca4d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259698183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efc3fec949511460565f634830426fb3dd701d243f4f403ed90ff751f119ef2`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:02:18 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:02:19 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:02:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:02:21 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:35 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:37 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:37 GMT
CMD ["irb"]
# Thu, 23 Apr 2020 22:02:44 GMT
RUN mkdir -p /usr/src/app
# Thu, 23 Apr 2020 22:02:44 GMT
WORKDIR /usr/src/app
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD RUN bundle install --system
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43793d1d9f4d9d9ce6fc8f97d1d68687625c7b4e57aa09d6adf5ebb266895e8b`  
		Last Modified: Thu, 23 Apr 2020 22:03:29 GMT  
		Size: 21.5 MB (21498902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e948832c9ef2ca707f145a7ad519664e307e2d25834d5692b2cf148a7eb319d6`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979ef030f5ad7106895b56d6747491a2b3844292a750cb82b4545f017477b7b9`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 793.4 KB (793413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb050cae0f3a8591dad3d18ff7d1a479a5c083d0935dee3f7717f4c7ac43fd`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141cab285713ee04a1409f4c15fad7c902718666bdb1481f11e70ed142e09e73`  
		Last Modified: Thu, 23 Apr 2020 22:03:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk`

```console
$ docker pull jruby@sha256:a548e0afb764874c48897a8f94d1748065d632d3fc64c644bf65d5097a057e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:13d74469d921aacdc14cc4b0d65becb6d6b6bc75b9cb9ee36d901cd745ed26d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (264033247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9251c44dda39f2f6c433bea04c05f174558591193d4b795c51c475c0d0daf50`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:01:26 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:01:26 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:01:29 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:01:29 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:30 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:47 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:47 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:48 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87b9a02d7bee0864f14805ea9d392e8afadff24c367495f285e353b48f6053d`  
		Last Modified: Thu, 23 Apr 2020 22:03:12 GMT  
		Size: 25.6 MB (25613328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bdcd0555968fb3667c3ad364dc50a426ff8a34e163f8d32a4cd1e2575c7adb`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12e57d99d30fc5d4bf15c03c28c531eae0b82553121bfdecbef5289133c9b01`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 1.0 MB (1014183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32e402adb8fd8bdbc4908927ccbbf0e47d645d8ed9e741a0b74c6aa7c9f47c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk11`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2-jdk14`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2-jdk8`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2-jre`

```console
$ docker pull jruby@sha256:53aeba4995166458e27da7b7cb9a941d04800dbb07a5cf3dbd300a727ece360a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2-jre` - linux; amd64

```console
$ docker pull jruby@sha256:f484fee535baea7090a345804ef2d0515de1f3f3c1a17bf1a3a2c27b7e0b138a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148297275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e2fe825882aec44030dae787cfeb39ad250c74e08884716f364e2d5b13d151`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:00:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:00:41 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:00:43 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:09 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2933ef99f22bd61cff7611367805e2a5c1d0449fd74bc4f8b88ddedb4f885f38`  
		Last Modified: Thu, 23 Apr 2020 22:03:02 GMT  
		Size: 25.6 MB (25613208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3152da64902c815ca796efc45ee49884cd09e8018dc099c2ffac5f347a842acf`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564523b13c01741b66dd8e2d8a417966ee277a114aa303083ca037af551e2577`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 1.0 MB (1014148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d571dc0ff4cb7e9531a6e57788455ed5e2172e4c66ac0a7fd0c5a4c28e697ce`  
		Last Modified: Thu, 23 Apr 2020 22:02:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jre11`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2-jre8`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9.2-onbuild`

```console
$ docker pull jruby@sha256:82f0b7bddd96a9b5dba2bff7b2001823971648f6a07863505f6bc8c2dc5174f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9.2-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:10b5f6cbbb11db37f0a3e2fdf699419a1a8bcfd63bb6247c611e6b4cd8bca4d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259698183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efc3fec949511460565f634830426fb3dd701d243f4f403ed90ff751f119ef2`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:02:18 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:02:19 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:02:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:02:21 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:35 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:37 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:37 GMT
CMD ["irb"]
# Thu, 23 Apr 2020 22:02:44 GMT
RUN mkdir -p /usr/src/app
# Thu, 23 Apr 2020 22:02:44 GMT
WORKDIR /usr/src/app
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD RUN bundle install --system
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43793d1d9f4d9d9ce6fc8f97d1d68687625c7b4e57aa09d6adf5ebb266895e8b`  
		Last Modified: Thu, 23 Apr 2020 22:03:29 GMT  
		Size: 21.5 MB (21498902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e948832c9ef2ca707f145a7ad519664e307e2d25834d5692b2cf148a7eb319d6`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979ef030f5ad7106895b56d6747491a2b3844292a750cb82b4545f017477b7b9`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 793.4 KB (793413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb050cae0f3a8591dad3d18ff7d1a479a5c083d0935dee3f7717f4c7ac43fd`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141cab285713ee04a1409f4c15fad7c902718666bdb1481f11e70ed142e09e73`  
		Last Modified: Thu, 23 Apr 2020 22:03:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:a548e0afb764874c48897a8f94d1748065d632d3fc64c644bf65d5097a057e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:13d74469d921aacdc14cc4b0d65becb6d6b6bc75b9cb9ee36d901cd745ed26d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (264033247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9251c44dda39f2f6c433bea04c05f174558591193d4b795c51c475c0d0daf50`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:01:26 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:01:26 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:01:29 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:01:29 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:30 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:47 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:47 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:48 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:48 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87b9a02d7bee0864f14805ea9d392e8afadff24c367495f285e353b48f6053d`  
		Last Modified: Thu, 23 Apr 2020 22:03:12 GMT  
		Size: 25.6 MB (25613328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bdcd0555968fb3667c3ad364dc50a426ff8a34e163f8d32a4cd1e2575c7adb`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12e57d99d30fc5d4bf15c03c28c531eae0b82553121bfdecbef5289133c9b01`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 1.0 MB (1014183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32e402adb8fd8bdbc4908927ccbbf0e47d645d8ed9e741a0b74c6aa7c9f47c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk8`

```console
$ docker pull jruby@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `jruby:9-onbuild`

```console
$ docker pull jruby@sha256:82f0b7bddd96a9b5dba2bff7b2001823971648f6a07863505f6bc8c2dc5174f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:9-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:10b5f6cbbb11db37f0a3e2fdf699419a1a8bcfd63bb6247c611e6b4cd8bca4d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259698183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efc3fec949511460565f634830426fb3dd701d243f4f403ed90ff751f119ef2`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:01:53 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:05 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:06 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:01:26 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:02:18 GMT
ENV JRUBY_VERSION=9.1.17.0
# Thu, 23 Apr 2020 22:02:19 GMT
ENV JRUBY_SHA256=6a22f7bf8fef1a52530a9c9781a9d374ad07bbbef0d3d8e2af0ff5cbead0dfd5
# Thu, 23 Apr 2020 22:02:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:02:21 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:02:35 GMT
RUN gem install bundler
# Thu, 23 Apr 2020 22:02:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:02:36 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:02:37 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:02:37 GMT
CMD ["irb"]
# Thu, 23 Apr 2020 22:02:44 GMT
RUN mkdir -p /usr/src/app
# Thu, 23 Apr 2020 22:02:44 GMT
WORKDIR /usr/src/app
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD RUN bundle install --system
# Thu, 23 Apr 2020 22:02:45 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a01fbfad7fc489eface0e3ea2ca5e8c84746c8300dd06bc5634605666fbf99`  
		Last Modified: Thu, 23 Apr 2020 04:10:32 GMT  
		Size: 5.3 MB (5284595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478df40586973c72ae11ad4b0733defb36612ac5a39755ac96dee70d564af9a`  
		Last Modified: Thu, 23 Apr 2020 04:12:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f0dd11682ba1e8f6f0f9543ad7acbb6b130e91c223eee07b8d5a1b16455963`  
		Last Modified: Thu, 23 Apr 2020 04:12:43 GMT  
		Size: 104.4 MB (104441883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2c23563b627b8fc6c1bf8b11433a8f75b855dcc9bdd7a839d26216213da65`  
		Last Modified: Thu, 23 Apr 2020 22:03:11 GMT  
		Size: 7.7 MB (7660415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43793d1d9f4d9d9ce6fc8f97d1d68687625c7b4e57aa09d6adf5ebb266895e8b`  
		Last Modified: Thu, 23 Apr 2020 22:03:29 GMT  
		Size: 21.5 MB (21498902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e948832c9ef2ca707f145a7ad519664e307e2d25834d5692b2cf148a7eb319d6`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979ef030f5ad7106895b56d6747491a2b3844292a750cb82b4545f017477b7b9`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 793.4 KB (793413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb050cae0f3a8591dad3d18ff7d1a479a5c083d0935dee3f7717f4c7ac43fd`  
		Last Modified: Thu, 23 Apr 2020 22:03:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141cab285713ee04a1409f4c15fad7c902718666bdb1481f11e70ed142e09e73`  
		Last Modified: Thu, 23 Apr 2020 22:03:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:latest`

```console
$ docker pull jruby@sha256:53aeba4995166458e27da7b7cb9a941d04800dbb07a5cf3dbd300a727ece360a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jruby:latest` - linux; amd64

```console
$ docker pull jruby@sha256:f484fee535baea7090a345804ef2d0515de1f3f3c1a17bf1a3a2c27b7e0b138a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148297275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e2fe825882aec44030dae787cfeb39ad250c74e08884716f364e2d5b13d151`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:56 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 23 Apr 2020 04:04:57 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:05:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Apr 2020 22:00:36 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_VERSION=9.2.11.1
# Thu, 23 Apr 2020 22:00:36 GMT
ENV JRUBY_SHA256=f10449c82567133908e5e1ac076438307a7f0916f617f40fa314b78873a195dc
# Thu, 23 Apr 2020 22:00:41 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 23 Apr 2020 22:00:41 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:00:43 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 23 Apr 2020 22:01:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 23 Apr 2020 22:01:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 23 Apr 2020 22:01:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 22:01:09 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 23 Apr 2020 22:01:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4691f300007ec76b2f8f745e90909a915bf61c36851c32c6a65236dab6d982`  
		Last Modified: Thu, 23 Apr 2020 04:12:00 GMT  
		Size: 5.5 MB (5529312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52474d271babc8e8d1c4a38a22787111dfd51b457456ae72ade8b72b53367f31`  
		Last Modified: Thu, 23 Apr 2020 04:13:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30d0654650111e87158831d27673ebd89a3a00199ca25205c67cc2523646e2`  
		Last Modified: Thu, 23 Apr 2020 04:13:15 GMT  
		Size: 40.3 MB (40314443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ee607cbf0d72c23d613eb9cbaa2c0e17516479cb1fdf49294b0905892cb5c4`  
		Last Modified: Thu, 23 Apr 2020 22:03:01 GMT  
		Size: 7.6 MB (7634263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2933ef99f22bd61cff7611367805e2a5c1d0449fd74bc4f8b88ddedb4f885f38`  
		Last Modified: Thu, 23 Apr 2020 22:03:02 GMT  
		Size: 25.6 MB (25613208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3152da64902c815ca796efc45ee49884cd09e8018dc099c2ffac5f347a842acf`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564523b13c01741b66dd8e2d8a417966ee277a114aa303083ca037af551e2577`  
		Last Modified: Thu, 23 Apr 2020 22:02:59 GMT  
		Size: 1.0 MB (1014148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d571dc0ff4cb7e9531a6e57788455ed5e2172e4c66ac0a7fd0c5a4c28e697ce`  
		Last Modified: Thu, 23 Apr 2020 22:02:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
