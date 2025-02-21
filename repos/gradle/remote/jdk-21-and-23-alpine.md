## `gradle:jdk-21-and-23-alpine`

```console
$ docker pull gradle@sha256:9a6a6792e32277d26b8b90916bf94e1f447d51a8b28c3fe46fa334168701aa3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-23-alpine` - linux; amd64

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
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2377dc8d3710b6bf7410a46adf016bdb060a8b4a7114189518f7f60fae85e3`  
		Last Modified: Fri, 14 Feb 2025 19:25:44 GMT  
		Size: 20.9 MB (20949767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79312d97e63a3dd5a83b89c90503f5d3c5c8ce261682999e1d12cf54506ac32`  
		Last Modified: Fri, 14 Feb 2025 19:25:46 GMT  
		Size: 157.8 MB (157796824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573882c363c812b21ff606ea7d12eff8720580a29a875238f127d7f80b9f0da1`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1f65d07a350139d7390033a591e07d865c082f4b458bb56ff38bc143349c8`  
		Last Modified: Fri, 14 Feb 2025 19:25:33 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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

### `gradle:jdk-21-and-23-alpine` - unknown; unknown

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
		Last Modified: Fri, 14 Feb 2025 20:34:59 GMT  
		Size: 3.5 MB (3507650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1feb4e801a5b3e4a2d3fc3cfb2a36fb33b904cfe991ace55b064bfc1cbacb72`  
		Last Modified: Fri, 14 Feb 2025 20:34:59 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-23-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c5e35bfb65e2b7a0c035675a1c15bde47442cfeda9306db924b1c503d058d3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 MB (513021849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a1219cbc5fd1c3eded3539b4a2c6c9d02ced77dc4b062885628f32c0905b64`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22460361c4e9e1ac6bf5bc45209d88abdf89352662d6ea415fdaae2281c39acd`  
		Last Modified: Fri, 14 Feb 2025 22:43:26 GMT  
		Size: 21.0 MB (21005533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d006405dd14f86430a341fc9e96608553ddc4de8ca7c21843b389282b46a2`  
		Last Modified: Fri, 14 Feb 2025 22:43:29 GMT  
		Size: 155.8 MB (155787997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3703c2f380b3b4e3eeae969e60074a2cce6d72889dc412466f29ef5ebfc440f7`  
		Last Modified: Fri, 14 Feb 2025 22:43:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060a7bd90d15285d6041f307b0a65f5415677f1d9d59e445a6c3b5b27f5f9cc0`  
		Last Modified: Fri, 14 Feb 2025 22:43:25 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585166c57f683db2388f459107da8896d0bf2dc6ba7c35fa95f8abdbba2eddc8`  
		Last Modified: Sat, 15 Feb 2025 07:22:46 GMT  
		Size: 163.4 MB (163379650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9f14e418558076d24cb3290695507d6e63b7abda5014f02a14738904f4b02e`  
		Last Modified: Sat, 15 Feb 2025 07:22:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9b81fb5d0f73befeca9743975c62393addb3d760d8bebbe8368e505c8ef80b`  
		Last Modified: Sat, 15 Feb 2025 07:22:40 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8318a05af6b21dfc2d0089ec89fa2c65f6a7b332781e7f5b8f61b893dbe5c53a`  
		Last Modified: Sat, 15 Feb 2025 07:22:42 GMT  
		Size: 32.2 MB (32230359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8061051c4b56ee2cf032feea74c7ede96e6f40b584e16f1071abc79eea49250`  
		Last Modified: Sat, 15 Feb 2025 07:22:45 GMT  
		Size: 136.6 MB (136562020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a72e0bd7e36ab8e8c65a23bbafd845f4a9f1e4b8374d186dd762263c2efeb70`  
		Last Modified: Sat, 15 Feb 2025 07:22:41 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:da77f4820a8ff1952041f83d624d12e47a6d17c6cbf1863d1f10e392db27c654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5519ac3aac6d887ac2dd2729e88e5581ed47fe4c3d568c71e14186e0574d952`

```dockerfile
```

-	Layers:
	-	`sha256:f4b0569164a89fd8149ec6ece6988864d32cdb2c7baaed2679c02e47c0c3ce08`  
		Last Modified: Sat, 15 Feb 2025 07:22:41 GMT  
		Size: 3.7 MB (3656565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa59b9a8c07e9bcd35dbba7f9525ab6f591234d56d81db3373d2cd2ce3f4ef7`  
		Last Modified: Sat, 15 Feb 2025 07:22:40 GMT  
		Size: 30.9 KB (30937 bytes)  
		MIME: application/vnd.in-toto+json
