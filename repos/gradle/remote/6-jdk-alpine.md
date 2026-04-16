## `gradle:6-jdk-alpine`

```console
$ docker pull gradle@sha256:bd9615edde90aebec221ed4b7720ab9b12e27584992637972c583f6f6ecd7e5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:6-jdk-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:bef37f829b5ab8132ea77a1b3a22f182b284b7514d5749c9ae4297c4f64968d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314373507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f13c6ee2091529c55e3e51a226641b75711879af1c70ed4d478b4e62e9a588f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:32:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:32:56 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 21:31:30 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 21:31:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 21:31:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 21:31:30 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 21:31:30 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 21:31:33 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 21:31:33 GMT
ENV GRADLE_VERSION=6.9.4
# Wed, 15 Apr 2026 21:31:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Wed, 15 Apr 2026 21:32:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 21:32:14 GMT
USER gradle
# Wed, 15 Apr 2026 21:32:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 21:32:14 GMT
USER root
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec914d871e26d0465399fedbb12a944add78359e4bacb45111654e407011389`  
		Last Modified: Wed, 15 Apr 2026 20:33:10 GMT  
		Size: 16.8 MB (16837789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e0f2de0712b22eb820b820ec9d10381f0162a40034dd9db90063cf9bc5b7f9`  
		Last Modified: Wed, 15 Apr 2026 20:33:13 GMT  
		Size: 140.9 MB (140916718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97836bb5bbf19dc634eaea3ff5cfbc9b0ca22932b1bbb49c9a806a0bb040b842`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c470514f36b76e7d4fbd25626009aade331446b35fde7acb2f42ae8b0b5c53a1`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7bdb183d802176d023968b995984644d22be4490109cc524816be6803691d4`  
		Last Modified: Wed, 15 Apr 2026 21:31:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2217397ff8c86d018eca5baa5678f63337a0487742af4cc5430eeec242fe8e0`  
		Last Modified: Wed, 15 Apr 2026 21:31:55 GMT  
		Size: 44.6 MB (44623419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cd5adb42c640259407e06f0da0e4d29ff0aab31d21f7eb2a8257da6e1e1a2a`  
		Last Modified: Wed, 15 Apr 2026 21:32:31 GMT  
		Size: 107.7 MB (107696678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f587204869388b5ec1fffec67b1a798ce1cb1e006bbe92cf4ec17db70f98b9ee`  
		Last Modified: Wed, 15 Apr 2026 21:32:28 GMT  
		Size: 431.3 KB (431265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:fb2be2806bc0bd015c0ec124121722ca818d96b08120fef03b836cf142a7d7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa8b18fe83c8a5627e6cdd1d10f2e570339b632533f7f9917ede299fb58dad9`

```dockerfile
```

-	Layers:
	-	`sha256:54f08d91ad2305c6b1fa51c75a89b95ae95f0eaedec400e1a1df1ebff28c289a`  
		Last Modified: Wed, 15 Apr 2026 21:32:28 GMT  
		Size: 4.5 MB (4496213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1c463881d3a88df711e1bf6e3c45b0cd1799064de53fe2c6d3dd53b443e7992`  
		Last Modified: Wed, 15 Apr 2026 21:32:28 GMT  
		Size: 24.0 KB (24003 bytes)  
		MIME: application/vnd.in-toto+json
