## `jetty:11-jre17-alpine`

```console
$ docker pull jetty@sha256:ad1f9a22bf3f5a20cdbb4490a6b88575c33e2cbe91228a84d9faa5ffc88074a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:11-jre17-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:6705c24691c94fe0b73ed8a0d15310a485f3e6ca287a397ab966ba5e544ea804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80609025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90222885a68236fe1a9fc3ae88f9e2c6a216083587f946501d1af3b2578d6dea`
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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5dffd0be08c464d9c3903e2947508c1a5c21804ea1cff5556991a2a47d617d8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_VERSION=11.0.20
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.20/jetty-home-11.0.20.tar.gz
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
	-	`sha256:63d23e9cf3a3a50104650ef5ced46aaea90097d347ea2de4ac6d383c714d6fe4`  
		Last Modified: Mon, 24 Jun 2024 16:41:30 GMT  
		Size: 8.5 MB (8537069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f4495e3c099ff9a9cbd7231503e5e7f292fc87fb7909a2c47a00a9f35ea6c7`  
		Last Modified: Mon, 24 Jun 2024 16:43:14 GMT  
		Size: 47.0 MB (46959732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fefa52dfd13bfe5e56976673c607022ab807a337ece8ed1b3b2fe80b6fc6b3`  
		Last Modified: Mon, 24 Jun 2024 16:43:08 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec78f29d94d3220d72728fd08770c3936f34db4c2ec633448b6444a7d251087`  
		Last Modified: Mon, 24 Jun 2024 16:43:08 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e03940fa04db95fa4f1b0e2dd41f449d8ad4bd5ea6947fb59254e58ace81e3`  
		Last Modified: Fri, 28 Jun 2024 20:56:20 GMT  
		Size: 21.7 MB (21692370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc055cb8ca979f735a9e6fb9d1c87865e71635672db16a1dce8e85c613ea3b3`  
		Last Modified: Fri, 28 Jun 2024 20:56:19 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jre17-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:27327a70e3589f7fe932f9867b5769431e01af726a27e723838669fc618cc55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d118ecce404b3dce7837e81ecda4528347ccaf48bfb1b1aef4fef3f6c91236aa`

```dockerfile
```

-	Layers:
	-	`sha256:17606fee7fcfa99ebe819679785efa3f310389523939857d7635468c58022c17`  
		Last Modified: Fri, 28 Jun 2024 20:56:19 GMT  
		Size: 1.3 MB (1265631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0d37acc95ad2630edeb6da2fee6cb44af8326e13488b46fefc3c0c68aee619b`  
		Last Modified: Fri, 28 Jun 2024 20:56:19 GMT  
		Size: 19.9 KB (19933 bytes)  
		MIME: application/vnd.in-toto+json
