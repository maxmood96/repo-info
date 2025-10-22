## `jetty:12-jdk21-alpine`

```console
$ docker pull jetty@sha256:f884fa5d37f75c7f39c17f629d37b2ba58f0e00139a94768b00a622816f41f5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:12-jdk21-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:f087a97c3b75abc637eeb5413ef24d32bb152f86ec36b67ce183d49c0f638f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229741854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6399e75bc5dad470e9070299bb128c8ba213de7180f94d00f60b04652cacaea4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4773cfdc59d66b75f4a68ac843b2b5854791840114cf8bb1b56fb6f7826ae498';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='73c4cbe10f4f385383d9cb54d34f2bee2c68b5265f9e3d954f3326948c40c0be';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_VERSION=12.1.2
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.2/jetty-home-12.1.2.tar.gz
# Thu, 09 Oct 2025 00:19:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 09 Oct 2025 00:19:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
WORKDIR /var/lib/jetty
# Thu, 09 Oct 2025 00:19:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 09 Oct 2025 00:19:17 GMT
USER jetty
# Thu, 09 Oct 2025 00:19:17 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 09 Oct 2025 00:19:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 Oct 2025 00:19:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2a5ff902df392c9f6430cfcee73bfa86c2856161d3162cbe1ec519b6da89a1`  
		Last Modified: Wed, 08 Oct 2025 23:34:06 GMT  
		Size: 21.1 MB (21112159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ef1487a229d2c2defc8ef70f98308c6bb819c1ee443e3f4d90d7399d6edd29`  
		Last Modified: Wed, 08 Oct 2025 23:36:49 GMT  
		Size: 158.0 MB (158029025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede95b48c87bb31f7470a39694663bb7da86718f456e8968ca1fb4e0f2661f20`  
		Last Modified: Wed, 08 Oct 2025 23:34:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64da9540a58e0598f9af16f6180d6ca8a17f6b7ec33c0b9b6c94ac191adf2cbc`  
		Last Modified: Wed, 08 Oct 2025 23:34:03 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3812ddd2282c828d59e7786be8265c1eb86fe085cfb85097d2f480090b6ebf43`  
		Last Modified: Tue, 21 Oct 2025 20:14:55 GMT  
		Size: 46.8 MB (46793931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e417c512eb76669fcdfa221f9038366ca21ee4500bf00a4d44171afaf035b51`  
		Last Modified: Tue, 21 Oct 2025 20:14:52 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:033256979ec50affa6473acc9e0491d1f6247c45d99d536b784c5526bec161bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1466545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1baeaf1ec1fb25249ac792e6f687279308b473c1f6707d63fe0dcb779fcf2b`

```dockerfile
```

-	Layers:
	-	`sha256:f24ada9eb5f710d2075893e8455c649cdcab2310e1fad1dc319014ded8cc7aea`  
		Last Modified: Tue, 21 Oct 2025 23:18:04 GMT  
		Size: 1.4 MB (1446528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf32907003bd9c62af14dd2aa1eef5ccfb7ab8253d3eafe12a84e5303021ab40`  
		Last Modified: Tue, 21 Oct 2025 23:18:05 GMT  
		Size: 20.0 KB (20017 bytes)  
		MIME: application/vnd.in-toto+json
