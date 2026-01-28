## `jetty:11-jre17-alpine`

```console
$ docker pull jetty@sha256:792c77dfed2cd02be89b667d796206c86828c840d420f07514f4fa9c6d9d1b4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:11-jre17-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:0588987872192a53bf1edfc9201f1ce0c08437a273fd848f05707cf6014fbbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82588608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e447dd99cf6891598858dd3e3f6fa5d08d849141f437e4ab77480991905ea753`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:57:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 02:57:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 02:57:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 02:57:45 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 28 Jan 2026 02:57:45 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 28 Jan 2026 03:08:56 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6c3047e8edd3878e8d2a1cee95c04606042c6a55954ad365d20b58f88cc9ecd5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 03:08:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 03:08:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:08:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 28 Jan 2026 04:15:16 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 28 Jan 2026 04:15:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:15:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:15:16 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:15:16 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:15:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 28 Jan 2026 04:15:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:15:16 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:15:16 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:15:16 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:15:16 GMT
USER jetty
# Wed, 28 Jan 2026 04:15:16 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:15:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:15:16 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712170bbbcf08e7e6d5fdc5e77492f5ee689ccc346dfd3323e70ed3cd4ce6391`  
		Last Modified: Wed, 28 Jan 2026 02:57:59 GMT  
		Size: 16.3 MB (16293985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec4236d96f40951be5c39840082eb0bf7c851bf489142edaf46c7902a13d804`  
		Last Modified: Wed, 28 Jan 2026 03:09:07 GMT  
		Size: 46.7 MB (46718954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9247b2da494fffed9d04179a8f1dab65aa3413f202ac970e4af2c4429403c50`  
		Last Modified: Wed, 28 Jan 2026 03:09:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8189bd200c048407210efb45fd23b31a6a50959b4337697e85a6200477c05b`  
		Last Modified: Wed, 28 Jan 2026 03:09:06 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3c1b48a6401e50881b33ab77e9588af5c2f83fd130ceacabcc14877c9c267f`  
		Last Modified: Wed, 28 Jan 2026 04:15:23 GMT  
		Size: 15.8 MB (15766511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605fb4c4afc22d2ac341cecbcf09d4196ee627516f159a22c47940d2590d192a`  
		Last Modified: Wed, 28 Jan 2026 04:15:23 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jre17-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:82cf8ee6402c88ec7aa4e0d99ea1004c67e228d0e7aae289969e7d9b92616a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1038080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf36c119956dc7bb5681668118551f2b1ecbb781b8d171fd2e7294e0e0e67d5`

```dockerfile
```

-	Layers:
	-	`sha256:b3121b7a52055e5661881b5e979d3aff2f4e603051f317367810bf457e96192b`  
		Last Modified: Wed, 28 Jan 2026 04:15:23 GMT  
		Size: 1.0 MB (1018097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280a20f5210339e82f25309b474997c5a74332838211588d205c53123c40b88e`  
		Last Modified: Wed, 28 Jan 2026 04:15:23 GMT  
		Size: 20.0 KB (19983 bytes)  
		MIME: application/vnd.in-toto+json
