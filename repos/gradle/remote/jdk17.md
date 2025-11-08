## `gradle:jdk17`

```console
$ docker pull gradle@sha256:1985e7d5891cba47a77571dcb71d1ad07cd1a33f95ad107d4a216eba60c2789a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:jdk17` - linux; amd64

```console
$ docker pull gradle@sha256:f1f8130f470094013a50922f62af1f7b3cd352ff9c1715445cccd8e1bae90bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 MB (396751398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc940ae1d8c51025c859096f96f60c20ab657e9a7ba4bad55cf5a8b070980a7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:44 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:50 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:22:00 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:22:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:22:00 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:22:00 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:22:00 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:22:18 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:22:18 GMT
ENV GRADLE_VERSION=9.2.0
# Sat, 08 Nov 2025 18:22:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Sat, 08 Nov 2025 18:22:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:22:20 GMT
USER gradle
# Sat, 08 Nov 2025 18:22:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:22:20 GMT
USER root
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25920ebbd6a84721e1e5049be4abb4372aac6b434e2d35ecadb1e0531e9c829`  
		Last Modified: Sat, 08 Nov 2025 17:59:16 GMT  
		Size: 23.0 MB (22959363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c7168445ec5b684bbb75dd952c2f5ccc6f4fa9d7473349ea381615bfe0637b`  
		Last Modified: Sat, 08 Nov 2025 18:21:56 GMT  
		Size: 144.9 MB (144851049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45898453371862116f2fa2a01423984dca5a071ed2eaf303071a673dae89df1b`  
		Last Modified: Sat, 08 Nov 2025 17:59:14 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c42b4fc61f80b85e95d240e8b993ff3872653af5f525bdfb818646431eb40ac`  
		Last Modified: Sat, 08 Nov 2025 17:59:14 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610001b71381be22aec047605bf4bf0d6bb9c4b0e820bac521897ea463d904f3`  
		Last Modified: Sat, 08 Nov 2025 18:22:49 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474c4ece946eaf1f47228b7c4205be226ca6ef5d50f0f2ee50cbada28897a4c0`  
		Last Modified: Sat, 08 Nov 2025 18:22:55 GMT  
		Size: 63.6 MB (63637523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9544c351e9a2e1e1d9d41a4d809c3cfeabab0a622d22be5b251be86f46f104`  
		Last Modified: Sat, 08 Nov 2025 21:38:11 GMT  
		Size: 135.5 MB (135521656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a869d5e9395b9eb4fbbb2307601fbe71f473870ea05e10d55c2a4919eef36`  
		Last Modified: Sat, 08 Nov 2025 18:22:50 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17` - unknown; unknown

```console
$ docker pull gradle@sha256:08ec82bf23e0ece5e22aff2be5051e2a6e412f371208a46603c947f5cc4b6c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23736a519165e8f7579e48f938affc7c0301c9bf4855f390316581be844d02e1`

```dockerfile
```

-	Layers:
	-	`sha256:73fd5c6ec649302c72b7de98c67fdc016ed74380fe926e17a41a77064f7f5dcd`  
		Last Modified: Sat, 08 Nov 2025 21:32:26 GMT  
		Size: 7.4 MB (7392241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4312c27fbc0336fe40db5cc4cc1346940749aa4baee3dcf122b60529fbecf7`  
		Last Modified: Sat, 08 Nov 2025 21:32:27 GMT  
		Size: 24.9 KB (24852 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17` - linux; arm variant v7

```console
$ docker pull gradle@sha256:a797705af9feaf134419b8ef0fe6cea1f46f0bbfe1e75a83c4499cbf4ea6253c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.1 MB (391139363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4dac59812b07a25733f21caf6ba4b2d2d7038d213709b767e370ecffa7f53c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2d8c6de9cdf8a483982e8423b5c3023652fde1b947d05d599967c073d3d016`  
		Last Modified: Thu, 09 Oct 2025 21:11:00 GMT  
		Size: 21.4 MB (21383305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a559b7733a9936df19b013c333de79c25442918524e2ac1302c5029b72937`  
		Last Modified: Thu, 09 Oct 2025 21:15:37 GMT  
		Size: 142.2 MB (142180759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93df06c9d557b6e1406f2a561d3f93213c30201489b3b973a3424b3f37e94077`  
		Last Modified: Thu, 09 Oct 2025 21:10:59 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802045651bd8d4985b06ad857f89b2b56fb95c0222a4fc289ae18a82a758c752`  
		Last Modified: Thu, 09 Oct 2025 21:11:00 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de07524d589c95686ab3800d67ab639fd6d75bd206c9ba8437663ac540c4120`  
		Last Modified: Thu, 09 Oct 2025 21:18:09 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cca7eb309e4b26b709df6c0dac247e0d5d39bbb176155680e2bacdbb31e208a`  
		Last Modified: Thu, 09 Oct 2025 21:18:16 GMT  
		Size: 66.2 MB (66173829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37c3bb4401b81026862b611852d6a3e4c629db050d58ce374329e261cc389c4`  
		Last Modified: Fri, 10 Oct 2025 00:11:44 GMT  
		Size: 134.5 MB (134514675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1297e155f304425691b85989095405cb8f618876301eb46850bee518f825e744`  
		Last Modified: Thu, 09 Oct 2025 21:18:08 GMT  
		Size: 31.3 KB (31300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17` - unknown; unknown

```console
$ docker pull gradle@sha256:3f15916258b9f0a9c28614478d48fe7ee506e37882336c623bcca60b038cd779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7349048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7c87a4e2dc09a2493d37ccc98cdef4c43f7b8037040e5a600d1bcb432498ab`

```dockerfile
```

-	Layers:
	-	`sha256:da6d2df3f249206443f9d63ce33970b298edf9cf72131e5b91e6a934008ea4d9`  
		Last Modified: Thu, 09 Oct 2025 23:24:56 GMT  
		Size: 7.3 MB (7324006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb1e8f9a63b6e6706169207c400bf4eda7fe6d69ea0ef606052fa177c115984`  
		Last Modified: Thu, 09 Oct 2025 23:24:57 GMT  
		Size: 25.0 KB (25042 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:da63d9133767f3909965e878e56beb354fe6217b77c956e9607f811eab92b96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.4 MB (395382250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed75e0e9185278312f2085c6d0b7def8067fb0853920eb0582b2786d85208fa9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:16 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:23 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:22:50 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:22:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:22:50 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:22:50 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:22:50 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:23:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:23:08 GMT
ENV GRADLE_VERSION=9.2.0
# Sat, 08 Nov 2025 18:23:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Sat, 08 Nov 2025 18:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:23:10 GMT
USER gradle
# Sat, 08 Nov 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561253e11209acbb43fcd6b388c3ddffbca64af1dcbc277fc57abdad62bf159f`  
		Last Modified: Sat, 08 Nov 2025 17:58:50 GMT  
		Size: 24.2 MB (24167132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469f4e46e93d94ef5404dbc9cd2c1262c5d42a1eab43113b343c428d3e2c92f9`  
		Last Modified: Sat, 08 Nov 2025 18:22:47 GMT  
		Size: 143.7 MB (143681466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e005444c1ba34cfa232667001d45aee7021a6ed83e7e96b65184777c0ce00b64`  
		Last Modified: Sat, 08 Nov 2025 17:58:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c79245f97781260d40c83fa2256cfca9667676168b1eeaee191ac429046aa`  
		Last Modified: Sat, 08 Nov 2025 17:58:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3678a085e98b34e86e7aeefcf5e35d9f55d6b4a528d0b10450202a71ddad559a`  
		Last Modified: Sat, 08 Nov 2025 18:23:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eadfe4ad6d544a1cacccc65d96299c6659ea6efc2848ff39cca6276ba58343c`  
		Last Modified: Sat, 08 Nov 2025 18:24:05 GMT  
		Size: 63.1 MB (63086997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0cd67221ef0cf8841e9b241431d8aab813c279ba2c8fa987d520ecbedafbb4`  
		Last Modified: Sat, 08 Nov 2025 21:40:42 GMT  
		Size: 135.5 MB (135521660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2550294b3a7f9c4eb3bfb8aa0c13bfb43b3c120d7e9ab47e7d71ddc1001226f8`  
		Last Modified: Sat, 08 Nov 2025 18:23:44 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17` - unknown; unknown

```console
$ docker pull gradle@sha256:4506d370ae53aec8fb4e358fc58c182ec25fa09be43283d3fee376a8e856cae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7555010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa66884129ce08c979a5efd921b061f31946fccc0a69a85d4eb92631900ea03e`

```dockerfile
```

-	Layers:
	-	`sha256:ab234e88b3b81a4f9e01daf8d7ef35a538e9d338c6c7ccb47702fade43846a22`  
		Last Modified: Sat, 08 Nov 2025 21:32:38 GMT  
		Size: 7.5 MB (7529963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f401503e6993a9082a6557525f77260c27eebe2d2fc4ce620e5f365319ce95fc`  
		Last Modified: Sat, 08 Nov 2025 21:32:39 GMT  
		Size: 25.0 KB (25047 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17` - linux; ppc64le

```console
$ docker pull gradle@sha256:301ef6627176660e71555eceb380a2ae8a47cee593f5c04c4b92a3af4c48d190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.2 MB (406216659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a688d5e40557c5757d6825da0c3ab71c2f6423d0ff8ac768e92ca7871b23de`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40485ed64a16d829ecdf6f09ebfcef0f10e3da8b5606ce65ebf8149476226327`  
		Last Modified: Thu, 09 Oct 2025 21:15:18 GMT  
		Size: 24.1 MB (24101794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427cfd53ba4103e00aa5a78f39271befc3b7508f724fb3bf6838b8bc4b0c3f3`  
		Last Modified: Fri, 10 Oct 2025 00:20:43 GMT  
		Size: 144.4 MB (144375868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41b63d5c0accb28cdb4995fbeded359e9a1006ce7f7204ede7482747b3aa094`  
		Last Modified: Thu, 09 Oct 2025 21:15:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0adc1d40481ae3857281a9dc04940c166c80f6b31e4b1ca10dbdf47ffaa25577`  
		Last Modified: Thu, 09 Oct 2025 21:15:15 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ce6247231618de222cae1d7e24bb298375a6eb0684f3ae4b2d87e837005c1b`  
		Last Modified: Thu, 09 Oct 2025 23:15:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54a31da486ebc74e7b72ebf51b33d04b7b76b5751dea99faa727f904df04152`  
		Last Modified: Fri, 10 Oct 2025 06:13:22 GMT  
		Size: 68.9 MB (68882019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2964f7a45dc632e66e0b92cd12deced4da6b338fb9c39ea66ed2ae533de201a6`  
		Last Modified: Fri, 10 Oct 2025 06:13:38 GMT  
		Size: 134.5 MB (134514677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f659c5ac7d88b4fffc07c18b1463f2fdc1660f96841e3d9993d4041c24f182d`  
		Last Modified: Thu, 09 Oct 2025 23:15:32 GMT  
		Size: 35.0 KB (35018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17` - unknown; unknown

```console
$ docker pull gradle@sha256:4548c1c5784c2ea54f0c0528dac30d69beb0b0c92c5bc27d67d98c49f6ebe1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7461535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb889f94fe05c76cbf8479443f13da77f0d9092e49d065454fd9d1f1c60d05fa`

```dockerfile
```

-	Layers:
	-	`sha256:8e7b0af3a568da16c8b874c192ab32b96d1e3f4dbbebd2edb0d32abd400857aa`  
		Last Modified: Fri, 10 Oct 2025 05:23:35 GMT  
		Size: 7.4 MB (7436570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61776a449249c1cb0d4aee695f5c9e16a8896a015e59311e641772be41e56e0`  
		Last Modified: Fri, 10 Oct 2025 05:23:36 GMT  
		Size: 25.0 KB (24965 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17` - linux; riscv64

```console
$ docker pull gradle@sha256:72555373d68c18e29a13fc1184e0d0fe7fb106e6171db5a12004a1a18a24058b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395866201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb516efbd30a15ee1e0653836da70e88fbf7b11bf25f8036d6ae6fd18d086b1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ab17616cf4e436097dac72b5902ca2cd73114fe92dc0252d55ec741bd29f55`  
		Last Modified: Wed, 15 Oct 2025 06:43:49 GMT  
		Size: 20.1 MB (20143051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551035489d743f17dc9740f3c01b799c7d98b9883451ccb9480760aadc3b4234`  
		Last Modified: Wed, 15 Oct 2025 09:15:47 GMT  
		Size: 138.6 MB (138580506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a88fe41db3f5505f916ebc5c378fca961448a3cfe5efaada32fd02f9b995cd2`  
		Last Modified: Wed, 15 Oct 2025 06:43:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b81bb73b26c3bac26deebbdec70892c0e1d5ba5913751f81f98d8564db2059`  
		Last Modified: Wed, 15 Oct 2025 06:43:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35baf8f9885781a12d6702617fc1d49ae2c453146d31276dc16db4ab1464591`  
		Last Modified: Thu, 16 Oct 2025 01:07:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecca37a0fd22a26292ee8c68b60a3e86a4e5f88ed7e647e2b6ebef0a8ee9444`  
		Last Modified: Thu, 16 Oct 2025 01:07:17 GMT  
		Size: 71.6 MB (71637758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f602920248223629f1a3c7f928f7a66f41bf384a9ce38496c1c172fa30a28b`  
		Last Modified: Thu, 16 Oct 2025 02:32:59 GMT  
		Size: 134.5 MB (134514728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2db23ac0a2093ed39f6ae1a5af42b5acf0e8cff629a9dca605942ccdfc372d5`  
		Last Modified: Thu, 16 Oct 2025 01:07:09 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17` - unknown; unknown

```console
$ docker pull gradle@sha256:7f00f59f62ba5e35e92e9e1743be22098a5c1138a92eb041a582ed8a6f6becef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad074f6de234e6c13c946f0409761f8e23c38d51452b96d172e6c511307bd50b`

```dockerfile
```

-	Layers:
	-	`sha256:df0f63fd4f4c07049f42bc6631fdae692dec799cb0dc2ec7d620c48a7a2084f9`  
		Last Modified: Thu, 16 Oct 2025 02:23:11 GMT  
		Size: 7.5 MB (7487312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aac4b216d66001f685ff8b211eb51fb7736e820b03882170d0d1256a99ab731`  
		Last Modified: Thu, 16 Oct 2025 02:23:12 GMT  
		Size: 25.0 KB (24965 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17` - linux; s390x

```console
$ docker pull gradle@sha256:b6f38f8dc9d2339044379c66373b5a615ab6b57307189df7d5e412852133f67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386661711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6910ecb298d6be536ce627f8d0932bc5d4db1bfc41fcc25ae7562211c0ddbcf9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb2418258ce4193adfb9d0a430930e1ef9ab71ec6b05b10dbbf0f87254a3e80`  
		Last Modified: Thu, 09 Oct 2025 21:12:32 GMT  
		Size: 22.1 MB (22128715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3a2ab96e3758fc2e9f906850ab64cf8dc3657a6d1e791d0f19b94dd1d62fae`  
		Last Modified: Fri, 10 Oct 2025 00:03:31 GMT  
		Size: 134.7 MB (134729439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428bf1bb7be4032968b19f00023bfad9e6c34268672d4b0b0f6e136eb1c0af59`  
		Last Modified: Thu, 09 Oct 2025 21:12:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8460cf5afef340d12e453c261d8edc9b01b4efccf6356612b4bb9f5fc582370f`  
		Last Modified: Thu, 09 Oct 2025 21:12:29 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cf1757f80e205c7df993366a4a43db853facb886df8c2ba696b222942fd5a1`  
		Last Modified: Thu, 09 Oct 2025 22:27:11 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fa139b39b33cb7442348d6e09778af1a11729374a7779578d0519b2932fb13`  
		Last Modified: Thu, 09 Oct 2025 22:27:17 GMT  
		Size: 65.3 MB (65343967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496568edf10545c76d902e2dd85fd9c75f6888ae1f0c021251c112b1bae9f89`  
		Last Modified: Fri, 10 Oct 2025 00:03:54 GMT  
		Size: 134.5 MB (134514675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c05e4555a502548239814f255ddac5e18b25a2bf6af8e9a1bce77756a8df2e`  
		Last Modified: Thu, 09 Oct 2025 22:27:12 GMT  
		Size: 35.0 KB (35006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17` - unknown; unknown

```console
$ docker pull gradle@sha256:adafdc5f183a67ada30fc3cf72bca6c54c288348d149437b4861488847fd71c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7355629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded0ee4782092921d8592243652fad6f9e182577eb8b8a6d1a6b09288e6634`

```dockerfile
```

-	Layers:
	-	`sha256:b7b3f46808d25b395095fae06eb3c26eae9d57bd21d97151dba7fa6f440a7bda`  
		Last Modified: Thu, 09 Oct 2025 23:25:27 GMT  
		Size: 7.3 MB (7330739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19962633fcdf0a5ef68b1324edb5dc321555d078ac94fc7164ed341113595536`  
		Last Modified: Thu, 09 Oct 2025 23:25:28 GMT  
		Size: 24.9 KB (24890 bytes)  
		MIME: application/vnd.in-toto+json
