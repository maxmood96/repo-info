## `gradle:jdk17-graal-focal`

```console
$ docker pull gradle@sha256:307bf1f5eee3a696fd5c6c17d012a296522c5e3e0254015255adc4dc3419ca44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-graal-focal` - linux; amd64

```console
$ docker pull gradle@sha256:40b12429cc59cee7b7c147667de37a641ee824f2c114469e1ba56945bf04fcfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589513539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3e85c06e475f385c746951c0a67249c7212e684f0f998643a7fb1e569cbc33`
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
# Thu, 29 May 2025 19:22:22 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:22:22 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:22:22 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 29 May 2025 19:22:22 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_VERSION=8.14.1
# Thu, 29 May 2025 19:22:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER gradle
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER root
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c96427c72aa0fd65eb42adfeccc56b3c4177d91c2bd6206e0721c2acae6ed8f`  
		Last Modified: Mon, 02 Jun 2025 16:49:10 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff69aa94caf536b41459b041508e8211f85cfa3b8a0fc10507d57b42a6c92645`  
		Last Modified: Mon, 02 Jun 2025 16:49:13 GMT  
		Size: 133.5 MB (133484220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87945cd30a79aa1649a21185925bf20da534cb858168e65a5b8668e0a3d93fa3`  
		Last Modified: Mon, 02 Jun 2025 16:49:17 GMT  
		Size: 291.1 MB (291064104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fbd14b2f591bbdbe39651ee9f21e5809fc504bd15499f032c701f6b6934b01`  
		Last Modified: Mon, 02 Jun 2025 16:49:13 GMT  
		Size: 137.4 MB (137395573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a9951059b8cfb79b0106317c88d2f4d9504903b7e97cc9c46336528ac8fba1`  
		Last Modified: Mon, 02 Jun 2025 16:49:11 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:b00d8b21d890a1c2c18d78ceedae184a424f644ac47e36ff80c44dc367a32b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b57137710df1467dcf38ce7cc24681a9fb0a8b4bfa1601ba008d522bb05790`

```dockerfile
```

-	Layers:
	-	`sha256:6f637bfc6da0108b705de63875d29d5004336b5e861f5102bc8ac5d13843f67a`  
		Last Modified: Mon, 02 Jun 2025 16:49:10 GMT  
		Size: 9.5 MB (9496703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79ce75e78147d138f4cafbd2a7a2374cdb01e3ebbbad4cfea72f58202c19656`  
		Last Modified: Mon, 02 Jun 2025 16:49:10 GMT  
		Size: 30.1 KB (30055 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-graal-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:205ab3b329439e7c35be6176e1c2a687ff09fe5551cd117ea87bc6eb33c4de36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.5 MB (573548363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ee0035c178ec645bc5e46501729ddc38936624452c19b62b46ea90efb74578`
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
# Thu, 29 May 2025 19:22:22 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:22:22 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:22:22 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 29 May 2025 19:22:22 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_VERSION=8.14.1
# Thu, 29 May 2025 19:22:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER gradle
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER root
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e597dc209c6014ca33b97e7e44230911098c531cad055aac4f204d1dac79303f`  
		Last Modified: Tue, 27 May 2025 19:50:18 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b34cb536f9c53894fa71233844e9634a04d6dd6a71245cf872794053e5e39c`  
		Last Modified: Mon, 02 Jun 2025 17:07:27 GMT  
		Size: 126.6 MB (126609513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfb8df26c3b91ae83769be34cb1170108cf2474d5a6c7daa2158f1c561412b7`  
		Last Modified: Mon, 02 Jun 2025 17:07:32 GMT  
		Size: 283.5 MB (283501741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb4bef6f78d6b46e2164df5f686d708753e9e18b3b6257d38de9ad79c6517f`  
		Last Modified: Mon, 02 Jun 2025 17:07:27 GMT  
		Size: 137.4 MB (137395569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b928673a5cca13958e4781c8c8faa17baab6f691df8f808ce5683d698d9f69`  
		Last Modified: Mon, 02 Jun 2025 17:07:24 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:03b9cbff15ab2d985e60f5f857f0ee94ade905e72db9248e9dbc642a38339e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9504371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a0db5b5748beda159239e5dbdc55859b5f61b1c8718ed34faef910e97fb1c3`

```dockerfile
```

-	Layers:
	-	`sha256:3a553c12b72a48d5a5249e830ed31eef4baa13ac14dda1ca53bd4ba8d4e684c7`  
		Last Modified: Mon, 02 Jun 2025 17:07:24 GMT  
		Size: 9.5 MB (9474056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:558c22cbf2a342f492ba6dbfbfc561b395e4cb501a08d0fe9015e1528f316d2e`  
		Last Modified: Mon, 02 Jun 2025 17:07:24 GMT  
		Size: 30.3 KB (30315 bytes)  
		MIME: application/vnd.in-toto+json
