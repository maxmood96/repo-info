## `gradle:jdk-lts-and-current-noble`

```console
$ docker pull gradle@sha256:418b53108a22de86f29fe3c0ef8a217cc5a212b51b9f156a746c73ccce35b078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:jdk-lts-and-current-noble` - linux; amd64

```console
$ docker pull gradle@sha256:9b59e05beef50f3f3726750e97a87a25797b55186a087bd92a3bfcdee67ce359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.6 MB (498643935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64a9a1bd7ece3d140f6deac795cfa40c7caa8bfcbc78a10a6fff09f4415cff1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
ARG RELEASE
# Thu, 31 Jul 2025 17:27:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 17:27:11 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9020b2985154ebec2e5c41f920cdec5c883d205708c665845a35e46dde13f95`  
		Last Modified: Mon, 15 Sep 2025 22:14:43 GMT  
		Size: 23.0 MB (22958669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb527ddfa98902e1fba0b7248248e722d817019355ef80708d963ebf829ec568`  
		Last Modified: Mon, 15 Sep 2025 23:13:33 GMT  
		Size: 157.8 MB (157809527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2d782ae30b18df0053991978bd0e30982aa4009af2766a228c3cd40be32e77`  
		Last Modified: Mon, 15 Sep 2025 22:14:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed5e853e5b0022b9f4b01830885f97148d5d67a34f2e15c2875b689cd40b24`  
		Last Modified: Mon, 15 Sep 2025 22:14:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9139d7fb129e8d34b95120d45fe366f48d93582a245044fd3634c07a3fde7d77`  
		Last Modified: Mon, 15 Sep 2025 23:15:55 GMT  
		Size: 90.0 MB (89975200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5282b37474a3bf2dd002d9d7efad919d606a3b198795547cbc1d5783d5579186`  
		Last Modified: Mon, 15 Sep 2025 23:15:41 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fd1cb8d2dc934a196ffa75d13e0a4c208a75910a93acd314a2dcbf57b4cbb6`  
		Last Modified: Mon, 15 Sep 2025 23:15:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a1ab427ddfc33bbfb4de9d5633827251a30735aee61760fcb1f97e6411f0a0`  
		Last Modified: Tue, 16 Sep 2025 03:22:01 GMT  
		Size: 63.6 MB (63637061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221b232bfc2baa86d25241ef7fcdf6a7bb2419debc77cfdba9ac6d0d8e0747c0`  
		Last Modified: Tue, 16 Sep 2025 03:22:09 GMT  
		Size: 134.5 MB (134535991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:46035b0ae80549028dc60839c8a2fae214d83d6300951b4d449b5582186d2afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7526889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a461f9dc88b1d13b4b96e04122254a9fef39d06e9e924d4176788054b35df31`

```dockerfile
```

-	Layers:
	-	`sha256:bba68bb31bb30032952ca1b22e29dd5a1443871dd9025916f2711b5c9180b9ce`  
		Last Modified: Tue, 16 Sep 2025 02:26:06 GMT  
		Size: 7.5 MB (7493745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee2e2d3bba8be039f5ee6f380810049d2c3ddc9c5804d3cd0d1104ed8947ede`  
		Last Modified: Tue, 16 Sep 2025 02:26:07 GMT  
		Size: 33.1 KB (33144 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:77878cd31cd30354056b255d3974b85782a01807a3bfc520b7252e7679df147c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.8 MB (495841775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f5ea4e182217aed2b6a4185223324d5959f33b6adf5fefb44c6dee140150a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
ARG RELEASE
# Thu, 31 Jul 2025 17:27:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 17:27:11 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d357382cc9ec400c3d0e600a41995cfa29d5bac12344f10f0fcad998643ddd15`  
		Last Modified: Mon, 15 Sep 2025 22:13:36 GMT  
		Size: 24.2 MB (24165714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee07afe111e80b348852ee9c230e1054aaf0e5202c7ddabce17758c28959f94`  
		Last Modified: Mon, 15 Sep 2025 23:13:59 GMT  
		Size: 156.1 MB (156088887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f991d8add32f4635a3a654883ecffbaa6d6460d9ec86409a7f45ab6dd821850`  
		Last Modified: Mon, 15 Sep 2025 22:13:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493eb04a2cc1efa6a27aa9defdf67248f10423e992e68cb289e0b9e14a1ef24b`  
		Last Modified: Mon, 15 Sep 2025 22:13:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47e31039212cdf607d6590d516cc20690be16d8ae4158105263841a628cab2`  
		Last Modified: Mon, 15 Sep 2025 23:15:54 GMT  
		Size: 89.1 MB (89092803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1097144c9c6cdeeb67a17ae14d949f12a04daab152a8ad4a645b205107bd1d4`  
		Last Modified: Mon, 15 Sep 2025 23:15:43 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f1cc9f218ab17a329aa56536189b95ca3fdd4d76b65d4d206dc2bf97e624fd`  
		Last Modified: Mon, 15 Sep 2025 23:15:43 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2f5251ec6051bbebdedd76a852807da1aa20b2d655200279e7e8bf7c074a91`  
		Last Modified: Mon, 15 Sep 2025 23:15:56 GMT  
		Size: 63.1 MB (63086986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5746f69c938f0f074ae9fcd8ebe392c25cceccec123f1aecf3d2f6f55c7ad34d`  
		Last Modified: Tue, 16 Sep 2025 03:26:28 GMT  
		Size: 134.5 MB (134542032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:b69ac4f9c36b57bd323b88818a0d535bc5e3eafd393f6eae7675abf1238e8bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7664403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607390215795b5f5a95cb1ef07a025810b321e4bbcacfbffb1ed0baa2ebda860`

```dockerfile
```

-	Layers:
	-	`sha256:dd2beaf35d1f5f52db6cac01cb41d3cac978940582bd0ce9a1ae1fd7d3d3f9fb`  
		Last Modified: Tue, 16 Sep 2025 02:26:14 GMT  
		Size: 7.6 MB (7630940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e0fbd8689a8a46a8a1f51338495a4677a2e8e8f58d5fddd556a47e017ab656`  
		Last Modified: Tue, 16 Sep 2025 02:26:15 GMT  
		Size: 33.5 KB (33463 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-noble` - linux; ppc64le

```console
$ docker pull gradle@sha256:fd1dc0f6a4d9a417ad25ee052b2a723727e084a2cd3480b49c06195e17e98e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.7 MB (509696072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820b4a92a061e3b9bc0af06371c3b4f3d1474eff71222f5dda77eeb3f92370a4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
ARG RELEASE
# Thu, 31 Jul 2025 17:27:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 17:27:11 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51c0d56abd1175ca1d077b190f670b7bf37d8534c47076746ea522b8dee24df`  
		Last Modified: Mon, 15 Sep 2025 22:18:00 GMT  
		Size: 24.1 MB (24101619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae423e12727408d7fc4535f074c449c2d878c3f98492dac2bff0570d2264f6`  
		Last Modified: Tue, 16 Sep 2025 00:37:48 GMT  
		Size: 158.0 MB (157969921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb13022736037a0563430d6f7bad8c7860cd0ce6fb6d8376dc8ccafc4cb8863f`  
		Last Modified: Mon, 15 Sep 2025 22:20:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc9e9e5ce3ce07a122afd1768e503d301074f9ef219a8da3ea7ca6adeac19d2`  
		Last Modified: Mon, 15 Sep 2025 22:20:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f363951324dac7004eff8657a6bd347133c49eafeeabeae348922e9a8380a804`  
		Last Modified: Tue, 16 Sep 2025 00:02:43 GMT  
		Size: 89.9 MB (89918588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cf4d0956291d74ac4453730e47cac8f39e66c40558102196884c6d1c0b542`  
		Last Modified: Tue, 16 Sep 2025 00:02:37 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf1534cb76675ef21f757bc87304093f2513be53b86a150be4be1fca6178cba`  
		Last Modified: Tue, 16 Sep 2025 00:02:37 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f239d8188a24603ed292422a898a794c2dcd8bdae72d9ce25e69fdba4684aaf3`  
		Last Modified: Tue, 16 Sep 2025 00:02:44 GMT  
		Size: 68.9 MB (68881930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335998121fecb6e6e3f2b980372b0342c1063bde294fe743530b896d68a8580b`  
		Last Modified: Tue, 16 Sep 2025 00:02:31 GMT  
		Size: 134.5 MB (134516852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:6c3668b73899cd96c2437524196463bf3143b1a01e675832df1e7bf006482f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7576958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea1fce6e9d970bff894881f3df10e91618cf7bebce0525a94b89a4dfac56ae8`

```dockerfile
```

-	Layers:
	-	`sha256:868327a53644fe7875c2f62a38419a362826ad14f84f7ba3397dc6062968f82f`  
		Last Modified: Tue, 16 Sep 2025 02:26:21 GMT  
		Size: 7.5 MB (7543682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0998726116a90d4a10890bd7fd61b7bd77130abfa5e4037884397a4390558eb0`  
		Last Modified: Tue, 16 Sep 2025 02:26:22 GMT  
		Size: 33.3 KB (33276 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-noble` - linux; riscv64

```console
$ docker pull gradle@sha256:2c6eb3782fa0692fae193628b451a0435a8623149d6434d821d83eb1a846175a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.5 MB (498523952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468791e05a6c74b5c96ef76a5c0e177f83cc90973f89091d737c000c46580441`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
ARG RELEASE
# Thu, 31 Jul 2025 17:27:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 17:27:11 GMT
ADD file:0b905a81cc9e876b16249002e7c59885fde69ab451fd1b6e5768dd8a4b2a9d1d in / 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:6d2d7ce17575561a3deb2625d73936f72b9f13abdb7e3366b85dbb55c4289f94`  
		Last Modified: Wed, 03 Sep 2025 03:54:05 GMT  
		Size: 31.0 MB (30951461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e05c85638de70f8f21df158410ecf0a5207672128a0166e3af98b72b870a03`  
		Last Modified: Wed, 03 Sep 2025 16:52:20 GMT  
		Size: 20.1 MB (20142005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662bef574df0c7604fd37e3130258c6c7be4385e972249d1682ddfb82d376f7`  
		Last Modified: Wed, 03 Sep 2025 18:45:03 GMT  
		Size: 153.6 MB (153602030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c636b23d95e3990d7195368616ea9c53b6c17a96b3f00182e8d715c3eea3fc2`  
		Last Modified: Wed, 03 Sep 2025 16:31:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9de73c51580215f2b94261f411003b593ea4404c3119bdd3e1a0f03c3376dbc`  
		Last Modified: Wed, 03 Sep 2025 16:31:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3347f7e3a61591893bb6cae97f166e9e4552270d7453a0825ae3220a631965`  
		Last Modified: Fri, 05 Sep 2025 18:48:38 GMT  
		Size: 87.7 MB (87670661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50fba7277a258eed89d386237854cd8ece003f98adeabc973562d9549885c0`  
		Last Modified: Fri, 05 Sep 2025 16:44:20 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57661d45de2f30d23a87d94b3fe1fd3b575f82c45e94f5952115017e2ee1f6b`  
		Last Modified: Fri, 05 Sep 2025 16:44:21 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca9142ea3a671348e0fcf706b07b0df089853459c82a74dee70cd6205ad99c2`  
		Last Modified: Fri, 05 Sep 2025 18:48:54 GMT  
		Size: 71.6 MB (71636897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c659cada0d3f7e227cbd0c021e5efbe1030b1710e449e5b7cfeddd67b45cc37`  
		Last Modified: Sat, 06 Sep 2025 06:16:20 GMT  
		Size: 134.5 MB (134516860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:42788de2e204360cb207795f01f59d19b65f47feae67a5a01594762b1100a183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7628984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cedc00c7737e324360c24d2cfefbfcdf2186f4cd996d8323da13d20d27fb6ad`

```dockerfile
```

-	Layers:
	-	`sha256:53ed1726ef0db31a032a8d3b9dbe28c6a382473973bb363edad09e09ba9d4b89`  
		Last Modified: Fri, 05 Sep 2025 17:23:12 GMT  
		Size: 7.6 MB (7595709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c447de0f8ed86f6f28a446f610aea36826d69ee2c80c33fa8b6aa97ac3a68a4`  
		Last Modified: Fri, 05 Sep 2025 17:23:13 GMT  
		Size: 33.3 KB (33275 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-noble` - linux; s390x

```console
$ docker pull gradle@sha256:8a6e5e4025978d6f7b42fd80e3cb63c65073e7d0b6f6f065fd132e101acd67c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.2 MB (484163889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba4dfdfc00ef316c95caa5418b37d0a24ced8b939a3e2e86a230e80c976129d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
ARG RELEASE
# Thu, 31 Jul 2025 17:27:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 17:27:11 GMT
ADD file:c24f61277b8ba0fc6a9f5e3c821b272fa1878e300fa010e5e8c6bb6b789470a0 in / 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:1d6a499251c4e5e59ef209845254eb72c5efde9542271f270cf1a08fa823dfda`  
		Last Modified: Wed, 10 Sep 2025 16:24:53 GMT  
		Size: 29.9 MB (29906591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e39ac76690d771e82962f65d2af15ae7bffa0b0a9d16cba37e9ff713533b1e1`  
		Last Modified: Mon, 15 Sep 2025 22:17:41 GMT  
		Size: 22.1 MB (22128786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3df9a187159d7209a420af2fee3c96d9be5f6277a4afcafa7a30e602bce52`  
		Last Modified: Tue, 16 Sep 2025 00:13:12 GMT  
		Size: 147.0 MB (147036881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cbb8ca8c8a70c10bbf28d6d78e4ee394d1d7e11bd8f347e33343ef53ef69fe`  
		Last Modified: Mon, 15 Sep 2025 22:20:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9c34448681e9a18522e8701fd43bb6d461e2c36c76917a427b1dd1675d3bdb`  
		Last Modified: Mon, 15 Sep 2025 22:20:32 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2e28e430cd6e085f39f8cfe861001eb0a029335b990bd5a71c1632bcfbe1f1`  
		Last Modified: Mon, 15 Sep 2025 23:52:40 GMT  
		Size: 85.2 MB (85226552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1c4ea27aa396280e45d5d1502ccd4f78336dc44d98d657f8ea3c71dcb5a4f3`  
		Last Modified: Mon, 15 Sep 2025 23:52:36 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c096a0bbcd25d13092707f8e180e08509049e619982ef73c61d1c470fa01f8`  
		Last Modified: Mon, 15 Sep 2025 23:52:36 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a4cf1ab16e2fa36f25ca6fa30a82318fad30a4e8ccd03394e1ac9b2c55bfd`  
		Last Modified: Mon, 15 Sep 2025 23:52:40 GMT  
		Size: 65.3 MB (65344221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3c929174e1f86d897ab9ffc49e9a505dba1fb8654a63a9a8ec69a7174b68f9`  
		Last Modified: Mon, 15 Sep 2025 23:52:28 GMT  
		Size: 134.5 MB (134516826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:3db722baa295012aed3789fe26ce57630d1a7ebc166b315d3955237136d2bdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7469712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9975e549a73f886189451ac345256ceb3197c3759e9cea21dab90698882986`

```dockerfile
```

-	Layers:
	-	`sha256:7e6898583338f9e29d74c7197fe6207522a001da4b64727ca278cf5d1e92bbc4`  
		Last Modified: Tue, 16 Sep 2025 02:26:33 GMT  
		Size: 7.4 MB (7436568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5891e4e3289d35d3969725a2d8e72053d02ccd2d959b214962d63f1b6c5633a7`  
		Last Modified: Tue, 16 Sep 2025 02:26:34 GMT  
		Size: 33.1 KB (33144 bytes)  
		MIME: application/vnd.in-toto+json
