## `gradle:jdk17-alpine`

```console
$ docker pull gradle@sha256:5beee04f4c08985b5522ec7c68611fb8744f2fbbd19227305f544e6beebba876
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:6e76303d25605223c8bf3c79508dbff6bbc79e1463e739e994b526b363bef785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354747864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327f26dcb87bc0311e67983fc395cc27a604f7b95a08d9cbaf726456303bcd72`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:53 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:53 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Mon, 22 Jun 2026 19:57:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='960b4090b75a887bb21a915a294bee3a97cd11876967c95e5bd29d9ec4812e17';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:57:02 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:12:51 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:12:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:12:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:12:51 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:12:51 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:12:53 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:12:53 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:12:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:12:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:12:55 GMT
USER gradle
# Mon, 29 Jun 2026 17:12:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:12:56 GMT
USER root
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb24b7abeaf5ce9e23187de02071382730c0873637800e8a9adcb59301992717`  
		Last Modified: Mon, 22 Jun 2026 19:57:16 GMT  
		Size: 21.3 MB (21290166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9a403ef070b145efc0a24ea5ea18c62cf96257bfefd784d70237ec8671df1f`  
		Last Modified: Mon, 22 Jun 2026 19:57:19 GMT  
		Size: 145.1 MB (145051633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8954f1747c4e5c426ae38631e95b0494950eb78209f25ea413a0d591f5bfd8b0`  
		Last Modified: Mon, 22 Jun 2026 19:57:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f47b51787bf9ee6cbfe3b6ad72acc64ab2cd047c11d06a156720b184193e59`  
		Last Modified: Mon, 22 Jun 2026 19:57:15 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6aeac044a803255c4533e1714c1ac66715aaf4d7b4c8add9c0be67544c2c19e`  
		Last Modified: Mon, 29 Jun 2026 17:13:12 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05197511bca5fb67904a8972c57cd8df7a6d6b6e12342d8882da1051e83568df`  
		Last Modified: Mon, 29 Jun 2026 17:13:14 GMT  
		Size: 43.9 MB (43936210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f9a3a01507a23cd2ffcb6acf5c0ddf6d519c1f777fab9eb3ff73cccf8d8572`  
		Last Modified: Mon, 29 Jun 2026 17:13:16 GMT  
		Size: 140.6 MB (140596357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea5824e632bc6948f8d5a635df19d62cd8f07f9f776847af8d51101216fd277`  
		Last Modified: Mon, 29 Jun 2026 17:13:12 GMT  
		Size: 25.6 KB (25623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:d22ddde0ebe3bc53e88744f0a01c4a3efe53e60a8424fce1c17790d6f3a12f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f745dff84298e432e1dafc246d6ed8475a2da0539576ad973f32dfdc83ddec3`

```dockerfile
```

-	Layers:
	-	`sha256:cbc539298856832e49ca717a73e2c4df7191f765b06db099343dde35c7e041b8`  
		Last Modified: Mon, 29 Jun 2026 17:13:12 GMT  
		Size: 4.7 MB (4708683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a110b440a750a43bff95b21f8350a72d14551212c0036603b11756ed79c1c63d`  
		Last Modified: Mon, 29 Jun 2026 17:13:12 GMT  
		Size: 22.6 KB (22638 bytes)  
		MIME: application/vnd.in-toto+json
