## `jetty:9-jdk17-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:864e02fe95b23217ccc03c354021a3e1383283fbf75680f114b732ca5dfc0ac7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:9-jdk17-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:2d13cf498248d0a1deb37d8b2a8aca19921922820b2bf6e961461ed6cc10cbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178046240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54660882d3c9c83b074db5fcfb1fd66bf291eafb2a82c3688699dd6722d73f92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='839326b5b4b3e4ac2edc3b685c8ab550f9b6d267eddf966323c801cb21e3e018';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:f1b5e1235bfbe173503864b0745991f6acbc1cb3cc585db25db55cc975d8c4a2`  
		Last Modified: Mon, 24 Jun 2024 16:42:55 GMT  
		Size: 144.3 MB (144332006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b1cd3263773d4ffacbc48e3c623670d0f823ddab3860cd77eb3e012e2c02a`  
		Last Modified: Mon, 24 Jun 2024 16:42:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48fadb2170d58cb6bea4140e5d4cad7173488b82a2763a9f56369fe59647a1b`  
		Last Modified: Mon, 24 Jun 2024 16:42:43 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75902f3b3b82ed47d7cd3f11d7b8818c1e1fd6b953fee74b5928f1655e70ad17`  
		Last Modified: Fri, 28 Jun 2024 20:56:14 GMT  
		Size: 17.2 MB (17151810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77e03539f4e9620d8187cdd56b4d9ad06206f202c0be93f75ef8ed73f99b535`  
		Last Modified: Fri, 28 Jun 2024 20:56:13 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:f62af417533c8f3b5bac040fe40df59cff42b9d36d91cd4205b16c2f0b8fde91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1370011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59005d00c5bf42029b58d010eaf8cf4cf00378f6ce414baeafde3ba6a4c2241e`

```dockerfile
```

-	Layers:
	-	`sha256:bbeb7c06f38a72e9b0964580adff7bdbee25c603f43d63c49187d4f88f6c3223`  
		Last Modified: Fri, 28 Jun 2024 20:56:13 GMT  
		Size: 1.4 MB (1350045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44656a99aa4704e51478c1f5025ee3d718c9e1675464dd83fd3b31a9c3e031a`  
		Last Modified: Fri, 28 Jun 2024 20:56:13 GMT  
		Size: 20.0 KB (19966 bytes)  
		MIME: application/vnd.in-toto+json
