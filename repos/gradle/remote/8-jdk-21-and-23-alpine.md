## `gradle:8-jdk-21-and-23-alpine`

```console
$ docker pull gradle@sha256:c0759f3e3c044bd11800825203f25b10d841fd42ba97d486c232aec016613a2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-21-and-23-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:98cc59ebe8be5b4082d3520bc91b20f644074fb304d2809c62ca9ed8d4d9880d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.1 MB (517062380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d673266643e33049714e67b5f588959135fd4a982d902c16077899642b98399b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Jan 2025 15:45:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 15:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Jan 2025 15:45:23 GMT
CMD ["jshell"]
# Tue, 21 Jan 2025 15:45:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Tue, 21 Jan 2025 15:45:23 GMT
CMD ["gradle"]
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Jan 2025 15:45:23 GMT
WORKDIR /home/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_VERSION=8.12
# Tue, 21 Jan 2025 15:45:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
USER gradle
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
USER root
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dd9da19be08de8eeb42d3f2f5bdb9d0952fe4dbb564ac392c809214d2fcb94`  
		Last Modified: Wed, 22 Jan 2025 18:27:57 GMT  
		Size: 20.9 MB (20908652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa228cd6761e4035fad401c9f20acf8bf991d6a9dbdb4bcff3e041095457a35`  
		Last Modified: Wed, 22 Jan 2025 18:27:59 GMT  
		Size: 157.8 MB (157779493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46732d7b5e2c50958fd20897caeb7d830ab5ccd1fcc233d7f15254879bfbd728`  
		Last Modified: Wed, 22 Jan 2025 18:27:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9486ecc987a6a559a8e3cbc55b64d16dd26729eea5b319ac691c82331b4b945`  
		Last Modified: Wed, 22 Jan 2025 18:27:57 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6571aaaa6998906258efcf061b053d27ccc46808eced780dd6f2e76be7ecfc`  
		Last Modified: Wed, 22 Jan 2025 19:33:20 GMT  
		Size: 165.5 MB (165513371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f29534440a6165cf3b86244524e55b296ab0bb315fb1c8f69d25962f7cd432`  
		Last Modified: Wed, 22 Jan 2025 19:33:18 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742b027ba7ef19ce106db602f3a91a7563046f9490fefbd2905f56881d4ad6b0`  
		Last Modified: Wed, 22 Jan 2025 19:33:18 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba1b7aae30c786a345e2776a0f5ea8a169632407cc79209e7ee6987998567df`  
		Last Modified: Wed, 22 Jan 2025 19:33:19 GMT  
		Size: 32.6 MB (32596390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05aa98cc3923425962974e9cf4ecbb068e531b3f7852fe7264760f203c941dd`  
		Last Modified: Wed, 22 Jan 2025 19:33:21 GMT  
		Size: 136.6 MB (136564113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ae03a97d646776b0ec61c8f8c7a4fa0840569b1ed23eb5e7163127cc3c6158`  
		Last Modified: Wed, 22 Jan 2025 19:33:19 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:c13ac922a77575a666e7ae943c469accc70161b50332461a82b1eae6eb5f060d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3537326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c855705035f51e84569a0a5eecdbe55b7e21feda766d7f8099f8e7ae776de99`

```dockerfile
```

-	Layers:
	-	`sha256:6d6adac68ea5a099a240ca95c9e1bfa12fcf50c1035fd5867872f6ace9c57d5d`  
		Last Modified: Wed, 22 Jan 2025 19:33:18 GMT  
		Size: 3.5 MB (3506630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31da7976b306d3db9e7febc302ab23176acaa170d21864a18821117c9ad85595`  
		Last Modified: Wed, 22 Jan 2025 19:33:18 GMT  
		Size: 30.7 KB (30696 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-23-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c271b1e2213989e178b3e80b214a577387b233bc7060d69acbc0c891f6db8bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.7 MB (511725078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6ae345f34d2c0a7b2e647979e5d20ab7ce4ebcd14869bb6e6caf36cc07633a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Fri, 20 Dec 2024 17:54:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER gradle
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER root
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc244ccb78c83c616d89c961944730515db1ce4b088ac7593cc03ac34c0d4128`  
		Last Modified: Wed, 08 Jan 2025 22:23:07 GMT  
		Size: 21.0 MB (21045593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd6d9e215458bf60cc37b5f9d43f854e2f7deb3e214d789e41a5532191628dd`  
		Last Modified: Wed, 08 Jan 2025 22:23:09 GMT  
		Size: 155.7 MB (155740223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b43c975953e9ceb754b9f33b2cd8438d8575a721a6688e782191cee70cb27db`  
		Last Modified: Wed, 08 Jan 2025 22:23:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c95cdcd14fec6605b67e15ca570f07f28c8f118f89e0e0f1b67d30c33df163`  
		Last Modified: Wed, 08 Jan 2025 22:23:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eac65a68b73adad943f46b48a9f11928e5c695c5b00fa40ced8b491382c8db3`  
		Last Modified: Thu, 09 Jan 2025 08:45:20 GMT  
		Size: 163.3 MB (163316142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c5cfa68417cf0ccfca69f26e25961bd3ec869e601e2544d336ad0757604406`  
		Last Modified: Thu, 09 Jan 2025 08:45:16 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7737c9009c0a2453af8b9539d5808c14ec894d405adaffdb6dc09ed3c890b21d`  
		Last Modified: Thu, 09 Jan 2025 08:45:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dda146f268bfc73162deb1b57975f641d1371f71923c12fde9e7caef8d3d09`  
		Last Modified: Thu, 09 Jan 2025 08:45:17 GMT  
		Size: 30.9 MB (30904851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516c5261b8b9cb372470994b04540867282c9941d766ab2c924c2c07c0806533`  
		Last Modified: Thu, 09 Jan 2025 08:45:22 GMT  
		Size: 136.6 MB (136564222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22406c58c796b54df0975cf27df98a749c030fb4fe08a6a27ea6c392f65a8675`  
		Last Modified: Thu, 09 Jan 2025 08:45:17 GMT  
		Size: 59.5 KB (59536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:a6afc93fb1ed98097573ec61fc13204f2c614ba9959ebccdae9fcea687bb5170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f35c5720c177cc8d1655e24d70ab70ce21c291dff8925764a244f9a0bddd2a`

```dockerfile
```

-	Layers:
	-	`sha256:9da14350bccdac787895dddd386e9817ffd02b7661a28856c0c9a18bb45c96b7`  
		Last Modified: Thu, 09 Jan 2025 08:45:16 GMT  
		Size: 3.6 MB (3571651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b670415e4683e7185d9c6ed65ff84bcc6b46d328135bf3da553117e09e0a4b`  
		Last Modified: Thu, 09 Jan 2025 08:45:16 GMT  
		Size: 30.9 KB (30934 bytes)  
		MIME: application/vnd.in-toto+json
