## `jetty:12-jdk23-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:2b273173b9b1481d60515b822acc274fa9a4c1f5e6200405f1d085aa58b23e47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:12-jdk23-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:13050c622b6e5c8fbc787bda1dcc9620ef3840614e5c00a3e46521fefc2a767d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227347280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bb53c4dc532f3fcc20989a04d3db3ae955f3d5e30ea6d1ebd0945c9181549a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 01:48:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 01:48:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 01:48:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Oct 2024 01:48:51 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 03 Oct 2024 01:48:51 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Thu, 03 Oct 2024 01:48:51 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 03 Oct 2024 01:48:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 03 Oct 2024 01:48:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 03 Oct 2024 01:48:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 03 Oct 2024 01:48:51 GMT
CMD ["jshell"]
# Thu, 03 Oct 2024 01:48:51 GMT
ENV JETTY_VERSION=12.0.14
# Thu, 03 Oct 2024 01:48:51 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 03 Oct 2024 01:48:51 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 03 Oct 2024 01:48:51 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 03 Oct 2024 01:48:51 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 01:48:51 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.14/jetty-home-12.0.14.tar.gz
# Thu, 03 Oct 2024 01:48:51 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 03 Oct 2024 01:48:51 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 03 Oct 2024 01:48:51 GMT
WORKDIR /var/lib/jetty
# Thu, 03 Oct 2024 01:48:51 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 03 Oct 2024 01:48:51 GMT
USER jetty
# Thu, 03 Oct 2024 01:48:51 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 03 Oct 2024 01:48:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 01:48:51 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d6c61b4122c4041551807008b7fb7c5a6aed794c67e600039f12b1bfb26541`  
		Last Modified: Thu, 24 Oct 2024 00:58:09 GMT  
		Size: 23.0 MB (22953333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c1f57d70da5691d45e3b453ea602f88dec1cb5124492947b1c8bf718aaefa7`  
		Last Modified: Thu, 24 Oct 2024 00:58:11 GMT  
		Size: 165.5 MB (165513205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6884f085d1c712fbde3dc66a7118dea03eaa2f60358e17066d1be1e1bbab5`  
		Last Modified: Thu, 24 Oct 2024 00:58:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e8c7349cbe3bf93d50773b69fbb2323de87e868f68e5f257129801a4ae5d57`  
		Last Modified: Thu, 24 Oct 2024 00:57:57 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5047187a709f7150b894b56c6359cedcee192d3212d652f475ea5eb454e2a59d`  
		Last Modified: Thu, 24 Oct 2024 01:53:16 GMT  
		Size: 35.3 MB (35252861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411d263d25226ef466be3d693ee77d8be6660aa5c5579f0ea44c5b7a191c8001`  
		Last Modified: Thu, 24 Oct 2024 01:53:15 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk23-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:f8846fcf77f2da645e6affa61d558448389198b6df86e53ae9916db6b01682d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1333205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f5b49a9f3175806a2c4d6a67c20041cce2e7ca59087123768bc5336d1aa90c`

```dockerfile
```

-	Layers:
	-	`sha256:f3d35d841800a5d8c5480db572cc77652c1afa559eb5b77ea77d7adf718db1a6`  
		Last Modified: Thu, 24 Oct 2024 01:53:15 GMT  
		Size: 1.3 MB (1313176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662ee00c8ca8b3f7e66aa66b6a730ff6c42dfa432350b0004b33f9c96b901caf`  
		Last Modified: Thu, 24 Oct 2024 01:53:14 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.in-toto+json
