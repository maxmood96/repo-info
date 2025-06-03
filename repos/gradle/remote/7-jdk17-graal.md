## `gradle:7-jdk17-graal`

```console
$ docker pull gradle@sha256:fdf28b3e1b71fe6a490972ac3a4c5529b07bfebed68d2b353558bd2e3c4b8bf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:dd860e7f4ec22b4a80e6c69e56f5ff38b74e32a2e892326991c6912aa99c9f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.1 MB (592120999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c277230d5bb9059add79ae53094e429576326a70c694de840d442faf01e142`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Jun 2025 18:03:22 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:03:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:03:22 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 02 Jun 2025 18:03:22 GMT
ENV JAVA_VERSION=17.0.9
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 02 Jun 2025 18:03:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 02 Jun 2025 18:03:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
USER gradle
# Mon, 02 Jun 2025 18:03:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
USER root
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96e5ff217e206da5ed15b4c0e73356aed3db7371e8ac77f6efd832228e99593`  
		Last Modified: Tue, 03 Jun 2025 04:17:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd9eb53db1ce4610c23cada176fa3870a7740bedd1345d4e24981ae259b494c`  
		Last Modified: Tue, 03 Jun 2025 04:17:02 GMT  
		Size: 148.6 MB (148554892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e947b8b059228e675371cd635f2191361274d4208c23267b6aa9676e13eb77f`  
		Last Modified: Tue, 03 Jun 2025 04:17:04 GMT  
		Size: 291.1 MB (291064025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f19768c7677af82a7c513829549f957eb29d4ae91532c8b55ff9844de46823b`  
		Last Modified: Tue, 03 Jun 2025 04:17:01 GMT  
		Size: 122.7 MB (122730525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f7b7cc678e2c42c18ea7fc56c8042a35c13ac2b9dfd0406a1a5724ebf81e44`  
		Last Modified: Tue, 03 Jun 2025 04:17:00 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:afe94a7e06b39bd85fd447783cb27c2f99cdb3c45ef8a2ec81bdbf40ab7247c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8726364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0854a9833b0f580240fc9d06534a77da3fe27e80594b74053429fa91233566a0`

```dockerfile
```

-	Layers:
	-	`sha256:dabc0d33653c6eb51a0e2f007a0fb299d82250ebf4824b3e63f84aa85da6c7c5`  
		Last Modified: Tue, 03 Jun 2025 04:17:00 GMT  
		Size: 8.7 MB (8694236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47206ffcf86df5de96927e1a123263f012af2fb7d851e01747f5ed0b10f80ad4`  
		Last Modified: Tue, 03 Jun 2025 04:16:59 GMT  
		Size: 32.1 KB (32128 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2b071229bb291ea4754ac41a3147072d5949f3584533d1137ff6f9f2ee05af18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578823086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20325384e08a5d159ff8e412523e168789386d09c0ca674578bba874f53a76cd`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Mon, 02 Jun 2025 18:03:22 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:03:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:03:22 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 02 Jun 2025 18:03:22 GMT
ENV JAVA_VERSION=17.0.9
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 02 Jun 2025 18:03:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 02 Jun 2025 18:03:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
USER gradle
# Mon, 02 Jun 2025 18:03:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
USER root
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Thu, 29 May 2025 06:11:37 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a084dbc9b7efa126554be6b387c36437dd79574d6672a7d118b4ec83c3f0d72`  
		Last Modified: Tue, 03 Jun 2025 04:48:04 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22900b68b25711552ba19e9c1d789101c568031c82e0d748f01f2ee09135990c`  
		Last Modified: Tue, 03 Jun 2025 04:48:08 GMT  
		Size: 143.7 MB (143678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1a62405761e3338c8afab8d6be7fd1e9ace8333ec936ac3bda6cf7470e1504`  
		Last Modified: Tue, 03 Jun 2025 04:50:59 GMT  
		Size: 283.5 MB (283501804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681bbc1ead989b69fc56e533bbcd10095efe6918d394512747b4dade3cf05dbc`  
		Last Modified: Tue, 03 Jun 2025 04:56:41 GMT  
		Size: 122.7 MB (122730530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c3d34147580e9e1d08bc11c4d5fba7748c7ad2e95d13873fad583df9fe842f`  
		Last Modified: Tue, 03 Jun 2025 04:56:38 GMT  
		Size: 59.5 KB (59511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:7db9cede888b9d359e6f3684f38b8ebe83962988095411779ed5c2b3d4b50138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81483c83d4a0b7b0acfb898a6363527c023a9896d001421aabe3fc5c9953178f`

```dockerfile
```

-	Layers:
	-	`sha256:6a8e857163e278040a7a6cbbb85a44577f518baa479600bbec2ded4ccf923e9a`  
		Last Modified: Tue, 03 Jun 2025 04:56:38 GMT  
		Size: 8.7 MB (8689932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc1ac4abc0ed768acdd662c08fd4e66a9388c5e928b7ea0ce4e15a63a986697`  
		Last Modified: Tue, 03 Jun 2025 04:56:37 GMT  
		Size: 32.5 KB (32459 bytes)  
		MIME: application/vnd.in-toto+json
