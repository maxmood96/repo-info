## `jetty:11-jre17-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:2355f47fe30879e1e9fa8d39e80f30995f44bf91d049967c3307440d56175682
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:11-jre17-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:c1680848e6e92e0b958efba48de01a3b622cc3a5589861e8432c5c7e20c5b926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81167473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4578cf2cca174c01901c09bb68cac2d2490eec7e45a6b89c94f53ad8f895e1f9`
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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='63bae276cc322532b451ae7473127c92a75db16cc95473577f133cd09349822a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_VERSION=11.0.22
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.22/jetty-home-11.0.22.tar.gz
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
	-	`sha256:0b502c76566e71337b4737a25ae762dd54193bc78dba7f7474ea005c07de9efc`  
		Last Modified: Tue, 23 Jul 2024 01:08:16 GMT  
		Size: 8.4 MB (8371901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b7c21f90c416505c5901e5ae2dc4a6a315754d31af26e1d7d23764d79648f`  
		Last Modified: Tue, 23 Jul 2024 01:08:21 GMT  
		Size: 47.0 MB (46988362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fda088e83ffe4cb0dd87d2788cf604b5681474d8e4ffe7a92e24e0b992b0a9`  
		Last Modified: Tue, 23 Jul 2024 01:08:15 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7031008d0f5d9a0cf6c47471b6ba33130dc95daad90f22cf4837c5ea3d0687bc`  
		Last Modified: Tue, 23 Jul 2024 01:08:15 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01d2a75ab3d7ea9187e6640c17817db678f7c740e39330e32c11cb0553f1cf4`  
		Last Modified: Tue, 23 Jul 2024 02:02:01 GMT  
		Size: 22.2 MB (22181080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8dffe23455205b06c5aa82cf8f0e7ce011234339fc4cfeae2f645ceb235124`  
		Last Modified: Tue, 23 Jul 2024 02:02:00 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jre17-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:f0972bf3b16958c4a68e0f68cb45a6b7d6a2ac647128f97beaf87e7e3574e183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **936.5 KB (936507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae638ea611dfcfebdf87883d2bf904733963080e0727056d76290512fe753d1`

```dockerfile
```

-	Layers:
	-	`sha256:d8b9a6e408b80ea074e9321c67b371507f07a466edb9b3cd791e19278bb48b7b`  
		Last Modified: Tue, 23 Jul 2024 02:02:01 GMT  
		Size: 916.6 KB (916569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4428b4fea9af659d5c209b0fc74a1a13a79b8deaeea0caac4b3b0cc945e37e2d`  
		Last Modified: Tue, 23 Jul 2024 02:02:01 GMT  
		Size: 19.9 KB (19938 bytes)  
		MIME: application/vnd.in-toto+json
