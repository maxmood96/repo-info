## `jetty:9-jre8-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:bb021a28f23c3c2e07e1dc256ec26f73193ff53082ed57f9bf7d3b112f06b47f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:9-jre8-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:59a71d120060dee501e0a201239a9f49041c61f231a412c9898d0afb65813247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72745982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9710f5952e7e992a3f9df781ae464ec47a25f1d3541289015bd069df8308351`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 09 Sep 2024 08:47:04 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
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
ENV JAVA_VERSION=jdk8u432-b06
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7f7c265560dd5a42533bf282831d7d2f044a7ff7f4c310b40a0f9f8e19ff12e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae4a7091318439a22582d83eb8aea2835f2d69cd676dda553fee3e529df2828`  
		Last Modified: Tue, 07 Jan 2025 03:31:03 GMT  
		Size: 16.0 MB (16005457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af11ddd595e2b74a9b722af0c9dafadead6e3bba40f85f2315287ced3705fcf`  
		Last Modified: Tue, 07 Jan 2025 03:31:04 GMT  
		Size: 41.8 MB (41818718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9431085ea9f47302df8b525243552dbfbdedb7f0e9d4ae4b5fff0bdba985338e`  
		Last Modified: Tue, 07 Jan 2025 03:31:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2433f318eeaf47ceba55c535d79c262193cb62bbf946de4b0c11cf6100a1f9f7`  
		Last Modified: Tue, 07 Jan 2025 03:31:03 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f388091b75965205b46d350c2d8b9f3025c58b78bc973a7ca8c3bdcb55e3152`  
		Last Modified: Tue, 07 Jan 2025 04:20:22 GMT  
		Size: 11.3 MB (11303734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24da4af1cb55ba9592fbfd23b6aa211d8e6dc7d7dbefabd833f11fc5b55d79fa`  
		Last Modified: Tue, 07 Jan 2025 04:20:22 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jre8-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:f7c8953ed9421ec61faa7dbe24a26ae3b1da0fa78885bae3cb62af350f3078f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1033861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f5b502d470ea1f21c7478317292002c992a0e7c2150bcf260a0d705d60da97`

```dockerfile
```

-	Layers:
	-	`sha256:d9ec308b294ad588f22274a44b59fcdc1b698f88bfd5c8217e79f2e55ad0c6cd`  
		Last Modified: Tue, 07 Jan 2025 04:20:22 GMT  
		Size: 1.0 MB (1013833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c19b7527ba98937f9c179d4fc03aa83893ca1a4863fde6180b9fdd7c534a55d`  
		Last Modified: Tue, 07 Jan 2025 04:20:22 GMT  
		Size: 20.0 KB (20028 bytes)  
		MIME: application/vnd.in-toto+json
