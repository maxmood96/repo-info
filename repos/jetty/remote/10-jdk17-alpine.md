## `jetty:10-jdk17-alpine`

```console
$ docker pull jetty@sha256:685418917a4ba988cef04d250727e6551f2b93124bbec36d6ba339ff0c02df68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:10-jdk17-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:cabff35bb8ac42bcfcc100c8822d93b9dc92b7e7d6de0e605d970fdbd3e4830d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180694588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bd75b40722f77388d10faa1c61cc7bcbb0798709fc96eac258e43679024091`
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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2e83ac152fb315db0d667761f2120b64504800f641a513044e834a1a41f29bc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_VERSION=10.0.26
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 19 Aug 2025 02:05:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
WORKDIR /var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
USER jetty
# Tue, 19 Aug 2025 02:05:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 02:05:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d125b9b630f45fe9fdd3dc16a36920f92fa7c1e01344de92d6b6e6f6b50c5db`  
		Last Modified: Mon, 04 Aug 2025 19:11:32 GMT  
		Size: 21.1 MB (21104306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889e463e11980d977e77842be54e94ad63e877ec78f1f31eb301c571bf31e842`  
		Last Modified: Mon, 04 Aug 2025 20:12:08 GMT  
		Size: 143.8 MB (143849315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491fe72c6c247575080814d36438026b9d982ae49ccfcf86ff607e533f3b376`  
		Last Modified: Mon, 04 Aug 2025 19:11:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bb5da1a24523a0af1966f13d7bc9ffb567c894c91c19968adcfc1fe0ea1653`  
		Last Modified: Mon, 04 Aug 2025 19:11:18 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf209b0e14a5f381d85ce5581752b18315c921dfc2cb53789301dd2a0e903b8f`  
		Last Modified: Wed, 20 Aug 2025 17:24:01 GMT  
		Size: 11.9 MB (11936994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d1d3ceb42db7a6c2caf2ce5b1f2c715d81a18142f8342038e730ad1ca89a7f`  
		Last Modified: Wed, 20 Aug 2025 18:26:29 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:572acca693668dbe893296c3c488c371fc38fce88689fa04e709b892b3babdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1237800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef96b1dad844b65c814bb12b05985827f8ecc9075464cc1887d90d9a69dc1bcd`

```dockerfile
```

-	Layers:
	-	`sha256:eb865de5e12b1e2ea73a7aa59c58412353c6933b8f5bc3d5094b0fe2f50203fa`  
		Last Modified: Wed, 20 Aug 2025 20:16:14 GMT  
		Size: 1.2 MB (1217771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90237d5fa7c2c34ec670991887b1f36594b8075feba9bbb9e10bf69600417a73`  
		Last Modified: Wed, 20 Aug 2025 20:16:15 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.in-toto+json
