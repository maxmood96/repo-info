## `gradle:7-jdk8`

```console
$ docker pull gradle@sha256:16faf5d950e71bbb56b1eeacb3e6d31b9669b9b99965a3a3be048dffa765bacf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:7-jdk8` - linux; amd64

```console
$ docker pull gradle@sha256:495e00c432dcd69b9bb94b4f4b8b44c08a625ae399e5eac35f82e29137df0ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279754890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef86a61f4225e1bff4b082421e9670868715c09e8208ccb3b2b890db42dc913`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08483b5f2cfe43842a06f46c6081326e0c2dc3b3243317fd12e60f348d678964`  
		Last Modified: Tue, 12 Aug 2025 17:24:18 GMT  
		Size: 16.2 MB (16150643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3dcc561c9cd39b92ec4fc57a6058ff42002ecf195e80d8ad5748e80389c1ec`  
		Last Modified: Tue, 12 Aug 2025 17:24:18 GMT  
		Size: 54.7 MB (54739766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582c1bed63e3dd80b9aabcadc64e63ef4bcde37bb178fa1bc799c832e74f204a`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6337a833f3117c3db42fc6b211b32a6b6874d435444ee9455d2e28d83e3326d1`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff651311d8629b62b233eaed65a9be274d0dc6cfa20ad75b2e27f6aa55166f8`  
		Last Modified: Tue, 12 Aug 2025 17:53:10 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46f298dc2555d812802f9224dda3056f07e9f4d6e287f333213a3888730e689`  
		Last Modified: Tue, 12 Aug 2025 17:53:28 GMT  
		Size: 50.8 MB (50796401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94235c58cf38aa9fce711ba458b1d13da23bda63265dfb96f24ce70082d8f5bd`  
		Last Modified: Tue, 12 Aug 2025 20:37:50 GMT  
		Size: 128.5 MB (128469414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a553dc4fff43efeb8c3aaf76a9c093207afe78614f95a56ed076ed697591ae`  
		Last Modified: Tue, 12 Aug 2025 17:53:12 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8` - unknown; unknown

```console
$ docker pull gradle@sha256:767f6c5c32abeb33db8ca74a2de22735c00a7e5d802cfa87535b684cc48a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7757909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27eaf17edbaf17734efbce911c12a8d6e4014288caf1ca2c4d9fd687203d9cb3`

```dockerfile
```

-	Layers:
	-	`sha256:a98fdacb7862e88a2ded387435159c0b3113d1f805e225f02fdfa32109e8e2f1`  
		Last Modified: Tue, 12 Aug 2025 20:20:10 GMT  
		Size: 7.7 MB (7734084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:828f7504d1c4d92e4f982d4ced9e2c51667079a8655cf2fca3c08e0718eaa7a4`  
		Last Modified: Tue, 12 Aug 2025 20:20:10 GMT  
		Size: 23.8 KB (23825 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8` - linux; arm variant v7

```console
$ docker pull gradle@sha256:b65f6c0f533d7d0c5c8e68b4f7063b095665af7a978c386fb020ab778a2288f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274436445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b43d5fb038192a52c51db350effea503816b8b47dcbd060992ed83868b8d49`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:56dd1608fa49343c3815b8373825d581303e97b21994ce0e1d099bf09251caea in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:6530e67fdf3958f32e486561f05a1170b5fbcd419c51eb435b13993ecadad7b3`  
		Last Modified: Tue, 12 Aug 2025 17:02:44 GMT  
		Size: 26.6 MB (26642919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da254942fc2ae7b2cdf3f227af1c842bdebbd1573712272ea2efe9e8d35cdaa`  
		Last Modified: Tue, 12 Aug 2025 17:25:53 GMT  
		Size: 15.9 MB (15889812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a6be2aebf0453513058e04e2e021e6b799d01485c519c5b5ad36e363988739`  
		Last Modified: Tue, 12 Aug 2025 17:25:59 GMT  
		Size: 50.1 MB (50130721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c528ef2f62fbc4bff3549a5f540325a914be06447a617e6af79eb229989572a4`  
		Last Modified: Tue, 12 Aug 2025 17:25:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27262e97c185fe0eb8dd7b3e8c4a4e35e95d78b77a1bd3ea7f90a760cb33def0`  
		Last Modified: Tue, 12 Aug 2025 17:25:52 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f2c44e8de729447b9527a8f89748cc13e415523b54b2a71a489f46b21cf154`  
		Last Modified: Tue, 12 Aug 2025 19:10:58 GMT  
		Size: 4.3 KB (4293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4dd718c0da516e580b319e24ffa2225fd9bdd62013fc639ead5a6ac777bd8`  
		Last Modified: Tue, 12 Aug 2025 20:21:34 GMT  
		Size: 53.3 MB (53265523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c887e3a1694e19f4e2aa37488ef41bd653851ee139525e8731b067886efd67b`  
		Last Modified: Tue, 12 Aug 2025 18:19:30 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c3a57b1c7a55a2b61ef655460a5da781fa4a3d0335d7c94ba04e9298871d73`  
		Last Modified: Tue, 12 Aug 2025 18:19:43 GMT  
		Size: 31.3 KB (31291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8` - unknown; unknown

```console
$ docker pull gradle@sha256:2cac0b8d0ef74d5fb70c5a4a32203f7fb8bc3839c64796e7de232aa5c5d29e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296cb9794e8e2fb43c9dff9daff879370a4d6a4c40a6ca6c95beaf9381276cdc`

```dockerfile
```

-	Layers:
	-	`sha256:42cc93529a6148653c81b1a13b7d90c69efec4de140701ef1b423a709c2b7a03`  
		Last Modified: Tue, 12 Aug 2025 20:20:18 GMT  
		Size: 7.7 MB (7737124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3861b0b7eaeccd14f3e6da78e9192037c165ad7e5725b2dec91201e6f478df17`  
		Last Modified: Tue, 12 Aug 2025 20:20:19 GMT  
		Size: 24.0 KB (23956 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:496174cbb215bb9e3ebb52ecc98493bfb456c919ba471128de0917dcc378142e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276134087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e335f6ca9db596cb5c4e16f37516f9880011b6e1464003ff2a5ce754009797c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e940b12283a67ff1c771864e58b58f224257969d16e19a179b3f8289c4d4dfcb`  
		Last Modified: Tue, 12 Aug 2025 18:31:10 GMT  
		Size: 53.8 MB (53839507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30fdff5a53ba3d2e43df30b5277041df566c24f5be4476b4e386dad68d69e`  
		Last Modified: Tue, 12 Aug 2025 18:31:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0ff686944578d38ac0413872ba73e79256657b51fdd048ef40b36aa1225695`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca61b221d4bdee56f44d43a21efbbdd13f7b8113ec030f1791d6cabe9d28f68c`  
		Last Modified: Tue, 12 Aug 2025 22:48:35 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba572d53c0f1415847ac6f35f72ef2ffa20ba09489c7a85a35844f03f33894c8`  
		Last Modified: Tue, 12 Aug 2025 22:48:47 GMT  
		Size: 50.3 MB (50335886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d77f51f7581cd966a2c85bcc39256af3b74afbaafcd4e8cd18a6cd5c5d54776`  
		Last Modified: Wed, 13 Aug 2025 02:30:28 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7e5df4435a171305ace317d8e8816b7c2d9960c60a153d0016e86516b9ba05`  
		Last Modified: Tue, 12 Aug 2025 22:51:58 GMT  
		Size: 59.5 KB (59509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8` - unknown; unknown

```console
$ docker pull gradle@sha256:9fc62cc78da5ab0f9126e16f4fea1a3bde4f4df8c78ad13a3bd6b251c786a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed07d8f557e11fd33928fc0692d60b35ba4447c91b08f69ba3668af2f05e485`

```dockerfile
```

-	Layers:
	-	`sha256:8fc74f7256f02aa7b7c0a38c8b14d21858fc29116feadd5ec663076de9b177fd`  
		Last Modified: Tue, 12 Aug 2025 23:19:02 GMT  
		Size: 7.7 MB (7740627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24545c5e10a8ec347448926b742c5ec1a767b0d44317fb3f178658530d7def1e`  
		Last Modified: Tue, 12 Aug 2025 23:19:03 GMT  
		Size: 24.0 KB (23998 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8` - linux; ppc64le

```console
$ docker pull gradle@sha256:5118af5281dd0fd3cec21846285c8f9789ab661ffd81b8bf56b81b421890265d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287498728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c844fec9c28f9539ebe657b2529273c4b93127040efdb3231119f3c4975f074`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c50520b2833414582dcec4e87265a64dd9e5acd7b3ec03378e25ec51523b3`  
		Last Modified: Tue, 12 Aug 2025 17:29:14 GMT  
		Size: 17.6 MB (17624214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3563e462f65953d910e2846e6de3725502677044b4826058e62802811ea8a0ad`  
		Last Modified: Tue, 12 Aug 2025 17:29:23 GMT  
		Size: 52.2 MB (52167149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b266375691d61b72291e1f0d9e5169842674c1de091aecfdb3193e356c28d2ad`  
		Last Modified: Tue, 12 Aug 2025 17:29:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00321eef6c5bf0386430936d8260d05c426c784f7873c0c85189e55e3fa08055`  
		Last Modified: Tue, 12 Aug 2025 17:29:13 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a620d3ad5dab5aea71edc410e1caf4f42c1ed16c4064842952cbf05d8d261be`  
		Last Modified: Tue, 12 Aug 2025 23:44:31 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc98c161a95c6c2ffb085a9c1dfa9341bfb0ede07796c40edd14129cbf4401b5`  
		Last Modified: Tue, 12 Aug 2025 23:44:40 GMT  
		Size: 54.8 MB (54753007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348d027e17a4f1b73f9637195e64b2f5171c4b8ce2debb797dc6efb5583d437f`  
		Last Modified: Tue, 12 Aug 2025 23:50:03 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc822736c7c07e0b3a5490c2e6a3e7752f69b833d4960eda959ddfd769a1769`  
		Last Modified: Tue, 12 Aug 2025 23:50:32 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8` - unknown; unknown

```console
$ docker pull gradle@sha256:20652992ab5b8122a42f227c8f117d395fa81e79e9b68254aeea4645caf6385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0a47ecaf0c3fb68d4b0e8e58814cf057c9e8c6da24e67d8eb59efb1e2ec3ac`

```dockerfile
```

-	Layers:
	-	`sha256:ba68c7c22cb63a5386d948250c4bb1829d6dfc9ed01af0e9199fa396d5235b1f`  
		Last Modified: Wed, 13 Aug 2025 02:19:22 GMT  
		Size: 7.7 MB (7740149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044588dbccf9a2f762bb62e9f20feec228085f57bf7e57187fd66ce631f44e19`  
		Last Modified: Wed, 13 Aug 2025 02:19:23 GMT  
		Size: 23.9 KB (23886 bytes)  
		MIME: application/vnd.in-toto+json
