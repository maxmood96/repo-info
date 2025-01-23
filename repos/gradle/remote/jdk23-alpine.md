## `gradle:jdk23-alpine`

```console
$ docker pull gradle@sha256:6178c0b80c3209ed05524843daec16714299f2b19c57f1cd136904d564381b10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk23-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:79aaf244af6fc97162ef71b80cf2031bc4d69cc00624df89d96e1f52111ff79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.3 MB (359282508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459890b560e74e311c27e5a471e2bb3f5a171bba9f29b111da8ebadb17d34fad`
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
ENV JAVA_VERSION=jdk-23.0.1+11
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Jan 2025 15:45:23 GMT
CMD ["jshell"]
# Tue, 21 Jan 2025 15:45:23 GMT
CMD ["gradle"]
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:b036c7155a60b615396ddad215fb861a167307052837fe5cbea35c1c2efede2d`  
		Last Modified: Wed, 22 Jan 2025 18:29:13 GMT  
		Size: 20.9 MB (20908701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6794ccc64e3c7639382edb891b5478057ccc395d93c6712bc3e6ec88a888d1`  
		Last Modified: Wed, 22 Jan 2025 18:29:17 GMT  
		Size: 165.5 MB (165513270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab353b9580c12ddc17b81c4b55561ef1ec3fc19289bc332abf9c261d13500ac`  
		Last Modified: Wed, 22 Jan 2025 18:29:11 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318d9b065e9f4dbfdadc4e637ddf25a427c4ded49283151a4f6abf879e4dd167`  
		Last Modified: Wed, 22 Jan 2025 18:28:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e927ddb262a1ebc03160f7a3930e3cdbb81e2ede3011950f157174981743c361`  
		Last Modified: Wed, 22 Jan 2025 19:32:53 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1916764bb53685890f0e89cdf7254ca585e9d4834943e51366893fb81595521d`  
		Last Modified: Wed, 22 Jan 2025 19:32:53 GMT  
		Size: 32.6 MB (32596468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9999ff7972ce2a13ba9424c29f096e2f636a39229909e8724dceeb97203de7`  
		Last Modified: Wed, 22 Jan 2025 19:32:55 GMT  
		Size: 136.6 MB (136563987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365003005fb781416de04362c4fa2a9b73010a45a8fe2676fc24ef02385afa4d`  
		Last Modified: Wed, 22 Jan 2025 19:32:53 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:fad2fb1c4d1de0412d562e01ae3c803231c9c312a26863517684c0561a2c2343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3371063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f60e89b03d9d0d342c213069acfdfc05da6be932ac4c0e635f8d6f85554f7f`

```dockerfile
```

-	Layers:
	-	`sha256:0156998219085d47381e4c38c77a708c4b70ddd30fc414c64a3b4e15e4632692`  
		Last Modified: Wed, 22 Jan 2025 19:32:52 GMT  
		Size: 3.4 MB (3350151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4103e7726dfe0ecbfeaa3f29af89e0839b60707f780827355fafaa86c3a0298`  
		Last Modified: Wed, 22 Jan 2025 19:32:52 GMT  
		Size: 20.9 KB (20912 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk23-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d42f14b3e9f477c7781f8bc5233660e147e6779f69d245b88241e8eb7c006cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (355984680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efc6f0faa2c48bbd06597580585d17b3177d452ce87aa36cf89d247c5035ef5`
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
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:f1bbbd31510343a48ad85d8eb5271f29474a062af26db072842b265cedbebf51`  
		Last Modified: Wed, 08 Jan 2025 22:24:19 GMT  
		Size: 163.3 MB (163315877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d5a373cae903ba2284309e6c480b8b7059d21583d5f833cfc77927aabd4563`  
		Last Modified: Wed, 08 Jan 2025 22:24:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1618db5c82c2ef581bd482cf264175fc635fff361d83cb0cfe1166d3be65fcb9`  
		Last Modified: Wed, 08 Jan 2025 22:24:14 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6a860603590fc7750059b6f50f689014568c1027dc8f00b31fa03d6fe9c302`  
		Last Modified: Thu, 09 Jan 2025 07:05:34 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f77981274526cd0283edc06b449fc9d900b63067763bb408a90ed0349a70506`  
		Last Modified: Thu, 09 Jan 2025 07:05:36 GMT  
		Size: 30.9 MB (30905224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55afbd90e976a01a10934ac322e20d173f0037bd9485aa960c4810580bd3297`  
		Last Modified: Thu, 09 Jan 2025 07:05:38 GMT  
		Size: 136.6 MB (136564216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d496c15de76d7900d97c6a202c064014c56e425c4fb22a532df640f3c69ba`  
		Last Modified: Thu, 09 Jan 2025 07:05:35 GMT  
		Size: 59.5 KB (59539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:ccb2e3e69622bcaf6a00419f0b553ebecc6e435076251c05c77bf5d4a298c5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3436807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ccd6226c8ab64eb1c0acf6ddd1aef59b1b1c45cd9c73a45b3a81d35f8553b2`

```dockerfile
```

-	Layers:
	-	`sha256:e9b9c11a7c6c39f2edf41b5659b81e5ca65afc17fc96a2b04f96efd72df756d8`  
		Last Modified: Thu, 09 Jan 2025 07:05:35 GMT  
		Size: 3.4 MB (3415746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6ef106c14e72e16589aa7fdecd1ffb14670725811ecc92a429ea120c6ca1d6a`  
		Last Modified: Thu, 09 Jan 2025 07:05:34 GMT  
		Size: 21.1 KB (21061 bytes)  
		MIME: application/vnd.in-toto+json
