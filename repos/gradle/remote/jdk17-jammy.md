## `gradle:jdk17-jammy`

```console
$ docker pull gradle@sha256:321d0d38e48356f6ebd197f006acd7630e26e069385b4c15e5b4a292028e471a
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

### `gradle:jdk17-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:b18541522f778423b91d1d8a14a9bc25d47cb49bb169f47e2e254605404a9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.0 MB (382980501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d9048d21037f5ce66aa9735446165b3f9b569e8f835c76b73c29a2eb3ae284`
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
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_VERSION=8.14.1
# Tue, 27 May 2025 02:26:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER gradle
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER root
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12374d151daa9c3bb73958acbbec3fd73660471d62d5baa757b0aad242ed301`  
		Last Modified: Mon, 05 May 2025 16:35:11 GMT  
		Size: 20.7 MB (20693924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df9f99dd57e52fc7f17b5a87b20a40913b94681e6ad0a05ab6b06e6f3323e48`  
		Last Modified: Mon, 05 May 2025 16:35:14 GMT  
		Size: 144.6 MB (144646728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e714bcd1365a261036c2ae10a62cdc0011efb8586eb6b59b19e6b3d065bba3`  
		Last Modified: Mon, 05 May 2025 16:35:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141779bd67f4ce6dfe1c84578df8cfa3a860859d4ed985965e00660f8404b05f`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4efd7a9b867ada6df8b68f83df5c9812bdccff61131161b1780ec0d7717c5fc`  
		Last Modified: Tue, 27 May 2025 18:59:18 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3e4512d9459aa9d5e5d91395b05de95136d20ae998f03d0a59e970161e50bb`  
		Last Modified: Tue, 27 May 2025 18:59:20 GMT  
		Size: 50.6 MB (50649974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ddca30f5a8f4325705d2df263d9ddd607ec1fe04910226a6472fedd1fc5a63`  
		Last Modified: Tue, 27 May 2025 18:59:22 GMT  
		Size: 137.4 MB (137395577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5da3a8585ddf830967cea81a7413424725648e4993a7ef5c194b80109d54da5`  
		Last Modified: Tue, 27 May 2025 18:59:18 GMT  
		Size: 54.9 KB (54889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:304c6601f85f46d777e7934d07f039cfd7ee8c2569a9810d8feeb6b1e5dd4c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7655929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d4c1d7db1ef497189adeb75aabccfde070d9183fef7934f870b848019716c0`

```dockerfile
```

-	Layers:
	-	`sha256:d415263c628136601723a8b31d5b339fb0cce6b81b502f06a9dfc4de1948322d`  
		Last Modified: Tue, 27 May 2025 18:59:18 GMT  
		Size: 7.6 MB (7634357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0570d9296c2012a3f46647a570d1705146756075660501ae0a984e5e04c563e4`  
		Last Modified: Tue, 27 May 2025 18:59:18 GMT  
		Size: 21.6 KB (21572 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:e0334bbba482d468619aa9be2ddd4409a5c2750b19950314d8f17beb8ccc027d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 MB (380346455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95fa0dd6f10ec8d11d00cd536b6baff3d75a0caf63e09d0e73740ec8ae744eb`
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
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:0644b965bac173b3de427d73c19d20e4fb61d50785a17a303e350f86b7865f26 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_VERSION=8.14.1
# Tue, 27 May 2025 02:26:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER gradle
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER root
```

-	Layers:
	-	`sha256:bbd8385a156b4afe216eb6b84f86bc7178bca4ab42ae42bb98f3576ca9f4e17a`  
		Last Modified: Mon, 28 Apr 2025 10:43:57 GMT  
		Size: 26.6 MB (26640827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cf0ffcd11b616a815412db1d2bff041f71811d4f309c91b8970835a52450be`  
		Last Modified: Mon, 05 May 2025 16:42:44 GMT  
		Size: 21.0 MB (20988777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8694365b4cc1e125c5b98cb3efb56cfe7e7dd40ea73d72c2d56427b84264c382`  
		Last Modified: Mon, 05 May 2025 16:42:47 GMT  
		Size: 142.1 MB (142121687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e94ec0b7b08ddb69c790b66656dfd1642dc9a05e671666b301cc1579fc55ac`  
		Last Modified: Mon, 05 May 2025 16:42:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a356e52b736e1b4571a2c700fececb5dbba80f5458ab4bd0eaf3f2f31e0f9292`  
		Last Modified: Mon, 05 May 2025 16:42:43 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c8d947912878e281a9f6611a6633b829e3e41844aed4ad41d9d376bc9760bb`  
		Last Modified: Mon, 05 May 2025 17:06:12 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9733634f38cc50cf3a1bbc895c379b7534ee33c511122dd3106703347f5b9a`  
		Last Modified: Mon, 05 May 2025 17:06:14 GMT  
		Size: 53.2 MB (53161507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c62e3c9298e5db3d4c6985345ce8500b4e4ddae663dfd95addfec7987d8cde`  
		Last Modified: Tue, 27 May 2025 19:22:19 GMT  
		Size: 137.4 MB (137395584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f878136869cf5819cd51352133d2ee970591570bd5126d9392cbb0d7985d8a`  
		Last Modified: Tue, 27 May 2025 19:22:15 GMT  
		Size: 31.3 KB (31301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:0bb707317946190e74c935f26eeb9ec991432f5c8f3de91081deeaee4d9d2853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7574336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b2299ebea67a09bdca844217b969e1ea415e1f3bed53f985838cb2ee0aff00`

```dockerfile
```

-	Layers:
	-	`sha256:77e926c30532a7cb9e7f52cf71840d55db24bc285c197e83fda40b01d1ee5506`  
		Last Modified: Tue, 27 May 2025 19:22:15 GMT  
		Size: 7.6 MB (7552648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17a95c5940529bf7a8affa3433bcfc089e0ad436b9dfa423d99b362f6e27626f`  
		Last Modified: Tue, 27 May 2025 19:22:14 GMT  
		Size: 21.7 KB (21688 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:244de23ddb884fa181a3d01aeaa4a7c7771254ef0d9064a33dcc360ac34c97cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.6 MB (380613353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef764efbc39d2694b825653abef7e8f6435cffca6704f8a4597a2d9e0f026c4`
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
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_VERSION=8.14.1
# Tue, 27 May 2025 02:26:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER gradle
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER root
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7922ecca004f885e4d578cd030e98e8313d9c54961757f32071268d070e6f39c`  
		Last Modified: Mon, 05 May 2025 16:54:21 GMT  
		Size: 22.1 MB (22069611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c709a8f69116a7889d82bdf4b46aae16fa22741435b93e9e6919a09257cea0`  
		Last Modified: Mon, 05 May 2025 16:54:24 GMT  
		Size: 143.5 MB (143512216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d572ba8adc859c7599957daffc4c83a5b6339558fc58e2533f11ba6615fcca`  
		Last Modified: Mon, 05 May 2025 16:54:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb73ed5aaf1b40ec2eb13b6b251ed11f634d20d980b951c605cb4872a1a17f`  
		Last Modified: Mon, 05 May 2025 16:54:20 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb8efa48727f602865e92a50295bfe4a682e0ba6ad39bf9e425d28c8e5895c4`  
		Last Modified: Tue, 27 May 2025 19:41:51 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d580f5126edabd9b88fcfb3868a5f8c7ab4d2d9f851ed0609fe09921819394c`  
		Last Modified: Tue, 27 May 2025 19:41:53 GMT  
		Size: 50.2 MB (50215472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659f0eda78597ca101df94db24adfa24ce2a5184f134e6918f5bc6ea4942afcc`  
		Last Modified: Tue, 27 May 2025 19:41:55 GMT  
		Size: 137.4 MB (137395532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf701b0aee9472d3db9a937e730cd5448645c9f25fcad1186f876a4a8803e814`  
		Last Modified: Tue, 27 May 2025 19:41:51 GMT  
		Size: 59.5 KB (59519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:9411789b4cb5dd488ebae47d6ce8be39fbf1b6d323674f04b8176ed8fd5c24ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7757705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682f11054dfdae4070b6ac7f5518b10bc0dfd8473dd7cbad1c1121ff959d75d6`

```dockerfile
```

-	Layers:
	-	`sha256:6367d50fcba0edbec61a157717e2772e5cb5f6309c1f5fe6a9ea6079b4c4c3b1`  
		Last Modified: Tue, 27 May 2025 19:41:52 GMT  
		Size: 7.7 MB (7735983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f9759c5d188f49bfef3d12af8c26a3cb1debd2be02011ae8a6d373863ea52c`  
		Last Modified: Tue, 27 May 2025 19:41:51 GMT  
		Size: 21.7 KB (21722 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:6e833e5d467860ca756c5ed7b237a2390ffb52203d7173eca297f40e5f8efc8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.3 MB (393337371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd7a1824446e1a84652ba009b912bf4902d9bb980a8b5a21a979ba7613885c1`
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
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_VERSION=8.14.1
# Tue, 27 May 2025 02:26:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER gradle
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER root
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030e17dabeaee2abe18705baffa778812190fd888e2d93ddca61e34824fe7137`  
		Last Modified: Mon, 05 May 2025 16:44:12 GMT  
		Size: 22.6 MB (22580873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdfa440ad4a9f7489ea9803672249774cd6c65d163773f9a931c2679d2398c2`  
		Last Modified: Mon, 05 May 2025 16:44:15 GMT  
		Size: 144.3 MB (144288964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f11387beb843fed02e4b41a2fc1dc7ef780b47038b3c895bca9ef717d6a8783`  
		Last Modified: Mon, 05 May 2025 16:44:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d5f9b15cf12066413f41532230f3e367cf4cbc1debc59c0345e3e27ee8d524`  
		Last Modified: Mon, 05 May 2025 16:44:11 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570a25392de57c4f94680d3d25014532a1df80a814af8edb6a6b5b01edacc219`  
		Last Modified: Tue, 27 May 2025 19:22:53 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5e683ade69831726d7e736be166fad084e1f07892397c6825ab753cee0dd69`  
		Last Modified: Tue, 27 May 2025 19:22:56 GMT  
		Size: 54.6 MB (54586943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7712336dfecd877085532addfad7140674dda909299f99f99f893c84de1f9b75`  
		Last Modified: Tue, 27 May 2025 19:23:00 GMT  
		Size: 137.4 MB (137395579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95174c9017cf94f79b347f3bb5af8e3838924ec26222544e4b84122a29be111a`  
		Last Modified: Tue, 27 May 2025 19:22:53 GMT  
		Size: 35.0 KB (35005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:b1e9f87a50e9dd3fb4b3ab02f52eaa7bdd20b11359444903ece2fcc144b4f32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a42a9fca572ba516edb802457d34945fe8c97be7bf0545541f5793803f79228`

```dockerfile
```

-	Layers:
	-	`sha256:698b4a76572ad385f17cb04aa517dbf6bcbcde714ed84837f34e2b1d787cc5d9`  
		Last Modified: Tue, 27 May 2025 19:22:54 GMT  
		Size: 7.7 MB (7665202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ba4334ff56e33c973bb7ff4cea35968ec1f3f1487f158853697039a1ba6f26`  
		Last Modified: Tue, 27 May 2025 19:22:53 GMT  
		Size: 21.6 KB (21623 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:7e03735d418b630bd1cf05df12416401e94e15f22ab395d42ea30c26df1a2661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370899377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e350e0f4d2771dacd1e38e629f4f03e41199b8b897f364fb7dd2ef11c05d57ab`
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
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_VERSION=8.14.1
# Tue, 27 May 2025 02:26:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER gradle
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER root
```

-	Layers:
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Mon, 28 Apr 2025 10:44:16 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322614b4e3696874979d165b487ee74084fd2dfec90e79d60237e5045bed39f2`  
		Last Modified: Mon, 05 May 2025 16:39:00 GMT  
		Size: 20.4 MB (20412723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcad03b2e2e34c3f6ba73ba9c1897a5d55794630cdf108b1921cad4c676ba93`  
		Last Modified: Mon, 05 May 2025 16:39:02 GMT  
		Size: 134.7 MB (134680768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4e1cb4391478c552284bd7d22e7be38d0bd1c0d5de73e9ebc45cacb8d675c2`  
		Last Modified: Mon, 05 May 2025 16:38:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045c8b2ff1b59f1336af5cdf651695a739364996c06bf79672615d06b926ff0d`  
		Last Modified: Mon, 05 May 2025 16:38:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19e8538df3239b0daa980f447ed64e490907cb3abfed25d0eecdb1e4af75b83`  
		Last Modified: Tue, 27 May 2025 19:17:34 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2931f15ea0a826e5515e694da589751ea94be710c839c75313d346b2cf664244`  
		Last Modified: Tue, 27 May 2025 19:17:35 GMT  
		Size: 50.4 MB (50368526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc2d5dfb68dad18669f7d8b840bbef2d1f3a24435dd23cbdf787b1fa4047fda`  
		Last Modified: Tue, 27 May 2025 19:17:37 GMT  
		Size: 137.4 MB (137395578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bccbcb04a530803e388e49b70385791c9a0e4e46859a21620432a6160d3bf95`  
		Last Modified: Tue, 27 May 2025 19:17:34 GMT  
		Size: 35.0 KB (35005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:afca80fb1495e17661f780f7ee82edc2fff86939bffe9625b8f6b0ed377d4bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7579611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be39b57dfc980be9c327db4005e05a8ae757f16dcb6a1b37837ffe4539334737`

```dockerfile
```

-	Layers:
	-	`sha256:5f45cec601509563917c72a4bc6f2bb51ffd4555d0f412a5e5568259a7df384c`  
		Last Modified: Tue, 27 May 2025 19:17:34 GMT  
		Size: 7.6 MB (7558038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd9a8b8af23a472b6d4cc81450c74933b2a85c91a196062080e30d6f20808c6`  
		Last Modified: Tue, 27 May 2025 19:17:34 GMT  
		Size: 21.6 KB (21573 bytes)  
		MIME: application/vnd.in-toto+json
