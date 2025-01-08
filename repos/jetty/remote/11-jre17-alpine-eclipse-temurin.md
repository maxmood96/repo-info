## `jetty:11-jre17-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:cd1b77b7692af64c4a66d0448626a4d53d1438376bef56564e6664ddd5ab030b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:11-jre17-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:03410cf2a99ca04e02a575b74aab8b9137723a947090bfed6a8a1803aa776900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81825222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe4fd0c6455121fc5897fe6ff92d6fd2225efe780376d8120306bbf334b1fff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 10 Sep 2024 00:22:25 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Sep 2024 00:22:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 00:22:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7a2df4e2f86eca649af1e17d990ab8e354cb6dee389606025b9d05f75623c388';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_VERSION=11.0.24
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.24/jetty-home-11.0.24.tar.gz
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
USER jetty
# Tue, 10 Sep 2024 00:22:25 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Sep 2024 00:22:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3be6309784e750acbbddcbbec5051aad3fd9304d38121eb182aa37c3b1b0e9`  
		Last Modified: Tue, 07 Jan 2025 03:31:28 GMT  
		Size: 16.0 MB (16005475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227bffdbb3c5798733584f4145104fca6f564817b7bcc24702402a3d6b873e6a`  
		Last Modified: Tue, 07 Jan 2025 03:31:29 GMT  
		Size: 46.6 MB (46615870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecb2a742830ad9ce12a06c34afa3685eb6838ebaa7a41a41dcadd28f989adb8`  
		Last Modified: Tue, 07 Jan 2025 03:31:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ad8ee870f6d136dbf2617f78dd3426ea9ace39a7cb45936425350de1fc4d9`  
		Last Modified: Tue, 07 Jan 2025 03:31:27 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a3f4ed25925e7a85ccc94344f004c6b2ec46b9073c11f72afa5d27fdb8e3b2`  
		Last Modified: Tue, 07 Jan 2025 04:22:30 GMT  
		Size: 15.6 MB (15585803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41994c51d51bd85c1e44583f8c0af325b7229fa97fde7fac2e7d2df86974044`  
		Last Modified: Tue, 07 Jan 2025 04:22:29 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jre17-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:cf4482f803276c75fd9545eb05c1e7b932b8dcb65082ee164777d91f4e7d4bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1015795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3976ff89655d451562f91ea7e9c328b4b177ac54b7fa9a98eb134345ed53fc2`

```dockerfile
```

-	Layers:
	-	`sha256:d1702a02a9c47b177b4bb2f9abbaae7967f121998ca21fcd9cf87aa686331656`  
		Last Modified: Tue, 07 Jan 2025 04:22:29 GMT  
		Size: 995.8 KB (995770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94e3305dee82743316449b88f13cb98d0841800b3c7d2459d4bed628d7fe0ef7`  
		Last Modified: Tue, 07 Jan 2025 04:22:29 GMT  
		Size: 20.0 KB (20025 bytes)  
		MIME: application/vnd.in-toto+json
