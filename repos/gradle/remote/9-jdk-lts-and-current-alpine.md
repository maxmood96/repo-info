## `gradle:9-jdk-lts-and-current-alpine`

```console
$ docker pull gradle@sha256:9bd159f79611b42ee3debfefd407ecd1ac87db027fc4da16fd71b62e228d2d0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-lts-and-current-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:4ffb848c617ca610e522ca2566ea21c3900fd86f5ba17769f5f706920cf99655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.7 MB (451686512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aec83cc3d1102244a2356620e8d51b02af3917301257287be4190ec8b798e62`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4773cfdc59d66b75f4a68ac843b2b5854791840114cf8bb1b56fb6f7826ae498';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='73c4cbe10f4f385383d9cb54d34f2bee2c68b5265f9e3d954f3326948c40c0be';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["jshell"]
# Thu, 31 Jul 2025 17:27:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
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
	-	`sha256:71d4b0cd66eaaf13cd2ba9f86b5283d4e60123831697995abf2175e948565c08`  
		Last Modified: Tue, 05 Aug 2025 16:53:54 GMT  
		Size: 90.1 MB (90133297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a241821bd7068e5c2b646e0de913df5da44578eb78aa4b43cd6e32076e6ccff`  
		Last Modified: Tue, 05 Aug 2025 16:53:34 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6e93b4d32a3763a82b535a7407e5682841a1abd91b8e79137378309220980d`  
		Last Modified: Tue, 05 Aug 2025 16:53:34 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e34b51e7b0cc6c78d7dee2520748d0757f433cfb127d0d229d677b10df5f5f`  
		Last Modified: Tue, 05 Aug 2025 16:53:39 GMT  
		Size: 44.1 MB (44080965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e6e0acc5fda707d694054b6df4704ad30c93702e124b12ab2452d6baca4bd1`  
		Last Modified: Tue, 05 Aug 2025 19:03:31 GMT  
		Size: 134.5 MB (134480544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4c97983b1b6abf03cdeae656fc30129169f30ed9432b83120561daf755867c`  
		Last Modified: Tue, 05 Aug 2025 16:53:36 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:8a5bd791876b53ab8a6c218d2504cd19e277d6c13767ea6fae4783c0e4cbeb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4827062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cb77d0ff30b4dd598b3dcc707a90e5c8612d39603b36207f00870bd8ea3d18`

```dockerfile
```

-	Layers:
	-	`sha256:97d5041a7760a9ed1f1079cd7de1fcf81d2c9f2b96b9825eb1fb39eb9cb6123b`  
		Last Modified: Tue, 05 Aug 2025 17:22:29 GMT  
		Size: 4.8 MB (4794785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca757ec35015dec828ea99ed223346f125ecc43b8ffdeb921ae9f542da5fec9`  
		Last Modified: Tue, 05 Aug 2025 17:22:30 GMT  
		Size: 32.3 KB (32277 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-lts-and-current-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6f8dcf4b1ed2d92c74a7cc8b69b86cbff7b43eb1e0d833f39806198b9f0e519a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448547488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76336e2632171056f967f055d440636807383a940602a40a53db4b8c8996d2b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4773cfdc59d66b75f4a68ac843b2b5854791840114cf8bb1b56fb6f7826ae498';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='73c4cbe10f4f385383d9cb54d34f2bee2c68b5265f9e3d954f3326948c40c0be';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["jshell"]
# Thu, 31 Jul 2025 17:27:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
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
	-	`sha256:d25024b780853f575b629414a1e68849407cccfa863b2153b171ebd2528ddfab`  
		Last Modified: Tue, 05 Aug 2025 22:06:46 GMT  
		Size: 134.5 MB (134480607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a2e8ae78e95de765b967838a9541c3545b9cb495f01ce01ee501c38572449b`  
		Last Modified: Tue, 05 Aug 2025 17:18:38 GMT  
		Size: 59.5 KB (59541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:5dec7ea5c48378715406c77ec390ce2a881146328e80decf5c799625dc5f4522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c623332870ccb842f50860576f4a291fbd054c2eff3903352ed03cc638095c`

```dockerfile
```

-	Layers:
	-	`sha256:10458bd439ab5ca607b4d4f90deeb9edd73de98b10f7c441545466178815e039`  
		Last Modified: Tue, 05 Aug 2025 20:21:55 GMT  
		Size: 4.9 MB (4944338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac8091999f4b2fb247ee75078f74f2acc9d9d6d4eeee39bbb6c9eaca0579709`  
		Last Modified: Tue, 05 Aug 2025 20:21:56 GMT  
		Size: 32.5 KB (32516 bytes)  
		MIME: application/vnd.in-toto+json
