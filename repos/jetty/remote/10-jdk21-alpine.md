## `jetty:10-jdk21-alpine`

```console
$ docker pull jetty@sha256:4d45eb346d6390b0585e469d3c06fc9f6cb31b8cb0c0e98b35d2419df2ca3755
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:10-jdk21-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:97710df6b284fe94d9e011c2a2a1d7b7d7020fa6efe6af28255d53d74572a7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193527072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d9c4bcc018b37093ac6b132c484c55deacd9b760510eeed689bb86f2c69d97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 31 Jan 2024 21:20:39 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["/bin/sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f68a9122054149861f6ce9d1b1c176bbe30dd76b36b74c916ba897c12e9d970';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|x86_64)          ESUM='8e861638bf6b08c6d5837de6dc929930550928ec5fcc81b9fa7e8296afd0f9c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["jshell"]
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_VERSION=10.0.20
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
WORKDIR /var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
USER jetty
# Wed, 31 Jan 2024 21:20:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jan 2024 21:20:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60acd7138d3e0a8e35e097d75b62e0b1cfd99cdad83e29656157ec622e1c51e2`  
		Last Modified: Mon, 24 Jun 2024 16:42:45 GMT  
		Size: 13.1 MB (13142550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc2499efbfe7968f2522df896fbe2f8a8c2134f7cc93e191f836eec5d02edb4`  
		Last Modified: Mon, 24 Jun 2024 16:43:37 GMT  
		Size: 158.7 MB (158716169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c492bf7da0e834114a9d2878918d8cfe522854c4df9fc7730e2f4b72b32775`  
		Last Modified: Mon, 24 Jun 2024 16:43:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d851ea679543ce279a7828ea806caaaa880c9ae89f2ded39374d44dd11a2fd2`  
		Last Modified: Mon, 24 Jun 2024 16:43:24 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3257f032376ed8f6f18a7c613a22c103e7fb73b6248051aa66d5022b44fab233`  
		Last Modified: Fri, 28 Jun 2024 20:56:31 GMT  
		Size: 18.2 MB (18248479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e23ee54a5c0d754f595340fa336f34747b272c4abf47c8d885e1d0cad584008`  
		Last Modified: Fri, 28 Jun 2024 20:56:29 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:9f79dfd579e1867abc64d80a6fdf1f398bc8afe60928855480b2a00b98ffbe0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1381322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e230520a17787c52b29594cc0484eaf4c79e4accbe6f8740d035879bf3bdcd`

```dockerfile
```

-	Layers:
	-	`sha256:5de23c0584337a6132bd5e20c5ac8a7ce5353d407d478efc01a6579c4a996717`  
		Last Modified: Fri, 28 Jun 2024 20:56:30 GMT  
		Size: 1.4 MB (1361381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4196e39396d535d87dc34d0087b20721c6391e02b1f0573f20663455af11d0d9`  
		Last Modified: Fri, 28 Jun 2024 20:56:31 GMT  
		Size: 19.9 KB (19941 bytes)  
		MIME: application/vnd.in-toto+json
