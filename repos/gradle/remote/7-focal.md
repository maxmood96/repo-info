## `gradle:7-focal`

```console
$ docker pull gradle@sha256:8e7c0b2011adcf0c7393144116651aa8c98765a82b10b08723d9675e15e58b94
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

### `gradle:7-focal` - linux; amd64

```console
$ docker pull gradle@sha256:a642b27cdec6eae1bb4a696eaf6a29c5a52cf528a306a6b1c5a1faf6223fa35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.7 MB (382743872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0730fa609cb9c0c2ef350c3ae8eabcb3f7d33c08b087dae7ab8e8ff90b0e5d0b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER root
```

-	Layers:
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abf7de48bf61d8700ee29081c26013a23696726040c9e6751bb168bdd2535af`  
		Last Modified: Wed, 02 Oct 2024 02:22:43 GMT  
		Size: 20.7 MB (20690249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f8517ea61e4a010800898a4cca56f8fa94ec516d7effcdcead202e65b612fb`  
		Last Modified: Wed, 02 Oct 2024 02:22:51 GMT  
		Size: 145.2 MB (145178339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17807b561f1bd54e5005df1bc8f4c77520cefbf578cca727540bb2cc620c19ab`  
		Last Modified: Wed, 02 Oct 2024 02:22:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508551d943a48581219b583ae8d7df4ac6bb09624c896d899bd102815f84b8a2`  
		Last Modified: Wed, 02 Oct 2024 02:22:39 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac09f18d6b5e89a1d2774c3cb95a296b9b43fd4575c1afbb13e8e6bddf143284`  
		Last Modified: Wed, 02 Oct 2024 02:58:07 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee35447804af0801e882300ac4a92442c3d25adc2a39f21bc190eb9f8882e92d`  
		Last Modified: Wed, 02 Oct 2024 02:58:08 GMT  
		Size: 65.5 MB (65499344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a195d31f2a12c3998053d54fb4053f2a3983daecedd3aedcabacd98c11e7d8`  
		Last Modified: Wed, 02 Oct 2024 02:58:09 GMT  
		Size: 122.7 MB (122730527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad97497778dad3ec8e5669f2ce6dea5c4edeb6a5cf076a4173ec89c4a9586969`  
		Last Modified: Wed, 02 Oct 2024 02:58:07 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:2b34874b0e18380adcfad6715ffbe24578b6f489eb71034680d351d29a26b63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7735623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cee2766ed95c28612494b93e0042311465d58822e4d6a1846e1f7e8cdf9256`

```dockerfile
```

-	Layers:
	-	`sha256:ffc2b53102a8bc61ec00a420bfaf9468bebbb254df76986bbb0989149bc5c685`  
		Last Modified: Wed, 02 Oct 2024 02:58:07 GMT  
		Size: 7.7 MB (7712383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffdad53ef61b4dd5f89ac9f91de8f9554a05b953cd1586cd3cdc356537638010`  
		Last Modified: Wed, 02 Oct 2024 02:58:07 GMT  
		Size: 23.2 KB (23240 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:d790501f14427cbc6915f1e77d6f19763f59ad791250ecba9243194453b12ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370145201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d676bc4b43f42d90ee8a588bd2cf0d4d690abb58026e0af2aabe91aa47fb37`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER root
```

-	Layers:
	-	`sha256:8360546e6d28ec60104c18634d12f2178926b9e6c3aed4d2bff7b0c7062e0858`  
		Last Modified: Wed, 18 Sep 2024 22:25:20 GMT  
		Size: 24.6 MB (24600195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4223d6b90c591b7925ad88dc2b3c428b596ec4ebe1305322d85df6715044cee`  
		Last Modified: Wed, 02 Oct 2024 01:51:57 GMT  
		Size: 20.0 MB (19975503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15abea42832a6635e6e51dce771b70ec797855174b2a7627d8dd38f9656d1183`  
		Last Modified: Wed, 02 Oct 2024 01:52:06 GMT  
		Size: 142.6 MB (142645396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a5e2eb121764bba840e3bf748d14b922fdc1aa6fcfc5ad47db5fdbe77bc376`  
		Last Modified: Wed, 02 Oct 2024 01:51:54 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a99459dbb8ceec399da9ca702f60de44013d4efd58fce226b018386d31c6aab`  
		Last Modified: Wed, 02 Oct 2024 01:51:54 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143aea47879be8097440c72227f2635346e25d1dcd106cd4b3b0d2ecc215739f`  
		Last Modified: Wed, 02 Oct 2024 03:33:35 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da72c18180feb15aba82e8a855938bd306b68503e558bf5fac56e42e8edff57`  
		Last Modified: Wed, 02 Oct 2024 03:33:37 GMT  
		Size: 60.2 MB (60155666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79233fffdef68a4299489c48bd531528f651c5c4d2098e1e3ba4bb979153c65d`  
		Last Modified: Wed, 02 Oct 2024 03:36:52 GMT  
		Size: 122.7 MB (122730526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4269feb6b4f2e7dd0c935b74740a1633e1dcde7e26081182afd4e87e56caa8b`  
		Last Modified: Wed, 02 Oct 2024 03:36:49 GMT  
		Size: 31.3 KB (31299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:0eb4cbb9155386db0432f09841250b8556c2068bd58728fb270581bee5edcb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7656457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47039c3d796a7d51a13dffc6eeef6d5532e4bb4780746a8e2de95b296676f960`

```dockerfile
```

-	Layers:
	-	`sha256:a27fa71b9d3620f49383cec8877ee5dece4f7a0adbd2b35e7dfd5d266ccfb874`  
		Last Modified: Wed, 02 Oct 2024 03:36:49 GMT  
		Size: 7.6 MB (7633068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2b91ed50ac804630bbae542af5c33b10192bd49e1bedd2edee110800834cbce`  
		Last Modified: Wed, 02 Oct 2024 03:36:49 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d2d9046207d5f86e331132d544b57770e04ce718cf63e0cd716201887b6d1f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380655974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184044431affff225c6db81009614c53cf2ee09ed70f54e4d9ff513d20362c37`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER root
```

-	Layers:
	-	`sha256:ddfa9988351830f28e89a086658d4d3623317edf2488495fdf55c5ed9263c83b`  
		Last Modified: Wed, 18 Sep 2024 11:17:55 GMT  
		Size: 27.2 MB (27203992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a669dda813438b27e374b0bb2c42c17eb69814a1bacc35ff29437307a3d3c8`  
		Last Modified: Wed, 02 Oct 2024 01:27:08 GMT  
		Size: 21.4 MB (21391266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d627751e91f762ad81aedee04f3d2ec7496d05187b3abe977ea2b5e1ff9dc2`  
		Last Modified: Wed, 02 Oct 2024 01:27:14 GMT  
		Size: 144.0 MB (143967208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9d4bf46b846b9c6fe13cd67edbe4f624db13951354fed659a0bb9e1d00898c`  
		Last Modified: Wed, 02 Oct 2024 01:27:05 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935a82581405ad1c9399e69114fa9ccc468124b727debb69fd45abbf27347224`  
		Last Modified: Wed, 02 Oct 2024 01:27:05 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4b4d02a2762635d7712e0361e60891329e207705f78d68bf94442b32f96c19`  
		Last Modified: Wed, 02 Oct 2024 05:47:31 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d569345da193a47ca32d4c4fd296c3d3dc733ba302aa6a5662ef894791a833`  
		Last Modified: Wed, 02 Oct 2024 05:47:34 GMT  
		Size: 65.3 MB (65296831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3110b9de6e79632d974eec03a2ecd27afeb78404744f83325778d1acda9f939a`  
		Last Modified: Wed, 02 Oct 2024 05:53:00 GMT  
		Size: 122.7 MB (122730527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a3a13677ad72f973cf3e55cc98cb4d017ea69710d25694df8af202f38e31d0`  
		Last Modified: Wed, 02 Oct 2024 05:52:56 GMT  
		Size: 59.5 KB (59521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:b296298ee8dd9726de637e99cf665ce776bd08a28efb31c19af0c995fc1961e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7837642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8c56b02b05253b7f1cac3d75d123413fb436fa0dbd73ed375164c82e825c2a`

```dockerfile
```

-	Layers:
	-	`sha256:2a06dd6acd57a365eeec30eaae2667d449668ba243ec745da9a644d60ebeec6b`  
		Last Modified: Wed, 02 Oct 2024 05:52:56 GMT  
		Size: 7.8 MB (7814199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54339e5ce58abee4d30a591d40a1abd0e6b9fc2cafdf68eae56ad26ddc8b89c1`  
		Last Modified: Wed, 02 Oct 2024 05:52:56 GMT  
		Size: 23.4 KB (23443 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:405449f91933cc9b58c76d9422566927c31a582d093253ea59f1151a7c499aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.5 MB (397544798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b792c30348babff22a0ec3f6edd129acc04e13f32f9a8d3ea73b86bcc7582f00`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER root
```

-	Layers:
	-	`sha256:92ebc0bf195e4cfb272e0c863b69e6327a1601581a197046391e118d61fc5c6c`  
		Last Modified: Wed, 02 Oct 2024 01:54:32 GMT  
		Size: 33.3 MB (33315563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e0c0df869e3c2a63e2a16ad943955b86a099575e924ef7e1de288dc3b6e9c8`  
		Last Modified: Wed, 02 Oct 2024 02:08:06 GMT  
		Size: 22.7 MB (22730148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d730452a6dcce511a3c656eb8061d22c30b20afe44ad8cfd7169bc9873a02f`  
		Last Modified: Wed, 02 Oct 2024 02:08:13 GMT  
		Size: 144.9 MB (144865379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839e73329b9ba3e4beaf048bc943dd8c1aaf7c7952cb5e1af11c1fe873cd9102`  
		Last Modified: Wed, 02 Oct 2024 02:08:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e669691b13ebe935fb0c7c2827e617a4f716239f304f56f2b23b5b30e5805`  
		Last Modified: Wed, 02 Oct 2024 02:08:00 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ee63a4b8ceb87bf09d94ce2392f824cd7d48db2d395dbfa62f67af45b8294`  
		Last Modified: Wed, 02 Oct 2024 03:35:50 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c69675397130aaa345c093cbbd5ee42b334940bfc0d28e6f3a675a21b1c5fd3`  
		Last Modified: Wed, 02 Oct 2024 03:35:53 GMT  
		Size: 73.9 MB (73861543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc4e99a2507750475dbb78184e630afdc8a9d1485605f8404999f1d039511a2`  
		Last Modified: Wed, 02 Oct 2024 03:41:30 GMT  
		Size: 122.7 MB (122730532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fee66591e2bfe3d910283ac41049bec5cfac4797378f5466e9d7cc84280b1eb`  
		Last Modified: Wed, 02 Oct 2024 03:41:26 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:2a55a0152ad1b217ed3a03fec896d54145878fd6272172f46b34225a86b77a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1eca586fd6812812b170f343aae704f13bce8cca7ead988c0fda655bfe1183`

```dockerfile
```

-	Layers:
	-	`sha256:053d8d5c429456bae3d1d09ce0f0299a6ed9148525c6d74dfd888e3a6d23a89b`  
		Last Modified: Wed, 02 Oct 2024 03:41:26 GMT  
		Size: 7.7 MB (7743151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40092900ae8f1b4d44ded63922490bff949efe98064ae8a5976b750f6ee384d0`  
		Last Modified: Wed, 02 Oct 2024 03:41:26 GMT  
		Size: 23.3 KB (23314 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-focal` - linux; s390x

```console
$ docker pull gradle@sha256:56d3af80450709a7711e7d32c16dd3411be243698b29492d56d36103c1835ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.2 MB (369182416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ebdb00a920a13aedadd52cdc9d6c8f722213303862d2babfb440ba3176f71b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER root
```

-	Layers:
	-	`sha256:85fe938be9f572e53cd94b22adba9a4570ac5459c1a93a4c1f44f3a71d092586`  
		Last Modified: Wed, 02 Oct 2024 01:21:47 GMT  
		Size: 27.0 MB (27012320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b794c453affb50704c00b28f6d0aa427d6baebc5752c280b41605be8d2ffd1e2`  
		Last Modified: Wed, 02 Oct 2024 01:22:50 GMT  
		Size: 20.2 MB (20158550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315716cf0f787cfd4772e08d8f2742e6de7e1b3aefa7f193d2feb3996c63c0c`  
		Last Modified: Wed, 02 Oct 2024 01:22:58 GMT  
		Size: 134.4 MB (134408576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70650ac35af854105f166c7cb257372a3e29e4af9c323a4acfb304b8e7b69b8a`  
		Last Modified: Wed, 02 Oct 2024 01:22:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f6aab277d97ea3f77a85a2da596b9ca85db6b4e2f7fc51d2834afaa5611448`  
		Last Modified: Wed, 02 Oct 2024 01:22:47 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f255b4026ec77c7224a53507e4082181b2dd3964561f9b0b7685a6ff3ae691b`  
		Last Modified: Wed, 02 Oct 2024 02:58:41 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf722e87b3e4c2e7415d8757a5cc67f587ac653b2cb8d832a3bbb3ad311c937`  
		Last Modified: Wed, 02 Oct 2024 02:58:46 GMT  
		Size: 64.8 MB (64830806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28aa38fbb3b2fa89c4af01c0839e59daa08b79c535e40383133f20abc1f5c1`  
		Last Modified: Wed, 02 Oct 2024 03:02:32 GMT  
		Size: 122.7 MB (122730530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aff94e4c14800b1232d3ad1ffce84f6b8f22f1343cb5898a4557ab958f9c67`  
		Last Modified: Wed, 02 Oct 2024 03:02:30 GMT  
		Size: 35.0 KB (35006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:0ea9e6ebedcbc8b4bee46cba8b5b0959d73d7f2d1b76fac43b352683432eebc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7658389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa2b532238a8dcb95e42e3f05782279fb11087dfa5a8870668a8ba1c0ae8379`

```dockerfile
```

-	Layers:
	-	`sha256:89cde5989147f242824a5f73a6bdf9636afc24dc880e2451cc057b629466511d`  
		Last Modified: Wed, 02 Oct 2024 03:02:30 GMT  
		Size: 7.6 MB (7635150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c2ac241f9a57991dfb6184e8012d3240fb51d68a49bf1c4b20faf61b8ff2231`  
		Last Modified: Wed, 02 Oct 2024 03:02:29 GMT  
		Size: 23.2 KB (23239 bytes)  
		MIME: application/vnd.in-toto+json
