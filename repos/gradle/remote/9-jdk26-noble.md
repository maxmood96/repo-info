## `gradle:9-jdk26-noble`

```console
$ docker pull gradle@sha256:dc6ed1d75d015948e5076e940049ef3fc36e19a913b7eddb01c736b7304d4586
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

### `gradle:9-jdk26-noble` - linux; amd64

```console
$ docker pull gradle@sha256:137922f91cc2720dec2211c287d64ed5f3f3fd39a1eee9574ed094f515ae5978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352111182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381341707bd57047460c8ef8192c2b6bec38775e92dbf5463e664c2285fa326f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:05 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 08:15:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        arm64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        riscv64)          ESUM='f1b762d6d86599627983df200f215bc970444a697159ca3fae93208756b44715';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_riscv64_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:15:21 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:13:49 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:13:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:13:49 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:13:49 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:13:49 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:14:06 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:14:06 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:14:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:14:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:14:08 GMT
USER gradle
# Mon, 29 Jun 2026 17:14:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:14:09 GMT
USER root
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8db1c2680b0d5b376e8fec61d6508c298699625c43378344db199c0bebbd67`  
		Last Modified: Tue, 02 Jun 2026 08:15:36 GMT  
		Size: 17.5 MB (17463892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28cfb6c33e0732145e2fb90f60ad4ac7ba15195df40cc6d9b6c1e64c19505b9`  
		Last Modified: Tue, 02 Jun 2026 08:15:38 GMT  
		Size: 94.7 MB (94653529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be3a777610ce7f408606e8affc3859cdc17925e8779ea6ac91b71dc9c6366cf`  
		Last Modified: Tue, 02 Jun 2026 08:15:35 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3436e5c339a955af9030ca566e5fbd098b71c2524de55b9cf13e0bbbe45a96d`  
		Last Modified: Mon, 29 Jun 2026 17:14:29 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e459ac954dbb2b04dafe296885146cf81dc74bf38c10ae67d2c60f33520e08b1`  
		Last Modified: Mon, 29 Jun 2026 17:14:34 GMT  
		Size: 69.6 MB (69635500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7246d5e6c0bfae01ec9d828dac5185c5c85896522780b156300c69aa8ef8523`  
		Last Modified: Mon, 29 Jun 2026 17:14:38 GMT  
		Size: 140.6 MB (140596026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250b051ac4c8c5175825034d1450b11e66e00dbd2ac434a080bc996cbd43ad3b`  
		Last Modified: Mon, 29 Jun 2026 17:14:28 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:7e95aa694d65ad8f867a65fa716313fa2e5c2ca9a64b6f184327af2055c76128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7312788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51aa406a10f9771fca0aa2682c2042b238fe5b9067e1ce69c63068f066ba2286`

```dockerfile
```

-	Layers:
	-	`sha256:df0187f1a85d8e164a3d03b5f1342747078fb2b497c9443c882ab275c4f4f0ae`  
		Last Modified: Mon, 29 Jun 2026 17:14:29 GMT  
		Size: 7.3 MB (7289115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62826feed1e745effc0854ad43de5ca4c9f883b52eaf7da63b1124aa586d18b9`  
		Last Modified: Mon, 29 Jun 2026 17:14:29 GMT  
		Size: 23.7 KB (23673 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:23f49165a1bacae1925f2d837a6aa9f3899bdb2d4732ede17146217dc1a9dd92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350887031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f982e9e794b2475b6be645259da707d85e4b8d122125a60a959c706de7beadbd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:16:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:16:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:16:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:16:28 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 08:16:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        arm64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        riscv64)          ESUM='f1b762d6d86599627983df200f215bc970444a697159ca3fae93208756b44715';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_riscv64_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:16:50 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:13:37 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:13:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:13:37 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:13:37 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:13:37 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:13:56 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:13:56 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:58 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:58 GMT
USER root
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d591618577210cc9d63fd4e321e9c9caf2af010243339b5f3c10e8fc51f88593`  
		Last Modified: Tue, 02 Jun 2026 08:17:07 GMT  
		Size: 18.7 MB (18656830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a066be6a90ede643defd34d47d66b204ede2409915ae820253ac7091249ca9`  
		Last Modified: Tue, 02 Jun 2026 08:17:10 GMT  
		Size: 93.6 MB (93630033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2f66b51917ee12fbcf8b3dc0a96a0acabe0910501a73beed45bf2d4c912b9d`  
		Last Modified: Tue, 02 Jun 2026 08:17:06 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379c7829800957daffda94f77e99c13aa9994a2ffd3d573924016fcdc40b9df2`  
		Last Modified: Mon, 29 Jun 2026 17:14:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b05fba14f22edb59e0504d672421963a0d39fba4c0f4c77a0b08391211407a`  
		Last Modified: Mon, 29 Jun 2026 17:14:22 GMT  
		Size: 69.1 MB (69094597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98339fe6b91fb40d1e834fa0927c696b1464f5e48307bbe49aa8354468c71cfc`  
		Last Modified: Mon, 29 Jun 2026 17:14:23 GMT  
		Size: 140.6 MB (140596021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2b632c4fdab9cc33abe53bd7d337b0b89d20e7b9fa63fb7d24039e470001a3`  
		Last Modified: Mon, 29 Jun 2026 17:14:19 GMT  
		Size: 29.3 KB (29327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:4dbc893956f47724b5b873b1e50e4ee360806a6a01bbe50baf1c6b6e905e2af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ae33ce37c79369ad91c355e559414e8a4db0d1b036a862384d077d468e4006`

```dockerfile
```

-	Layers:
	-	`sha256:255bd8d8a77f744cb888af201eb1176d2f43bc81b5f07af0ea8e3ba2f2d59cda`  
		Last Modified: Mon, 29 Jun 2026 17:14:19 GMT  
		Size: 7.4 MB (7426785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c888125458c13e3d105cf5b41e479737625690c98644cefd4c44d3bf8587776`  
		Last Modified: Mon, 29 Jun 2026 17:14:19 GMT  
		Size: 23.8 KB (23822 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-noble` - linux; ppc64le

```console
$ docker pull gradle@sha256:991d921d5bd21849a339e0b4b649ddb7c2f74f5e145c35535042a5d23a5958a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362077513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f314142af9caa5692eeed1aae588a97d5c414d0fd973741638d1092c823eb4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:02 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 08:15:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        arm64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        riscv64)          ESUM='f1b762d6d86599627983df200f215bc970444a697159ca3fae93208756b44715';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_riscv64_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:15:58 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:21:22 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:21:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:21:22 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:21:22 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:21:23 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:22:15 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:22:15 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:22:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:22:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:22:20 GMT
USER gradle
# Mon, 29 Jun 2026 17:22:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:22:21 GMT
USER root
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff079377f8bfab2d37e499094664a0bdae75c48db96afaf694c6aa4cec4ad41`  
		Last Modified: Tue, 02 Jun 2026 08:15:08 GMT  
		Size: 17.3 MB (17330408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ec8146bb87205708a2aa26ea92f3579a8dc1949e70e252232d10d3ab3d04e2`  
		Last Modified: Tue, 02 Jun 2026 08:16:31 GMT  
		Size: 94.0 MB (94029054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1df4ced883fbc3b77349dc6f069f3607c401ae5de46bcd9b8fb9056fb54212`  
		Last Modified: Tue, 02 Jun 2026 08:16:29 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2ddc79fc6c0f9423ab7e2e9c8a80eaa2676941c60a1739546302ac5ad3dafe`  
		Last Modified: Mon, 29 Jun 2026 17:23:04 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc2a7e9126fc38ffb092c8e956355588e43e97aaa01882047a6322986d4b6a7`  
		Last Modified: Mon, 29 Jun 2026 17:23:08 GMT  
		Size: 75.8 MB (75803735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee7d7b809a33cbfc6bea2c60ae93d345189c8dd8ef9d642a814ac6f851c87c4`  
		Last Modified: Mon, 29 Jun 2026 17:23:10 GMT  
		Size: 140.6 MB (140596024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e88511486ef499a7e1d8814362bec159855fcdd696ea5e2745fee0f8e1bd60`  
		Last Modified: Mon, 29 Jun 2026 17:23:04 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:eb3919c91b3cc897bcd74dad34007f88728cb30005f17126a96866c83945c5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7347868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de839f8d279241ce1af6e98e18af86c05faebd682be1c0a2ab933a61945d911`

```dockerfile
```

-	Layers:
	-	`sha256:e1088988dd3baa9da3bb28f427a37d7f4563845693d694c0236ea6bd4551f04f`  
		Last Modified: Mon, 29 Jun 2026 17:23:05 GMT  
		Size: 7.3 MB (7324148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:745e313a41668e36b173ab8a2a96bbfa11da14903b381789d609515e48b58c7c`  
		Last Modified: Mon, 29 Jun 2026 17:23:04 GMT  
		Size: 23.7 KB (23720 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-noble` - linux; riscv64

```console
$ docker pull gradle@sha256:738f2fb940af3a96925baf2d44ca2431f596a9da63532c9af0ef097a6649ac92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.4 MB (356386352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d1cc0c0de07128af66eab8f4d44c9efe372965bd8a3e8997b925640dd4087a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 20 May 2026 02:06:08 GMT
ARG RELEASE
# Wed, 20 May 2026 02:06:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 02:06:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 02:06:59 GMT
ADD file:f1fd7ee282731834f2f36b17e9b538e569ade4ce8b89924b635551ff3a45c706 in / 
# Wed, 20 May 2026 02:07:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 18:29:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 18:29:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 18:29:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 18:29:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 18:29:14 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 18:44:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        arm64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        riscv64)          ESUM='f1b762d6d86599627983df200f215bc970444a697159ca3fae93208756b44715';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_riscv64_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 18:45:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 18:45:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 18:45:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 18:45:10 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 18:08:14 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 18:08:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 18:08:14 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 18:08:14 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 18:08:14 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 18:11:01 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 18:11:01 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 18:11:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 18:11:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 18:11:29 GMT
USER gradle
# Mon, 29 Jun 2026 18:11:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 18:11:36 GMT
USER root
```

-	Layers:
	-	`sha256:924f9a731915e06f77b3487378ddf9426f8422fa1d96461bef1d0e0a35c36743`  
		Last Modified: Wed, 20 May 2026 02:15:52 GMT  
		Size: 31.0 MB (30965919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6462371901b37d6eaf6efde543f245a6a2c576189263e2109906e93a1a0d36`  
		Last Modified: Tue, 02 Jun 2026 18:35:06 GMT  
		Size: 13.9 MB (13850432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c594897d11aa19194aa3184106d667f2b8fb7175c40425dcd29bc9408316062`  
		Last Modified: Tue, 02 Jun 2026 18:48:38 GMT  
		Size: 93.2 MB (93219282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0c33c6fb066ba1f4a49cfe809c0150e8df0989469edb093fd925a500337e42`  
		Last Modified: Tue, 02 Jun 2026 18:48:25 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e66f0fd0bd6269e34cef3efd1f6e49faac645c893785ad4b1199f8d5e4c183b`  
		Last Modified: Mon, 29 Jun 2026 18:16:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80518c1d487aaed6ceccd715f088325f3720c9ae63eddde2818137324a312d84`  
		Last Modified: Mon, 29 Jun 2026 18:17:11 GMT  
		Size: 77.8 MB (77750492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886992e2baefd3384dfe67b20568d5dbb93f6a0146c7bbb57291f0a78def988b`  
		Last Modified: Mon, 29 Jun 2026 18:17:20 GMT  
		Size: 140.6 MB (140596025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15e17fe4bdf232e0c2ae0d84e53fcaeb0f037f8551aa5f4ed1913e54141ba73`  
		Last Modified: Mon, 29 Jun 2026 18:16:48 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:93f8ed28c0d254276e03352c3504a0116348b9549b623e0d65ea0bb4c403f874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051f1ba35ba13cad7782eab234b8b82169732bca129df79e9ae90c5e0e7521c6`

```dockerfile
```

-	Layers:
	-	`sha256:389721e1a3d6ecb20bb5b68d72255d8548198001167db593440c65b65437a7f6`  
		Last Modified: Mon, 29 Jun 2026 18:16:50 GMT  
		Size: 7.4 MB (7375512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd93a8b8803b58767f2affa5cf178fced70c05ea150e5eb9fe5f73f83fbd8cad`  
		Last Modified: Mon, 29 Jun 2026 18:16:47 GMT  
		Size: 23.7 KB (23721 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-noble` - linux; s390x

```console
$ docker pull gradle@sha256:f3b643c48d2281a835fa7d0555a9d991face07de992ec8f79f62530d48288662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349254843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27cc97d4afe76f0a37af9fd0e2e989a59f9c446a25277c5f1394a5165d9ec931`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:11:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:11:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:11:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:11:43 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 08:11:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        arm64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        riscv64)          ESUM='f1b762d6d86599627983df200f215bc970444a697159ca3fae93208756b44715';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_riscv64_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:11:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:11:57 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:13:16 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:13:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:13:16 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:13:16 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:13:16 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:13:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:13:34 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:38 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:39 GMT
USER root
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3afa073aa7a7c45f661e23430cbd31f86d9ac387df8b959000a18e39bc7a9d73`  
		Last Modified: Tue, 02 Jun 2026 08:12:20 GMT  
		Size: 16.3 MB (16312073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b00cbe8e459715698ba2594eedc68b091f9875848f35556ca9c62512defdc03`  
		Last Modified: Tue, 02 Jun 2026 08:12:21 GMT  
		Size: 90.7 MB (90665398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928c64c9657b051260b74e2a3f360acf195525f4b38cc5dd2cd74ec69397734b`  
		Last Modified: Tue, 02 Jun 2026 08:12:19 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39d1506a5f78e4a8108b8827ad97a02b49c1d8013a796c667531763f4715d4e`  
		Last Modified: Mon, 29 Jun 2026 17:14:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b87ad9d04f2f4a85067bdd662bb03956a4db4d5efc2f16e3253fd614794659f`  
		Last Modified: Mon, 29 Jun 2026 17:14:13 GMT  
		Size: 71.8 MB (71764319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c746860fede6db9895b7e8bf320b6962df2178803c42b405557e04da70be257`  
		Last Modified: Mon, 29 Jun 2026 17:14:14 GMT  
		Size: 140.6 MB (140596029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f841daccd12d14a2e07a2bcd8688bac5ac7055d67afa65c7435bcc9c66cce3a6`  
		Last Modified: Mon, 29 Jun 2026 17:14:11 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:196de63e1232bb55968f643d15effd8240ba1c7767027a803f4848a2e0d1efdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7243272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5875be383db7c623c83f625cc1674a71cd7b3ba6033b17fdd2f9141b70c12af3`

```dockerfile
```

-	Layers:
	-	`sha256:98bdd512b54843cabad730425d9594649ca285964ae4043fa25f044f9d754d3a`  
		Last Modified: Mon, 29 Jun 2026 17:14:11 GMT  
		Size: 7.2 MB (7219601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aafae2dbcf53229825c0b12d02b707ad1c6471fca6660f7919853f2e584e7973`  
		Last Modified: Mon, 29 Jun 2026 17:14:11 GMT  
		Size: 23.7 KB (23671 bytes)  
		MIME: application/vnd.in-toto+json
