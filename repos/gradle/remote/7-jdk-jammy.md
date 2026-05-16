## `gradle:7-jdk-jammy`

```console
$ docker pull gradle@sha256:40d37edc2c3be072c3f26bc50d1bad14d58edd816e5d7cdf786d28eff57b8739
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:7-jdk-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:a8fc7f938f2e1edc5b51d15b3567bed084f6cd36388fab1d986b0e7f610c7275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.7 MB (375679841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd198ad497b8ecea03123649751c67f90fdfcb2a020c985e79154e9498539cb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:15:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:15:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:15:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:15:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:15:47 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:15:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:15:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:15:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:15:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:15:55 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:44:06 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:44:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:44:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:44:06 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:44:06 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:44:18 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:44:18 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 15 May 2026 21:44:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 15 May 2026 21:44:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:44:21 GMT
USER gradle
# Fri, 15 May 2026 21:44:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 15 May 2026 21:44:21 GMT
USER root
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909fe7dc1afc2b7c2ce46b1d0166713560a7d2f913022d4e991dd6d98701a2b3`  
		Last Modified: Fri, 15 May 2026 21:16:11 GMT  
		Size: 20.7 MB (20696952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937c31685fefe899abb3e773bf9e4fea73fcbd2cc6f2e126fe41ac4a69b28397`  
		Last Modified: Fri, 15 May 2026 21:16:14 GMT  
		Size: 145.9 MB (145912351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ba0d2efe79548df209692310f9d4cc47306c76336e362f4f125b29470ab56f`  
		Last Modified: Fri, 15 May 2026 21:16:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb50d9aa1fdda8a54b2787672840c41a0cc1165e14d3f515c888e3cde82ffb`  
		Last Modified: Fri, 15 May 2026 21:16:09 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e69907c407d109c99185d080be830e805d765bd7c0bb05f63c616c917753247`  
		Last Modified: Fri, 15 May 2026 21:44:40 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00151167531fcc57a6b18a140509e8997ac7bb9c0943c83606c9be3e01a8a8d6`  
		Last Modified: Fri, 15 May 2026 21:44:42 GMT  
		Size: 50.8 MB (50802753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013aa3f67bac7f532a6cd8faab3e676222d20f3a6ae067258d525d864bb42466`  
		Last Modified: Fri, 15 May 2026 21:44:44 GMT  
		Size: 128.5 MB (128469422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ab45fcd0e429762c86ffd3edff4712e9195d68ffdb2b4d40a2bcfd8512d01b`  
		Last Modified: Fri, 15 May 2026 21:44:40 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:ca7b33776a197e19029e31c9e25b60cdc2fe8f5ceb6c1f4b9740d9d5312be42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7799626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d20694b9e0092bb1ff4754c098ef71b9915daa18e21a4f6a47e06fccb5f669`

```dockerfile
```

-	Layers:
	-	`sha256:6f1fac7d23c0d17bbe072a21c2189fb5292432779cfa657d74d0ebbb499300d9`  
		Last Modified: Fri, 15 May 2026 21:44:41 GMT  
		Size: 7.8 MB (7775049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea197d28b9b51a039c482e3f0a716516e7b4eb1d1fc089800ff2201029c06b0`  
		Last Modified: Fri, 15 May 2026 21:44:40 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:d1d69c1c63a973145f0396365a48ecb60beca64584fdc11508e9481f6f65a9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.8 MB (372793535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1768429ccb76eb82952d2c0dc9373ad4c07e175fd739737625baf38ac380f5f8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:51:37 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:37 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:41 GMT
ADD file:1699ef25ec41cfa214b8beff2f000963a775084d9ce11ff74fa817bb458c27c3 in / 
# Sat, 09 May 2026 04:51:41 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:12:13 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:12:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:12:28 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:42:49 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:42:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:42:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:42:49 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:42:49 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:43:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:43:08 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 15 May 2026 21:43:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 15 May 2026 21:43:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:43:11 GMT
USER gradle
# Fri, 15 May 2026 21:43:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 15 May 2026 21:43:12 GMT
USER root
```

-	Layers:
	-	`sha256:422dc0f0ec960f769d890f368bdf0a0ba195325ef487f5b07a4d06efaa7b2c41`  
		Last Modified: Sat, 09 May 2026 05:25:04 GMT  
		Size: 26.8 MB (26841796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e854a0ec63edd6d1ed46a4e0af7c4a85743bf98c06662cc83d0f5002adf10a`  
		Last Modified: Fri, 15 May 2026 21:12:44 GMT  
		Size: 21.0 MB (20990812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de6409377c797a96d6583705f82200ea6100c61e8ae0b806fe9684ab6b178a5`  
		Last Modified: Fri, 15 May 2026 21:12:47 GMT  
		Size: 143.2 MB (143187344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844c7846ce6616a29508ac673ca9d0abfe395eccc97a693f25493035ee52084d`  
		Last Modified: Fri, 15 May 2026 21:12:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08489d864a67abe3ddf2a6e0e643822b2ced9036760ca7f4c35ba4e23753eb1`  
		Last Modified: Fri, 15 May 2026 21:12:44 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ff8883d919160c4e5f95804661716103dba5477434e696dbed55484e5a28e3`  
		Last Modified: Fri, 15 May 2026 21:43:30 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a203244ecc06c58c4bdd60aeea98fd4271f6be562d2376d049d1e6187f75cd7`  
		Last Modified: Fri, 15 May 2026 21:43:33 GMT  
		Size: 53.3 MB (53266089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192153c989621bbbd207750652beb7e9af43f0fcaf42df937487ccd664f1f2b7`  
		Last Modified: Fri, 15 May 2026 21:43:35 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c0b76b1bf4aec5d45a01243b5fb23ee00143e4cd084a78e798a0065c011d9f`  
		Last Modified: Fri, 15 May 2026 21:43:30 GMT  
		Size: 31.3 KB (31290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:aa0d5362cb82da5d8ca17f4141706947af341ae0852c710cf4f6ab43711b23c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7718119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8987846d209a5047d159283d46080e90c1911a9985a1a4e3d1bbc29a2fddd326`

```dockerfile
```

-	Layers:
	-	`sha256:cf462453f1415e8610a2227768b16779d549080d4918c85a5e876499dd15a698`  
		Last Modified: Fri, 15 May 2026 21:43:30 GMT  
		Size: 7.7 MB (7693383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab6570497aa1696dad7ed5b31636ab94ed7646611eb441ed0636bbc5a3ecda5`  
		Last Modified: Fri, 15 May 2026 21:43:30 GMT  
		Size: 24.7 KB (24736 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:61e57a4dba5cfe202851df85a8d08828cc18511e78b3624d09b9417cb9f66f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 MB (373362489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b83ed1729fe6ca3c0e7e529075ed01c77550a6dede56fa4f97961f2fa698578`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:16:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:16:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:16:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:16:20 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:16:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:16:29 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:44:47 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:44:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:44:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:44:47 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:44:47 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:45:04 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:45:04 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 15 May 2026 21:45:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 15 May 2026 21:45:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:45:06 GMT
USER gradle
# Fri, 15 May 2026 21:45:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 15 May 2026 21:45:07 GMT
USER root
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bc8906a7610c5b0a4df49ed0c81a0753ae645c3b3d827930f9e97113bd2c00`  
		Last Modified: Fri, 15 May 2026 21:16:47 GMT  
		Size: 22.1 MB (22110130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44773ebf0b26708d3c1a138319ca2dfc1dea75e131eb674bbea177043ac0460`  
		Last Modified: Fri, 15 May 2026 21:16:50 GMT  
		Size: 144.7 MB (144741869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af9943ce0bcdad9ab8323df7c126e54f6dbd8374052a398c962c880573588b3`  
		Last Modified: Fri, 15 May 2026 21:16:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ae8d3db94381716ad314cd2a45c3486c7c18b7eb32c026331be40f76fb6e8f`  
		Last Modified: Fri, 15 May 2026 21:16:46 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37a92d0ecf79164d1a1f8db1f5c162be21398b98a47f4b22424a9c429c6da79`  
		Last Modified: Fri, 15 May 2026 21:45:25 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55d2d6fab0a8d5469aacc410dd6ab3a7419bf1f7af196cfa75ee8773388251c`  
		Last Modified: Fri, 15 May 2026 21:45:27 GMT  
		Size: 50.4 MB (50368136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432dfd14b765d0346ef426c4b5a4bf719e735818d8ace168311e9fd8c9dd8a7`  
		Last Modified: Fri, 15 May 2026 21:45:29 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e967e80d98a0b087bc2766b85a5b110b8832fb86fcb0415c91f7b37aa9b211a`  
		Last Modified: Fri, 15 May 2026 21:45:25 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:85de8bf07dbc0505200cdc3edde5f9843226445f56e5eaa9b90431b3bc738a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7901517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3115c9345a734ae1c70db35ed010323109d917b2fe3ed2c0e0a48859b3332dd6`

```dockerfile
```

-	Layers:
	-	`sha256:f058913793366f9cea20d41bb4735cf7515aaea3e07b342d1d007eeb7522586e`  
		Last Modified: Fri, 15 May 2026 21:45:26 GMT  
		Size: 7.9 MB (7876732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eebf587473d893c61a46c8036e51403249b014c7cb0651fad3de9e1224aff2b`  
		Last Modified: Fri, 15 May 2026 21:45:25 GMT  
		Size: 24.8 KB (24785 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:5679ffdb38b8237169d2220aef7d0d764ebc8447d4289f0327336eb9ca0872e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386304941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9760cb530366208b95a23d47ffcc04c6d722b0c8a5c26242c13dad63930e55e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:12:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:12:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:12:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:12:31 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:12:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:12:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:12:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:12:45 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:56:44 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:56:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:56:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:56:44 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:56:44 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 22:00:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 22:00:38 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 15 May 2026 22:00:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 15 May 2026 22:00:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 22:00:46 GMT
USER gradle
# Fri, 15 May 2026 22:00:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 15 May 2026 22:00:47 GMT
USER root
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ba0627ad64b0a6b1ebf88e18bcc537d7ccaf8ddfb659f50480d115f4660520`  
		Last Modified: Fri, 15 May 2026 21:13:21 GMT  
		Size: 22.6 MB (22589674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccde48847baa039e482b5a40c28108c264b0836efc8273fd6129013727164050`  
		Last Modified: Fri, 15 May 2026 21:13:24 GMT  
		Size: 145.8 MB (145773796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7253369a6abf18b9171f1221e5b46f0c48d97181e284e3df6ef53f33d248de8b`  
		Last Modified: Fri, 15 May 2026 21:13:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c539817e8010f3f18434713ca4911e7a7c6eb473e295887c368508793e0eb`  
		Last Modified: Fri, 15 May 2026 21:12:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5763c3aaa04c0d604ebe97bcaa6f74e7b7d8d210c77634632ca302d80567f37`  
		Last Modified: Fri, 15 May 2026 21:58:03 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb123c371532b4727881d8673f224dcf490e5d95a86f648fd5d657d9343f7125`  
		Last Modified: Fri, 15 May 2026 22:01:26 GMT  
		Size: 54.8 MB (54783537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced941d49f589da9e7f1f865494bd7058c15ed2eb2af8e3a34d23e2c46f691fc`  
		Last Modified: Fri, 15 May 2026 22:01:28 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acad288d8b7142187b72b9dde6220ac295a3ace72c2a5576caa73aed423eaef`  
		Last Modified: Fri, 15 May 2026 22:01:23 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:3ed5178a86a980f2c63fe3492bbb007d15e0ab64e1cdc0cf61daf87108ef13fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7830585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f5c1283a34221b8f1470675261992b6492d8bab26e0c95e9020c967d29f74c`

```dockerfile
```

-	Layers:
	-	`sha256:4a4d1858814fa03a61c6d872a1daefa274b6440f9fa9f47a8c6dc0d4e7983364`  
		Last Modified: Fri, 15 May 2026 22:01:23 GMT  
		Size: 7.8 MB (7805929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2fb12d8d1fa0ae48489b75aea403a105f7f4bc1d0be5e19748aef64bbc9d9b5`  
		Last Modified: Fri, 15 May 2026 22:01:23 GMT  
		Size: 24.7 KB (24656 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:50c58728917aaa5fa29192c46d583527fc0d5a7bf52274d05db48f00e0223e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.5 MB (363534621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26655c2d755ede16fc44ad26799b5717e203d1c3f0a8c4c328013d22eeb67cde`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:12:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:12:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:12:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:12:42 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 15 May 2026 21:12:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:12:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:12:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 21:12:56 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:41:15 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:41:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:41:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:41:15 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:41:15 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:42:47 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:42:47 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 15 May 2026 21:42:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 15 May 2026 21:42:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:42:51 GMT
USER gradle
# Fri, 15 May 2026 21:42:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 15 May 2026 21:42:51 GMT
USER root
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae77d3b5f2cc94fd4e05c475655187c63284802cb4d3d3bf62e4de800a5ca60`  
		Last Modified: Fri, 15 May 2026 21:13:33 GMT  
		Size: 20.4 MB (20419503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc78ef64a42cf04e89b70e62492e4ce4e2cb215eadef27e7217f92bfaef439bc`  
		Last Modified: Fri, 15 May 2026 21:13:37 GMT  
		Size: 135.9 MB (135919301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7ea29159b5fa1e507623a8485a25db8fc1decc03e96d20c1f5bedada985127`  
		Last Modified: Fri, 15 May 2026 21:13:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a8ffe1ad79b6ad54f5963ecdc3367f8256404e487fe328ab2d34279fe75997`  
		Last Modified: Fri, 15 May 2026 21:13:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665a64d49e09fcc2fcf3fa8022733be266ada23b751c15ffb0221b824e0baaa2`  
		Last Modified: Fri, 15 May 2026 21:42:14 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44900d90455b38e4bae0fbd7e453178d3d0a1ce28453dbb21ab57d572529789`  
		Last Modified: Fri, 15 May 2026 21:43:23 GMT  
		Size: 50.5 MB (50482311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1b25d34067e97a0e92f3c245fe71b4e3037f8df43f75024a45c34540afac16`  
		Last Modified: Fri, 15 May 2026 21:43:25 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4919286037dfcf08951a020d6e58d1ab71776fc7d30c9976f2258a336b18293`  
		Last Modified: Fri, 15 May 2026 21:43:22 GMT  
		Size: 35.0 KB (34994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:ff0458ab844affb27844110071384239d85feacf85a5ddf53bb91887fd223beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7723302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63935ef90983a9fc3e479324e683c3b719a9a7eec4cf4519f0e63adbb7731431`

```dockerfile
```

-	Layers:
	-	`sha256:fc6e44660ef1f1affb722f7a1dee7cd40cec82ab4e53189cf701c5bb3df38d41`  
		Last Modified: Fri, 15 May 2026 21:43:22 GMT  
		Size: 7.7 MB (7698725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d043a0b91054e32ee40dbaabcaf87814bcb4eb8577091eb4b3e33c8845c1ef66`  
		Last Modified: Fri, 15 May 2026 21:43:22 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json
