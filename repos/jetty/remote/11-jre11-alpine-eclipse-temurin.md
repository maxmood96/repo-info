## `jetty:11-jre11-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:691c1142cbf8ed4295342ae14bef658054acd1ed616b3708d5c34304b68b391d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:11-jre11-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:f6e7b4623746734362fb26345100584c1151c1f196a5607ac339c20f03c0d58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79077115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88125694013cdfa4aed45ca8cfcba637bf745c16095e47f06a5813b9c65c64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:57:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:57:59 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:58:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='a37e818c23e19a0f3f6a77827eac9c6dab572c22efafa6c0e888cce2555d39a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:58:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:27:40 GMT
ENV JETTY_VERSION=11.0.26
# Sat, 08 Nov 2025 18:27:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:27:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:27:40 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:27:40 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:27:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Sat, 08 Nov 2025 18:27:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:27:40 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:27:40 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:27:40 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:27:40 GMT
USER jetty
# Sat, 08 Nov 2025 18:27:40 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:27:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:27:40 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da322013c3a3e15f50b875d45b515b19f6df7ee1a9bc2ecbc19bae96a2a4ced`  
		Last Modified: Wed, 07 Jan 2026 19:03:21 GMT  
		Size: 16.3 MB (16289781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d07fa442272c6b6b7d37eaad510b9abacfb13413bb01971120588a4ea75080`  
		Last Modified: Sat, 08 Nov 2025 17:58:12 GMT  
		Size: 43.2 MB (43214642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f5f62162419ffc91b31a781d9372bd81ae2c5a7b7794a7fb64943e88acf6ed`  
		Last Modified: Sat, 08 Nov 2025 17:58:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c474a9ef5e2665aac3c45c688976fca94a3d70d262d657c659cabae6fde8105`  
		Last Modified: Wed, 07 Jan 2026 19:03:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68990320ffe8c458f04ec4c0f1ffb8cf40881daa9cf1c8eed673ddcfc9fc827f`  
		Last Modified: Sat, 08 Nov 2025 18:27:47 GMT  
		Size: 15.8 MB (15765955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e417058b301e8a41d2c1ae86d6f91ce22e2d8bb748cb63aff9e69fc1028f7194`  
		Last Modified: Sat, 10 Jan 2026 21:48:18 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jre11-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:503defeb5882e84c46c4dd7efdc8b4181985bbdf78c373814face317a384ca05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1050566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1da75cbd99f465bcb5f2ec4e787c337f3cfdf77e58a84889114a8a1b5911861`

```dockerfile
```

-	Layers:
	-	`sha256:2efb2b1b3096b9ed13f488e08dcce4c31f7cfd1303b6418494bf7453e4162905`  
		Last Modified: Sat, 08 Nov 2025 18:27:46 GMT  
		Size: 1.0 MB (1030584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7537ef4dd8adfbfa73aac748442d7a80a93d218e11aa8fcf04a745cd84ea27ea`  
		Last Modified: Sat, 08 Nov 2025 18:27:46 GMT  
		Size: 20.0 KB (19982 bytes)  
		MIME: application/vnd.in-toto+json
