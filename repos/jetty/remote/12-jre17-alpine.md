## `jetty:12-jre17-alpine`

```console
$ docker pull jetty@sha256:bd459f3dbab38536f284357086671d9116ed22943cbb0d570bb33dcb4e8835c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:12-jre17-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:8452d51142450253251fb0fdf8c5abcaaefebcfcc1db993c4d8433ecb523d3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102619477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3090a4c0be290ec73c6303421ca64deb1d8be47840b3b9070b48b327844de5f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='88424be8b71d7c801c39866cf19d3b7c49b1c499cdccfa292e103c7cba08c21b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_VERSION=12.0.25
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.25/jetty-home-12.0.25.tar.gz
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Aug 2025 04:54:08 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
USER jetty
# Fri, 15 Aug 2025 04:54:08 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Aug 2025 04:54:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Aug 2025 04:54:08 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2752d65a63e3b8c4fb7950d2928bf6d39b65f2e10205b7bd13ccf5294fda1fba`  
		Last Modified: Mon, 04 Aug 2025 19:11:28 GMT  
		Size: 16.3 MB (16280115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d077c3d94f53d4cc9f31623b79dfdf4d879371fb6b3eab31f31f44109e12af30`  
		Last Modified: Mon, 04 Aug 2025 19:11:38 GMT  
		Size: 46.7 MB (46664526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6416375b2a72eefb771654e6a1bb9ca50021d4e891a59c6feb058b7ecb5d0`  
		Last Modified: Mon, 04 Aug 2025 19:11:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b392aaebe6179613c78f2474bff6aecdd37380275b7d032d281864c29542def`  
		Last Modified: Mon, 04 Aug 2025 19:11:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f57bee95599657e1de412244f79e8768dddac7109c4ae7e1e761590983bbde`  
		Last Modified: Fri, 15 Aug 2025 18:20:43 GMT  
		Size: 35.9 MB (35870864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bec988f7e34fb7db42d15c49094ad77cda5e5a7f5c24d70c42d8bc6bb934763`  
		Last Modified: Fri, 15 Aug 2025 18:20:37 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jre17-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:47fb9696cd9375dbc6d935cd0dcdace025fd016df3eee6412c08fb3751ad4250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1150554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1a110bb673f3e7ba01b2897b73d9775bfa800fdc3024e8bb0d0b4a78acf06a`

```dockerfile
```

-	Layers:
	-	`sha256:9e676aed05822f09743efcdc73fbaa3aca901fe04ad32a3ca15bedfdc3927de1`  
		Last Modified: Fri, 15 Aug 2025 20:18:12 GMT  
		Size: 1.1 MB (1130529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac10a9c48ff12ce8f540b5014c2875f45d76bba806264219866b5450aef73a7f`  
		Last Modified: Fri, 15 Aug 2025 20:18:13 GMT  
		Size: 20.0 KB (20025 bytes)  
		MIME: application/vnd.in-toto+json
