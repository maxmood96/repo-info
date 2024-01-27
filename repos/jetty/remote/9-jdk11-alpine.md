## `jetty:9-jdk11-alpine`

```console
$ docker pull jetty@sha256:b442b1d6122d7696c6e564278b4d79a0fe6be3361f281407e5a6a73ecf910e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:9-jdk11-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:c6a1eb14515efdc78809810a46188f7bfb99b573e9a5ca5f15dd7035d0a808d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169572915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17652e3fa93b7b2863d32ac61772c45f1379791e22203faf1b05dbc4c9305a35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:52:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 27 Jan 2024 00:52:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 00:52:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 27 Jan 2024 00:53:00 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 27 Jan 2024 00:53:37 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Sat, 27 Jan 2024 00:53:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b541c99a5de71ebbe53e7815f9222e377b814fa1025f9f5274cb7bad226809f8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 27 Jan 2024 00:53:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 27 Jan 2024 00:53:48 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 27 Jan 2024 00:53:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Jan 2024 00:53:48 GMT
CMD ["jshell"]
# Sat, 27 Jan 2024 08:53:08 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Sat, 27 Jan 2024 08:53:09 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 27 Jan 2024 08:53:09 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 27 Jan 2024 08:53:09 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 27 Jan 2024 08:53:09 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 08:53:09 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Sat, 27 Jan 2024 08:53:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 27 Jan 2024 08:53:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 27 Jan 2024 08:53:18 GMT
WORKDIR /var/lib/jetty
# Sat, 27 Jan 2024 08:53:18 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 27 Jan 2024 08:53:18 GMT
USER jetty
# Sat, 27 Jan 2024 08:53:18 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:53:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:53:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d043da2becbad64efc04c3177047b954002aa6a615a5716af19ecff2d3ff3ed0`  
		Last Modified: Sat, 27 Jan 2024 00:56:34 GMT  
		Size: 8.5 MB (8528146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d770813566ace7742087c2bce62d8d9bd663f7886f3b58f416026074632f870d`  
		Last Modified: Sat, 27 Jan 2024 00:57:24 GMT  
		Size: 140.5 MB (140489170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7ed25e6ab7a24f87e7e0744e91fe7f632968e4e3576013a381f17a992fb2e5`  
		Last Modified: Sat, 27 Jan 2024 00:57:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3eb764dc0954e0f7f98a91f4a30e02ddc68d011d4703d21207b2f1fbf2d3964`  
		Last Modified: Sat, 27 Jan 2024 00:57:14 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afabb89954bfc30183f8a596a718ac7da0d1a71823630b232d91ec6566a2ad87`  
		Last Modified: Sat, 27 Jan 2024 09:05:32 GMT  
		Size: 17.1 MB (17144347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca88fb935700ad17bc73cc01c364c5fa355fcf7b0eb3b3e69751ba862bccaf19`  
		Last Modified: Sat, 27 Jan 2024 09:05:31 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
