## `groovy:4-alpine`

```console
$ docker pull groovy@sha256:2de5f5c8e9e5f521d3307a29d6933244a13e27cc064acf59c03d21b3824bb2ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `groovy:4-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:5b3641ffb4e6e260bcc835d46886f126614522b8e7c49bbbdd0c859572e99e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 MB (190753263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f40d741b7aa0eaef7a394f886dcd9d1e0ccc2d71a7122570ecacbdd35dd8eac`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 17 Mar 2024 02:31:45 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["/bin/sh"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 17 Mar 2024 02:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 17 Mar 2024 02:31:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='839326b5b4b3e4ac2edc3b685c8ab550f9b6d267eddf966323c801cb21e3e018';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["jshell"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["groovysh"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 17 Mar 2024 02:31:45 GMT
WORKDIR /home/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_VERSION=4.0.20
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
USER 1000:1000
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60acd7138d3e0a8e35e097d75b62e0b1cfd99cdad83e29656157ec622e1c51e2`  
		Last Modified: Mon, 24 Jun 2024 16:42:45 GMT  
		Size: 13.1 MB (13142550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b5e1235bfbe173503864b0745991f6acbc1cb3cc585db25db55cc975d8c4a2`  
		Last Modified: Mon, 24 Jun 2024 16:42:55 GMT  
		Size: 144.3 MB (144332006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b1cd3263773d4ffacbc48e3c623670d0f823ddab3860cd77eb3e012e2c02a`  
		Last Modified: Mon, 24 Jun 2024 16:42:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48fadb2170d58cb6bea4140e5d4cad7173488b82a2763a9f56369fe59647a1b`  
		Last Modified: Mon, 24 Jun 2024 16:42:43 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d093ede3485839a80f5094a02a016c0306ac17003c09d4d44075e2f7aa8f2564`  
		Last Modified: Mon, 24 Jun 2024 17:57:41 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5141f910b88460c4a1927e6a6e21e3bb1988eda0d8503c3df2da8f3e60dfa06e`  
		Last Modified: Mon, 24 Jun 2024 17:57:42 GMT  
		Size: 29.9 MB (29858999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3385675cd38e19a9a9915984d43d1ed8213fbdcf2e01bad2dfd400812e72bbd3`  
		Last Modified: Mon, 24 Jun 2024 17:57:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:b94fafe6f7c9cd16802ae05e178baf4e6138b9a5db442731261c3d8217a24ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1258022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b8f6feee538bb959a2b17c54d52d8238133d5917fe072cdd9e5bc9feefa6c1`

```dockerfile
```

-	Layers:
	-	`sha256:de7d153aef43f1747bb238e2086943b6fbb8e04b88243e828dcf87a199110088`  
		Last Modified: Mon, 24 Jun 2024 17:57:41 GMT  
		Size: 1.2 MB (1233889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa36b728902f4f31d2eb1e6e153fac85a69c08493b257fbd156b8dc31f8e43a9`  
		Last Modified: Mon, 24 Jun 2024 17:57:41 GMT  
		Size: 24.1 KB (24133 bytes)  
		MIME: application/vnd.in-toto+json
