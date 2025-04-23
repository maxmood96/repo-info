## `gradle:8-focal`

```console
$ docker pull gradle@sha256:e7f4932023d1561f8a6fdb9235fa86f74f7053c0979397dba6a8fe39c011ff0b
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

### `gradle:8-focal` - linux; amd64

```console
$ docker pull gradle@sha256:8e1a8e5fbe3699d5a4d27092595fe4ef8414c535d39afbcd874ec28fd6bd1225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398544451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ca91fef00972fd79c5a49b5a5698e64dbd2899b56ab93b5e6fa59f6d180b0e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Apr 2025 14:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 14:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["jshell"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["gradle"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Apr 2025 14:24:24 GMT
WORKDIR /home/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_VERSION=8.13
# Tue, 15 Apr 2025 14:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER gradle
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER root
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389b4ac3a5360565e942e50cc2ca64d7525b15370f755f1f830acc1938be61f8`  
		Last Modified: Wed, 23 Apr 2025 16:32:23 GMT  
		Size: 24.0 MB (24015270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cdde6261a9469fe321fbd58410cd970c4b45c36d6e8b1808293a43f7cb9fea`  
		Last Modified: Wed, 23 Apr 2025 16:32:27 GMT  
		Size: 144.6 MB (144646780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551fb6f86e245af42940ff128ea35832b07d731efe29f7868b8429115a380c84`  
		Last Modified: Wed, 23 Apr 2025 16:32:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16364506555ac0fdbd82302f7d2e3a8fe50bbef2a03331cbb923951e7d20fc31`  
		Last Modified: Wed, 23 Apr 2025 16:32:22 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fc47258989b62707a6e50d6fb0773f375b130bb3323b3364b5ee890382ef14`  
		Last Modified: Wed, 23 Apr 2025 17:10:30 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5426f7af25616c806a7aebf9849daeef809742e9420e84d3142358b19ae722a8`  
		Last Modified: Wed, 23 Apr 2025 17:10:32 GMT  
		Size: 65.3 MB (65322067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ffe17710389706ab47d71c5f6034307aebca2df6260fc49c708fd061dbbea6`  
		Last Modified: Wed, 23 Apr 2025 17:10:33 GMT  
		Size: 137.0 MB (136988257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b5ba773d15e635fcf7582900e5f411eee508ec6df15891a9823a7dec5576cf`  
		Last Modified: Wed, 23 Apr 2025 17:10:30 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:489ca83617951cae7be283b56a992d8a2dcbe400cbbc8e34bba4a6101824858f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7997162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6422467c3bcda78c4f4fd359ef3e35a84e5264ace8413d8ee7c6c2e1a37a933c`

```dockerfile
```

-	Layers:
	-	`sha256:48171a4b12a963a16cd2380d56bbc0762005854b4941597e5a80f2eec64729cc`  
		Last Modified: Wed, 23 Apr 2025 17:10:30 GMT  
		Size: 8.0 MB (7972987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e140ed214d214ad23b736f63105fb798c233ba1a81e4d3014df5aeccb463b85`  
		Last Modified: Wed, 23 Apr 2025 17:10:30 GMT  
		Size: 24.2 KB (24175 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:6fc0391caeae8d6230428d0c36738a982a29e6e9064d37d6b862458998017190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385548517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52c3c4f3a1c5e2882eea5ddf38530ea25b228a36c58b898f6f89ef4aba013a2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 08 Apr 2025 10:45:56 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:45:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:45:59 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 08 Apr 2025 10:45:59 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Apr 2025 14:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 14:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["jshell"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["gradle"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Apr 2025 14:24:24 GMT
WORKDIR /home/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_VERSION=8.13
# Tue, 15 Apr 2025 14:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER gradle
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER root
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a6513401af4b15656bd4d266c3ca963110d6e02b0d96d42eab62794d3497ca`  
		Last Modified: Wed, 09 Apr 2025 11:47:45 GMT  
		Size: 22.8 MB (22782976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b499066d1df990e5f59d5df0c81ff0a81828b052be09a5a9dc7890f4d5e490`  
		Last Modified: Wed, 23 Apr 2025 17:07:15 GMT  
		Size: 142.1 MB (142121880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89495599f119cf2e8bd357be9ed6a300d61eb0d4f4a40cb6ab26ea857725b46`  
		Last Modified: Wed, 23 Apr 2025 17:07:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5867effff03acb989a5c72b68575fdc1aa26a4a535092828bdcfaecd60dbbe64`  
		Last Modified: Wed, 23 Apr 2025 17:07:11 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a56f6faa6e12e740c30fa9621e7ace4c4234529b3c53cd0b99d104b7db2de`  
		Last Modified: Wed, 23 Apr 2025 17:13:34 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5117ddafc86049a5bda649e95829c4a5f12f31c184a4e74c8181d7b581ed351`  
		Last Modified: Wed, 23 Apr 2025 17:13:36 GMT  
		Size: 60.0 MB (59993341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11344c578d734224f3e429a258481ab78d1ccd6888f967621a95de76319669bf`  
		Last Modified: Wed, 23 Apr 2025 17:13:39 GMT  
		Size: 137.0 MB (136988182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9106bb448e83854c25e8c1ba36fd75281bb33782762e41c3b811189c841e5c`  
		Last Modified: Wed, 23 Apr 2025 17:13:34 GMT  
		Size: 31.3 KB (31302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:b719acac0b842e749bb383c288f94d548e6e8d8f27339406fad2ea7a0bc6bf6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7918161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4d6c63e5271dadffab56a38c06cfe5232036bfb4583a80c28b5a862b9d065e`

```dockerfile
```

-	Layers:
	-	`sha256:d2f55aa9bf1ef53baaeeb9574cdb2740a2b1f4e6cae4238548df22a5ee78f4ba`  
		Last Modified: Wed, 23 Apr 2025 17:13:35 GMT  
		Size: 7.9 MB (7893807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a8bb161d1527e4504c61bc6464e2b49b6ed2c08485e33201e126e50d8c028b`  
		Last Modified: Wed, 23 Apr 2025 17:13:34 GMT  
		Size: 24.4 KB (24354 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e499bdc319f4b60be4c7136cf53c25cad9a19046deac0fc08f696395cced8181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.3 MB (396319155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bb5406c9737cb00fe10fd737ea9d063719b05f930d04bfc8271bc1e162179e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Apr 2025 14:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 14:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["jshell"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["gradle"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Apr 2025 14:24:24 GMT
WORKDIR /home/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_VERSION=8.13
# Tue, 15 Apr 2025 14:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER gradle
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER root
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf97b101bef517d80b9cbee79290d924905491d9a342c620bbd9e01b2e16e84`  
		Last Modified: Wed, 09 Apr 2025 07:03:48 GMT  
		Size: 24.7 MB (24698158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33243fe5eaf0c61005b367f81eabc7b92fc91426ed395dff8e39c419841caabd`  
		Last Modified: Wed, 23 Apr 2025 16:35:40 GMT  
		Size: 143.5 MB (143512884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8090fa16c03f79ddff1dae49cfe564cd783fdec9aade829ba9db6f7c7df141c3`  
		Last Modified: Wed, 23 Apr 2025 16:35:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee8b258b8e08234182e68b0380cadedbe1cfa51e7776d2b928bdcf9f7a93943`  
		Last Modified: Wed, 23 Apr 2025 16:35:35 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdfa8bfbf957e3a2e798245fcb53a2677f8948d3302d430efaee02768198a32`  
		Last Modified: Wed, 23 Apr 2025 17:32:15 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a048627a98c563bc97d4a588a65d8f972504d04cc636fe23abd3e8667e7323`  
		Last Modified: Wed, 23 Apr 2025 17:32:19 GMT  
		Size: 65.1 MB (65075867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6427f05ddd673efac19ec2083393ee1416c76480e6ad42024c169895831c92bb`  
		Last Modified: Wed, 23 Apr 2025 17:32:19 GMT  
		Size: 137.0 MB (136988263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aca8991b185c22d75c29c064705ef1e3f66b479e3c9db9171478bfd01249371`  
		Last Modified: Wed, 23 Apr 2025 17:32:16 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:f0f3ba4c93eb34857dd61ae05125e4d89bbcb32c8d5b7837b51d1516baaa6c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8099134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305f8f1691e6bbdac4a13288ff7393b8a2ff09e5c1acb385b501c6418616d011`

```dockerfile
```

-	Layers:
	-	`sha256:19b9148692806c7fb5ffcbc294ab4fccb57f1f2984e2f2de55b7f6351b1bfd44`  
		Last Modified: Wed, 23 Apr 2025 17:32:16 GMT  
		Size: 8.1 MB (8074715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad3347c475b04ae0c21950d4c2652ccf2901e321506c4af2edf96eb4031bdfa0`  
		Last Modified: Wed, 23 Apr 2025 17:32:15 GMT  
		Size: 24.4 KB (24419 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:eb603ea0f4eee654f88a1223d1220e7ea510f258f368c6533b99018360cfe204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.0 MB (413958570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e2caccc0976e7137506e06ed48b71f75509f3cb8670190645a503a607dece9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 08 Apr 2025 10:47:01 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:47:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:47:04 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Tue, 08 Apr 2025 10:47:05 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Apr 2025 14:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 14:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["jshell"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["gradle"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Apr 2025 14:24:24 GMT
WORKDIR /home/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_VERSION=8.13
# Tue, 15 Apr 2025 14:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER gradle
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER root
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14383eb7ffd2da9b89ac5f0997387d480eeaa50e4e50dfc17f99337849d5ce37`  
		Last Modified: Wed, 09 Apr 2025 04:45:10 GMT  
		Size: 26.9 MB (26906685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e0838eb6fb26f6e623e1c0bb5b13be9aa8c24e1ba219e38dd7e45ffb2f6fd9`  
		Last Modified: Wed, 23 Apr 2025 16:41:16 GMT  
		Size: 144.3 MB (144289683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbdb119e9c2055449bb402949f11ba021979c27058e9c75c759ec599085e4b1`  
		Last Modified: Wed, 23 Apr 2025 16:41:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273f048d8a058e68006c4e67658b1d2aff9dcd421f970313dcb09082bb11d430`  
		Last Modified: Wed, 23 Apr 2025 16:41:12 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40eb6db30e67adcdb8ff1934a888fc78824e4b11a4f0b2289817a5312167c578`  
		Last Modified: Wed, 23 Apr 2025 17:23:44 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe728402295b5a21e65664310024ff8454dd11490b7b61a80c0dd4b1aca2936`  
		Last Modified: Wed, 23 Apr 2025 17:23:53 GMT  
		Size: 73.7 MB (73655278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7394c1237305bf95a3936bb39cf62afe54104c22bd23b03ac6fd5725f34b45b0`  
		Last Modified: Wed, 23 Apr 2025 17:23:49 GMT  
		Size: 137.0 MB (136988179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f691d7b3d32f4c9258ad1f7451142a9e139b67baeaff433dd0da0b9f0072e44b`  
		Last Modified: Wed, 23 Apr 2025 17:23:44 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:ac9eef20562b294acf8c25a4a80ca81fecaeb3727e8b02a755cb5097d8282437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8028036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742a89aca2bf741ced759a122d4ed4a1ef9bf3cef884ef1f6ac6e2d0c14d1ef3`

```dockerfile
```

-	Layers:
	-	`sha256:118e20c1f2869d6d8f806acbced40fb43a5f6debc2b14fc27d90f421adf21e11`  
		Last Modified: Wed, 23 Apr 2025 17:23:44 GMT  
		Size: 8.0 MB (8003764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d476a303ddbf0577ff74fb5cca3b5c69b189b0e404de1e045639a02b1e20b77`  
		Last Modified: Wed, 23 Apr 2025 17:23:44 GMT  
		Size: 24.3 KB (24272 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-focal` - linux; s390x

```console
$ docker pull gradle@sha256:a4eb13aab891743d2236ee6d73da574b1e7994cef0e10750717213a071c9be15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386116578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c147c2322232980d41b6216898977b15b241776abe1c3e35d978fbf8c6e5ef`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 08 Apr 2025 10:45:20 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:45:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:45:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:45:20 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:45:21 GMT
ADD file:82f0132f510f24adc12d74491187647b94a14baa7a57fd22a67a5c3767541496 in / 
# Tue, 08 Apr 2025 10:45:21 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Apr 2025 14:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 14:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["jshell"]
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["gradle"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Apr 2025 14:24:24 GMT
WORKDIR /home/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_VERSION=8.13
# Tue, 15 Apr 2025 14:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER gradle
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER root
```

-	Layers:
	-	`sha256:b35596e17e863edd4c594d026a60e36f73cc6a076370f55a24732114fd25ff68`  
		Last Modified: Tue, 08 Apr 2025 11:48:56 GMT  
		Size: 26.4 MB (26368190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec497bba37750e6512ca4044fad1dda0580a50b230f4119d854d2686cc785864`  
		Last Modified: Wed, 09 Apr 2025 04:20:01 GMT  
		Size: 23.4 MB (23405337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5e5a2f7b68d12d7341d7474d688a4c4b95d12a2a479d321a2a6f241f6cdef4`  
		Last Modified: Wed, 23 Apr 2025 16:37:15 GMT  
		Size: 134.7 MB (134682163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd00f6359aba774a58e70008e8179795c9d3c6896b4c657a0ef70f6590607e1a`  
		Last Modified: Wed, 23 Apr 2025 16:37:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c8feb892a73e93f1806a8b40751bf2e594807637ce3b34b50cb59bc38d5481`  
		Last Modified: Wed, 23 Apr 2025 16:37:13 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9379ae1f3a1e27e482ba2ef55867b6f9e47debf02f8f6c38a5e42da5728e440`  
		Last Modified: Wed, 23 Apr 2025 17:17:24 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fa8785a38ccc9edb41d9e06bc0f8a6ac1cd222ffa09785f9ac47c97da85c95`  
		Last Modified: Wed, 23 Apr 2025 17:17:26 GMT  
		Size: 64.6 MB (64630916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0481e2d11fb9f7a84ee580938297888d8cc45b7037ba0293790f5ee607bf9689`  
		Last Modified: Wed, 23 Apr 2025 17:17:27 GMT  
		Size: 137.0 MB (136988178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca637c42899cea7ec71956159ac02ae97609b95b2d0b4b62237aaef055b9db0d`  
		Last Modified: Wed, 23 Apr 2025 17:17:24 GMT  
		Size: 35.0 KB (35002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:b612a8896f6a1a962897bdbb9330734a372d35b3e9060ade6dc6c3e5bc06dc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178203119a363dd37db422e7dd25842561b0f5f1593f2dfd6fdcd096ec6e783c`

```dockerfile
```

-	Layers:
	-	`sha256:634b6fe8f6eb62699ebe70e9708d6330fd9f36a56731360cc21f30116f4ef10c`  
		Last Modified: Wed, 23 Apr 2025 17:17:24 GMT  
		Size: 7.9 MB (7895843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a8caff9f3cd4dce40e89ba5b9a65836ddecfd6791d1fdbff43eeff1e5f8663b`  
		Last Modified: Wed, 23 Apr 2025 17:17:24 GMT  
		Size: 24.2 KB (24175 bytes)  
		MIME: application/vnd.in-toto+json
