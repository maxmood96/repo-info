## `gradle:jdk20-graal`

```console
$ docker pull gradle@sha256:950f61be5d883e497d84ff3a190bc5573dbd7effa4a2add269492a0ffdf3d078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk20-graal` - linux; amd64

```console
$ docker pull gradle@sha256:14da6942c7394ef842e92884108fdc9a32173ae2edca646be42f24b9cab5b085
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.8 MB (589811385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65b24c78f5640986ffb8c954c39924aaecf5ad7a52fabf3c291c54faecb356d`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:31:46 GMT
CMD ["gradle"]
# Wed, 16 Aug 2023 15:31:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Aug 2023 09:49:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 17 Aug 2023 09:49:06 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Aug 2023 09:49:06 GMT
WORKDIR /home/gradle
# Thu, 17 Aug 2023 09:49:56 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 17 Aug 2023 09:49:58 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 17 Aug 2023 20:22:33 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && JDK_VERSION=20.0.2     && GRAALVM_DOWNLOAD_SHA256=941a85a690e7b1c4e1fcfac321561ca46033bba3ac4882dd15d4f45edd06726c     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JDK_VERSION}/graalvm-community-jdk-${JDK_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version
# Thu, 17 Aug 2023 20:22:35 GMT
ENV GRADLE_VERSION=8.3
# Thu, 17 Aug 2023 20:22:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=591855b517fc635b9e04de1d05d5e76ada3f89f5fc76f87978d1b245b4f69225
# Thu, 17 Aug 2023 20:22:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=591855b517fc635b9e04de1d05d5e76ada3f89f5fc76f87978d1b245b4f69225
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 17 Aug 2023 20:22:40 GMT
USER gradle
# Thu, 17 Aug 2023 20:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=591855b517fc635b9e04de1d05d5e76ada3f89f5fc76f87978d1b245b4f69225
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 17 Aug 2023 20:22:41 GMT
USER root
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e126c7a1c77e06e289d340c79a4ec7b044d5a6ffc29d2e90c51257cd43354ac9`  
		Last Modified: Thu, 17 Aug 2023 09:59:09 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd01e4e2d13010238b28f52c2f9c386b8aa502256e441f22948b0b825a060a4`  
		Last Modified: Thu, 17 Aug 2023 09:59:27 GMT  
		Size: 126.4 MB (126413532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030cd193cd3a59589bfd8546513696b81b21568824a2c19bc06f4bd1451b5f8d`  
		Last Modified: Thu, 17 Aug 2023 20:32:24 GMT  
		Size: 302.3 MB (302288035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70117545e52bcf144119ed58f36d94ff364e36edcd410ce7207c3e1bc1e0d21`  
		Last Modified: Thu, 17 Aug 2023 20:32:07 GMT  
		Size: 130.7 MB (130667327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60247d6ff073db8e8d991030cf69825521af6c6c658c8a3a1f1b56057be769e`  
		Last Modified: Thu, 17 Aug 2023 20:31:58 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
