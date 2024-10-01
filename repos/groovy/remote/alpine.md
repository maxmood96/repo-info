## `groovy:alpine`

```console
$ docker pull groovy@sha256:f041993afd4b6eafc5517d612c221148f5a14fd552baa11e1ca4062921bcf1ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `groovy:alpine` - linux; amd64

```console
$ docker pull groovy@sha256:56937eb80690199ef2e96fc768320b965f675cc01922b17b6ff36bdb2805c635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192031297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5772b0e3125131ff5ceeb5078ce6be01b7bf6f7f7df4c893aa0993f05adf81d6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6d274a292a717a6f8d00a3ed0695497405c5c634c27fec1692dd13784f6ff6fa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Mon, 30 Sep 2024 16:23:25 GMT
CMD ["groovysh"]
# Mon, 30 Sep 2024 16:23:25 GMT
ENV GROOVY_HOME=/opt/groovy
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Mon, 30 Sep 2024 16:23:25 GMT
WORKDIR /home/groovy
# Mon, 30 Sep 2024 16:23:25 GMT
ENV GROOVY_VERSION=4.0.23
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && (rm -rf "${GNUPGHOME}" || true)     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm -f "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Mon, 30 Sep 2024 16:23:25 GMT
USER 1000:1000
# Mon, 30 Sep 2024 16:23:25 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c34627c847892ee87160ccb0488eb4484039dd04d400e9e86561f15459495`  
		Last Modified: Fri, 06 Sep 2024 22:44:13 GMT  
		Size: 14.0 MB (14032627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a797ec6e8389f8017685a5168b0bcd0ebec6f42e3bfb325a3f260d56afc8b5`  
		Last Modified: Fri, 06 Sep 2024 22:44:23 GMT  
		Size: 144.4 MB (144394608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e3299f059b933428266eb1e665628370ebb22006295cae5f33b8294545ba3d`  
		Last Modified: Fri, 06 Sep 2024 22:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538a095b96fac90e1a596046e0c0d4d75aa1451f8f278cdfbe5148c9ea35b5d7`  
		Last Modified: Fri, 06 Sep 2024 22:44:11 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c457890b07cb62fb254fbb0ef87824b6acfa67ec4a8fb41c55c3c5c125ca04`  
		Last Modified: Tue, 01 Oct 2024 01:02:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48378a8f383f363b6f871f3f1b2332500e05bcb3e9b4ca7f92c2b06290b085`  
		Last Modified: Tue, 01 Oct 2024 01:02:46 GMT  
		Size: 30.0 MB (29976774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104fc86e6d3bef550de695d3e5db399323eed9af83d9b93fc03ea250a1e35ae8`  
		Last Modified: Tue, 01 Oct 2024 01:02:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:alpine` - unknown; unknown

```console
$ docker pull groovy@sha256:eab8d32552a4742107be83e3c211d187a67845385728aab516c7846f57c58f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1064965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01b45e478253ec271bf2d4fb9ee6a3ff437a4389f1097a8b637983ca6662f31`

```dockerfile
```

-	Layers:
	-	`sha256:bed028417df2b4d05792be8bb918c493a29733bb12e62c2781e1544b90aad473`  
		Last Modified: Tue, 01 Oct 2024 01:02:46 GMT  
		Size: 1.0 MB (1040823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fe86f00791d67da50409bed643c47150e2ab40241025da2b49e054abb28056c`  
		Last Modified: Tue, 01 Oct 2024 01:02:46 GMT  
		Size: 24.1 KB (24142 bytes)  
		MIME: application/vnd.in-toto+json
