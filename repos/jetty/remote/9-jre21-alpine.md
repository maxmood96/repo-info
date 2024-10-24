## `jetty:9-jre21-alpine`

```console
$ docker pull jetty@sha256:354f840ea7027a17538e61a57d6fa2e67817e06efa2580bc11d98e2f6fa67bc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:9-jre21-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:b3d5e82d48ec6fd70f8ae1e1bb2454a33b433d7b357175f57c0a8c05bca85f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86275360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92111c3fb406d8b4d116fedd51999b111657a625699aeaf1477f291a1d0bcdf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 08:47:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 08:47:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='12b988a3d934e3eb89c6a981a93f8e2adf0a62cc9030487dee76c0c29b93714d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='2dfa33fb8e9474e6967c6cf17964abb5ddce9c17fa6a9f8d7aa221a0ae295df9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_VERSION=9.4.56.v20240826
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
WORKDIR /var/lib/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
USER jetty
# Mon, 09 Sep 2024 08:47:04 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Sep 2024 08:47:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21462eb7489fd19f70190aa3178a536d40e967ba1c2fdf9df5bc94504f76c865`  
		Last Modified: Thu, 24 Oct 2024 00:57:56 GMT  
		Size: 18.3 MB (18307433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d754a55bcb1a496349bc9137804190c4b74ef018fea6ec76baa57d287a56c96d`  
		Last Modified: Thu, 24 Oct 2024 00:57:56 GMT  
		Size: 53.0 MB (53039157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b67c35e63fb4b675107f90beff070fa05f274ea3d3759a7d3157bc59473ab`  
		Last Modified: Thu, 24 Oct 2024 00:57:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068e70c969c92dbfa8997ba6c6e565303b33619d300fd9b1ea0b199b539a15c2`  
		Last Modified: Thu, 24 Oct 2024 00:57:56 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b3ada43e600834b7753e28fc3a7a3bf4615ce81855f6b42f3ad417310eadb2`  
		Last Modified: Thu, 24 Oct 2024 01:57:15 GMT  
		Size: 11.3 MB (11300890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3504838257fcb1394d51bb705aacb4e8e974673d3e8754a2abb0d3241239ed`  
		Last Modified: Thu, 24 Oct 2024 01:57:15 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jre21-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:3c005d76daff91cfb31db46a52604f61fcb47840f13cdc7ae19a4d2f432220fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1017321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62a8c32d525b3b4afd2a9207bf3fbd46a7706ee84ec9ab588f23237b3b71425`

```dockerfile
```

-	Layers:
	-	`sha256:5b6135e1d072fb559cf7a8722f177f82a3a99a227d9e9722f9b09bad2d71a258`  
		Last Modified: Thu, 24 Oct 2024 01:57:15 GMT  
		Size: 997.3 KB (997272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d55a526c3e6e5882ce831fb03c65ea2cb2182302c551560d4a0eb8263c23e1`  
		Last Modified: Thu, 24 Oct 2024 01:57:14 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.in-toto+json
