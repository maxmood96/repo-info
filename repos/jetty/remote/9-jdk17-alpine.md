## `jetty:9-jdk17-alpine`

```console
$ docker pull jetty@sha256:e1d10d2c4d3af4daa881a0b2e925dd5589ecdacd33563556f57747ec6d30ca0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:9-jdk17-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:ff38287410570cc53d6af7f7aea0d0ac0d2867cb7ff98cc335642e67d2aa6992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (179965168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4833155479602b025b0317324fda4f8c18bf11c11e2931b271952ea21919513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:10 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4dfea527f66034c5b6f4ca26afe692ae292fd267fd3b295c7f54f6461c65fd33';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:58:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:17 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:17 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:17 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:17 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da2b7fa39d9ca89504884bfa364de57e68f656d1fd46f04941d3d34ffdbca30`  
		Last Modified: Wed, 07 Jan 2026 18:56:12 GMT  
		Size: 21.1 MB (21112255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9308f1b3f4d73b7c1a1aaba0b8eda9e9155caf3619e236d0c1a8b410704ef`  
		Last Modified: Sat, 08 Nov 2025 17:58:34 GMT  
		Size: 144.0 MB (143989616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3851e26ddd2575c157cfd1ad2a673f8e8b4541dd5f6a0b8a2f65d3935e10fe6`  
		Last Modified: Wed, 07 Jan 2026 18:56:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03fcaf37379fff8027b1eaf41f78daa4bf57cd4f423a9e9d7015d3bbcf9bb53`  
		Last Modified: Wed, 07 Jan 2026 18:56:11 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fd13ecc0552e1cff3f98e90809a93582cd0ad1dff36a00da1a4ec28e05e2fd`  
		Last Modified: Sat, 08 Nov 2025 18:26:25 GMT  
		Size: 11.1 MB (11056561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dded897743ecfa084998ed4cf88ecf1940f0b8049ea93d59e1c973b56dd5379a`  
		Last Modified: Thu, 08 Jan 2026 20:14:38 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:7d2efdf78be3778b6c1686c8eb7045b00d6dc48dc00e5e854b764da8009f3092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1226152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e53b88f60f3a92ad01cd6f6d022b68061032d74b83e825488561a9d1559cfea`

```dockerfile
```

-	Layers:
	-	`sha256:c6cd4d6fee21be11bd84c45b16d89f7a04d3c38a86e3f999f0c75f2e3547c90a`  
		Last Modified: Sat, 08 Nov 2025 18:26:25 GMT  
		Size: 1.2 MB (1206141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e569ab6e2386d8ca61914be1830bdae5830bf562284fe45f473e1b9c7af7b39d`  
		Last Modified: Sat, 08 Nov 2025 18:26:25 GMT  
		Size: 20.0 KB (20011 bytes)  
		MIME: application/vnd.in-toto+json
