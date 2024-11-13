## `gradle:jdk-21-and-23-alpine`

```console
$ docker pull gradle@sha256:a5fe94ff4d5f840291c7358be23471f85a239bcd82118ffac640739d9f057975
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-23-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:db06dbd1e14bfb3ecf4959962d506d52088ceb5645438d79ccbe7e6abd64e75a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.7 MB (517697115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff9d0048d4dc61701f69908e1ac542b3275d17ff920b9e8ad2d757403a4b83`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
# Wed, 13 Nov 2024 00:13:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Wed, 13 Nov 2024 00:13:30 GMT
CMD ["gradle"]
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Nov 2024 00:13:30 GMT
WORKDIR /home/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_VERSION=8.11
# Wed, 13 Nov 2024 00:13:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER gradle
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER root
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3adb1b361694716f735538e25636db9c915b45c870e744223f3d3020d515c1c`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 23.0 MB (22953393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d061b3c52fbe2566fade57c090519f152f4d1f34b92c4b11e8483dac15082f7`  
		Last Modified: Tue, 12 Nov 2024 02:38:52 GMT  
		Size: 157.8 MB (157779470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2bd53639fc30cf5eddf18027f47695541b28435d6281a1a15c32da7ca9aa58`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a697b41d652b4fc39bbe88232ba2e043ef173cd912c76b91efc830b8a63aef`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a0793abb2a91c71aad2b2215ac835043620d40ddb69394392beed4d4abe0a3`  
		Last Modified: Wed, 13 Nov 2024 02:07:43 GMT  
		Size: 165.5 MB (165513464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5010fb171f35adfcb998c771da359e83844a385a53ad05bff52d050d9c91be`  
		Last Modified: Wed, 13 Nov 2024 02:07:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a776e47d2300cb4c5ce8bbb946fbf3ef9419ddd77bd0154c24e799b9e9d5e38f`  
		Last Modified: Wed, 13 Nov 2024 02:07:38 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5204365f033468cf010a5611c442ef39a4baee8d437439ee76a787bcac8e75`  
		Last Modified: Wed, 13 Nov 2024 02:07:40 GMT  
		Size: 30.9 MB (30898890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace31b26659714c7c46fa460e088c365d441f2aff715a07bb97caff9a5169319`  
		Last Modified: Wed, 13 Nov 2024 02:07:45 GMT  
		Size: 136.9 MB (136923964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70101b313763322d84e189845a2439dda31445bfe5108013dab73c1569c49380`  
		Last Modified: Wed, 13 Nov 2024 02:07:39 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:e9e8ffbfbe6254376f5d294a7c7f229288a6e38784257cfa3adda9ea1e4f1dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3508181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c29d15bb16ef07fb138ee9ed3b5469e8c1364ec53a1ff0f6a88c85bd287b16`

```dockerfile
```

-	Layers:
	-	`sha256:bbb855b21e5c791c7665a0366ec6dfb719f8870c229c157bfe2e078c0402d139`  
		Last Modified: Wed, 13 Nov 2024 02:07:39 GMT  
		Size: 3.5 MB (3477487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33eb494f21ce9f6ec25d4c54dc6261d46224113b582776b73a2a45efda3df25d`  
		Last Modified: Wed, 13 Nov 2024 02:07:38 GMT  
		Size: 30.7 KB (30694 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-23-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:205f084c87327db30adc4e1b9b35dbafc95bfaa74c39b912bbd0470462b2a62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.9 MB (514879064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179e2dc6de4e93b347c7b793c0d331732e98dbf28069d0aaee8fb5e3f1acdacb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
# Wed, 13 Nov 2024 00:13:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Wed, 13 Nov 2024 00:13:30 GMT
CMD ["gradle"]
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Nov 2024 00:13:30 GMT
WORKDIR /home/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_VERSION=8.11
# Wed, 13 Nov 2024 00:13:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER gradle
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER root
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e35b18e3113b7f2ff24b09398759411d2064bbc52968a3357a6760d0c2b1f9`  
		Last Modified: Tue, 12 Nov 2024 11:26:38 GMT  
		Size: 23.7 MB (23731447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b806ac52aaa3c8490fa6b3dd22ae812301f6f5c44fa49b5a018968085c7122`  
		Last Modified: Tue, 12 Nov 2024 11:26:42 GMT  
		Size: 155.7 MB (155740143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9ded69f2ba88afd032f75904fa06352f2e21efc7c1605110be0cd41826b116`  
		Last Modified: Tue, 12 Nov 2024 11:26:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd6388061c8e51722cae25a719ac0df553a94b65fc1af2ca10864f4bd2635ba`  
		Last Modified: Tue, 12 Nov 2024 11:26:37 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e062f780be7aa8083c23d71d57771c1077be9edf1592ef9b4dc8e1affa5d8dfd`  
		Last Modified: Wed, 13 Nov 2024 08:38:56 GMT  
		Size: 163.3 MB (163316171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0a76eff248a41245c201e2e30bdd9c2a034d3c7a5fe4edf9df2a243bf3e06f`  
		Last Modified: Wed, 13 Nov 2024 08:38:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebe6d211d8af452a45420d8a028cbb495d11fd8d3898cb80828cf21f7b8db8f`  
		Last Modified: Wed, 13 Nov 2024 08:38:50 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7489e2526b3f13fd5980259e07635de7399fab9923ead34ef174f0d148fb231`  
		Last Modified: Wed, 13 Nov 2024 08:38:52 GMT  
		Size: 31.1 MB (31075597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d636ef71d3e7817a46a096b6a80d3b1156ab3c0b2d98cbf31e51aa9918cdf81`  
		Last Modified: Wed, 13 Nov 2024 08:38:55 GMT  
		Size: 136.9 MB (136923945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478f12702eb611bc9d177d8d3ad15a7e932216c4892f0ac88fe06c54753d5a7a`  
		Last Modified: Wed, 13 Nov 2024 08:38:51 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:5539d4e89268bfe0013a5ab67bebda56ae239007d14a10439a63cac872ba4e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3612008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d879fcec8a064bb0731de852d019d22de44363c4722a58973e1491419f84560`

```dockerfile
```

-	Layers:
	-	`sha256:2ed2ec67b25c49b26b29f2ee6c85053cb8718b52adf6cfedefee57cd9e9de54d`  
		Last Modified: Wed, 13 Nov 2024 08:38:51 GMT  
		Size: 3.6 MB (3581078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0075ad284c943771143a4ee2170a6968f38029bbdaa14a23de8f3072d8aa53`  
		Last Modified: Wed, 13 Nov 2024 08:38:50 GMT  
		Size: 30.9 KB (30930 bytes)  
		MIME: application/vnd.in-toto+json
