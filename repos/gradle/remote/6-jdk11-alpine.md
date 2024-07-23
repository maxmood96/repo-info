## `gradle:6-jdk11-alpine`

```console
$ docker pull gradle@sha256:e84ee3cd25a518754d6d4d3f36e74e34e76f745da207a804ce16e912a1d8b8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:6-jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:c0bdd9133c1502b6ffa693bd078591c36b87fc23c41286d1d8f2ad6340d7c6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296660896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994b5f85eb4d138a374df86307c13bdfc8092b80aa268a40d70b1a8941f97543`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b45c467be52fe11ffd9bf69b3a035068134b305053874de4f3b3c5e5e1419659';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["jshell"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f359cd8d0e18fe23ad96c88a4ed275ce3c28c031f134b2223544d799cb126`  
		Last Modified: Tue, 23 Jul 2024 01:05:20 GMT  
		Size: 8.5 MB (8537043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87267a151054e11857fb24bf9e6346353ea09cebe4ed3ed139eb18460fe0c4`  
		Last Modified: Tue, 23 Jul 2024 01:06:04 GMT  
		Size: 140.7 MB (140686030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f874197a9f80451cacd73e17573fd76276f089d329bb564115fbc0f2c830d1d1`  
		Last Modified: Tue, 23 Jul 2024 01:05:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb836745c0f2669509f78a387d020a86cfca8379fb4ef0f3136942bd882edd`  
		Last Modified: Tue, 23 Jul 2024 01:05:53 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb4e691159729e4466b40a92a44962abc4734f5768cd86488fc1573b12206b`  
		Last Modified: Tue, 23 Jul 2024 02:02:12 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe2fb82ed0b55375a06ed55181cda4ed165c25d2f0e1e2220e8689e926d111c`  
		Last Modified: Tue, 23 Jul 2024 02:02:12 GMT  
		Size: 35.9 MB (35888554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c61617b0e2106094fed24398a6f37125b4c3930c270034587ed9bfdc5f1dd5b`  
		Last Modified: Tue, 23 Jul 2024 02:02:13 GMT  
		Size: 107.7 MB (107696738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83f3e48aceaf8e8d473ead889e78db3a42b1bbf8410f234a53dd0145429ff8d`  
		Last Modified: Tue, 23 Jul 2024 02:02:12 GMT  
		Size: 431.3 KB (431278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:fae97721c56d454e0251cd2521cf26e29c5a2140f2118be897d61acd8e0a6883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3336647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c4653e1736474af67c42855b3e648a9336b89d1dc31e570cfaf818e421f66`

```dockerfile
```

-	Layers:
	-	`sha256:87eeea8316bcc89cc80d2f7b1b21761e9256b098d56fd2605f32fcdf56a5a985`  
		Last Modified: Tue, 23 Jul 2024 02:02:11 GMT  
		Size: 3.3 MB (3316081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebccb32912beae5fd5b27637b6f48c46041491f4023aee9823f60759d7c264bb`  
		Last Modified: Tue, 23 Jul 2024 02:02:11 GMT  
		Size: 20.6 KB (20566 bytes)  
		MIME: application/vnd.in-toto+json
