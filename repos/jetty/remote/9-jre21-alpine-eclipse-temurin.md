## `jetty:9-jre21-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:57d9fed10599d3ddadc3fccbcdf2135fc1d00fd6b69334baf49847b27e8727da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:9-jre21-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:c23b7641ff1b43cd594c1242f7a3c762e1d654c7715130c78ec380a934c74723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84223061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39c472876dbde9f4530d935d3f049681242ac1ec2342e6440f742d26585b637`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 14 Jan 2025 05:07:03 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='53877576d3a9dcbf2024789208aa5f045cc65a5645b07d67124b09c2a84f4e1a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        x86_64)          ESUM='f252e13683b381f9f3bfa4948c827ebd80b8e5bd444a1f99de02c56d76c7ad4c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
WORKDIR /var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
USER jetty
# Tue, 14 Jan 2025 05:07:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 14 Jan 2025 05:07:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cd406c8d97cafcb893e824126c17fa19907b2bbc8d759931089e1be1e75750`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 16.2 MB (16176564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f6a226ed936757680facf9b217f62a2af16b663a69df8e4b3ece925e27ed2a`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 53.1 MB (53059918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6744199aa66ab985e37e72924f1568a6751afa2c508c42a1b3b945f3a8850a7`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda86626eeb372589c3378d030f4522ba1b0c78ec58b1db87960fa4e5fcd3e34`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b533db45b4a553b78d9b090116e1a306330f7dea31b5a12419af6d417e0def`  
		Last Modified: Fri, 09 May 2025 10:04:09 GMT  
		Size: 11.3 MB (11340233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b71c80c0bfaf5052ebf72cdefcbbae5419bc715187706e38655ca6d87845f83`  
		Last Modified: Fri, 09 May 2025 10:04:08 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jre21-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:20e05d6cdfc1e7c2532f1e741436f624baa8fb23864dee6c6e4faf28117870d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1018475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf59d174824fcaff8f093e2f63a40a698e1ab6ab62bd558f26ebdc1625cec94`

```dockerfile
```

-	Layers:
	-	`sha256:7b93b22017c09f6209840370534aaea1ef229d5e7738b11e80adc0fdb77cbd5f`  
		Last Modified: Wed, 04 Jun 2025 16:55:11 GMT  
		Size: 998.4 KB (998427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a08a7f090e0d1b8cb8022075f3a5d9dd382dcbb602cac8ec37158e73358de3`  
		Last Modified: Wed, 04 Jun 2025 16:55:11 GMT  
		Size: 20.0 KB (20048 bytes)  
		MIME: application/vnd.in-toto+json
