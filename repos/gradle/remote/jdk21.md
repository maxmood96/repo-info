## `gradle:jdk21`

```console
$ docker pull gradle@sha256:931361a340a7013c4efa13fe2fb4d76beea5aba416b45d097b27a5e04ddd6af9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:jdk21` - linux; amd64

```console
$ docker pull gradle@sha256:8200f74350058d609103bce6a21f36a9999c0d2a1f42cfb102129b5729e57e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394791923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb91e1fc1e9062c26f6a018e10c84d8d7b0e14727cc846769cdafd84fddf014`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d2822c71e1c49e3b52ca63c8ad15833449ee66e6c398a302eb046c556826e0`  
		Last Modified: Sat, 17 Aug 2024 01:12:37 GMT  
		Size: 17.4 MB (17415429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482fbf153ddc486288887c925609aba1a06123ef449197541916204000b32be3`  
		Last Modified: Sat, 17 Aug 2024 01:14:02 GMT  
		Size: 158.6 MB (158587052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880c2e95b386c797a96f9abf3551e5738cf995742285d5f45314d75676ed6d7a`  
		Last Modified: Sat, 17 Aug 2024 01:13:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345e90384d5ee5660e84765dd35dad15285b72490c36414bb649f3ffb9298c2d`  
		Last Modified: Fri, 23 Aug 2024 19:28:22 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bf6771a6f9c1e146795f3336c066448d1ba5b424267b5846aaeac5ed8e6b96`  
		Last Modified: Mon, 09 Sep 2024 21:01:15 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca615a0a97740a00c28540e161c3c2fae7609b557e04baffdeb2aeafded5812`  
		Last Modified: Mon, 09 Sep 2024 21:01:16 GMT  
		Size: 51.6 MB (51559370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7911e494b623f36c191359a157dc19e8009e8157c90559cc057fe375c4b1d17`  
		Last Modified: Mon, 09 Sep 2024 21:01:18 GMT  
		Size: 136.7 MB (136727833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978034044185dcc17dac8dd1e07ed3a773e2c86f0c17b03d4dafe96fc63ead92`  
		Last Modified: Mon, 09 Sep 2024 21:01:15 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21` - unknown; unknown

```console
$ docker pull gradle@sha256:4b265b7b3f07da28eb63205dbefb66b70a92253d85005515c776c90ddb094926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7283868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851e70c13848888feddc38ea2ad4ba93d58d237b2409414d649bf9af343e0cf0`

```dockerfile
```

-	Layers:
	-	`sha256:8a300c82a51ab90ed90c83a268cf9a93e0790aaf7ded862ad13e7264b725fc69`  
		Last Modified: Mon, 09 Sep 2024 21:01:15 GMT  
		Size: 7.3 MB (7256141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a44da1bf784028e1926a5fcfaf9a42fecb8c7834d3128aab9520c58d685fa9a5`  
		Last Modified: Mon, 09 Sep 2024 21:01:15 GMT  
		Size: 27.7 KB (27727 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6a394c23c05c5664ce260009906304b8f8b84a1c84419bc16fba2952229006e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391922984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914337bbb2c734bd93b73f474ff6a235016dee946c6a7b81a2e49476fff40b0f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a41cbd65bedaea8ec6506f879288194980af2b58962cdbb7a3f74472ba89d1`  
		Last Modified: Sat, 17 Aug 2024 01:35:29 GMT  
		Size: 18.8 MB (18828020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844625103df5730b175530991cf1aa8bfc1484eb61d967e68c9eb7c0fb721310`  
		Last Modified: Sat, 17 Aug 2024 01:36:44 GMT  
		Size: 156.8 MB (156756765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99d21c2f2420d3cb394597a37125582947b7c6843676a6725f3d8b0705b26f3`  
		Last Modified: Sat, 17 Aug 2024 01:36:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eac00a2b896d62546657fb40fd4036157467b8c822bd65df018f27e811786f`  
		Last Modified: Fri, 23 Aug 2024 19:45:51 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b7950d6d15ed9b16a849486d595767bc4ddc609e12fddae318506d24621760`  
		Last Modified: Mon, 09 Sep 2024 23:01:40 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc47569e9968f8f7a89e331ae2cd1495ec0f8ea3a1e73f44aaca7789c299601`  
		Last Modified: Mon, 09 Sep 2024 23:01:42 GMT  
		Size: 51.1 MB (51147094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d8b7544cd76d3dc18c739d756ea435cc8d429750334bc8266af5d406f6f4da`  
		Last Modified: Mon, 09 Sep 2024 23:01:45 GMT  
		Size: 136.7 MB (136727834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c84e8bd18973ddcc69aa55a2e620adf5b0fdceea1e9558d656eb77f5ea3632e`  
		Last Modified: Mon, 09 Sep 2024 23:01:40 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21` - unknown; unknown

```console
$ docker pull gradle@sha256:4ff2ef0f003556b578dbed9cfa48a82a84119aa16c0dbf714c4f986a57ed5c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9af011c40a89c4cc25dbd6c9815819cc9db04596bcfe91a62d9b6e66628e658`

```dockerfile
```

-	Layers:
	-	`sha256:873e9e23ebe2b52ab84ef8d8a95d0c9b96e38253a9757826d10f6cb4a0e2af44`  
		Last Modified: Mon, 09 Sep 2024 23:01:41 GMT  
		Size: 7.4 MB (7358746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568de1b3d866efea875ba9f52dd4e86d5dabd32c4ef9deddcd5aaa483dc4f785`  
		Last Modified: Mon, 09 Sep 2024 23:01:40 GMT  
		Size: 28.3 KB (28282 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21` - linux; ppc64le

```console
$ docker pull gradle@sha256:c6cd304e43a82b462752456d04acf14d68dfbcd890964823f1863855b25cf7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.5 MB (405497577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f93304863e8b40879a1df1120bea37bbf7a5660ab9d4b7d4a8a5592e041d1f5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0693fdc769b35059bf46757710f7d052660918503e58a5fb55e877e19ecee155`  
		Last Modified: Sat, 17 Aug 2024 01:01:59 GMT  
		Size: 18.7 MB (18677262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adff0505d99e478036daaae057082ae9b0e7ceda29cf98f82024f0e3e4a8648`  
		Last Modified: Sat, 17 Aug 2024 01:03:36 GMT  
		Size: 158.8 MB (158827315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d78001781864e09a0adfe84d01aa38bf46b539dda934a9c063e6bbabe3d8b92`  
		Last Modified: Sat, 17 Aug 2024 01:03:21 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b3f667528847c8b4bfe17a7e0a159d15aedd6d47a8576d9056b44828690e74`  
		Last Modified: Fri, 23 Aug 2024 19:25:08 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abbd6b872be8a0a8538d4c1696bbdd5c2ee8cc16557930e22e4e5adb21ddb04`  
		Last Modified: Tue, 10 Sep 2024 00:47:24 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d711a713f86e8a1ce43716dfc55e48bb439aafbb5ea5aecd85d9f4e973e4aadb`  
		Last Modified: Tue, 10 Sep 2024 00:47:29 GMT  
		Size: 55.7 MB (55670603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a1be12860a559d421e037793de727d3a1c6f6590b976019167ca136f5f7039`  
		Last Modified: Tue, 10 Sep 2024 00:47:28 GMT  
		Size: 136.7 MB (136727836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9211ef2a8984469327a0770f8ef1863dc71ca9e8d80f7528b0b578b0c25d96`  
		Last Modified: Tue, 10 Sep 2024 00:47:24 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21` - unknown; unknown

```console
$ docker pull gradle@sha256:16cd24854aedfecdd73d57e7ca34d18139f4d5f19f45dc78eab8d38b79b05631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7317349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e9750f585542fea3d9ea2195d70bdbe89717420e8a3f7d79303e4e5a151ede`

```dockerfile
```

-	Layers:
	-	`sha256:de49f668a8773f228d084a013f229ba30de897e2d4b0b61d6e3095c857563ed1`  
		Last Modified: Tue, 10 Sep 2024 00:47:24 GMT  
		Size: 7.3 MB (7289460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336977fadf876b9ea4c4c9cfa10b29e7dc914cf3c3662a55a7d60cbafe3b3329`  
		Last Modified: Tue, 10 Sep 2024 00:47:24 GMT  
		Size: 27.9 KB (27889 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21` - linux; s390x

```console
$ docker pull gradle@sha256:a19a577074c76a2eabacd0611c9a4e9c0e756c1f13832a9da5fbb18bdffa6563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.9 MB (380947016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28deea63013cccc48f40f063096c717c706300e71a68942798618ccb6bb6a3aa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a4353a8eb4f285ecb7c45d930598defa46de85e4d28e5771f4f8c7a0fa8740`  
		Last Modified: Sat, 17 Aug 2024 01:33:24 GMT  
		Size: 17.2 MB (17229109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057af079d08ee2fbff2ca8ad164d528eacbe94ee1f9a85ae79d0f5f1ab9cfb92`  
		Last Modified: Sat, 17 Aug 2024 01:34:33 GMT  
		Size: 147.1 MB (147066657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a982e2a160e64ee722914fee986660174435053bb391352415abccf2604afca0`  
		Last Modified: Sat, 17 Aug 2024 01:34:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a3df4884b80fe04847a9024a37eb44ac6c0f5067c193779d628df22b264442`  
		Last Modified: Fri, 23 Aug 2024 19:48:16 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a5d304cf22c9f88c8303298c27641e4c699ecb4d1d73e6f91a92d5bd3f3593`  
		Last Modified: Mon, 09 Sep 2024 23:51:55 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b8b23145c8a7aa6cbc506baebb875c8678f9c80f895e9362d269e8985883e0`  
		Last Modified: Mon, 09 Sep 2024 23:51:57 GMT  
		Size: 51.3 MB (51277999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda8024b1f953615b9658ca539ffbb25c2019da9aabadddfe002b3f856bb5513`  
		Last Modified: Mon, 09 Sep 2024 23:51:58 GMT  
		Size: 136.7 MB (136727833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99f894056190cfa67fe7f06254befc1ca92a99805305f759224d5e82ff71dce`  
		Last Modified: Mon, 09 Sep 2024 23:51:55 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21` - unknown; unknown

```console
$ docker pull gradle@sha256:3cbfa132ef087f6449c36b954269a4ef98da9c56fbd68090502b0f1d7dcc4668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db77af918fcadc8ccc4cc8b2aaf293a49e8c7e5de58785df5fe040924c783f1`

```dockerfile
```

-	Layers:
	-	`sha256:68d4649bcf79e45781bc4b16a94d530d0bb0208bab9b2bcbe2f4fa014d75fd4d`  
		Last Modified: Mon, 09 Sep 2024 23:51:55 GMT  
		Size: 7.2 MB (7183653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c957c56b7e1614e7633da3a31d644db2e41a5c5e38d7e1aeaa1da32feec32417`  
		Last Modified: Mon, 09 Sep 2024 23:51:55 GMT  
		Size: 27.7 KB (27725 bytes)  
		MIME: application/vnd.in-toto+json
