## `gradle:jammy`

```console
$ docker pull gradle@sha256:8b2b86662dbd50d001f6c4de895ba76c049131c8423d61137e1da464fcf11468
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

### `gradle:jammy` - linux; amd64

```console
$ docker pull gradle@sha256:51350d1d313e287a02c2c9fe63e0f7162e751c65b70c219fc690d997145eade5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394792576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa11ff5c018b459152097983acc71d14e3e910e28a9f0b70403242414a9e1100`
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
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Aug 2024 06:00:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 06:00:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["jshell"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["gradle"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Aug 2024 06:00:50 GMT
WORKDIR /home/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_VERSION=8.10
# Thu, 15 Aug 2024 06:00:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER gradle
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
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
	-	`sha256:96ffcce9774775bc227a945558bac85e1e0cebd3e7876fc113f308d41c6db979`  
		Last Modified: Fri, 23 Aug 2024 20:05:58 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd643102f51d1eabc61dc7e08acccc714a4a194acd1940022115b279ba675a8`  
		Last Modified: Fri, 23 Aug 2024 20:06:00 GMT  
		Size: 51.6 MB (51559502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f18330555cc1e7d3ea3ba52f355ff5ff174bfb0f5f1b1ba66782c030b729582`  
		Last Modified: Fri, 23 Aug 2024 20:06:02 GMT  
		Size: 136.7 MB (136728345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80326f55d193305767447a09df4b16f68c69d89f3be8be4951014fff488a0c6b`  
		Last Modified: Fri, 23 Aug 2024 20:05:58 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:fb6a5193fb042caa6b384a79f44b2a9a4705f0b801e0f87f3676ed61fa42904e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7282898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa2e1478ce2936d28cc36474127dfbbb7a0e32e9d751e413d60b93cab856fd7`

```dockerfile
```

-	Layers:
	-	`sha256:5d0bb73018a2df4c27dd4a985c1fda063fc6db1c1b8b8f8aa953522f28b27d4f`  
		Last Modified: Fri, 23 Aug 2024 20:05:59 GMT  
		Size: 7.3 MB (7255179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7471b72a75e840b066559a216d15458e92586821dc0eabb22e84302a88ba2a53`  
		Last Modified: Fri, 23 Aug 2024 20:05:58 GMT  
		Size: 27.7 KB (27719 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:09622cd3edbb458094c4a87a4932d7e848e3da09fb0edb14ea60007b73f168cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391923320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20e7ab33747af1c91b3f4316de25057c99a8df1786b35eee99c9bb7b5bdd0e0`
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
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Aug 2024 06:00:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 06:00:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["jshell"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["gradle"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Aug 2024 06:00:50 GMT
WORKDIR /home/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_VERSION=8.10
# Thu, 15 Aug 2024 06:00:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER gradle
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
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
	-	`sha256:682e899d62ac819c356c884d31afb0c425addf08d0343f6a571c7a9fc6fc48a1`  
		Last Modified: Fri, 23 Aug 2024 22:31:35 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4595057804b22e5d81ecf2da1e9661870e0e82ca5278f589c9c822ae9dad39b6`  
		Last Modified: Fri, 23 Aug 2024 22:31:37 GMT  
		Size: 51.1 MB (51146939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf9d2553e49c26c85934ade46012725d886fd2918d899df3bd0121cf9cb4b2`  
		Last Modified: Fri, 23 Aug 2024 22:31:39 GMT  
		Size: 136.7 MB (136728330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053fcfea23b989b4178f836b5e5859ea32f6a7f83d7915522eb7d39c571b7479`  
		Last Modified: Fri, 23 Aug 2024 22:31:35 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:993eb76a6b1b655ae535c9097f36ef7a17d6cf27d7cc647be3852d88bb848b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62907dc30880d86444141424d214bac29d54f25151695fa89936a6c9671fbd4`

```dockerfile
```

-	Layers:
	-	`sha256:f1dab049c3dcf7c799d90788586c03d0108f69076149db49ccf13b725fd08d83`  
		Last Modified: Fri, 23 Aug 2024 22:31:36 GMT  
		Size: 7.4 MB (7357784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a788ec204bd32fd993d4d511597d3394cf6e51368677fd8f195ab8554be84902`  
		Last Modified: Fri, 23 Aug 2024 22:31:35 GMT  
		Size: 28.3 KB (28276 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:e553fcd25f04599214675673f8f69a90bbbabf14711a263e6b3784fc816c430a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.5 MB (405498390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3d9d6a0d51e58175b51b7c5787e135c43885367670782702754ba950f18dab`
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
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Aug 2024 06:00:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 06:00:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["jshell"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["gradle"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Aug 2024 06:00:50 GMT
WORKDIR /home/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_VERSION=8.10
# Thu, 15 Aug 2024 06:00:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER gradle
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
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
	-	`sha256:4712b3a6b92ef53db2320fb9e7f1a14d228749a87199c1ff22d567208a281352`  
		Last Modified: Fri, 23 Aug 2024 20:24:58 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8025c3501d3241b1987daea63a5026499deb6194a67fc1a0e528fb1c273b9abf`  
		Last Modified: Fri, 23 Aug 2024 20:25:00 GMT  
		Size: 55.7 MB (55670914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a761ace32cda04e7591d945d84b998e89181719028ce1e120d63098fc63abf9`  
		Last Modified: Fri, 23 Aug 2024 20:25:02 GMT  
		Size: 136.7 MB (136728338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba08887c57dcf834e1edc6669bc8527cd8061c1099f19605adaece81f7acc9b2`  
		Last Modified: Fri, 23 Aug 2024 20:24:58 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:56debc7cd1fabb0d9dd89321e4ce09b8c869c3e52828b6709d50b55879c5127c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7316377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3275561f80b9e83d1a1562cd8e003375a79b0ba05fa55a4e60d8603a1f1c045`

```dockerfile
```

-	Layers:
	-	`sha256:fcf50b64d3acdfd0aa12b80953719530aa8a81d1d4e5b688ca3a9e3195aee439`  
		Last Modified: Fri, 23 Aug 2024 20:24:58 GMT  
		Size: 7.3 MB (7288498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b1210f5185d746a6406fdeb569236a02f658c6205a48cbcc9aefc5872f572bf`  
		Last Modified: Fri, 23 Aug 2024 20:24:57 GMT  
		Size: 27.9 KB (27879 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jammy` - linux; s390x

```console
$ docker pull gradle@sha256:7dd7082e5906018c0e02e644d2ff1d14a7d300dc5487355f35f97241375a16f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.9 MB (380947344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d676935834ed367762d4958008497ffd0c970b8379971be3da59a32da6ac976`
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
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Aug 2024 06:00:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 06:00:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["jshell"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["gradle"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Aug 2024 06:00:50 GMT
WORKDIR /home/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_VERSION=8.10
# Thu, 15 Aug 2024 06:00:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER gradle
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
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
	-	`sha256:41e575abf1a327fa4b2033556cfbe4734cd9a45f1826b5d61584511027dab541`  
		Last Modified: Fri, 23 Aug 2024 23:50:26 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3e1a2040e67434ddc0bb42378578a84a7ad78328ad1e8843d83547849fdabf`  
		Last Modified: Fri, 23 Aug 2024 23:50:27 GMT  
		Size: 51.3 MB (51277823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b9c80854b4aebbb4361fd6005f1dd87f5e4f436c7b3b2f46d0701c00505eda`  
		Last Modified: Fri, 23 Aug 2024 23:50:29 GMT  
		Size: 136.7 MB (136728338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fc2a441b098e450e17c2a191d2155c8862cb2af4f47023489a7ac7670200f7`  
		Last Modified: Fri, 23 Aug 2024 23:50:27 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:119cc52bd72cd377143e7a46153da4812f27e39cd7c461bbfed5beb986ac8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd7628c8f6f196e1a65b13cc4bb3c0886384323d10f15d17846fb75f72a1849`

```dockerfile
```

-	Layers:
	-	`sha256:794709cc61bd2e4f40e62f74a7aeabec342476e5ae954bb9fc4dd74fa7d2d541`  
		Last Modified: Fri, 23 Aug 2024 23:50:26 GMT  
		Size: 7.2 MB (7182691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:786e1b8242eb971115b9e57f07e570d5a434cd708b322e961f41578cc27d50d9`  
		Last Modified: Fri, 23 Aug 2024 23:50:26 GMT  
		Size: 27.7 KB (27717 bytes)  
		MIME: application/vnd.in-toto+json
