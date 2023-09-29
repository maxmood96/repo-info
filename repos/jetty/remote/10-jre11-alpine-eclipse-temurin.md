## `jetty:10-jre11-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:dd6a6ba324a02f5547daf088379301dabc38dc80dee44500ff55eacfbd9b4cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:10-jre11-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:d7f4006cfaa9fd3257aee4fc19c79631568855a5bfdebab6b28e32dc6538624a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73700435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6988c2d6997066fb4f23cd0ffd5a638dd756b8645a0c20641e3b5a79dee6a9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:24:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Sep 2023 23:24:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 23:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 28 Sep 2023 23:24:25 GMT
RUN apk add --no-cache fontconfig java-cacerts bash libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 28 Sep 2023 23:25:02 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 28 Sep 2023 23:25:29 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d34ea3d1e3852548546c69d7d73addb873e7926e66147b8596b7c11fad9ee057';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 28 Sep 2023 23:25:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 28 Sep 2023 23:25:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 28 Sep 2023 23:25:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 29 Sep 2023 04:50:11 GMT
ENV JETTY_VERSION=10.0.16
# Fri, 29 Sep 2023 04:50:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 29 Sep 2023 04:50:11 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 29 Sep 2023 04:50:11 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 29 Sep 2023 04:50:11 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Sep 2023 04:50:11 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.16/jetty-home-10.0.16.tar.gz
# Fri, 29 Sep 2023 04:50:11 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 29 Sep 2023 04:50:19 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 29 Sep 2023 04:50:20 GMT
WORKDIR /var/lib/jetty
# Fri, 29 Sep 2023 04:50:20 GMT
COPY multi:04e96d62b43d0ed55ad32900f133ff3fa46502048db2c67b0ea7a783ed3acc37 in / 
# Fri, 29 Sep 2023 04:50:20 GMT
USER jetty
# Fri, 29 Sep 2023 04:50:20 GMT
EXPOSE 8080
# Fri, 29 Sep 2023 04:50:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 29 Sep 2023 04:50:20 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4092d737c5d0c601ddadd8d075b756e55cc717065ae83683571965c2117a9`  
		Last Modified: Thu, 28 Sep 2023 23:28:20 GMT  
		Size: 9.3 MB (9276514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b289a5fd229559ccafe8f5112c00b18d6e5627802c2c25d3328753c3691a7d`  
		Last Modified: Thu, 28 Sep 2023 23:29:32 GMT  
		Size: 43.3 MB (43296769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9b6b27840d0a351f1083fcbe7120a005d2f80191a33f8ae92d59b2c429a62a`  
		Last Modified: Thu, 28 Sep 2023 23:29:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9288481f08366a13ff613c0eb5ab6728fd0f2a0981a9a20ba4e29924f804e82`  
		Last Modified: Thu, 28 Sep 2023 23:29:26 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcc721b9a4fde607aa8c6b696b2598df656466ce475b5359b364ce5ba4dcd80`  
		Last Modified: Fri, 29 Sep 2023 04:59:01 GMT  
		Size: 17.7 MB (17722673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d7d57703f0ea238373b72a577b51347c7dbf0ed7d98d1b9df5fd9285691f6c`  
		Last Modified: Fri, 29 Sep 2023 04:58:59 GMT  
		Size: 1.6 KB (1620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
