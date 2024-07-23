## `jetty:10-jdk17-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:6adffa6fa277397bf1711b71bc5e3e739006759941fa5252b003383ba50d1d81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:10-jdk17-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:f91ed519018113bcefb0c3bbb56992b64e5e085749198f06df1c42d8942c147e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179389973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce9aa91bfa597b3b25d6bf162435a6a2e18773eb54acb9fe1cdc680a292582`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 08 Jul 2024 06:35:54 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Jul 2024 06:35:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 06:35:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6d274a292a717a6f8d00a3ed0695497405c5c634c27fec1692dd13784f6ff6fa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["jshell"]
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_VERSION=10.0.22
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.22/jetty-home-10.0.22.tar.gz
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
WORKDIR /var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
USER jetty
# Mon, 08 Jul 2024 06:35:54 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 06:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e118bbc909a65083d314d2da5fe1f703619cf9810828b0d739ed6962de633f2`  
		Last Modified: Tue, 23 Jul 2024 01:06:33 GMT  
		Size: 13.0 MB (13019343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1ac76beb96a2904db02448518399d50e48e50a297defebe2826e9ee08b2160`  
		Last Modified: Tue, 23 Jul 2024 01:06:42 GMT  
		Size: 144.4 MB (144394579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ef59aa5e3addd013e241224f605436ae9f06f01ba0f31f5fc941fd4431d62`  
		Last Modified: Tue, 23 Jul 2024 01:06:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c934f25dfcf9de9f16e47a2fde109ba262dca0c1794676bc143cfc85e06b0035`  
		Last Modified: Tue, 23 Jul 2024 01:06:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aadb5f5446ee91f84517ab3e7e27c621f07b97b5a05a8b23ac4310d6b368a09`  
		Last Modified: Tue, 23 Jul 2024 02:04:13 GMT  
		Size: 18.3 MB (18349900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0428ce529f2bea01b8df1741462292c1b0b1608385485dea2b93a0025b97fd95`  
		Last Modified: Tue, 23 Jul 2024 02:04:08 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:6140a0514b58c0afe122915f3c5657f41e1ad342117e4428f813896a586ad94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1031059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491f1e2f1a7b42d5fa85441b042564d56cf7b1f34b033e5a85a13798ea347c73`

```dockerfile
```

-	Layers:
	-	`sha256:56b651b58fc7f1ff4c2c027965896bf82f84cb2c4ba987d62061854860c98477`  
		Last Modified: Tue, 23 Jul 2024 02:04:12 GMT  
		Size: 1.0 MB (1011113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b618a7da928028ed776b684ce264d93b322b2a489b4fa905d216eb5eac1947fc`  
		Last Modified: Tue, 23 Jul 2024 02:04:12 GMT  
		Size: 19.9 KB (19946 bytes)  
		MIME: application/vnd.in-toto+json
