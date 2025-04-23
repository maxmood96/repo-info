## `gradle:jdk-lts-and-current-alpine`

```console
$ docker pull gradle@sha256:50faa22838c8ee715ff7b64cea44c8b1efec8d075a7ac16e9cfe6511a63cb7bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:c3606058540622a9c339452783b20ade2131872800aa51489a16d9a52254f4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.2 MB (442211492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d06d1a59c4d18b8e4587a21abf53a1c5872583baf5a7996a35507db6bcc788`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Apr 2025 14:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 14:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='76dbb5152f15e509a5fc965936b2b912f806bb977853ab028c362c5340b1c4e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        x86_64)          ESUM='79ecc4b213d21ae5c389bea13c6ed23ca4804a45b7b076983356c28105580013';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["jshell"]
# Tue, 15 Apr 2025 14:24:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["gradle"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Apr 2025 14:24:24 GMT
WORKDIR /home/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_VERSION=8.13
# Tue, 15 Apr 2025 14:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER gradle
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER root
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29b21f5b2c17ebc06e9a99b3cfcd3cfc8e8a3fed872fff81641100e99586c42`  
		Last Modified: Wed, 23 Apr 2025 16:32:08 GMT  
		Size: 21.0 MB (20951300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370873e386b22025c28fa9279cae3a1cd222ac243a221679834774d0620fa7f3`  
		Last Modified: Wed, 23 Apr 2025 16:32:10 GMT  
		Size: 157.9 MB (157856438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb1def311668c63d0555cfb562a2dc952ee1c071f75d5f1805f7e6383c36365`  
		Last Modified: Wed, 23 Apr 2025 16:32:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa49a465cc24db7df330480bc605cd2f13f785972d1645eeff0397c467e58380`  
		Last Modified: Wed, 23 Apr 2025 16:32:08 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608a31b3d1edda7134e6cecafdd876189c17d7a618660e15ccab3cf606f9d8c`  
		Last Modified: Wed, 23 Apr 2025 17:10:27 GMT  
		Size: 90.1 MB (90082269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610ad8a6f93962d90cc2057c1c269420a7ac11113a5c54565f88a2739cd6ebc5`  
		Last Modified: Wed, 23 Apr 2025 17:10:26 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8702438464fdc6da9338a0f14da33b5309b09e08743fd487876fff5d3de25ba`  
		Last Modified: Wed, 23 Apr 2025 17:10:26 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b8fb3162756b2038329e4c24be028606b0c287ee2483185a8be87f51b1f7f9`  
		Last Modified: Wed, 23 Apr 2025 17:10:26 GMT  
		Size: 32.6 MB (32632421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e898d2442828e7c01e2add7f90883f72b8c46b69ebad65e686f2c8944288e`  
		Last Modified: Wed, 23 Apr 2025 17:10:29 GMT  
		Size: 137.0 MB (136988180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602b9021527ded1b96629815073947189efc84f777e97ddd28d8712132ac5420`  
		Last Modified: Wed, 23 Apr 2025 17:10:27 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:2b55b8cdca29d2baf2c87ba1983c2f7f83bb21d2a2e8cadffd781de3eb4d3f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62371414b628d7e66c6964518742120f2ccdd2b757a7602cc9b83ed02ab3808`

```dockerfile
```

-	Layers:
	-	`sha256:bac456c5df9891d1871e63aed2775a814fb56a62b9ae3ea64332dcf52030aee4`  
		Last Modified: Wed, 23 Apr 2025 17:10:26 GMT  
		Size: 3.5 MB (3455880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39a99155d41f7da53c1160f19b567496c476e554df99a46a8b7a3ad4341bf27`  
		Last Modified: Wed, 23 Apr 2025 17:10:26 GMT  
		Size: 30.7 KB (30683 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d9a854c6e9b3449209f98c5a2de950a98ec02fcb4da05b663744ef671285acac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 MB (439229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3d205f3e5628b07ee389f1f667ece75ee86cfbf90e978617c83fe15f9ebbff`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Apr 2025 14:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 14:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='76dbb5152f15e509a5fc965936b2b912f806bb977853ab028c362c5340b1c4e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        x86_64)          ESUM='79ecc4b213d21ae5c389bea13c6ed23ca4804a45b7b076983356c28105580013';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["jshell"]
# Tue, 15 Apr 2025 14:24:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["gradle"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Apr 2025 14:24:24 GMT
WORKDIR /home/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_VERSION=8.13
# Tue, 15 Apr 2025 14:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER gradle
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER root
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4dc4c8e3ac1404ce7eb282c94493325536d142e577ef37ec27bcf3edd09f4b`  
		Last Modified: Wed, 23 Apr 2025 16:40:20 GMT  
		Size: 21.0 MB (21006028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d79f5ae0d2c93d793230f628662fd05f2016bef787341ed080547de9a7f64ca`  
		Last Modified: Wed, 23 Apr 2025 16:40:24 GMT  
		Size: 155.9 MB (155857547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2937cc8994b85ca279db22cd32ec1c5629507ab48f3cedc8aa18f2e2fd9a5e`  
		Last Modified: Wed, 23 Apr 2025 16:40:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6eb77cc48cf78e63aa9b791516daa245f630c71218c0e01f1f3b964f2a4eb4`  
		Last Modified: Wed, 23 Apr 2025 16:40:19 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbaac463c40ed7616bd2198a3a6fd2410f9ed8b786195d89bc384ce4f357330`  
		Last Modified: Wed, 23 Apr 2025 17:37:43 GMT  
		Size: 89.1 MB (89066922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bac422e70617dfd02b2a6e63b71f4d51955f40c926eeaa7422b95b8a044928`  
		Last Modified: Wed, 23 Apr 2025 17:37:40 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07fdf99be25b59ddecdbc5d70b916e5e8be5dfb623ca59ff55ccd67a42e84c`  
		Last Modified: Wed, 23 Apr 2025 17:37:40 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feed6cb4d6581477bda1afc51b5e886f5d7d7558ed46767105e70811aae5279d`  
		Last Modified: Wed, 23 Apr 2025 17:37:42 GMT  
		Size: 32.3 MB (32255044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a618cb66413e696ef1343c574453fc07657bd32f90388db157ce267da3c0c2`  
		Last Modified: Wed, 23 Apr 2025 17:37:45 GMT  
		Size: 137.0 MB (136988119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e3d306018b6b8dcd4cc5645ba636417f98e4088b12a2750642607ad763626e`  
		Last Modified: Wed, 23 Apr 2025 17:37:41 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:4867641589277d530d5d43660f0f2809823fd0f76f8d6f052197f77bc37189d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56930c1e9ce12a1b76b9e754e0d36cd2546681f9ccfb79113e019edced865e7`

```dockerfile
```

-	Layers:
	-	`sha256:355ff295e292b56fe2479101d710358088adf8318d5e5643174ebf65b2e0650d`  
		Last Modified: Wed, 23 Apr 2025 17:37:40 GMT  
		Size: 3.6 MB (3605415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c5c704cf2303dadfe22b01105d1a79d1a66b10a2282d7e2a80fa75161b4bd20`  
		Last Modified: Wed, 23 Apr 2025 17:37:40 GMT  
		Size: 30.9 KB (30921 bytes)  
		MIME: application/vnd.in-toto+json
