## `gradle:jdk-lts-and-current-noble`

```console
$ docker pull gradle@sha256:c4e889186832cdcfd6248f21859b7642fe6cea6ffc9c0842538ccc476d1bfb7e
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
$ docker pull gradle@sha256:60d44600ebdd8055155557f256b8cbed568fe2392d9eef22cec00b110fe18e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340879789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03962ffdb2d1eff961cfdb38b34368102d6c5d688f381ad05e07bc349621114`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ARG RELEASE
# Thu, 25 Sep 2025 19:59:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 25 Sep 2025 19:59:06 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3fc35759502b620f010a9cd2b3da8454f8a49a156ceaebb00de1fd8335682d40';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
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
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751f17092206e57f1a1a273a304c3391c6b5e525e3b827f8f98aa95c6617ee0d`  
		Last Modified: Thu, 09 Oct 2025 21:14:36 GMT  
		Size: 17.5 MB (17458339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5f352694d8627292c2cf79e310b418dcabbc90dc635644e82f51bd9a986132`  
		Last Modified: Thu, 09 Oct 2025 21:14:38 GMT  
		Size: 92.2 MB (92168040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd412807b1d854d10ba7ed722cb2db269bdae28795b00a69549388cab7b9ea2`  
		Last Modified: Thu, 09 Oct 2025 21:14:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70191202cb65bbe9b6f23779152b9f3bc0911dd79c6ec4d40a6b09696f309f8`  
		Last Modified: Thu, 09 Oct 2025 22:16:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fcf289b04986f529a67c5c277b8e817c9c0a155fa66f67189b0cac56d89097`  
		Last Modified: Thu, 09 Oct 2025 22:16:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065f6a88d7035bb590f66c292ca0cabdff078668563d1ac5077cb15095e18a2e`  
		Last Modified: Thu, 09 Oct 2025 22:16:06 GMT  
		Size: 67.0 MB (66953654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916ee811447fb8062cf1ce2e33950e7231b551998399a67dd5da521aa8b38def`  
		Last Modified: Fri, 10 Oct 2025 06:06:16 GMT  
		Size: 134.6 MB (134572699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:7f43d95681ba33085f002c6cd61c570c0de250d4fd78d96feb4680caa5bab7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7265844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770456558f63072ccc2acc20a8fff1cac5d29df7165fe49278a50f9aebb5bca6`

```dockerfile
```

-	Layers:
	-	`sha256:f89da33b52d246732686a666c97b9366aed4397bc330964876676b8ee1a71c85`  
		Last Modified: Fri, 10 Oct 2025 05:22:48 GMT  
		Size: 7.2 MB (7236432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f9c6d5886b8ad9e7becfb81ed950e4b4dd7c63c4e0a0405265b0e7dfd2a774f`  
		Last Modified: Fri, 10 Oct 2025 05:22:48 GMT  
		Size: 29.4 KB (29412 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:97fbaf14f3367098c2c6fe4e2df015bb5e1cf32b470d71063486169d4f07cc21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339700957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb29fb4cc0831b2e481cf3301506f4adb509056487543af6d50b3f30a7c98737`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ARG RELEASE
# Thu, 25 Sep 2025 19:59:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 25 Sep 2025 19:59:06 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3fc35759502b620f010a9cd2b3da8454f8a49a156ceaebb00de1fd8335682d40';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
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
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f534f212b81280f9bb38024333dd966c72c7b4f9e4e38e47ce52ac0db5a8630`  
		Last Modified: Thu, 09 Oct 2025 21:16:05 GMT  
		Size: 18.7 MB (18652075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a019a5e915bc01822b117e3ff7b8cb7467c0c157494660a51b69c9ecea351a3`  
		Last Modified: Thu, 09 Oct 2025 21:16:16 GMT  
		Size: 91.2 MB (91175671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052dc0d5069685926780974e4c16a48da1ad8e760614f991e98d260844156d`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19963690b37236306d9546b3f31620a25da31c665df1d91163f9c4cf5ab45a0c`  
		Last Modified: Thu, 09 Oct 2025 22:15:29 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca05aa9cc274e0ce3df0f866f1ac00d75df9dbeb891387e60c22dc7d00e0a4b`  
		Last Modified: Thu, 09 Oct 2025 22:15:29 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbf64c360a289052330aa9105fcdd2a1f3b44072722845d600d14f4130e22b4`  
		Last Modified: Thu, 09 Oct 2025 22:15:34 GMT  
		Size: 66.4 MB (66429972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9e395458c03ef6a4790128c082767fa359d8b9283d905206b5eebcd0bcd8a0`  
		Last Modified: Fri, 10 Oct 2025 16:03:44 GMT  
		Size: 134.6 MB (134577618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:ab65e3dd4f22718d3b962ebe1428bd9da51ffd81b3c90ebfe43e5c931a4a27fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9ee504b82bb427fe53537bafc70a62f348d9446fcbdf8d0a2e426b06993b4a`

```dockerfile
```

-	Layers:
	-	`sha256:52fd6af7b86cdd53a70cf37d993ee0cb602672979833c12f54e9e9b67b8c401d`  
		Last Modified: Fri, 10 Oct 2025 05:22:53 GMT  
		Size: 7.4 MB (7374246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:364f2e264aaf94d5acf3e27ad7c485e9d4ec35917c80e79cf98294cffbfd435a`  
		Last Modified: Fri, 10 Oct 2025 05:22:54 GMT  
		Size: 29.7 KB (29705 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-noble` - linux; ppc64le

```console
$ docker pull gradle@sha256:50170139d988c3e33e77cfe9976c670937d2455ce2b9076e3437a7f3b83a1f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350836599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5362ebb8d56489f96ec0e1f02b41027a3bd5f1e1b4895f767502f764a0eff8fc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ARG RELEASE
# Thu, 25 Sep 2025 19:59:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 25 Sep 2025 19:59:06 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3fc35759502b620f010a9cd2b3da8454f8a49a156ceaebb00de1fd8335682d40';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
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
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3abef86328361e6a8fca4e97e2725838182e487a709b1cd23bd0d865c03378c`  
		Last Modified: Thu, 09 Oct 2025 21:20:21 GMT  
		Size: 17.3 MB (17340059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa97d42bf6d5c3b33aceb7ed3328b51ee36d1b9c1e84af0c37cc4e26510a06c6`  
		Last Modified: Thu, 09 Oct 2025 21:20:35 GMT  
		Size: 91.7 MB (91734228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1d4febf2b7aa769213c87b6ec5db4c41302b34879891f6660fe2e9a11f5cb`  
		Last Modified: Thu, 09 Oct 2025 21:20:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a128fc2cdba8326bf2ae9ca30a89946509495e917518393af147f6f7f54e6713`  
		Last Modified: Thu, 09 Oct 2025 23:18:00 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d3dd5351560766033fc8159f182a3e48f361cb21eac66e94b48ac3c13da1c`  
		Last Modified: Thu, 09 Oct 2025 23:18:00 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e639732c92b26e4038467475daeec60e9a1badc7e0e4ed4bf0a79aeaaa6fa2`  
		Last Modified: Fri, 10 Oct 2025 03:14:11 GMT  
		Size: 72.9 MB (72902610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254ec8e64e8ff3b275a667204d5371d9372012a207d574471b847edab4ee82e8`  
		Last Modified: Fri, 10 Oct 2025 03:14:10 GMT  
		Size: 134.6 MB (134552266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:0f7e0c15b283e2a29c7dc70769dbbfec6eed993a959ac3839113221ac6a95b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1ebd89536eb95d77cff7e24682a45511b724c0d9dcb2d5e6de3276e2a05445`

```dockerfile
```

-	Layers:
	-	`sha256:e2a169319e987761cc88d4f22543974b8ded4eb25c83b5a0106a86a967f62f9b`  
		Last Modified: Fri, 10 Oct 2025 05:22:59 GMT  
		Size: 7.3 MB (7288901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551866baae584fa2dd89507455609df2bea123135771993457a37be9b01e62c3`  
		Last Modified: Fri, 10 Oct 2025 05:22:59 GMT  
		Size: 29.5 KB (29534 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-noble` - linux; riscv64

```console
$ docker pull gradle@sha256:7d0440c18c3b5c55d0c793e4ef96dc70ac1bd811a83542de3e529e75c0538a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347436192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c37d31720f1476c5807133c2c09d33bd7d72b0f37c36693552a58b48aa86948`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ARG RELEASE
# Thu, 25 Sep 2025 19:59:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 25 Sep 2025 19:59:06 GMT
ADD file:13e2355f84c9f5f1ba6aa2fa1db4359cbe23312f7b2905fc8b976899a09fdfef in / 
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3fc35759502b620f010a9cd2b3da8454f8a49a156ceaebb00de1fd8335682d40';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
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
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:2d699e6bd7ed3cc40f40b8118f763dc4303b0e97b911de163cabf78f19b5d434`  
		Last Modified: Thu, 02 Oct 2025 23:21:18 GMT  
		Size: 31.0 MB (30950446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681226ecf08b5ed0c7a2ddb14b0aa1fa5dd9f08ee2ddf669cc5331ece21ce750`  
		Last Modified: Fri, 03 Oct 2025 19:54:08 GMT  
		Size: 16.0 MB (15954979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cca09b62c92482cb6874f3bf24b3ee869acb89243f8e34c1e3d93064fb6662e`  
		Last Modified: Sat, 04 Oct 2025 01:08:28 GMT  
		Size: 90.9 MB (90881850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f03e987e085b9325bfc3fbe514c2b59872211194c96856a70cd7ade9ff7c816`  
		Last Modified: Fri, 03 Oct 2025 19:54:04 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a11b58fb5e2268bf132d022583dec550a80dbc0b4ddc5d1f07d953d9b30e3af`  
		Last Modified: Sat, 04 Oct 2025 12:12:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54414438ee601e80414551276a5d62f59c01448478927a4830597f1e4022a57e`  
		Last Modified: Sat, 04 Oct 2025 12:12:20 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81cc9cfdc59ad34396c5895a79078ce43249a6869b2d90c9ae3bd95e5e08c2c`  
		Last Modified: Sat, 04 Oct 2025 14:55:26 GMT  
		Size: 75.1 MB (75092745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd9d887d62f1c4891126961ba1dfc52d9308ba868fc0137c26b6630db0ab37d`  
		Last Modified: Sat, 04 Oct 2025 14:52:16 GMT  
		Size: 134.6 MB (134552266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:d36b438d7fcb52a24acf5dc9b7f9bbdee8526b05f91163ecba2db0f23c904f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b102d6f852823b23b842e5b73fd447d12744b88616747ab6b8b81f261ee0f92`

```dockerfile
```

-	Layers:
	-	`sha256:79e068914aab91ffe4287f4512f1d59e79a195229e7547f27878b1dfe6c14a86`  
		Last Modified: Sat, 04 Oct 2025 14:22:21 GMT  
		Size: 7.3 MB (7340265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae92302bf276d25d56dce74547696a1c0316c946a5c525fd789304cf937b850`  
		Last Modified: Sat, 04 Oct 2025 14:22:21 GMT  
		Size: 29.5 KB (29535 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-noble` - linux; s390x

```console
$ docker pull gradle@sha256:f9e837e41a040a22813dabcb2d992ac8e3dee4e284072fb5cbdd250962428581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337945459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2af42fa7c3b970ab4a5af0bbacfa23b5d288b48545dd3520da80d14ab5cb0f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ARG RELEASE
# Thu, 25 Sep 2025 19:59:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 25 Sep 2025 19:59:06 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3fc35759502b620f010a9cd2b3da8454f8a49a156ceaebb00de1fd8335682d40';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
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
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfb92427b1b5b51197cd7f8a5b124de5df6948dd998a572f52acd673fcc9131`  
		Last Modified: Thu, 09 Oct 2025 21:16:07 GMT  
		Size: 16.3 MB (16311292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9c4a12d1592add81a3c43f464e0711613c57566642565a827c5bde1a7f0474`  
		Last Modified: Thu, 09 Oct 2025 21:16:17 GMT  
		Size: 88.3 MB (88331497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9df82c128d0dde3b805f57be5c887e7a79c70d44bd403eb3fdfd0eec20d35a`  
		Last Modified: Thu, 09 Oct 2025 21:16:04 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5511d81d9bdbb1a16c2221fe28ba7333e4fa8db6201707f1ebad9a468b4b3405`  
		Last Modified: Thu, 09 Oct 2025 22:29:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ada3272d34556da059d9980de76afbf7747a8a76b5a78fbf0a89082fd8fdbad`  
		Last Modified: Thu, 09 Oct 2025 22:29:01 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144efd121096953d395e1b201e8dd4d601b1cbe7e7021ce796e36d394e534128`  
		Last Modified: Thu, 09 Oct 2025 22:29:07 GMT  
		Size: 68.8 MB (68840394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2c440d9bedc6a549dc002400de518ae6df889d5b8173fa77af96ecbede9db4`  
		Last Modified: Thu, 09 Oct 2025 22:34:35 GMT  
		Size: 134.6 MB (134552218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:24f3a382a4ff6b9e4eee37fcc17e9de531aa95286925c5d51fd0a8ddecd6cc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7213694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cb5cdad0c7b1bb907df0cc71eeeee114e8b7c83ef3ffd9a003be9253717b13`

```dockerfile
```

-	Layers:
	-	`sha256:8b8f5698169049678c4a6d20a01d5e47fa82c21781068fe0bfa6ece5096275e3`  
		Last Modified: Thu, 09 Oct 2025 23:24:52 GMT  
		Size: 7.2 MB (7184282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3cf41aa32409dd04ec9e368893c20111e3fa75ea992a1acbd24e3d7922ff1d0`  
		Last Modified: Thu, 09 Oct 2025 23:24:53 GMT  
		Size: 29.4 KB (29412 bytes)  
		MIME: application/vnd.in-toto+json
