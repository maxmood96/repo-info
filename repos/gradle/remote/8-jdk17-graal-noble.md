## `gradle:8-jdk17-graal-noble`

```console
$ docker pull gradle@sha256:80ed690e4be7480fafd4a9eda7ca905795c26ae2fb94b4d7662fa02566b08395
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:133f5bd43e5563194a43acda910c58ce240ac7891318485620be0ceed4073614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.7 MB (606662713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998a4dffd4394a76cdae0a47cf642f8d07eeb4c9bf42ad2f9dbf1aff460c18ad`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776b31a15283ea628874de7216567f36299ba7615f07dfd3e36b400e8273bea`  
		Last Modified: Tue, 27 May 2025 18:59:40 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e761a16bd47fae79361010f4b91505f10c872f34fff7001f1866ef24690ed037`  
		Last Modified: Tue, 27 May 2025 18:59:44 GMT  
		Size: 148.4 MB (148428795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b692d04d09e44a8a0917dc9c4dea4a9cc731e6042c49389fac7d8c063f6490a`  
		Last Modified: Tue, 27 May 2025 18:59:45 GMT  
		Size: 291.1 MB (291064592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac56b9464de644f58ef0822a95d6ec3ba6ee38488515c5307f1b0a942236e44`  
		Last Modified: Tue, 27 May 2025 18:59:42 GMT  
		Size: 137.4 MB (137395582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d37b99e0705b86eef21934e6f264663e2c2efed987377b0415d0f1486ccda49`  
		Last Modified: Tue, 27 May 2025 18:59:41 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:261c272f7b41213b003ea04a070c2e6e298e7b8381f07a7cb13f7b3a771a41b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8808895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e074fc46810b4d466afe8473283aac102feff3954153ad6d068a7817b5d740`

```dockerfile
```

-	Layers:
	-	`sha256:f3dfff25e015afd0be92fc8d8ccdc17a5258329a6303da136ae3c4ac03d2e964`  
		Last Modified: Tue, 27 May 2025 18:59:40 GMT  
		Size: 8.8 MB (8781619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6571bcb73e2f3c71fe995cec5a1a7e8b4de4f4e391a7ce7ee3154e2631b50072`  
		Last Modified: Tue, 27 May 2025 18:59:40 GMT  
		Size: 27.3 KB (27276 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8f0b673deec92a0d82b09df5f416971e501f4a4e5b198ea5a300dd9319efbca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.3 MB (593337288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188d090cfe22972e08d3e4c8d02d816337ad41ac81773a094e7e6c23f38def91`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f4a130967abc8e527f507f6887c3f7c600bfa74a249b7a1077686270d72b6a`  
		Last Modified: Tue, 27 May 2025 19:37:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa323df40ee8608cc7b3f80b9aa63d0761f0c38580bcc2b38cefbf33e5f0d9c`  
		Last Modified: Tue, 27 May 2025 19:37:55 GMT  
		Size: 143.5 MB (143532216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3504146ee59b6c62aed11cb6f7bc328a5fbc4079fe0d1a4b178ae467ca79f338`  
		Last Modified: Tue, 27 May 2025 19:46:34 GMT  
		Size: 283.5 MB (283501816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578c15d82e29af1ecef431a80bd1134ed7a3cc5a97753987809fb762a78aa0a7`  
		Last Modified: Tue, 27 May 2025 19:46:32 GMT  
		Size: 137.4 MB (137395535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec2466130cfa94cf61dcdf18e5171273c931a6ce5c3da9c56e32ef6f4a6d73`  
		Last Modified: Tue, 27 May 2025 19:46:28 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:9ceb00818e433605cd688d52a89bc726135a45e5ad1350e01f0e36095b4e376f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8804682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d1acedf22e54bc63228b43c2ec4e8f453ce9e2f841be224b0603ffb020f2c9`

```dockerfile
```

-	Layers:
	-	`sha256:20f2e79ab87455bbe5b3564380ea310f752fd80a07cbd575353994f6b835fdc2`  
		Last Modified: Tue, 27 May 2025 19:46:28 GMT  
		Size: 8.8 MB (8777195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca35b31eb506134738cf531f7a22d0cdec26d744976389bc948d2e58f9d3281`  
		Last Modified: Tue, 27 May 2025 19:46:28 GMT  
		Size: 27.5 KB (27487 bytes)  
		MIME: application/vnd.in-toto+json
