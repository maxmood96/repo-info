## `gradle:jdk-lts-and-current-alpine`

```console
$ docker pull gradle@sha256:c7825e84912bdd43d8da9b705ee126724adcdf672f5db2d1802827909974d00a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:926117d57a10754611b86e96af654a4a821e500706b43ffb86892c85074717d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.9 MB (502914571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e845cfc173df1317db8eecc1860b6df6ba2ba01206f1b9f1cff0680f95425d5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Aug 2024 06:00:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 06:00:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["jshell"]
# Thu, 15 Aug 2024 06:00:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk22 # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk22
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["gradle"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Aug 2024 06:00:50 GMT
WORKDIR /home/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_VERSION=8.10
# Thu, 15 Aug 2024 06:00:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER gradle
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER root
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e64820c602a6421582ff22341d66b5c6938bee2115d203f3d03147a89505e`  
		Last Modified: Thu, 25 Jul 2024 17:29:26 GMT  
		Size: 14.0 MB (14039136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e44e3ea2cb8913609a6cdac111f101c4e181da4d2d872cc22c856078f0b88`  
		Last Modified: Thu, 25 Jul 2024 17:31:10 GMT  
		Size: 158.8 MB (158815391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238c673ab2bbd210a166189cde9795dce4799e4c34f357d90ba8c00ccf6a2172`  
		Last Modified: Thu, 25 Jul 2024 17:30:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b419905a3aad54d3952b04520433835e067c485a4162207785f187aea8578d9`  
		Last Modified: Fri, 23 Aug 2024 19:28:14 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84270218ff390d576ab84453f346b12cf242c55886e0f28b76b3dc7c453cb69c`  
		Last Modified: Fri, 23 Aug 2024 20:05:37 GMT  
		Size: 156.7 MB (156688668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4621ace54418b8847ba267f17faa0a3f6ac86a67d328140ed766fdfa700cdeb`  
		Last Modified: Fri, 23 Aug 2024 20:05:35 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff9a70703ef68df6494c900de214ef56d4ce32ba943c4c2079c308648616500`  
		Last Modified: Fri, 23 Aug 2024 20:05:35 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60e3cadfa7d1b84dc1a6d93a061ad63ca206c728024a36d9416f6dec37d85b2`  
		Last Modified: Fri, 23 Aug 2024 20:05:35 GMT  
		Size: 33.0 MB (33015919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371c9586ab33b61fec0e6a22d0fc473b07bcd0d8cfc48e80ae1757b85857f5df`  
		Last Modified: Fri, 23 Aug 2024 20:05:37 GMT  
		Size: 136.7 MB (136728684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba4082e751d88ef570dcbf721b0c572a38ecc7186538a9b43e2620180afc092`  
		Last Modified: Fri, 23 Aug 2024 20:05:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:beb1e0db71bbf35f097cbaf90d0a5e33826b00d076751a201d6a00c86d6d0dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3105065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550617565c3baf2d4e92e3421f84311d60ca903cfa10e50cafff3acdf9ccfce1`

```dockerfile
```

-	Layers:
	-	`sha256:46fb9f007f25d42b39bf39c3e3918e7a6701b588dd0c71cdfb6dc76428b7421c`  
		Last Modified: Fri, 23 Aug 2024 20:05:35 GMT  
		Size: 3.1 MB (3074478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda7bf48f680e5695da88b7cf7d03aba0b876db10d839fd1f6e57c66c02840de`  
		Last Modified: Fri, 23 Aug 2024 20:05:35 GMT  
		Size: 30.6 KB (30587 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:78252a03a38920c322fbf0c87eabe55c82f104a4896fa3f34c066ac29de01603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.4 MB (499410036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54267376bb5c7e2157af6be0ac31868e560c7a7b441fc449c3dd34613127dea`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Aug 2024 06:00:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 06:00:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["jshell"]
# Thu, 15 Aug 2024 06:00:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk22 # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk22
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["gradle"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Aug 2024 06:00:50 GMT
WORKDIR /home/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_VERSION=8.10
# Thu, 15 Aug 2024 06:00:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER gradle
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER root
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2478f4a9466e915a5997ded853c525c23643a703902fa3b4e95b2c80136f5c87`  
		Last Modified: Thu, 25 Jul 2024 17:46:42 GMT  
		Size: 14.4 MB (14369016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abadc835ffa030fc985e78cb8f354d889f827c5b2839069fedf76f9c6896a83e`  
		Last Modified: Thu, 25 Jul 2024 17:46:51 GMT  
		Size: 156.7 MB (156729061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0158a214eb3542371be651186374a14af2a6fe541da3f11897b547875db9c2f6`  
		Last Modified: Thu, 25 Jul 2024 17:46:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593a67afee94d7f74b36753ba56040649cdd97cdc81687b1822dc07ffa806e98`  
		Last Modified: Fri, 23 Aug 2024 19:45:43 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02149ee7750b28bb492b83afcea1835d5e17cd99977af156761aae530998bd9e`  
		Last Modified: Fri, 23 Aug 2024 22:36:41 GMT  
		Size: 154.5 MB (154451721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b73bc09a8ff1236502fb7bf0bf0ef0466cdfd5fa07b8455301a547c330a8eb9`  
		Last Modified: Fri, 23 Aug 2024 22:36:37 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf67710cb2dc176cb2ecabc0de16f1f0bad5d2981eba1d1d88004022e071184`  
		Last Modified: Fri, 23 Aug 2024 22:36:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8276a9d84f7138458226214707d82fce0d215670617b8b047fd95bf336d0b922`  
		Last Modified: Fri, 23 Aug 2024 22:36:39 GMT  
		Size: 33.0 MB (33040682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2346eaa4dd62384e24c16876e6244502966dc1e4ed439e7e6137966de0e1b0e`  
		Last Modified: Fri, 23 Aug 2024 22:36:44 GMT  
		Size: 136.7 MB (136728737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953e3c5d60ed38747c28ce76ebaefbef3302c36e33455f8fb2935150aef513f4`  
		Last Modified: Fri, 23 Aug 2024 22:36:38 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:d07216b8a430233f5a41d659b715f122631377c58cda7385dcdfcc5ab5e80d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4d00608e7102cf6e08c586332f87f2ed94502d2a39308b32cc60e4433fff34`

```dockerfile
```

-	Layers:
	-	`sha256:80c1f649a7e1279c43c65206980bd63e477c2d33e5de3b46a9ec6b1c9fc909fc`  
		Last Modified: Fri, 23 Aug 2024 22:36:38 GMT  
		Size: 3.2 MB (3179933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496e56ca11e494e894b0e78f3b91509f0d77b42d8bda58e8626f013642442450`  
		Last Modified: Fri, 23 Aug 2024 22:36:37 GMT  
		Size: 31.2 KB (31208 bytes)  
		MIME: application/vnd.in-toto+json
