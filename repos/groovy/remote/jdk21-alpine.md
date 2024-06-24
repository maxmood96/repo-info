## `groovy:jdk21-alpine`

```console
$ docker pull groovy@sha256:f5e9f1d84d5f3c15acf33bf07a0f32a07926d89f6be18d11b3309c9643e63e01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:jdk21-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:e5ec5e7db9923311dc99dcff3f28d3b82baee98b01824d7a3e2f4780404f7064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205137437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c152f845485a8f356b11aeea3d91cefab2c80d6abd09662591b0c39d16ce4c6`
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f68a9122054149861f6ce9d1b1c176bbe30dd76b36b74c916ba897c12e9d970';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|x86_64)          ESUM='8e861638bf6b08c6d5837de6dc929930550928ec5fcc81b9fa7e8296afd0f9c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:2dc2499efbfe7968f2522df896fbe2f8a8c2134f7cc93e191f836eec5d02edb4`  
		Last Modified: Mon, 24 Jun 2024 16:43:37 GMT  
		Size: 158.7 MB (158716169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c492bf7da0e834114a9d2878918d8cfe522854c4df9fc7730e2f4b72b32775`  
		Last Modified: Mon, 24 Jun 2024 16:43:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d851ea679543ce279a7828ea806caaaa880c9ae89f2ded39374d44dd11a2fd2`  
		Last Modified: Mon, 24 Jun 2024 16:43:24 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef014722d931e94b445f695b482f67460934441f920e2ad5d18548bc5b12373`  
		Last Modified: Mon, 24 Jun 2024 17:57:38 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792fe1bacd4786f6f0ff7da83c18415670a804b867963a373973a25c839124f6`  
		Last Modified: Mon, 24 Jun 2024 17:57:40 GMT  
		Size: 29.9 MB (29859011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef792939e0325d796259a0c0106cd4e002ee3c321e2fc3b8bd82f6194ff0a5c4`  
		Last Modified: Mon, 24 Jun 2024 17:57:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:70719eb9db43ff6bcc565feccd07949b00c825544167b303b60cd171201862f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1253713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbff59b002f364baeccead2304b9f18328ecb778caa7b88c62cc4f257f36891c`

```dockerfile
```

-	Layers:
	-	`sha256:113952d030e2b4b2f2b8b244fb502c43a51185fcf6af2290858e346b5587cc45`  
		Last Modified: Mon, 24 Jun 2024 17:57:39 GMT  
		Size: 1.2 MB (1231741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:925bdd9784faecc39050ca1647d7ba351e7e303c0c913052a034e3a066677208`  
		Last Modified: Mon, 24 Jun 2024 17:57:40 GMT  
		Size: 22.0 KB (21972 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk21-alpine` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:8b60e559f801aedf47b17c03a6dcaaa042abc4ef578405a70dd5a3a45ea2df4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203293888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1e57a14bfd339baf94278c1bdd4c70bfc634eaa0ad1bbb172a7271827b8390`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 17 Mar 2024 02:31:45 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f68a9122054149861f6ce9d1b1c176bbe30dd76b36b74c916ba897c12e9d970';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|x86_64)          ESUM='8e861638bf6b08c6d5837de6dc929930550928ec5fcc81b9fa7e8296afd0f9c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db88ea1e6a26d6517be6a6098be6964b10513b0bfdfea893bc9752c9c04b6e1`  
		Last Modified: Thu, 20 Jun 2024 19:04:39 GMT  
		Size: 13.4 MB (13425513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b0682e580b8b1aea7e2a977909ae9bbc90e100935552a7b6421a8e6dc7d1b6`  
		Last Modified: Thu, 20 Jun 2024 19:04:48 GMT  
		Size: 156.6 MB (156642191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5483442b5e5e84e7ae2ea9fae5136bd6c4f733ea6148becc7c0957531e3cd47d`  
		Last Modified: Thu, 20 Jun 2024 19:04:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133900c1550c17ba4fc70c056a0119b660f80ef8f03f73d3a2cf42e890cb8136`  
		Last Modified: Thu, 20 Jun 2024 19:04:37 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21ca1f6b2a1aea3944c906e2a998fe19991e46a1006e7af8ab7907390db71a8`  
		Last Modified: Fri, 21 Jun 2024 07:29:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc162ba5a8fbc926847a6f4626540e0a2318b1e8cff3c8cc7107585da0d20467`  
		Last Modified: Fri, 21 Jun 2024 07:29:31 GMT  
		Size: 29.9 MB (29866606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b128f420d04a17e4748d7ba393668257544fdbe1b1ef980af50e30c728d5bbf`  
		Last Modified: Fri, 21 Jun 2024 07:29:29 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:814ac8657c19a9ede4d0afc18c2b5f37f42f82d237cf8c8a8391cfe1056f8834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1359318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754a5b28ea4ddddc142935db12d556a964e94f8cfa8cdbf962bd7b67538d2c15`

```dockerfile
```

-	Layers:
	-	`sha256:126543bc4429b651e21e3b62a1c13fc1902710c2f21ac8b201f1c4d868e28f1d`  
		Last Modified: Fri, 21 Jun 2024 07:29:30 GMT  
		Size: 1.3 MB (1337040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2779290e6f71bd902fc1fc5d29e8c139f2d5781d7b3f7d84ccbc707e9e50471d`  
		Last Modified: Fri, 21 Jun 2024 07:29:29 GMT  
		Size: 22.3 KB (22278 bytes)  
		MIME: application/vnd.in-toto+json
