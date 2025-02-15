## `gradle:8-jdk-lts-and-current-alpine`

```console
$ docker pull gradle@sha256:b4b5e53cab723d0df47a0b88c900738cda28e8dd3a30ff55ed151ad29ca40135
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-lts-and-current-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:148befb3917ce5635366248c8941d64042db5a2a57aa357a6eefe42de57cc1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.2 MB (517153814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031988d1ff99a0ca762119181e622fc21a8941339badcbd1bb0436b1f377304`
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
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='2798990401d9c47eaeddb7d5148f577770e4c1013b9223290a43765463204ae4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='6c66470a9143ad562570a34c1583d9fa50bf904f6f9ced642e9d800ce043a0f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 06 Feb 2025 02:49:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 06 Feb 2025 02:49:08 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Thu, 06 Feb 2025 02:49:08 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 06 Feb 2025 02:49:08 GMT
CMD ["gradle"]
# Thu, 06 Feb 2025 02:49:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Feb 2025 02:49:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
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
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2377dc8d3710b6bf7410a46adf016bdb060a8b4a7114189518f7f60fae85e3`  
		Last Modified: Fri, 14 Feb 2025 20:34:10 GMT  
		Size: 20.9 MB (20949767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79312d97e63a3dd5a83b89c90503f5d3c5c8ce261682999e1d12cf54506ac32`  
		Last Modified: Fri, 14 Feb 2025 20:34:22 GMT  
		Size: 157.8 MB (157796824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573882c363c812b21ff606ea7d12eff8720580a29a875238f127d7f80b9f0da1`  
		Last Modified: Fri, 14 Feb 2025 20:34:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1f65d07a350139d7390033a591e07d865c082f4b458bb56ff38bc143349c8`  
		Last Modified: Fri, 14 Feb 2025 20:34:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f211e31433711749be26880eac113cbe1b6a3c098fdaa271d1ce929c9b400`  
		Last Modified: Fri, 14 Feb 2025 20:35:01 GMT  
		Size: 165.5 MB (165543715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178e3be26da556ef92982f28fc35124697ae6b8398b130f2d5a8c0b650c5d9f5`  
		Last Modified: Fri, 14 Feb 2025 20:34:59 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba54b1f06796fc2c639e798ac1f9e730c9fa2aa0f479cab1ab7f5e48a087ef0`  
		Last Modified: Fri, 14 Feb 2025 20:34:59 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fbf3e0c4834a52fd34e70910ee68c1f04a285923cfef6253f8872e77079b89`  
		Last Modified: Fri, 14 Feb 2025 20:34:59 GMT  
		Size: 32.6 MB (32600613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997b6bf2ffb0ed2213bbedf659f934df81a13ef53647ddb11b63bac42ebadb61`  
		Last Modified: Fri, 14 Feb 2025 20:35:01 GMT  
		Size: 136.6 MB (136562015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb2d83ab6daa4efbaf26cc6fc408857152b5b5baa5d490cadf315ee9d43ff60`  
		Last Modified: Fri, 14 Feb 2025 20:34:59 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:7dfd342af3fb79ade8860c89602258b962af867b84ea64ae1ed4d122254a9b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3538349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fad1c7ace6ef510137540f2db5c59c2405664ed2dc1deb2ed86e32ceb29a34`

```dockerfile
```

-	Layers:
	-	`sha256:854091cb65b98d7659218310c8a1481b423f5b6d9d0cd69f97593b77749ea40b`  
		Last Modified: Sat, 15 Feb 2025 00:19:13 GMT  
		Size: 3.5 MB (3507650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1feb4e801a5b3e4a2d3fc3cfb2a36fb33b904cfe991ace55b064bfc1cbacb72`  
		Last Modified: Sat, 15 Feb 2025 00:19:14 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-lts-and-current-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:339861acbb97c5eb5dd18b823576e962a6a5f441c301843a7aea820de9062672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 MB (512973850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d828c2e43b0b6c0e78167681a8d6429cbc5be4572c68ab99f342b6a2d39465d6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 27 Jan 2025 19:22:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Jan 2025 19:22:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='2798990401d9c47eaeddb7d5148f577770e4c1013b9223290a43765463204ae4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='6c66470a9143ad562570a34c1583d9fa50bf904f6f9ced642e9d800ce043a0f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["jshell"]
# Mon, 27 Jan 2025 19:22:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Mon, 27 Jan 2025 19:22:41 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["gradle"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 27 Jan 2025 19:22:41 GMT
WORKDIR /home/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_VERSION=8.12.1
# Mon, 27 Jan 2025 19:22:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER gradle
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER root
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceae889eece3aa36cf341c7932ef99f4d89a493af360439046e550e71531cbc`  
		Last Modified: Thu, 23 Jan 2025 08:04:11 GMT  
		Size: 21.0 MB (20965085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91982b0bcc61d4349a9fcabd87e95668dd380c29524c467c113811ae05961096`  
		Last Modified: Mon, 03 Feb 2025 21:32:39 GMT  
		Size: 155.8 MB (155788009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734a54ac17d43c14f5d87b8bee81f5ec03064c000624d33d054c3e8d6f565587`  
		Last Modified: Mon, 03 Feb 2025 21:29:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293ecd59e47da28b33b7e272716206e0fec2c8951cd65ba0e3a262f7de4b07a`  
		Last Modified: Mon, 03 Feb 2025 20:49:03 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567978479c67c76829b395babedbe91f3f64d4caab64670b0297efd10f3269e3`  
		Last Modified: Sat, 08 Feb 2025 14:37:10 GMT  
		Size: 163.4 MB (163379732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61ac301d36da8b85259572898de717fc887e0564d29fb07cc8f13002fb1142d`  
		Last Modified: Thu, 06 Feb 2025 22:17:07 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77e0a088695ab402f6127a2b16c9549f0bae0be31f263ad281495ee927aaa14`  
		Last Modified: Thu, 06 Feb 2025 22:17:08 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377cf5fd0418dc5cd7ba9de242d5be0888b6b42abc85b06a45bab07f0bbbeeb`  
		Last Modified: Sat, 08 Feb 2025 10:58:00 GMT  
		Size: 32.2 MB (32223269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e938284f21a7d3c715942f8a76cda1b5f34656b916ab3993975a4aa12dcee661`  
		Last Modified: Sun, 09 Feb 2025 03:28:03 GMT  
		Size: 136.6 MB (136562121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d506b44ec9f8cdfd34493fd3f392991415c860c9d828ad6de6f3c233327497`  
		Last Modified: Tue, 04 Feb 2025 07:18:11 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:acfb7e2f40305732bb829df804471cb3ad4589b442bf68f448a56ecbbaa0000f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f07c55c339377864abdecb5ec65ae5f484786238dab6277abd0d074ea96ddb`

```dockerfile
```

-	Layers:
	-	`sha256:feba3d004e79b075facc1eb5cdbca00bcf61bd4553ed2db124ae930fd49be5f6`  
		Last Modified: Sat, 15 Feb 2025 00:19:16 GMT  
		Size: 3.7 MB (3656559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5294811ed702934a400816ed7cc4926d2c67035ad402b5d5018c119e617294a`  
		Last Modified: Sat, 15 Feb 2025 00:19:16 GMT  
		Size: 30.9 KB (30936 bytes)  
		MIME: application/vnd.in-toto+json
