## `gradle:jdk17-graal-jammy`

```console
$ docker pull gradle@sha256:70eee6dd5eca3c7dca10ebe500b10e156bdd52c8d3ca8d983d6cecc1a432719a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:c8e2521de0db35ea67a1774a7989b366ff3d560308c43d50fafa9d1f8962b445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.4 MB (585375108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9ca7206969b133573d190b2d019977a7faa96e016ad40b4c87f6f5cb2527cc`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:44 GMT
CMD ["gradle"]
# Wed, 01 Apr 2026 20:10:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 01 Apr 2026 20:10:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 01 Apr 2026 20:10:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 01 Apr 2026 20:10:44 GMT
WORKDIR /home/gradle
# Wed, 01 Apr 2026 20:11:16 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 01 Apr 2026 20:11:16 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 01 Apr 2026 20:11:16 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 01 Apr 2026 20:11:26 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 01 Apr 2026 20:11:26 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 01 Apr 2026 20:11:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 01 Apr 2026 20:11:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 01 Apr 2026 20:11:28 GMT
USER gradle
# Wed, 01 Apr 2026 20:11:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 01 Apr 2026 20:11:29 GMT
USER root
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72c046dac3d155c0b38d2d613283506f2685a62dbcc050200ede78dd287f798`  
		Last Modified: Wed, 01 Apr 2026 20:12:01 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a5b3eb5c980da46ea684b22266a6ec53b7b4009073a0a24b35fc78240227b8`  
		Last Modified: Wed, 01 Apr 2026 20:12:07 GMT  
		Size: 126.7 MB (126736107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5619fd54b5b2dde2fffa8220dc57340542ef037c9927f79b71d6f52da4e1ef4f`  
		Last Modified: Wed, 01 Apr 2026 20:12:13 GMT  
		Size: 291.1 MB (291064304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293fe655221afb344fb0c8aa8f2e266330226168da1cf44fd51a78b1b8acd3f0`  
		Last Modified: Wed, 01 Apr 2026 20:12:07 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dd026b534d73345b3e9ee9cbc9c1f88bb91e87dd6d6bd69aedbb4394d5ad1b`  
		Last Modified: Wed, 01 Apr 2026 20:12:02 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:2c81b4dd2a1afeddfcbdd83dab9fd456fce3e5706cac32df956c7df8bbdba1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9416701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae2b5683d632a853c93c57e92dffd77a999fc024331b72bc30ea28d595b6083`

```dockerfile
```

-	Layers:
	-	`sha256:68216963e90c28882f533b48e605e40b249676feec34c3e08282ff8fffb74129`  
		Last Modified: Wed, 01 Apr 2026 20:12:01 GMT  
		Size: 9.4 MB (9389144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d869b31fd61ca6b208f2bce3ac1571ffe47d251b77136f14d190eae9eba4d1`  
		Last Modified: Wed, 01 Apr 2026 20:12:00 GMT  
		Size: 27.6 KB (27557 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ec757fbbc34cae92d705b39630689c3ea6d6e86115fa84bd314fbe023dc18ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.8 MB (571838261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b28ff61b482ed8b9a209fece48883e9b0e06b460c41ec09d3fe556d4759afd`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:43 GMT
CMD ["gradle"]
# Wed, 01 Apr 2026 20:10:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 01 Apr 2026 20:10:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 01 Apr 2026 20:10:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 01 Apr 2026 20:10:43 GMT
WORKDIR /home/gradle
# Wed, 01 Apr 2026 20:11:19 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 01 Apr 2026 20:11:19 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 01 Apr 2026 20:11:19 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 01 Apr 2026 20:11:31 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 01 Apr 2026 20:11:31 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 01 Apr 2026 20:11:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 01 Apr 2026 20:11:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 01 Apr 2026 20:11:33 GMT
USER gradle
# Wed, 01 Apr 2026 20:11:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 01 Apr 2026 20:11:34 GMT
USER root
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6da70512cb9dc26ce8c5390fd372d34c6e201bb8df7d6e4c672898d8b96224`  
		Last Modified: Wed, 01 Apr 2026 20:12:06 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce11dd9778e28236ad9b85befb7c31be3dc2e84945b407c52be9ba3b9b838859`  
		Last Modified: Wed, 01 Apr 2026 20:12:12 GMT  
		Size: 122.9 MB (122887442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af38b1dd68e4bee1025a97b614437cb09dc1e3b34f43a5b581df980109b4d870`  
		Last Modified: Wed, 01 Apr 2026 20:12:16 GMT  
		Size: 283.5 MB (283501859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e773bda31cd47dd2a93e2122ae0166819f105b2ce0bd636abf7b43c93b654a4c`  
		Last Modified: Wed, 01 Apr 2026 20:12:13 GMT  
		Size: 137.8 MB (137808333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6073aa290ebeb9cad863a6b1f4b26891d91f92dc98ceb6832fa7e4b517cdab`  
		Last Modified: Wed, 01 Apr 2026 20:12:08 GMT  
		Size: 29.3 KB (29339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:86b94ba1c7afac15b0dffbdb8a5e8a76a0f0d7c47b458c59df29f81df02f2b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9385620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d8cfa2bae80e0fe22a8eef676e487ffb1250433c908287e74b61c11fe5ccb2`

```dockerfile
```

-	Layers:
	-	`sha256:c2812503858f055b41f3f9773b264c7bbdd5053f05dd117213014ba734b4613d`  
		Last Modified: Wed, 01 Apr 2026 20:12:07 GMT  
		Size: 9.4 MB (9357900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf61f5e34311a9b76a8ceca03ee5fbefdac7baa89429fba25968a17ecdbf14ea`  
		Last Modified: Wed, 01 Apr 2026 20:12:06 GMT  
		Size: 27.7 KB (27720 bytes)  
		MIME: application/vnd.in-toto+json
