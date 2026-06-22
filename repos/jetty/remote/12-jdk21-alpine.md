## `jetty:12-jdk21-alpine`

```console
$ docker pull jetty@sha256:68730b4f6b433fb9c675ebae402375d223cc7f29b38e155cbee394d4d67f5c3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:12-jdk21-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:778390edbad514865b12ad4a2bc3864ade3423fa972539ddfd5acad40672084e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230237390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3314ddfc2986e644a200fc53fb5c832499accfedeb28450a560c519832e30574`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:09 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:09 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Mon, 22 Jun 2026 19:57:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:57:18 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:20:55 GMT
ENV JETTY_VERSION=12.1.10
# Mon, 22 Jun 2026 20:20:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 22 Jun 2026 20:20:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 22 Jun 2026 20:20:55 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 22 Jun 2026 20:20:55 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:20:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Mon, 22 Jun 2026 20:20:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 22 Jun 2026 20:20:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 22 Jun 2026 20:20:55 GMT
WORKDIR /var/lib/jetty
# Mon, 22 Jun 2026 20:20:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 22 Jun 2026 20:20:55 GMT
USER jetty
# Mon, 22 Jun 2026 20:20:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 20:20:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:20:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42b27ff362c29d4c86173d5eb45dc9fc28c27d52c5791cb63a9113e6f0e3646`  
		Last Modified: Mon, 22 Jun 2026 19:57:35 GMT  
		Size: 21.3 MB (21290130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c90809b4c96d37014d44d53b2f534fcdc3a9b2baa628af103045b46795a7189`  
		Last Modified: Mon, 22 Jun 2026 19:57:38 GMT  
		Size: 158.4 MB (158396795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7ee5d98789e02e3500e8e207c5963d76ea5e48dbe5f519229aeb3847e2bc62`  
		Last Modified: Mon, 22 Jun 2026 19:57:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68dfaba6ad42ab866380109a6c2636053416cb8f6e06672fa092a97451fd747`  
		Last Modified: Mon, 22 Jun 2026 19:57:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08819e82a9e0ad7a949d5db06e8e0f914e436bbfa57c7f8ff43683de3fe6c47f`  
		Last Modified: Mon, 22 Jun 2026 20:21:10 GMT  
		Size: 46.7 MB (46701756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec8b9ce5fd0729afba42fa7936ddcbaebdb8c02f6a20e22aae88e20be82919a`  
		Last Modified: Mon, 22 Jun 2026 20:21:05 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:8f2424d7302996cb4fc911589b43491502e95d8f4e8a171ad28b56919ba9c061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1418130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cc6a3dbd442e45778281ed8aefdb67bec60d42ea65ce3e6f9175bd4de04707`

```dockerfile
```

-	Layers:
	-	`sha256:f5f8f5b2f9e016fe8eba69f64f73fe7e58b047d18bf35ac44663cd773eb93ce7`  
		Last Modified: Mon, 22 Jun 2026 20:21:05 GMT  
		Size: 1.4 MB (1398143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4851f498def6e0bb240c1e20706482adeb66b1a39d75788a5a66a7dea399869`  
		Last Modified: Mon, 22 Jun 2026 20:21:05 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.in-toto+json
