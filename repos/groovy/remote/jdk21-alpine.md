## `groovy:jdk21-alpine`

```console
$ docker pull groovy@sha256:f67f2831165d72932c730b86ac3ff19b8be59a6e0647ca9a5ce9485f1b713b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `groovy:jdk21-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:803fe9c8c3dedcc046b2086b9ef3c3e5f2efbd9ab53fadb4e81fc968063ae33b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205013794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8931a7b844f2b5d1c48f75cba930f2379802377599c7a898b0d9f5957bfbab`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 20:31:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 20:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 20:31:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 20:35:02 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Wed, 24 Jan 2024 20:37:20 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 20:37:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ae933ea8eeb4a077f19277842ba95ba93d29177e44d53cec7a98afd3b9abb2c3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|x86_64)          ESUM='f1aef3652dd52778e81eb4897a88a34e38ca0159d22f160f7205e69907a0f14d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 24 Jan 2024 20:37:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:34 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 20:37:35 GMT
CMD ["jshell"]
# Wed, 24 Jan 2024 23:09:32 GMT
CMD ["groovysh"]
# Wed, 24 Jan 2024 23:09:32 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 24 Jan 2024 23:09:32 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy
# Wed, 24 Jan 2024 23:09:33 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 24 Jan 2024 23:09:33 GMT
WORKDIR /home/groovy
# Wed, 24 Jan 2024 23:09:33 GMT
ENV GROOVY_VERSION=4.0.18
# Wed, 24 Jan 2024 23:09:43 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Wed, 24 Jan 2024 23:09:43 GMT
USER 1000:1000
# Wed, 24 Jan 2024 23:09:45 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd32a74211c33dc91f4cd7a11dcd5977fcc3b3b6fe8b435951a5341b744d80`  
		Last Modified: Wed, 24 Jan 2024 20:45:45 GMT  
		Size: 13.1 MB (13138023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403c4d877b998762482a66a1422cf786267c9e5922268272b329bcc52faeaa41`  
		Last Modified: Wed, 24 Jan 2024 20:49:10 GMT  
		Size: 158.6 MB (158613071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73eef162f2708025567f5ef6c94ecbeb2d6e85e4343cc96da83093367a375ca`  
		Last Modified: Wed, 24 Jan 2024 20:48:58 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d13e04fe5ba030085094d071302edb0ad176664bf8e7361bc4fed4004c6117`  
		Last Modified: Wed, 24 Jan 2024 20:48:58 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e5ab6ec5764418762478bc5984d7b9146c372d36962c9fc887755e13b19600`  
		Last Modified: Wed, 24 Jan 2024 23:12:42 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b398ec4ad7bcd8f0933eb19e3654a184433ffb68d9b8c3cd738db2599ed13157`  
		Last Modified: Wed, 24 Jan 2024 23:12:43 GMT  
		Size: 29.9 MB (29851801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1066de34752e950d4d82288d32915214ab572e94aa7045a161ee8a1d9cef2de`  
		Last Modified: Wed, 24 Jan 2024 23:12:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk21-alpine` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:b6af757893f075ba6b84528752c32a1beaef79bbd7fefad0c123037cdbea1cac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203210468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574aa5cd61bec9816b49a57a09e7b38205a2f8aaa5373cee6552449b96e7caf4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 20:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 20:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 20:44:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 20:44:07 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Wed, 24 Jan 2024 20:44:08 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 20:44:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ae933ea8eeb4a077f19277842ba95ba93d29177e44d53cec7a98afd3b9abb2c3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|x86_64)          ESUM='f1aef3652dd52778e81eb4897a88a34e38ca0159d22f160f7205e69907a0f14d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 24 Jan 2024 20:44:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:44:22 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:44:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 20:44:22 GMT
CMD ["jshell"]
# Wed, 24 Jan 2024 23:23:39 GMT
CMD ["groovysh"]
# Wed, 24 Jan 2024 23:23:39 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 24 Jan 2024 23:23:40 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy
# Wed, 24 Jan 2024 23:23:40 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 24 Jan 2024 23:23:40 GMT
WORKDIR /home/groovy
# Wed, 24 Jan 2024 23:23:40 GMT
ENV GROOVY_VERSION=4.0.18
# Wed, 24 Jan 2024 23:23:50 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Wed, 24 Jan 2024 23:23:50 GMT
USER 1000:1000
# Wed, 24 Jan 2024 23:23:51 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192fc929b7a22573607d9ca1dd17681f2d36fa48e4022e8d4a19e8f711d7a971`  
		Last Modified: Wed, 24 Jan 2024 20:53:05 GMT  
		Size: 13.4 MB (13418260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d044c2a7afa1ec9e8c30b6fac2ee7ec47fdf306c95cd4aa274764409f67cf8e`  
		Last Modified: Wed, 24 Jan 2024 20:53:13 GMT  
		Size: 156.6 MB (156587913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a059ac7d034d7d2075920bfe9aef95393437717603304e3937252946f3aaba`  
		Last Modified: Wed, 24 Jan 2024 20:53:03 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d307a8fc344ae8f849a7883adac745dfbf6eda3b4d0037e2092e867ad3ed0ebc`  
		Last Modified: Wed, 24 Jan 2024 20:53:03 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd88b720017497d583c0205ceaf66aca55c1404c4f80e141b00f3939a0b67ee`  
		Last Modified: Wed, 24 Jan 2024 23:26:02 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b308a87aae757a17221cbc84ea0e9f30e69d8f6c96b5f492e6434a449bfda9a2`  
		Last Modified: Wed, 24 Jan 2024 23:26:04 GMT  
		Size: 29.9 MB (29854080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761833a59e07619f4631cc089877cfb369f4d167a2ab4221515bd5636df44bd7`  
		Last Modified: Wed, 24 Jan 2024 23:26:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
