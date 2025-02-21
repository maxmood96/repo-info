## `gradle:8-jdk17-alpine`

```console
$ docker pull gradle@sha256:8dbab10c7aeaf06c8b486555c76e3dcdb3181c47f90a57ea325e8722858a6759
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:8-jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:8e0366384082c1039c19fbd617340f141e1d901d0b4b33c5d1c5f9777f08c000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337529371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0254cb3b8ea2a1db854d7b1952f497c1a7d34081ddeaf23cd8d746f7780a99c3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='259c85e16f7bbfdfb3e0a2ec1c5d6e2063300d413422286583265a9d8a882358';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 06 Feb 2025 02:49:08 GMT
CMD ["gradle"]
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Feb 2025 02:49:08 GMT
WORKDIR /home/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_VERSION=8.12.1
# Thu, 06 Feb 2025 02:49:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER gradle
# Thu, 06 Feb 2025 02:49:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
USER root
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005dedaf12fb87fde98fc3799c94d82baad509672097fa595795ade7db4dbb8f`  
		Last Modified: Fri, 14 Feb 2025 19:25:52 GMT  
		Size: 20.9 MB (20949824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b93bccf647f23c56b988b134e0f24ce8aed01ba9162e974330b45abc9f2b21`  
		Last Modified: Fri, 14 Feb 2025 19:25:55 GMT  
		Size: 143.7 MB (143716354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c444d2c2cdf16cd81d9bded68ea50c3e23f3bdfb487b1e8eee9d03a206c05142`  
		Last Modified: Fri, 14 Feb 2025 19:25:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c67efadec52153c3e21caad3dc817dc99704b643bec8d9324830842d5d29b6`  
		Last Modified: Fri, 14 Feb 2025 19:25:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ada6264c6bfa2b6345856777e051edaa68348b2384b3d5b0985fd890d85fee`  
		Last Modified: Fri, 14 Feb 2025 20:34:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfd288d7c40ae2945f812a3a89133f86fec0a99fd8434365be54e324626d354`  
		Last Modified: Fri, 14 Feb 2025 20:34:57 GMT  
		Size: 32.6 MB (32600559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af041e4641658188c58b4f456430875d59ca515988143b14c2241b13cc5de7e`  
		Last Modified: Fri, 14 Feb 2025 20:35:00 GMT  
		Size: 136.6 MB (136562022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1367c710a7815e5d04cee46d484bf1868cf364ff4138ba81d7a72c29f23af7`  
		Last Modified: Fri, 14 Feb 2025 20:34:56 GMT  
		Size: 54.9 KB (54911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:f7b81ef2b7c07ffa4f8c9d871d83cf204dc807aa8f5104d7d379f3827a5ba531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3368356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ea9ce9e5e97e29807710448d1aff8e599f447f82f30147a1674fcedaf0b87c`

```dockerfile
```

-	Layers:
	-	`sha256:5153cdf3b1045763be6471adf8e2a2a477d39e0065d5eb67a83f775d3b71c87d`  
		Last Modified: Fri, 14 Feb 2025 20:34:56 GMT  
		Size: 3.3 MB (3346804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1336fe5c3fae44cb1a5fc320dac4273f95c60354daa120cad82880a240996a4`  
		Last Modified: Fri, 14 Feb 2025 20:34:56 GMT  
		Size: 21.6 KB (21552 bytes)  
		MIME: application/vnd.in-toto+json
