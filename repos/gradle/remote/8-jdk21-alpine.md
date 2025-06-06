## `gradle:8-jdk21-alpine`

```console
$ docker pull gradle@sha256:1010bd96a3d9809be14007fcd38b755d9171b0d88d229c97be17fb7c5d8398d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:ea534db974eda8e78c86cc40a0754e257f704c524096d70dc4101026208ce26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361187630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724495ccb5e38e6094bbeb1ca18d0a1caffe7fba448a79811f094c7b28423f7f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='76dbb5152f15e509a5fc965936b2b912f806bb977853ab028c362c5340b1c4e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        x86_64)          ESUM='79ecc4b213d21ae5c389bea13c6ed23ca4804a45b7b076983356c28105580013';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29b21f5b2c17ebc06e9a99b3cfcd3cfc8e8a3fed872fff81641100e99586c42`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 21.0 MB (20951300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370873e386b22025c28fa9279cae3a1cd222ac243a221679834774d0620fa7f3`  
		Last Modified: Thu, 08 May 2025 17:04:52 GMT  
		Size: 157.9 MB (157856438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb1def311668c63d0555cfb562a2dc952ee1c071f75d5f1805f7e6383c36365`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa49a465cc24db7df330480bc605cd2f13f785972d1645eeff0397c467e58380`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ad10442ad77496b1d1295cb44e7cec523affab43cad7ee55ae76ca4c6e2d53`  
		Last Modified: Thu, 05 Jun 2025 20:24:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bcd013a94421cc9f2c21f12239135fab7371595149ca73522eed9d1bd058bd`  
		Last Modified: Thu, 05 Jun 2025 20:24:18 GMT  
		Size: 41.3 MB (41283141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d08ebe8e9ca1613a48ccd8ebee02337e2e0be16f5733a20f47aae959508cb`  
		Last Modified: Thu, 05 Jun 2025 20:24:32 GMT  
		Size: 137.4 MB (137396142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeec7d4b0c2ab41e5b8622b4d3e08d92837d519f3c89d31c6104aaf9412578e5`  
		Last Modified: Thu, 05 Jun 2025 20:24:18 GMT  
		Size: 54.9 KB (54908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:e569b183507dbc16825889c8d4ca998b2c12b514be2c96c8329b20d9374688f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4751722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce64c04ce8a50da385d59a7d16790159bd656bed953a842e1fde45af1db6121`

```dockerfile
```

-	Layers:
	-	`sha256:f7e485017b144fc760b1e636967b683705007f385748cbb76a667ab27083f8f9`  
		Last Modified: Thu, 05 Jun 2025 20:19:14 GMT  
		Size: 4.7 MB (4726737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66bb4ae61f70d58bab877757c5db80fa4cff5038dc93f37282b201cf3c089002`  
		Last Modified: Thu, 05 Jun 2025 20:19:15 GMT  
		Size: 25.0 KB (24985 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0e29db7926b5b8a5cb937050b47130284bdea0302d9a7d46712547c98bde4b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.2 MB (359182550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07634bc97b872a68de0a5204bf4f7cd4b124b0d9c058e8ba5532d5e76c4a0d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='76dbb5152f15e509a5fc965936b2b912f806bb977853ab028c362c5340b1c4e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        x86_64)          ESUM='79ecc4b213d21ae5c389bea13c6ed23ca4804a45b7b076983356c28105580013';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4dc4c8e3ac1404ce7eb282c94493325536d142e577ef37ec27bcf3edd09f4b`  
		Last Modified: Thu, 08 May 2025 17:06:52 GMT  
		Size: 21.0 MB (21006028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d79f5ae0d2c93d793230f628662fd05f2016bef787341ed080547de9a7f64ca`  
		Last Modified: Thu, 08 May 2025 17:07:40 GMT  
		Size: 155.9 MB (155857547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2937cc8994b85ca279db22cd32ec1c5629507ab48f3cedc8aa18f2e2fd9a5e`  
		Last Modified: Thu, 08 May 2025 17:07:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6eb77cc48cf78e63aa9b791516daa245f630c71218c0e01f1f3b964f2a4eb4`  
		Last Modified: Thu, 08 May 2025 17:07:26 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e583e4df707c58b86e35fc098dcdc5e3e8eccfab64e326abc267bfe63c11f0b2`  
		Last Modified: Tue, 03 Jun 2025 13:58:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ca693fe327cfd246f042d800584f38569cb67702d24b51932f9fcd2ef9fdc4`  
		Last Modified: Tue, 03 Jun 2025 13:58:01 GMT  
		Size: 40.9 MB (40867132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e68f36dc4d07e90d81a04beef49289ad39338809f607f54d2e5f0c813882ba`  
		Last Modified: Thu, 05 Jun 2025 23:23:05 GMT  
		Size: 137.4 MB (137395811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7ebde23b4823ec352ebec76447b92eb965207ebd0a2e0e0e325bc3a846d232`  
		Last Modified: Thu, 05 Jun 2025 20:10:05 GMT  
		Size: 59.5 KB (59550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:e031a7f337b8cd4130a6e852536fbe3daf5f80bafce8f0ac7e7ec9bab6f74ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4902191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d844fd966c2fd10a4058df660b4efde73eaf2e80c0f73f6c11f5e90f95a9a24d`

```dockerfile
```

-	Layers:
	-	`sha256:42fa2ea716ab5a42408b4dad2a784e6266d7ecabe8db710614b3ab173eac617b`  
		Last Modified: Thu, 05 Jun 2025 23:19:29 GMT  
		Size: 4.9 MB (4876961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485277c1805a9b7bb123cd7c1f3b56415c920971a8e3eeb698dbb1d6dd84bf2f`  
		Last Modified: Thu, 05 Jun 2025 23:19:30 GMT  
		Size: 25.2 KB (25230 bytes)  
		MIME: application/vnd.in-toto+json
