## `jetty:11-jdk11-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:3610470b64a4f7a8d45498c35b819a0c69515ade3f4311fd6d47bb0e6cf34d7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:11-jdk11-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:d36af2b6aa6d7183e56a9da11ac1b2677f22503ffeac5747a8f8fcd179253c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176580755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ddf2e91463e9ad1b10bae0e8acf63300f8d9bef4e9102f76841804c75831ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7e9e5241d1378d75ae70e9b216d0d51d3aa2e61e187e92e09d117cb613e16ee4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_VERSION=11.0.25
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.25/jetty-home-11.0.25.tar.gz
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 12 Aug 2025 07:13:40 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 12 Aug 2025 07:13:40 GMT
WORKDIR /var/lib/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 12 Aug 2025 07:13:40 GMT
USER jetty
# Tue, 12 Aug 2025 07:13:40 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 Aug 2025 07:13:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 07:13:40 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32368a88ab88c011f9799e221ffa3a76a0557d8f869cb207cb6f61e0a1955762`  
		Last Modified: Mon, 04 Aug 2025 19:11:15 GMT  
		Size: 16.3 MB (16280183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d648ad0c3205513ffbb1e09ea89959604157e09c4cc8d981f5fa1b1e777c4f0`  
		Last Modified: Mon, 04 Aug 2025 20:12:02 GMT  
		Size: 140.8 MB (140841600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593271197e067f9172951dae5461f06c964edf69c2598534299fed88688fb565`  
		Last Modified: Mon, 04 Aug 2025 19:11:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79e640d46de60752e85b9c04c3a723384b01154acc6635a1cda3176da6ada69`  
		Last Modified: Mon, 04 Aug 2025 19:11:16 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d36e0b5b1706ab19ec6664767e9b62f58fc2a77a89414e0754a7538e35134d1`  
		Last Modified: Wed, 13 Aug 2025 18:41:55 GMT  
		Size: 15.7 MB (15654995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b971ba5d059917ee5a3f2b0cef76ed817cffd6fe6a3950d72d566de1a36e8a`  
		Last Modified: Wed, 13 Aug 2025 18:41:55 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk11-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:f529ad17ed4b0c71d215b3ad05c60989d375c42a088001e2a562b59943817a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1137859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac511d8bafcbae087356a1ba3f740723929779388da9aabdd0b0d6fa591e681`

```dockerfile
```

-	Layers:
	-	`sha256:1b0cb6844e239c30d2169df1c71e8f23ac0770cab53a5cf240149095dfd02339`  
		Last Modified: Wed, 13 Aug 2025 20:18:23 GMT  
		Size: 1.1 MB (1117830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc53f90f121f09b61bc6322037440099e5caafb36bf7edb64c831516c42f9ca9`  
		Last Modified: Wed, 13 Aug 2025 20:18:23 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.in-toto+json
