## `jetty:10-jre21-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:bad06f162151fb74e315012188c7035035038c2422eb2624002d152cd6683068
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:10-jre21-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:abbbf97d18c6c6bc2d3974a12c99c045b2ab054ca31e20781ee930ad958c9567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85433889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b72c291d0f7498712dbd77756b38b1c36fc667ae7963b86c636ed64af4739f`
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f495749fce8d8974323f30428c1183168f90592dc90bb94c96edab33ffccc94e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f499e2d5c596fd531c8427b2fb207c9eeabed783adad32aeed64b03dd476a231';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_VERSION=10.0.25
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.25/jetty-home-10.0.25.tar.gz
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 12 Aug 2025 07:13:40 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 12 Aug 2025 07:13:40 GMT
WORKDIR /var/lib/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 12 Aug 2025 07:13:40 GMT
USER jetty
# Tue, 12 Aug 2025 07:13:40 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 Aug 2025 07:13:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 07:13:40 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a46580b98941ec4960dce678993b8f83a0b4d2d146c9d4e59e3aa6e788c13e2`  
		Last Modified: Mon, 04 Aug 2025 20:13:22 GMT  
		Size: 16.3 MB (16280189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f9d657519484ce2f35f23c98dec4ef4411ffbb8df53ae594b3563de635b94c`  
		Last Modified: Mon, 04 Aug 2025 20:13:24 GMT  
		Size: 53.1 MB (53137934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf466e9ba1cfaf9351b9b793d92033975eb18f8b2ffadf9b5720caea1fcb9f48`  
		Last Modified: Mon, 04 Aug 2025 20:13:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb760d495f93020b467e7edca17a273394c877a25c14ce0d90a9a039e90bcb08`  
		Last Modified: Mon, 04 Aug 2025 20:13:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb9a1cdc41be1dd18516951e1a02c81b31429b89fb69ce8e0d6a373070d3910`  
		Last Modified: Wed, 13 Aug 2025 18:27:33 GMT  
		Size: 12.2 MB (12211793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eeac98813095ef3ebbfd5d0f10e53f01d71dc09d817866a25d3cebe3ab54fb`  
		Last Modified: Wed, 13 Aug 2025 18:27:30 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jre21-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:98100930979d2ad0c9088ea5a867bdf98b1f0e449621700796558897ddcdc311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1036639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff309b8e21ea51f972c82ca16427fa52be7748a48d0b0360725af49bc493b831`

```dockerfile
```

-	Layers:
	-	`sha256:4b5009b70d365bd4f7789e20710827cd3761b96fcf4fa368d330140796dbaefc`  
		Last Modified: Wed, 13 Aug 2025 20:16:52 GMT  
		Size: 1.0 MB (1016615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a261ab3be0d687f729d0f90d0d20f91722f37731a7700eb3756925536c128f`  
		Last Modified: Wed, 13 Aug 2025 20:16:53 GMT  
		Size: 20.0 KB (20024 bytes)  
		MIME: application/vnd.in-toto+json
