## `jetty:10-jdk21-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:3553532fcf515e721eee9473671a67f213c75807ec89769fd81a269ae13e759f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:10-jdk21-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:12edc8ad6024cebcc10bed9f40d92930e19f0a1352ee41aa061e948bd9fb7af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194142581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc7393a6e4653d285479053dd481d134373f779a80d6e5bc36948df5dbbbd04`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='2798990401d9c47eaeddb7d5148f577770e4c1013b9223290a43765463204ae4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='6c66470a9143ad562570a34c1583d9fa50bf904f6f9ced642e9d800ce043a0f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
CMD ["jshell"]
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_VERSION=10.0.24
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.24/jetty-home-10.0.24.tar.gz
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33fe879d02392d66b67cba4600cc2872bada6f0f9c6f12e03bc28954c9503c3`  
		Last Modified: Fri, 31 Jan 2025 01:30:49 GMT  
		Size: 20.9 MB (20908701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0604c1456bc1265d3c8fef31af65e2afe27c2f05223a629ee8933b6b82c3573a`  
		Last Modified: Fri, 31 Jan 2025 01:30:51 GMT  
		Size: 157.8 MB (157796936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d557eba0d26ec5bacef2322f762e2de53fd7c1ed89b725d0647ff0c90cdfefe`  
		Last Modified: Fri, 31 Jan 2025 01:30:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06733b8ef551c6a41488c7d76cb827857b548eb7effee9aeb3e77e88663c9b30`  
		Last Modified: Fri, 31 Jan 2025 01:30:48 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857084942042ed33a7b393fa2a868122d27eb77b87781d430a5cf378721f72f2`  
		Last Modified: Fri, 31 Jan 2025 02:15:34 GMT  
		Size: 11.8 MB (11791126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b952d04a94fdbc25d703733b294370ed0a7891c52302b7988afa4e14c192be20`  
		Last Modified: Fri, 31 Jan 2025 02:15:34 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:66f59bf781b5711e66df9d00a0abf67e1c0fda554d06f148359200174760225c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1233627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f50c78d52277e2964f888b84fe27348d987688e39490ecbca8e9aabe2013e4b`

```dockerfile
```

-	Layers:
	-	`sha256:a42cdccb90e91241ca282fe2182350eddb0939802aaf08fa9ee1b052882eeebb`  
		Last Modified: Fri, 31 Jan 2025 02:15:34 GMT  
		Size: 1.2 MB (1213600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28350d12962d9b1b65a11c02568703ef94534844d745b6f556fbd353849e266b`  
		Last Modified: Fri, 31 Jan 2025 02:15:33 GMT  
		Size: 20.0 KB (20027 bytes)  
		MIME: application/vnd.in-toto+json
