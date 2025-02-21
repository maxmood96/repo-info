## `gradle:6-jdk17-graal`

```console
$ docker pull gradle@sha256:7404a4b5f3b946fc48a78ea8aee9746f312e3861bf42cc21c10c76b519c44bfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:9f0dab3675988990b242c734944f6971942dce3f3b3d9888816cea4dbb0fe261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.8 MB (585780755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430d73bf61c0e06cca531a9c9bb9b8ca435b3cd204fb40e1d41d36995b389ace`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 21:10:38 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:38 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 18 Feb 2025 21:10:38 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 18 Feb 2025 21:10:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER root
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546d906f208d56067205490a692f929c02afc299bc535f4bd0eeade9aa77bc1b`  
		Last Modified: Wed, 19 Feb 2025 21:32:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa96c4a59437216c3499954e3be6ff7aa1c572c6a290c2b0643c1cb9ff523ac7`  
		Last Modified: Wed, 19 Feb 2025 21:32:36 GMT  
		Size: 156.8 MB (156833234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50698ddcd07fffd4b155686ef7af6876c242e31cb0687c1f22fd4bd75cfd2075`  
		Last Modified: Wed, 19 Feb 2025 21:32:38 GMT  
		Size: 291.1 MB (291063968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e177bcf1bd9b1f5d196fa7d145e4bbfe41916f3291f38b6b195a0edb4f284d`  
		Last Modified: Wed, 19 Feb 2025 21:32:35 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa974dd33b3adfa00fcabab0da4ee1e4407ef3369073758659fd0597088123c`  
		Last Modified: Wed, 19 Feb 2025 21:32:35 GMT  
		Size: 431.3 KB (431280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:16d231097618b9a755a4d21e0f1b7fdabca7c5879334ce8ef5a93197fa0dd334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8653849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e81ba82872b1a5403bdb840cfe1f8612bd376ac213f60f456d3ea1c04eba9b9`

```dockerfile
```

-	Layers:
	-	`sha256:afe5e957164136cb684a848e29606aaa42c8584ddbd2d26f3f402f9f3c8b347e`  
		Last Modified: Wed, 19 Feb 2025 21:32:34 GMT  
		Size: 8.6 MB (8627210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e3285575ed61b413cf88dd72d837fd1504fd2523958398b6042fb1c74539512`  
		Last Modified: Wed, 19 Feb 2025 21:32:34 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d09b37b5352e593e8588901704dea4490cc1d694886dd362d22528855adabc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.2 MB (572189395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8cffd09501c414c084778240b085d0930a8a3d982a227692d615b54fd6182c`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 21:10:38 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:38 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 18 Feb 2025 21:10:38 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 18 Feb 2025 21:10:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER root
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c3672261dc2856ad9db556b6b7d70b26f2f4a04a63075b1b1975899a7a5012`  
		Last Modified: Fri, 07 Feb 2025 06:32:25 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9e15997b1a1a49c0d880adef5336b4acffbe710980c3cd8b833c12f6fe257d`  
		Last Modified: Fri, 07 Feb 2025 06:32:29 GMT  
		Size: 151.7 MB (151671014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499020f46d33030ccb69f84d532a2d27acee826d1b527253bebbc506d1110f3c`  
		Last Modified: Fri, 07 Feb 2025 06:32:32 GMT  
		Size: 283.5 MB (283501764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeb8a0c78d1330c4c57e6fd7c8ec5090700a99a66345cc2e5392a195a1edab1`  
		Last Modified: Wed, 19 Feb 2025 22:41:22 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612715bdabde9f2023dcc06435842fec4c8576203de90fd1cd96e9c24ad3e101`  
		Last Modified: Wed, 19 Feb 2025 22:41:19 GMT  
		Size: 425.0 KB (425032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:117c8cddbbbc93bdc1dba79f88a868779ee1b97912026a1b4fb0661b211eaabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8649879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892df14e158935a856b49b83de72454c0552b932f4b48578122f0a22434e12b2`

```dockerfile
```

-	Layers:
	-	`sha256:8b6fb9106a28807a7ea1efd27f6b035f71fa59547bd4f160be3cdad9e4b849ec`  
		Last Modified: Wed, 19 Feb 2025 22:41:19 GMT  
		Size: 8.6 MB (8623052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e19134babdbd7cdbf9b4e8916be6b5ad3cee1b185d3dec072ee3f35d16395c`  
		Last Modified: Wed, 19 Feb 2025 22:41:19 GMT  
		Size: 26.8 KB (26827 bytes)  
		MIME: application/vnd.in-toto+json
