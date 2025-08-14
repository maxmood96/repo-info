## `gradle:8-jdk-21-and-24`

```console
$ docker pull gradle@sha256:37ad9d00a1a2b49438add36001330c6bde2b5e089a8d58088b4eb445303f7712
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

### `gradle:8-jdk-21-and-24` - linux; amd64

```console
$ docker pull gradle@sha256:3d57fcee4954b89cd78e1d32e9d84462e9b141510a85c72a2a56cbb632bdb905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.6 MB (501560858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf5b8701b26f0e519a1a0463c7baaa6b8b833e721b3acdf536edec3d72a7d71`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
ARG RELEASE
# Thu, 17 Jul 2025 03:50:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 17 Jul 2025 03:50:10 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Jul 2025 03:50:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["jshell"]
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51d8cf184477166509f3db9216fce57ab67d94b9b882f2f10ff2891baba2550`  
		Last Modified: Tue, 12 Aug 2025 17:24:54 GMT  
		Size: 23.0 MB (22958720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e2e04796b2ee0ed28666a3def2a846c561134cbd2d024b273991f8c85936f`  
		Last Modified: Tue, 12 Aug 2025 17:51:57 GMT  
		Size: 157.8 MB (157809399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967391d7d212b197d98e34a983091c6878b25ce3fb014d6f01065f6f6167096`  
		Last Modified: Tue, 12 Aug 2025 17:24:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9246e450bedd7659121fadbb2365286bed2c7be3365f401ba6cf042289bd63e0`  
		Last Modified: Tue, 12 Aug 2025 17:24:50 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c982c7491bb2bd256afd0c5b1a9e79b0bf416cc5c35c7bddfe45d179046f786`  
		Last Modified: Tue, 12 Aug 2025 17:53:41 GMT  
		Size: 90.0 MB (89975235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e02c573494beaecd6061cebdb9fecd33164a3698a9c668e43037534e3cc071`  
		Last Modified: Tue, 12 Aug 2025 17:53:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d25d61a7acaf27b7cdd7dd387d236ad1da790cab63bdccf5d40bc15360d6a0`  
		Last Modified: Tue, 12 Aug 2025 17:53:33 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e66d151bff83395352554cf244e55abc13f2513bf1a487b8c1a07939e539b92`  
		Last Modified: Tue, 12 Aug 2025 17:53:44 GMT  
		Size: 63.6 MB (63638854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a217f2740d292dec11ded4860591acec47d63da04e5e3b5fa25ccc16c01d435d`  
		Last Modified: Wed, 13 Aug 2025 02:43:09 GMT  
		Size: 137.5 MB (137451404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24` - unknown; unknown

```console
$ docker pull gradle@sha256:1ecfe9e781b794b049fae38364542e0afa1d01d429a656381d66d4ab241109be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7538155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ed206cf02cc36020677e683c4b108edff96d7b6c0beb68d16e0377693096aa`

```dockerfile
```

-	Layers:
	-	`sha256:b3076f977aedfdc0fbb1768f78e125151d6c9d214d901a898c2a8ae49e2ef53d`  
		Last Modified: Tue, 12 Aug 2025 20:22:43 GMT  
		Size: 7.5 MB (7506274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e178c6d6c2c08d7ea61c3457766f8c06be7ff92a465303b9b2ecb22cd63eabf4`  
		Last Modified: Tue, 12 Aug 2025 20:22:44 GMT  
		Size: 31.9 KB (31881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-24` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f80c6696b605f30701a3003ad5c1fce61210121b60a158c1ca07d926be2488de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.8 MB (498755703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bea0bbd912c9df5ce7e216d9e40e01bce5eb8efe799a09ea98d2634b9007e9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
ARG RELEASE
# Thu, 17 Jul 2025 03:50:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 17 Jul 2025 03:50:10 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Jul 2025 03:50:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["jshell"]
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5ce41d5de7afb59affbe0233d7397418d2e57ed330589e31f1678f08a6fa5e`  
		Last Modified: Tue, 12 Aug 2025 18:36:42 GMT  
		Size: 24.2 MB (24165644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf34575c4e3b3b166c464edf4e5028e3cfc1c601ff17cfbbf1e7acdee8e50ad`  
		Last Modified: Tue, 12 Aug 2025 20:03:06 GMT  
		Size: 156.1 MB (156088917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1966e7bdaa805e2a3fb4d7f8bd3b8b696ad43a80ee23c4e497b0c806325e31`  
		Last Modified: Tue, 12 Aug 2025 18:38:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc5dbd963a682bc03f830ef4c292f4d1afbbc2fe50658fe169297a94fa1dac9`  
		Last Modified: Tue, 12 Aug 2025 18:38:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31840c9fd0ad0317541aa7a5d6cdc9b03f3756914ac9498939d45a1ac06b5273`  
		Last Modified: Tue, 12 Aug 2025 22:44:54 GMT  
		Size: 89.1 MB (89092799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014c79d4c53498d0b79ee0764fc51e74ada6fe46ac62eccca002fb1bf018f910`  
		Last Modified: Tue, 12 Aug 2025 22:44:31 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c2a77f7c454197ecdde5fd8b5b5a09a9ec0f3728b551bae42ae5b1055b3d51`  
		Last Modified: Tue, 12 Aug 2025 22:44:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebecdddf807bf6520ea36d2b457506110bca8db7564abd26ab8cfa246b700bc`  
		Last Modified: Tue, 12 Aug 2025 22:44:43 GMT  
		Size: 63.1 MB (63087072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2f3c863093ad88a4236c0facffa3dc39182b6ae7df1beabe6a77f871e113f7`  
		Last Modified: Wed, 13 Aug 2025 02:44:10 GMT  
		Size: 137.5 MB (137456857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24` - unknown; unknown

```console
$ docker pull gradle@sha256:023a374f7603003067ba6821dddbd8a9e4b0d39d61e241c0814b08a44eb5b539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7675573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9197bf55549156d0c62add73dca1f20d7c20dec6a2f1d41d0e11c3fa234640`

```dockerfile
```

-	Layers:
	-	`sha256:936751ae7789cfc11567e7484b94207d817130e0c23505b7d2785832970fd8c2`  
		Last Modified: Tue, 12 Aug 2025 23:20:38 GMT  
		Size: 7.6 MB (7643421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c42b7414bece57aced7573f5971686928315d2e55f61e1950d0f89100269c21f`  
		Last Modified: Tue, 12 Aug 2025 23:20:39 GMT  
		Size: 32.2 KB (32152 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-24` - linux; ppc64le

```console
$ docker pull gradle@sha256:2effe88c72d931e7421afc4ccf853de75f9ed16ba3d86ba0997d556a5d81b210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.6 MB (512636880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c3d65accb1069843f4fdb261f53af28524d55c0600a8295186b57a83d6950d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
ARG RELEASE
# Thu, 17 Jul 2025 03:50:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 17 Jul 2025 03:50:10 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Jul 2025 03:50:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["jshell"]
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dac22db2acf299562658bdbfc8f885fd4929a06be6ed9a37bc4736330fe91b`  
		Last Modified: Tue, 12 Aug 2025 17:39:59 GMT  
		Size: 24.1 MB (24101582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e917ebf66df5f21e8f8a6fcb5fed8b8aae52537f9a9f89c75c0290510ce1a6b2`  
		Last Modified: Tue, 12 Aug 2025 18:46:20 GMT  
		Size: 158.0 MB (157969889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07ca97c37923f60b48017e671652f8ec10759b3245737ebab3d46e45bde8932`  
		Last Modified: Tue, 12 Aug 2025 17:58:35 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dafcc6f3cf8a0ab22e0589729586dc5636b06c81225f289939204617ecb117`  
		Last Modified: Tue, 12 Aug 2025 17:58:38 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d28503cfd98258ea3e8b8c558fccb2c823e2b2a2628c7d5867a58cf1e38d4e4`  
		Last Modified: Tue, 12 Aug 2025 23:37:01 GMT  
		Size: 89.9 MB (89918661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a254d618b6a175dc28fa8e09ba465ac3551389f44da02318044e9672a0ab7034`  
		Last Modified: Tue, 12 Aug 2025 23:36:51 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae32105212dcc21ecc56cff26b0928a6efd520adf50643f27571e5a6cf77a8`  
		Last Modified: Tue, 12 Aug 2025 23:36:51 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f12cd8e5f7ef6c555b62b1e925006822e214d45f1923f7c1a95206b0dd624c`  
		Last Modified: Tue, 12 Aug 2025 23:37:02 GMT  
		Size: 68.9 MB (68880395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6261a2164dd4e8c412e54f29c1df262f5cd7bb3be23bf9b8e84559b10d4b6a8f`  
		Last Modified: Tue, 12 Aug 2025 23:46:09 GMT  
		Size: 137.4 MB (137432662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24` - unknown; unknown

```console
$ docker pull gradle@sha256:a31f52fa46a7550e148f9cf0715813e2fe16c6f1f2814b40e812a85b6fc32efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7588175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76d9d6b412b1da5414fd863fde4ad32a4abf9fdf8bc2fa6e5ff8a196aac4adc`

```dockerfile
```

-	Layers:
	-	`sha256:bf02e0d26465a161a4123f5849b62a472f07066872ee3bee70d367556892ef55`  
		Last Modified: Wed, 13 Aug 2025 02:21:00 GMT  
		Size: 7.6 MB (7556187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab379995a32739d6a627864bb3c775c988e16f6b02cf3d9e49cb73da4378c582`  
		Last Modified: Wed, 13 Aug 2025 02:21:00 GMT  
		Size: 32.0 KB (31988 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-24` - linux; riscv64

```console
$ docker pull gradle@sha256:e7ea9773adc4536c031a4bdcda29f4a91bebe5118b7304a9cd5ff6017183740e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.4 MB (501439565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f205452b2c3325c4bfed786240dda7cb60ace4c9ac660088bacb91f55fcb8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
ARG RELEASE
# Thu, 17 Jul 2025 03:50:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 17 Jul 2025 03:50:10 GMT
ADD file:07f3c32dd2b7f6af0f399701257442794654b72aa96759b98cb033a715461739 in / 
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Jul 2025 03:50:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["jshell"]
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:b12e9b07091787c99b29dd2be63680c86c47e8be60a46566329007fb82cee41d`  
		Last Modified: Tue, 12 Aug 2025 17:05:53 GMT  
		Size: 31.0 MB (30951577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad34db99b8b6d3689c6e8a55f34d183fc435ecd3c12cf99054a4e88b66485262`  
		Last Modified: Tue, 12 Aug 2025 18:16:38 GMT  
		Size: 20.1 MB (20142191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ed77a84631ddb22d11797ed16369a4012b54722b11977b17b1c5735ce60cf6`  
		Last Modified: Tue, 12 Aug 2025 19:58:57 GMT  
		Size: 153.6 MB (153602021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c685ab3f81c4315d1b9d1a6a0a258e682da0586cba6f45d6504d6600701410f`  
		Last Modified: Tue, 12 Aug 2025 17:49:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c1ee18ad5ca7c547af330fcdd24445fee1c86fdbf70d30ea5020e8fb367b2b`  
		Last Modified: Tue, 12 Aug 2025 17:50:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d06b3a8c52584ad1fa6f24bb28a2c4d8531f0c9ffeb6416d63c361e14f5613`  
		Last Modified: Tue, 12 Aug 2025 22:47:03 GMT  
		Size: 87.7 MB (87670675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af106571268f7fe95e2657acabb732e25f95097bc6aa5b190e7f3e17a443de5`  
		Last Modified: Tue, 12 Aug 2025 22:46:56 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7d75468d508925598958a26d4aea8b039a633e38f7b832f8db8a4883d42cd5`  
		Last Modified: Tue, 12 Aug 2025 22:46:55 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e418d355dd1c558045491b44807777f32dda4ee79cab95b4ee6f3c3122e5ea`  
		Last Modified: Tue, 12 Aug 2025 22:47:11 GMT  
		Size: 71.6 MB (71636411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219db2a5d35e38c7f4c520efd158b47608ddb344345b4e1d59d06f7f60ecc0a`  
		Last Modified: Tue, 12 Aug 2025 23:12:05 GMT  
		Size: 137.4 MB (137432650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24` - unknown; unknown

```console
$ docker pull gradle@sha256:3ba1250ef3fb5af40e7750aff0558f2864a43d4fd3ab62527ea989daf493272d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7640207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e747c4e32344141806b049466d174c487602e8f6584397185a936a5f26622f9`

```dockerfile
```

-	Layers:
	-	`sha256:4534bebd86c1e84add31254a87d06e062c55dd4cce62bab34b4feae715c8b597`  
		Last Modified: Wed, 13 Aug 2025 02:21:07 GMT  
		Size: 7.6 MB (7608218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25bf62a9d9bb3c5fd3faa02645f8f70fadc3bf3e8f866803f376ae7c502afd08`  
		Last Modified: Wed, 13 Aug 2025 02:21:08 GMT  
		Size: 32.0 KB (31989 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-24` - linux; s390x

```console
$ docker pull gradle@sha256:ed6d80a7a700adbc9bc237810b1c66829b62a4e344f47e4d291877d32ca91588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.1 MB (487102965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9783852d3380127300d4bb896494c1f007d8ebf63f6dc467da833958836916`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
ARG RELEASE
# Thu, 17 Jul 2025 03:50:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 17 Jul 2025 03:50:10 GMT
ADD file:f751959e6b8dae58a35017dc82c7271708f085c111710b59527373699b0784b5 in / 
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Jul 2025 03:50:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["jshell"]
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:1c5d0b18c745fadd2e177b54d4df793f25b01437577bc09c72ae52a0f3f9aeb3`  
		Last Modified: Wed, 30 Jul 2025 11:30:49 GMT  
		Size: 29.9 MB (29932680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca1d3019421a7aa66519824ce0e982b25db3c4e4004543099d050378dee3b89`  
		Last Modified: Tue, 12 Aug 2025 17:31:44 GMT  
		Size: 22.1 MB (22128620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dde20cb1cc0afeadd58455ba9b92aa1d948a128d674b17c9a766205c845fa85`  
		Last Modified: Tue, 12 Aug 2025 19:59:19 GMT  
		Size: 147.0 MB (147036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ad87a33b450be1a83bae10a1e154b38f8d28b2a410cd79573a7581552ed69`  
		Last Modified: Tue, 12 Aug 2025 17:34:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d993136b80279c45bf94985aada87e93498dd4d46b42e123b919c7ed1c4f63d0`  
		Last Modified: Tue, 12 Aug 2025 17:34:45 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6ef4b488cb86586662eb6e2aa75c665ad5027b2c7770f5f13354c4ff8094d1`  
		Last Modified: Tue, 12 Aug 2025 19:01:43 GMT  
		Size: 85.2 MB (85226596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829a538bd87cc0f405c1c68572228f19754879eabc87cd9d71f4d56e1b8705ee`  
		Last Modified: Tue, 12 Aug 2025 19:01:36 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69a830bdaf8d9cf78b63cb9e38d4bab9970c7b94010a14dcb95a9fe1b3e5d1d`  
		Last Modified: Tue, 12 Aug 2025 19:01:36 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c244fa49848a955b09b3a18e4374c043528f9b2e3b0a5129b3c95df5475b08a8`  
		Last Modified: Tue, 12 Aug 2025 19:01:43 GMT  
		Size: 65.3 MB (65341422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d636ad06daa816998266764861da05bea06e36e230cbe4b6407e674d3de4123`  
		Last Modified: Tue, 12 Aug 2025 19:07:00 GMT  
		Size: 137.4 MB (137432727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24` - unknown; unknown

```console
$ docker pull gradle@sha256:42462804b8bc80f10ddc72f10a13df686950b6d2913a83e90e25f4248359110f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8539e4f7dfe8a0045b778b6ebc68e60ccca3875403ff58d927d4a62ac94d61c4`

```dockerfile
```

-	Layers:
	-	`sha256:2c3123512cf9635c9f462ba335c8bfa34e25365be35237c18a3fcb9d1bc65251`  
		Last Modified: Tue, 12 Aug 2025 20:23:12 GMT  
		Size: 7.4 MB (7449097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043a78f1086f0b8ef20d864051e583622a499a90a9d06f113800d42f3f2d1cd8`  
		Last Modified: Tue, 12 Aug 2025 20:23:13 GMT  
		Size: 31.9 KB (31880 bytes)  
		MIME: application/vnd.in-toto+json
