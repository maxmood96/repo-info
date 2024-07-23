## `jetty:9-jdk11-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:21e2e0e864dd28e130dcb0f32801c7d555f656e7f9230d91c54814bad8e681f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:9-jdk11-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:06ef92cc2a7ab7e6f1b82903b09a8246cd8b917093d1c3f0d5a03df5d58eb06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170063851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3545be5951c9309c7bdafac3b241641e4ae53a36e1f3a8735a46cb02f94f75`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 08 Jul 2024 06:35:54 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b45c467be52fe11ffd9bf69b3a035068134b305053874de4f3b3c5e5e1419659';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f359cd8d0e18fe23ad96c88a4ed275ce3c28c031f134b2223544d799cb126`  
		Last Modified: Tue, 23 Jul 2024 01:05:20 GMT  
		Size: 8.5 MB (8537043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87267a151054e11857fb24bf9e6346353ea09cebe4ed3ed139eb18460fe0c4`  
		Last Modified: Tue, 23 Jul 2024 01:06:04 GMT  
		Size: 140.7 MB (140686030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f874197a9f80451cacd73e17573fd76276f089d329bb564115fbc0f2c830d1d1`  
		Last Modified: Tue, 23 Jul 2024 01:05:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb836745c0f2669509f78a387d020a86cfca8379fb4ef0f3136942bd882edd`  
		Last Modified: Tue, 23 Jul 2024 01:05:53 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef4c174e2d4597796580d412a6500e23d5d06515f7dcb802c540521f9b5462`  
		Last Modified: Tue, 23 Jul 2024 02:01:48 GMT  
		Size: 17.4 MB (17419197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdfcc96fdcde1510b6f536b83804aead48b209244e757067672be25f2a0c56b`  
		Last Modified: Tue, 23 Jul 2024 02:01:47 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk11-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:b32bdac807fce6c9cb1f531dad4475d4994a1b9abf4c374f2ff1a3330d70b559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1296923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d490714895b7941c112506ac00618862f8a11ca7cc8a7bf423d9c21e78667dba`

```dockerfile
```

-	Layers:
	-	`sha256:abac63062138b31bed2e8fabb57140884c2b34b47bb181087f6d7389f98eabd9`  
		Last Modified: Tue, 23 Jul 2024 02:01:48 GMT  
		Size: 1.3 MB (1276961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838d438e6c5af71a047d2a3abaf979986317628a737128ceb70a37d54307d703`  
		Last Modified: Tue, 23 Jul 2024 02:01:47 GMT  
		Size: 20.0 KB (19962 bytes)  
		MIME: application/vnd.in-toto+json
