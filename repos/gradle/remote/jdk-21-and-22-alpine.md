## `gradle:jdk-21-and-22-alpine`

```console
$ docker pull gradle@sha256:a91195018348778890dd183a6018b4da3bac9288dfc8e47115f8a1914a5b9e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-22-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:f314d02cdeac08722558f54fce03724757d28233159249584a17bd48e51df624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.5 MB (501530722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5943c8e99a0a1238f6127212ae0c22241e93b94b38407225fc925dc8faf4b807`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 12 Jul 2024 03:13:38 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk22 # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk22
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e118bbc909a65083d314d2da5fe1f703619cf9810828b0d739ed6962de633f2`  
		Last Modified: Tue, 23 Jul 2024 01:06:33 GMT  
		Size: 13.0 MB (13019343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e3150815912943854e9da00bedbea033ff9c14aa65ecc14a40a7b3c6794540`  
		Last Modified: Tue, 23 Jul 2024 01:09:39 GMT  
		Size: 158.8 MB (158815453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ff9fc66c32a6a3d808f1331e8c8013bcae0148202aaafd087f535ffdd0e0b`  
		Last Modified: Tue, 23 Jul 2024 01:09:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5bd5d0f19bc0be0ab9a6d6d8ac05c50aeaeb491ba52a88a149395b81ea936e`  
		Last Modified: Tue, 23 Jul 2024 01:09:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3baa24e7957f7f9abd3a4e632018d9084e2ba29851fdc9a0f6adba06dfeefa`  
		Last Modified: Tue, 23 Jul 2024 02:01:27 GMT  
		Size: 156.9 MB (156935654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026ef4fd8e39655352ad75b60fa8c9a62367a4e30e22a2124d7cb5db11cda0fb`  
		Last Modified: Tue, 23 Jul 2024 02:01:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d93bf863c003073460abaae2245bb84c645dd78e4696a10be3dcfeac664bab9`  
		Last Modified: Tue, 23 Jul 2024 02:01:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb4e7cd0c5880fe5b5adeea488e10ec9535b220698f8ea9af42b11201fbce8f`  
		Last Modified: Tue, 23 Jul 2024 02:01:25 GMT  
		Size: 33.0 MB (33002021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cddb3dcda37e5819e256b4fb6ff794d682352dfc41f92a363c2c8a78e865c9`  
		Last Modified: Tue, 23 Jul 2024 02:01:28 GMT  
		Size: 136.1 MB (136132146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c171702b5d2fdc5c7f39f1f891813f1335d045e0bafc01c87e58ab5e265c1385`  
		Last Modified: Tue, 23 Jul 2024 02:01:25 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-22-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:08dd0243a0aa1b54ae4f0e618a356f6bf57a31e6790d515d5d2ffd106801e07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3078372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a392c7d3d9dd9d4520d26e7ae7954af7a55fa2a91301eaac39f3749d12f03`

```dockerfile
```

-	Layers:
	-	`sha256:593d8cda6a6968609ab465d28a5f1d632c78c357539f813447d23a17d658e23e`  
		Last Modified: Tue, 23 Jul 2024 02:01:25 GMT  
		Size: 3.0 MB (3047796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54dce6e785408d960b43c15cd83bddda0f2aab474d26b8eb50c7e0d7cbd8c02a`  
		Last Modified: Tue, 23 Jul 2024 02:01:24 GMT  
		Size: 30.6 KB (30576 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-22-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3fb929061b8f9fbe89131536cba3d8743c3a0a53c0fbe920d7a6e9f2dccbe974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.0 MB (497965074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec97d14870f584afc69efcfa0d604a9a8746fc2b9810320ccd27bf38f8bad7f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 12 Jul 2024 03:13:38 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk22 # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk22
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a966f22073e059f7f40825d33c5f5b14883597bbd313cc9566f6949f9549339`  
		Last Modified: Tue, 23 Jul 2024 04:14:40 GMT  
		Size: 13.3 MB (13301136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03beb0be73ef790fb48ba172c7044734c9f7413e5e8a6701d3e5f59b4d84754a`  
		Last Modified: Tue, 23 Jul 2024 04:14:48 GMT  
		Size: 156.7 MB (156728985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46b45c0f8ff6d70640017cf68d3fa3cf098ddf85e1f0293b12452b7bc15bd72`  
		Last Modified: Tue, 23 Jul 2024 04:14:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f48ebe7ce17adf2ecb7b03bf08601986a64619644900cd2669fcf9a8e0367e`  
		Last Modified: Tue, 23 Jul 2024 04:14:38 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db214bf0ae20bd167ff784a7b9aafb77117a5ea40ed8d6a08f17d40589cdf56`  
		Last Modified: Tue, 23 Jul 2024 17:46:24 GMT  
		Size: 154.7 MB (154683699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe000ebff89d3bb663f399e20721184cf1f6990419469a4b87b26b14a7ea30`  
		Last Modified: Tue, 23 Jul 2024 17:46:20 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf74d3d814afb2f124f88ff82996614ea8d8568fdbeefa972b1c381be4a84d2c`  
		Last Modified: Tue, 23 Jul 2024 17:46:20 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc822c3551f2d1c771e129f68060338c2724dec4a86eff24f186e4bd7195000b`  
		Last Modified: Tue, 23 Jul 2024 17:46:21 GMT  
		Size: 33.0 MB (33028957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d999288fd7d4d39251d2ad7ef40c47c60a29927d05d718ef4dfb23a4bcd02e8`  
		Last Modified: Tue, 23 Jul 2024 17:46:24 GMT  
		Size: 136.1 MB (136132147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fad90f97b3b6895d7aec71b7b39b0fd07e1b653072e25a33a31cfa1842b38ff`  
		Last Modified: Tue, 23 Jul 2024 17:46:21 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-22-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:54ac4ac56138f6930b8aae67bb2b6623506ee73c2857c01239cb9e0844efdd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7591fa53b779a0f75d44382429fc99e77bb0a1fc0f780e2d88f8ec47ce0317`

```dockerfile
```

-	Layers:
	-	`sha256:ec001864433748fabbdc9b5353e79c473e3906053d81ff67f0062b8897cb7dd1`  
		Last Modified: Tue, 23 Jul 2024 17:46:20 GMT  
		Size: 3.2 MB (3153253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11fdf81f169cae65aa8310ac446e82ed55e4cd752375df2d5f7344269eff4ace`  
		Last Modified: Tue, 23 Jul 2024 17:46:20 GMT  
		Size: 31.2 KB (31197 bytes)  
		MIME: application/vnd.in-toto+json
