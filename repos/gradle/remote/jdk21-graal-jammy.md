## `gradle:jdk21-graal-jammy`

```console
$ docker pull gradle@sha256:1a1d5c111eebaeefa73edfe586e636d572bd7684e21d738b7f999e7eb3bdce69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `gradle:jdk21-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:7e8c36e42ba8693cd4f3cd3fafb9250f12b1c62ded0ab541bcb43df405134c1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.7 MB (579652571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fba014c9a9acc103b65c1a49771c831e8b3b20c6ff8384e1c39b379cacc01c7`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 05:26:10 GMT
CMD ["gradle"]
# Wed, 06 Mar 2024 05:26:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Mar 2024 05:27:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 06 Mar 2024 05:27:26 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Mar 2024 05:27:26 GMT
WORKDIR /home/gradle
# Wed, 06 Mar 2024 05:27:52 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Mar 2024 05:27:53 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 06 Mar 2024 05:27:53 GMT
ENV JAVA_VERSION=21.0.2
# Wed, 06 Mar 2024 05:28:07 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version
# Wed, 06 Mar 2024 05:28:09 GMT
ENV GRADLE_VERSION=8.6
# Wed, 06 Mar 2024 05:28:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Wed, 06 Mar 2024 05:28:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 06 Mar 2024 05:28:14 GMT
USER gradle
# Wed, 06 Mar 2024 05:28:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 06 Mar 2024 05:28:15 GMT
USER root
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9d3b46f3b6abb79f8b005c1c5e8e147a5620ed383c863f9c0ee636d3e13be7`  
		Last Modified: Wed, 06 Mar 2024 05:32:13 GMT  
		Size: 4.4 KB (4352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80772bfcfdc92d76e63c8555b093457578c8cbb443b3ac14f74b194d6b77c52f`  
		Last Modified: Wed, 06 Mar 2024 05:32:32 GMT  
		Size: 126.4 MB (126394234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4cc1cc51d535cf97ad7ebede5c0016ccc2ecdd86d6b84033d70ceeb85b00a7`  
		Last Modified: Wed, 06 Mar 2024 05:32:37 GMT  
		Size: 290.0 MB (289986766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed1a0c3de871e46bc4091edbd9a057dc7c604cc2a58f8126320421004ff6bb4`  
		Last Modified: Wed, 06 Mar 2024 05:32:20 GMT  
		Size: 132.8 MB (132815748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a777e53fc55b6f21f8298b530e8193b0058f1db48ed3219d3599218f3de7d3`  
		Last Modified: Wed, 06 Mar 2024 05:32:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk21-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bddfcbbb7925e3b05ec2ae64e410a45f329f8792bf91bc8a96b14ca0a45cbe1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.4 MB (565357663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76691c4ea6a2673c2b0aac75757f0121f9ba3f95d4072fd0896f572d5e00aa4b`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:59:44 GMT
CMD ["gradle"]
# Wed, 06 Mar 2024 02:59:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Mar 2024 03:00:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 06 Mar 2024 03:00:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Mar 2024 03:00:44 GMT
WORKDIR /home/gradle
# Wed, 06 Mar 2024 03:01:06 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 06 Mar 2024 03:01:08 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 06 Mar 2024 03:01:08 GMT
ENV JAVA_VERSION=21.0.2
# Wed, 06 Mar 2024 03:01:19 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version
# Wed, 06 Mar 2024 03:01:23 GMT
ENV GRADLE_VERSION=8.6
# Wed, 06 Mar 2024 03:01:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Wed, 06 Mar 2024 03:01:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 06 Mar 2024 03:01:27 GMT
USER gradle
# Wed, 06 Mar 2024 03:01:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 06 Mar 2024 03:01:28 GMT
USER root
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a649eed9d65a1ba77c596e8bdf1afc1a63d443266a530149c9db9704bbec3c7`  
		Last Modified: Wed, 06 Mar 2024 03:04:30 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c0a058a9c64655069538df5ba137bb6cdd6c1ca50cfafe2ed0f13630a423c2`  
		Last Modified: Wed, 06 Mar 2024 03:04:43 GMT  
		Size: 122.5 MB (122470925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453d3b9fef55b9458f4369f035bf32205e65a8468dc3d5b24bfaedb310dd17d4`  
		Last Modified: Wed, 06 Mar 2024 03:04:47 GMT  
		Size: 281.7 MB (281665820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696bd873cc8c1bd655889b83f666a79bbbc1f968f38cea0377250b47298417c2`  
		Last Modified: Wed, 06 Mar 2024 03:04:35 GMT  
		Size: 132.8 MB (132815749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc52445ab2d696b165db2d35d0f2573c1e466e0dea570ca1014980a51f5e2c6`  
		Last Modified: Wed, 06 Mar 2024 03:04:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
