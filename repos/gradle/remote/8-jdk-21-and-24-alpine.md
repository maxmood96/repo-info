## `gradle:8-jdk-21-and-24-alpine`

```console
$ docker pull gradle@sha256:da82e20bef19fc09f588d64f6b58005e497874632392743aa8e0c105a668d1e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-21-and-24-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:aa6566ffaffabb4886a11e34b2caf1a9e53aa1c6b65e5af71d90fb7ba06a6fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.6 MB (454601807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ad7c99a7a8e949122584b324d8c808ffdf871bf79c9068640a6d1d0ffb2d91`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Jul 2025 03:50:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4773cfdc59d66b75f4a68ac843b2b5854791840114cf8bb1b56fb6f7826ae498';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='73c4cbe10f4f385383d9cb54d34f2bee2c68b5265f9e3d954f3326948c40c0be';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["jshell"]
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER root
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ba33acdd264f217998366b5d5fe9d078029b368628dd7dfecb38c4f20ff184`  
		Last Modified: Mon, 04 Aug 2025 19:11:55 GMT  
		Size: 21.1 MB (21104336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988afcd1754ba6102804ea7b8ff2f925fc2e53b57ad39c3cde06070767f70ef`  
		Last Modified: Mon, 04 Aug 2025 20:12:02 GMT  
		Size: 158.0 MB (158029044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960c5713500a85841f1ed2768d6f3a06d30e6af02bebbfc8bdb94124fc679a7c`  
		Last Modified: Mon, 04 Aug 2025 19:11:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d23bb5eb8f811c49dae8f456527014d33599bb070f12294d58ce498048c7a1`  
		Last Modified: Mon, 04 Aug 2025 19:11:53 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a46b02268affb00b71c4541e2969a1b20b81d6dad07f9eb5c3a3fbfee2eb44`  
		Last Modified: Mon, 04 Aug 2025 20:13:41 GMT  
		Size: 90.1 MB (90133313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b8b1c04ebb5a6c9f371ed6856aff0a8000ee130c39a04eaeb97e34279dc878`  
		Last Modified: Mon, 04 Aug 2025 20:13:13 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cdab06597294f04a2e68b0fc0800fbed35cafc0e042036ea4da58ec633866f`  
		Last Modified: Mon, 04 Aug 2025 20:13:10 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9a5789ed027c8237573510caad99cf4b1a94c33f5407f4d13eaf76fd982766`  
		Last Modified: Mon, 04 Aug 2025 20:13:16 GMT  
		Size: 44.1 MB (44081049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9eff42c2c7bd7419513dd942c25be5a10e01a49f7eb87f19d0a84fc7c7f49d`  
		Last Modified: Tue, 05 Aug 2025 05:16:22 GMT  
		Size: 137.4 MB (137395741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13deabd4e7bcf522a61a2d8f076a3cf634c3b6591941d6d19ae7d205d39db07d`  
		Last Modified: Mon, 04 Aug 2025 20:13:10 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:60aa602992ccbf02ab5bd48e807e9be42f6dadce671174e34bcdc10d93e20372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17325b882b45db2159cf58e466333ba3814cd77d5bfc1c7a832aa5347d1793c0`

```dockerfile
```

-	Layers:
	-	`sha256:905a421b4095896c5c9e801b88db159b53c30915a0319556b5be13846076d9d7`  
		Last Modified: Mon, 04 Aug 2025 23:24:08 GMT  
		Size: 4.8 MB (4808606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd67ff94c970c6be6478314b974f72b8d2ad6610c29ceb68b9b7fec19dcd0788`  
		Last Modified: Mon, 04 Aug 2025 23:24:08 GMT  
		Size: 32.3 KB (32288 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-24-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5631d147c3787d3dd42146011e60c8663974bf1ea14510b90f63df46ddf6d3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451462643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c0f7b4e9d1b22bf32b9ebc5ab4e07e897686f35139ef3aa2b12979255f23e2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Jul 2025 03:50:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4773cfdc59d66b75f4a68ac843b2b5854791840114cf8bb1b56fb6f7826ae498';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='73c4cbe10f4f385383d9cb54d34f2bee2c68b5265f9e3d954f3326948c40c0be';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["jshell"]
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER root
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a495748323e0cdac275f94a75856b53137d10e7dd79d59568fe601407fb00e`  
		Last Modified: Mon, 04 Aug 2025 19:31:51 GMT  
		Size: 21.1 MB (21148725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686152e11509087fae61a232dd8c14a35ba03ee6d67dc590eff8efd157e12de9`  
		Last Modified: Mon, 04 Aug 2025 21:27:06 GMT  
		Size: 156.0 MB (156022610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a5e3450f3fe69d4cac3d21cb8d6c1c51e6d6f96214aa277c280b7b8c543832`  
		Last Modified: Mon, 04 Aug 2025 19:31:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5af7201f64b2984b23a0f6114fdb4930c66ab8886bf4145e5fce7dda16c5f25`  
		Last Modified: Mon, 04 Aug 2025 19:31:49 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62007284bbb772665b8c015a42fad548fda66f092e52182abeb821d07d86ecf2`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 89.1 MB (89117489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67194274ebf0c5d3771866f4252553ff57920f17dffd30eeaa604d5d047c4850`  
		Last Modified: Mon, 04 Aug 2025 20:50:26 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e770370ff80515e7ca7c82609e6d8022a952de9ad0f4b9cb19d6d8b6cba32566`  
		Last Modified: Mon, 04 Aug 2025 20:50:27 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c64a75ecfa59154fca007c02b5fc7f026eee44489bb56405d0fb6fb077ecf10`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 43.6 MB (43584036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208e8b9d7537a34dae2b4854de99a8ab3f20a909238e0fe871902dd3069aa65`  
		Last Modified: Tue, 05 Aug 2025 05:17:39 GMT  
		Size: 137.4 MB (137395771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d47db4639cd5e7b6afc9a97701eca9dd7905205d9db4e57a36e817193a2ff7`  
		Last Modified: Mon, 04 Aug 2025 20:50:27 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:e88131bc1ee39672b9cad40c408f18f694ad8a6d1f86db824c398360474c2bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4990685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30978f0f0d78c14ec01d28101f4f63a4aa78ece1d93e42bf040e14f52af1c17f`

```dockerfile
```

-	Layers:
	-	`sha256:ab40f3b5a5f775a637877bcc44d3a562b57012842f3ed38741f25873b76bacce`  
		Last Modified: Mon, 04 Aug 2025 23:24:13 GMT  
		Size: 5.0 MB (4958159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d81d5e5f12428f1bee08cc604cb05e7604d0e97e4c795f5426b7a0f9f71169e6`  
		Last Modified: Mon, 04 Aug 2025 23:24:14 GMT  
		Size: 32.5 KB (32526 bytes)  
		MIME: application/vnd.in-toto+json
