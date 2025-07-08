## `gradle:jdk24`

```console
$ docker pull gradle@sha256:aa3bc1e0e1afdfa6c2cf04b5e721f6bfa4633a803dfd44742709a10382fa923a
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

### `gradle:jdk24` - linux; amd64

```console
$ docker pull gradle@sha256:9be3bc846ecc522f613f296d6b47b0db15f8210b8ad68524fed4ab27b32b2218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.7 MB (343742108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6711554a34537f05927cb1e39d4336be882aba2f85ac96d02e1e3feb08221695`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='4e953ec63e141b667e02f7179304c6553cbd13ba94b60dcadd8e45c7f309c89d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip         wget         curl                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER gradle
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER root
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ace9135fe177dbc977972cb7c32f6018a3eb9152d64603a95dc197980524d75`  
		Last Modified: Wed, 02 Jul 2025 03:10:35 GMT  
		Size: 21.3 MB (21327153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7355f79d186afa2bab0ee7e1b16311ebcdcccee2150ed0b2ce7a04588eac3172`  
		Last Modified: Wed, 02 Jul 2025 03:10:40 GMT  
		Size: 90.0 MB (89960858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b5ff4c98f7a2e9191dc5b8e6a94900ba8580310409cb1afd9d05df5da77d1d`  
		Last Modified: Wed, 02 Jul 2025 03:10:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8c573d792993c869e2fce905df56126023f5a66900da9561c98abe78a1cc20`  
		Last Modified: Mon, 07 Jul 2025 20:32:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109664e4341b8a9a74eb151b669d9ddb55c76909a592d2884c00d795a5c6dfb8`  
		Last Modified: Mon, 07 Jul 2025 20:32:41 GMT  
		Size: 65.3 MB (65281996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51b915f141522776ed00e330647b1549e789582805447ef937ebf881dc272e8`  
		Last Modified: Tue, 08 Jul 2025 00:08:52 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4019e6657c23672c6671dc48a6c8b1e4b161da53ecc33125e61c5ded315b6787`  
		Last Modified: Mon, 07 Jul 2025 20:32:37 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24` - unknown; unknown

```console
$ docker pull gradle@sha256:318987fff532f7334e23e3d21f27849044d10573045194c70b116d8c2b2c4ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7373534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675cd71c7cbd42b2621606b16b45b2dfd7bdb5a62c2e15f04b22dd3bd7a870d9`

```dockerfile
```

-	Layers:
	-	`sha256:73414afb72b873aefcb9d5bbfb9f1f9eb7b3bf9b5a8e44f4d5513293e1acc652`  
		Last Modified: Mon, 07 Jul 2025 23:27:20 GMT  
		Size: 7.3 MB (7348625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ab3f6263d9ef3324ba5a90e82fc54fdd541e50217fc8a214e238ca5668fe443`  
		Last Modified: Mon, 07 Jul 2025 23:27:21 GMT  
		Size: 24.9 KB (24909 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1234184354d886e8a263a68f08a30cc7462f5081c7f9e98d2e336b923d3dc1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342658853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3026e2e14e941e44eaa0858d92279093d971cca1a54761d9711eff7649d938`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='4e953ec63e141b667e02f7179304c6553cbd13ba94b60dcadd8e45c7f309c89d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip         wget         curl                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER gradle
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER root
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc4b4b28a18fd481255ce309af64064e14290b301cb6fb3f7a187e11a20ab3d`  
		Last Modified: Wed, 02 Jul 2025 05:15:37 GMT  
		Size: 22.5 MB (22506125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191c3c4642d1e10d593384bb863c5b5c9be00056d069846c4772d6c12dd8bdfa`  
		Last Modified: Wed, 02 Jul 2025 05:15:39 GMT  
		Size: 89.1 MB (89091846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd391f513e73c6decf50c0bf87e0e660c363eaac0c4fc47789e50ef7f83c501`  
		Last Modified: Wed, 02 Jul 2025 05:15:35 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d5d49777ab7e1f216c44205506a9881c915339171c33d2a5d7a80688f419d3`  
		Last Modified: Wed, 02 Jul 2025 08:03:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528cd657349b59fe6bb38cfe1b66a66ed96bba71ef1c1262eab954286c88dcf7`  
		Last Modified: Wed, 02 Jul 2025 08:03:40 GMT  
		Size: 64.7 MB (64746495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39d0f8a6b3e1a96e7a072d212ddd6cac9470bfef0a2756e8b9bbfa10684db5e`  
		Last Modified: Tue, 08 Jul 2025 00:10:01 GMT  
		Size: 137.4 MB (137395202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf87961aaf8cad3760dee3502436370fb111f59e74deb8c3df1d1b3de8140a1`  
		Last Modified: Mon, 07 Jul 2025 20:46:08 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24` - unknown; unknown

```console
$ docker pull gradle@sha256:a3088c7e8fedcbaeac11ea02e7d53d890e4b9ce118b8d754ef5ff0a34f8ec506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3a04d27cce2082e6d7fa12edc65d20169644c990e50d9de2e351e3e92f3294`

```dockerfile
```

-	Layers:
	-	`sha256:510ebc7b5d903b1d92596b60cf7b963ec2ac06d2c6269660759d70591a54b385`  
		Last Modified: Mon, 07 Jul 2025 23:27:27 GMT  
		Size: 7.5 MB (7486332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd8ffdc21badfd4a26102648baaedc5b5d803c8886bd49aef8daab3fb6033a9`  
		Last Modified: Mon, 07 Jul 2025 23:27:28 GMT  
		Size: 25.1 KB (25106 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24` - linux; ppc64le

```console
$ docker pull gradle@sha256:d3c53db12f33e16382a5e7a8c5be510e358c61b64e7295ddacfed7d198783444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354657886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1603cf84c0fb4455d8985c66181ff6d3427e11d253a2918b1bb4a321dd1534f4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='4e953ec63e141b667e02f7179304c6553cbd13ba94b60dcadd8e45c7f309c89d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip         wget         curl                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER gradle
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER root
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9068f1b3a05102ac7770db15bcfda0ee5e6d79e5b622b975e66c109c25c8426f`  
		Last Modified: Wed, 02 Jul 2025 03:29:48 GMT  
		Size: 22.0 MB (22049307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45edde785795b884f3f3a72283dd11b77b5294b82b16d4689a35c2b3748aab7b`  
		Last Modified: Wed, 02 Jul 2025 03:29:56 GMT  
		Size: 89.9 MB (89927512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3a4f00234cde67f0f04b3d3ea2fde93610708ba6b218e18fe1b8d9671abc07`  
		Last Modified: Wed, 02 Jul 2025 03:29:45 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4518fe192c66d0800c4a120f9c3d9c126e3fe1fdd166f1c5bd9efb7298d90892`  
		Last Modified: Wed, 02 Jul 2025 05:26:36 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2704fc1473ae7dea833f495344d528c0d72577a0230eac566424a648e57b2b02`  
		Last Modified: Wed, 02 Jul 2025 05:26:48 GMT  
		Size: 70.9 MB (70925710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6343d1819789fdcfa96e1dd24969d2751a2da84b9cd38af2286fea4776fdec`  
		Last Modified: Mon, 07 Jul 2025 20:45:54 GMT  
		Size: 137.4 MB (137395201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91abf5a94d3cabcaf7d53041d154b2419e289b76c6828f54d95213ab03584d3`  
		Last Modified: Mon, 07 Jul 2025 20:46:00 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24` - unknown; unknown

```console
$ docker pull gradle@sha256:007c92c2a9666e6de77483f11992c0fe19f4c01827e8cfd68c29cf81b4474cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59234887f290d60a8d521b909024891f2cfe333ea619685ac8b87c734b16de7`

```dockerfile
```

-	Layers:
	-	`sha256:b00069dae60d545ceafca4504d76058dac97721032489c239def53fbbb10deaf`  
		Last Modified: Mon, 07 Jul 2025 23:27:34 GMT  
		Size: 7.4 MB (7401043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03713f5ab0d8f60ad58d0ed1a3f2cdd48998baea5c3fd4b4a6f49c6692e79f2e`  
		Last Modified: Mon, 07 Jul 2025 23:27:34 GMT  
		Size: 25.0 KB (24982 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24` - linux; riscv64

```console
$ docker pull gradle@sha256:2fadd4a14de45be7a6a943665c3b9580b878bbd019fb6301e67d1d7c3fcbc5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.8 MB (347764651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd6160c615a1083cfe1f6fa97469029d5ab0a7cc74acc2e6b67f628ddfa0ebb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:202c5a7a84e813495c089800398f2ba18952221717db2c10e042ce4179ee6fc0 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='4e953ec63e141b667e02f7179304c6553cbd13ba94b60dcadd8e45c7f309c89d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip         wget         curl                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER gradle
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER root
```

-	Layers:
	-	`sha256:4ccdff8fdb11e14b8e0dab6804aeebce5855635c68b20f199dcf0efcd9b4c462`  
		Last Modified: Wed, 02 Jul 2025 01:17:14 GMT  
		Size: 31.0 MB (30951024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b83a31799d9ae0204fa0895a1a0c2a78245647b684f2a567bfbddeccf4ef536`  
		Last Modified: Wed, 02 Jul 2025 03:50:50 GMT  
		Size: 18.4 MB (18378865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22cfac65731296afe88a265eeb1c6502b3bee267292b92c957a5d952e6d62f`  
		Last Modified: Wed, 02 Jul 2025 03:50:55 GMT  
		Size: 87.6 MB (87627421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d705b25ed08ee641f4c513f3ec2b441811e60c248bef96dd0d73de51ef393d`  
		Last Modified: Wed, 02 Jul 2025 03:50:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cf2222aef9f1b161c151c065e6f77f9aeeaf70270bb172a790dd3a137baf52`  
		Last Modified: Wed, 02 Jul 2025 07:12:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e80758e6d68039ef761d7e5a04ee5ba74be307e358b20f0dab75df145e7387`  
		Last Modified: Wed, 02 Jul 2025 07:12:17 GMT  
		Size: 73.4 MB (73373475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb92b91d81721dbb86d0542db5683a4324db670be1311039171efbb19dbad70a`  
		Last Modified: Mon, 07 Jul 2025 20:50:00 GMT  
		Size: 137.4 MB (137395207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0894beab75af9be992894a951371822c9817e3b5cbfea0bcb552f4b1e6041365`  
		Last Modified: Mon, 07 Jul 2025 20:50:07 GMT  
		Size: 35.0 KB (35025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24` - unknown; unknown

```console
$ docker pull gradle@sha256:24a8dde866c0863d5736d4a643f1ff52707ce4aabcdd45df52d0f77908209078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7477385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e75dedb588a09068242f9c4d255668ad6593dfd6956c1120c3ff23fb6c7f943`

```dockerfile
```

-	Layers:
	-	`sha256:ee288d98f760bdef4ddc8bc26c5ae4357d94ccfe4b38f6999b4e6663a69a924d`  
		Last Modified: Mon, 07 Jul 2025 23:27:39 GMT  
		Size: 7.5 MB (7452403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70534fa77829f5fe6e9feeca930c6c76b133b887be55c348e076247d821e9a83`  
		Last Modified: Mon, 07 Jul 2025 23:27:40 GMT  
		Size: 25.0 KB (24982 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24` - linux; s390x

```console
$ docker pull gradle@sha256:8c22925a32edf85a4d6b00c8ba80fe61b694a0fca0609c891805cf2d3b8dac35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340051787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0e0a20f7e35bca26f626c087b43dbcbb26492f1a954392a5754ff9b9ad89b5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='4e953ec63e141b667e02f7179304c6553cbd13ba94b60dcadd8e45c7f309c89d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip         wget         curl                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER gradle
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER root
```

-	Layers:
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59b22ed00819aa6075cce8478fd9e73447517d6117262bd3188bcc2f931cc71`  
		Last Modified: Wed, 02 Jul 2025 04:24:14 GMT  
		Size: 20.4 MB (20415190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91a279a4acbb0e13f88b6109ca8fcdfb71f7375575338850c8cd344633eeca6`  
		Last Modified: Wed, 02 Jul 2025 04:24:20 GMT  
		Size: 85.2 MB (85217737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c96521c703f3fa8749cf7edba3901578423dc11fa3ac82652e4ab5d4b700a12`  
		Last Modified: Wed, 02 Jul 2025 04:24:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634d17452fa9864695a36ed3549b16e7f0f18d1ad1a3f155eef766a325f0e07f`  
		Last Modified: Wed, 02 Jul 2025 05:27:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc80cb9fb825d7fa75b4dda5aa5de87f9793c860cc99f96844104d0ba551853`  
		Last Modified: Wed, 02 Jul 2025 05:27:05 GMT  
		Size: 67.1 MB (67059402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b526f86e1ed021a7b5f14e4807866b6948be733994f34a4ac45aa240351b5aa`  
		Last Modified: Mon, 07 Jul 2025 20:40:57 GMT  
		Size: 137.4 MB (137395181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bf2aeca152022baa198de5ab6140e5715c5e86fa4cdca3ed173f92b4c86990`  
		Last Modified: Mon, 07 Jul 2025 20:41:03 GMT  
		Size: 35.0 KB (35014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24` - unknown; unknown

```console
$ docker pull gradle@sha256:290389957e32806989781a1bc6e40b7bddaf9c73fcb986cac5aebd9341e254f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7321371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bd5b279852398d49d1d3ab61b5017654f5665f15889f61f73ed03aaf16adda`

```dockerfile
```

-	Layers:
	-	`sha256:390cd65a5e72cafe36c8bcf8d7973449d0081c88a5108919eb64d5f10be0136d`  
		Last Modified: Mon, 07 Jul 2025 23:27:46 GMT  
		Size: 7.3 MB (7296462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f114170170a78c6415a071e73009ddf02411f3910345b21858c0cb2bbe8685c`  
		Last Modified: Mon, 07 Jul 2025 23:27:46 GMT  
		Size: 24.9 KB (24909 bytes)  
		MIME: application/vnd.in-toto+json
