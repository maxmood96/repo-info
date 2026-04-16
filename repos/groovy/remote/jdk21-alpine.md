## `groovy:jdk21-alpine`

```console
$ docker pull groovy@sha256:e5b2268b53c62bbba5510111eefc38ccee2f62a59f455510f6e4c98152dada4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:jdk21-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:19d562aba717b9de5f96766e0e702a812793d97d261dd651fbf0dd718d6aa3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217863828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9026d104fe5648e3db97d0011bee0fdb2b08240b8a0bc3c1f5d43f741a4840`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:52 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:02 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 21:32:26 GMT
CMD ["groovysh"]
# Wed, 15 Apr 2026 21:32:26 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 15 Apr 2026 21:32:26 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 15 Apr 2026 21:32:26 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 15 Apr 2026 21:32:26 GMT
WORKDIR /home/groovy
# Wed, 15 Apr 2026 21:32:26 GMT
ENV GROOVY_VERSION=5.0.4
# Wed, 15 Apr 2026 21:32:35 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 15 Apr 2026 21:32:35 GMT
USER 1000:1000
# Wed, 15 Apr 2026 21:32:36 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ef2c34364d42e41eb14af65c85cfcd9ba8407f18b51bde4f6428bff92388a2`  
		Last Modified: Wed, 15 Apr 2026 20:34:17 GMT  
		Size: 21.3 MB (21315853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136a888652a1277373c20061d1c0d79e332ba8eece5ba04c0c24fce61ce8940d`  
		Last Modified: Wed, 15 Apr 2026 20:34:20 GMT  
		Size: 158.1 MB (158118925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b440bedad35bcaf95f5c16474e5bcdc67677eca1377bc3b6bd9a64aa13552d0`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c1bb0b54884876ce179c9ad3683a68d7689b97597df8b1b2dfeeaaf5e7b60e`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47abba52e8c3bbf385f3b973402daed5358ee1d660ac46bde27abf5353a9b079`  
		Last Modified: Wed, 15 Apr 2026 21:32:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1a9f11c8e920ec16a365bdf0ff9cb3aa5b88e3ddc185fa3744272b33585462`  
		Last Modified: Wed, 15 Apr 2026 21:32:46 GMT  
		Size: 34.6 MB (34561249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeba9aaa0e9c6ebb96143b02f52c627b9100de6ca91d7def9d166bc63e1cbf98`  
		Last Modified: Wed, 15 Apr 2026 21:32:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:3ab4619f46ca39fed20e7248a54f5ad5fd63bf91f3ea33c6ae766508fd39e31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1234516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93ae4fdfa1290e3b3912c80c7af9021e5f220e47d3793c37645f560bdb3c809`

```dockerfile
```

-	Layers:
	-	`sha256:b90c50c5bc81d5d7376108d096825aa2ed8d550af68e33298474524ae38d0f6c`  
		Last Modified: Wed, 15 Apr 2026 21:32:45 GMT  
		Size: 1.2 MB (1209738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40344f145eabe36740f6332c927f449ce847b208e3a2ffe9b83a1433afaca8ad`  
		Last Modified: Wed, 15 Apr 2026 21:32:44 GMT  
		Size: 24.8 KB (24778 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk21-alpine` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:142c378e1cdcde83d158f82e7e345615a8b993271e3198e3d93f749f2cd91dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216209438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7984b837fcf6be3446b58d5bdaacdb97cccdfffc611f810e7ed561dddc169ce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:55 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:05 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 21:45:48 GMT
CMD ["groovysh"]
# Wed, 15 Apr 2026 21:45:48 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 15 Apr 2026 21:45:48 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 15 Apr 2026 21:45:48 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 15 Apr 2026 21:45:48 GMT
WORKDIR /home/groovy
# Wed, 15 Apr 2026 21:45:48 GMT
ENV GROOVY_VERSION=5.0.4
# Wed, 15 Apr 2026 21:46:03 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 15 Apr 2026 21:46:03 GMT
USER 1000:1000
# Wed, 15 Apr 2026 21:46:04 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaacc5fcb81aaf4c24ca62b7c7d748d4925abc4199e39981b80b93898777d06`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 21.3 MB (21303504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea8e162f72eb44c19a73f38e10d121143bdee45dc7426f76cb9f2b16ab73763`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 156.1 MB (156129898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37767c9371d4e03127e4bbe85929010c025d7d442785d1805b213575c0a75fd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12d0e0cbded327c9df870505ef20a84efb14dd8ccbe2a48a63e4120f61b65ba`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e873c73784b52d1b04a134c1583f7fd8ad09558c55397bccd45fb07b7beae`  
		Last Modified: Wed, 15 Apr 2026 21:46:13 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b2385d0d2334d0b1a2c8dc4742987d22292dfb29230812c2e3c45d729b2d01`  
		Last Modified: Wed, 15 Apr 2026 21:46:14 GMT  
		Size: 34.6 MB (34572554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f293fb84d8cca13e27b6946fe7e8cf34b57cfc49bb972d217f74ff0ec255cc15`  
		Last Modified: Wed, 15 Apr 2026 21:46:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:51b2ac69084a76776022d12cecd048a8072b2454316af5f9ac2ef583594563a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1384206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6598d58774d308e3b8e6de21bd9f34919d2e3db9dddec85a4448788a7e1760`

```dockerfile
```

-	Layers:
	-	`sha256:4db06e7b879047d80f17799ea24ff6963a25340b57ccec373dd05669a977c4bc`  
		Last Modified: Wed, 15 Apr 2026 21:46:13 GMT  
		Size: 1.4 MB (1359198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d165cb939ff5e2b51281c9548a2cee627b8091486535e2ea8f5748ee8f0164de`  
		Last Modified: Wed, 15 Apr 2026 21:46:12 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json
