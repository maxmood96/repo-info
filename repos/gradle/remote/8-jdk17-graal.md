## `gradle:8-jdk17-graal`

```console
$ docker pull gradle@sha256:3f44b510b07b172e931854da0eb2348727e96d3bacc96490795ece0bd73c02b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:2bce89e07e2952bb1700951bea7d4988df5e3d73b9cfbc547e1890cd55911999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590315534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae580ef0838e20d8c7fe4860f3e20185ba21de1c9feb460fc096c1012887dc0b`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_VERSION=17.0.9
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER root
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee27e55e051cc13a25cf93ac3bbacd52a4e17c9f8882ff123ca75ee54fbb5a7`  
		Last Modified: Mon, 03 Jun 2024 19:01:49 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2e4dbf1a57c5b03ab7dcca68d2dec9980ba2806a049d6ec0662f2588ffe286`  
		Last Modified: Mon, 03 Jun 2024 19:01:51 GMT  
		Size: 131.6 MB (131595486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ce5455df565d4d32d33205cc5d8b225817f2cc01cce0b9ae9917957b16378a`  
		Last Modified: Mon, 03 Jun 2024 19:01:53 GMT  
		Size: 291.1 MB (291064298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b1af03f9b7cab4bc8efccc621b4623e7f7bc50c13b84b6e05168a0208edf04`  
		Last Modified: Mon, 03 Jun 2024 19:01:52 GMT  
		Size: 138.1 MB (138062552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2e7b2ad66a4ff8693dd0d68c383667e6d9c22d043012727d9f0b027b747c8f`  
		Last Modified: Mon, 03 Jun 2024 19:01:50 GMT  
		Size: 54.9 KB (54909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:2125233fae66803d60f545d9cac62c5369592fe68b4468959222794f0c27aae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8614643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525b6934bd2107ee645cb0652267854f33ad97001eebc3c1467b24fa114dbd2a`

```dockerfile
```

-	Layers:
	-	`sha256:3b29dca258b1555076905f6d6aff22ee79c29e604762e1fff6b47a37da0d67ba`  
		Last Modified: Mon, 03 Jun 2024 19:01:49 GMT  
		Size: 8.6 MB (8582948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:480a611096701f5ee3ca74c3bf45f2f6c78150f5994e0065628da37588298c14`  
		Last Modified: Mon, 03 Jun 2024 19:01:49 GMT  
		Size: 31.7 KB (31695 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5497b4efb31aba092e087eecb6c290557aa62ea33c2bc6f19f2871753642beee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.6 MB (567605250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f499ffa19923d0213369e517cee26c381b1ac37973099d7fcebf804e550c19`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 23 Mar 2024 20:25:42 GMT
ARG RELEASE
# Sat, 23 Mar 2024 20:25:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 23 Mar 2024 20:25:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 23 Mar 2024 20:25:42 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 23 Mar 2024 20:25:42 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["/bin/bash"]
# Sat, 23 Mar 2024 20:25:42 GMT
CMD ["gradle"]
# Sat, 23 Mar 2024 20:25:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 23 Mar 2024 20:25:42 GMT
WORKDIR /home/gradle
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 23 Mar 2024 20:25:42 GMT
ENV JAVA_VERSION=17.0.9
# Sat, 23 Mar 2024 20:25:42 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
ENV GRADLE_VERSION=8.7
# Sat, 23 Mar 2024 20:25:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
# Sat, 23 Mar 2024 20:25:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
USER gradle
# Sat, 23 Mar 2024 20:25:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 23 Mar 2024 20:25:42 GMT
USER root
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58c90468198f173de8019e534267322c0fdaf708ca32e63e9990d628f2340a6`  
		Last Modified: Thu, 16 May 2024 22:38:03 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fdac5ad005ad9755489dc846c118af1f3f6b4ada67f3743c2d898d90af58a6`  
		Last Modified: Thu, 16 May 2024 22:38:06 GMT  
		Size: 122.5 MB (122468941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40c3af10ad9702ec720c6f89798037cd0866f044b0871adbda2e87fe1a2237f`  
		Last Modified: Thu, 16 May 2024 22:38:10 GMT  
		Size: 283.5 MB (283501908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90426592bc48e5d8349c7b7efcd596758e4f61dfcf28a8c7b87371827e16a68a`  
		Last Modified: Thu, 16 May 2024 22:38:07 GMT  
		Size: 134.2 MB (134210005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2338e0515ce2a7c8059b93624ef67913fd6903cd8c0b424aef284fb43fa8cc5a`  
		Last Modified: Thu, 16 May 2024 22:38:05 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:6bc5cbaf8668eeddf0162a606e43410dab0bfcb4f0bafd2563125d91008cf91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8606143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b778f656b1fa255eb969675fbcc89cd5983fda05b2f22f914a64776f781123e`

```dockerfile
```

-	Layers:
	-	`sha256:8a49c34a31ac542b233e185b7f01561b07a0e07d8fd3270cbb14b46f494d3758`  
		Last Modified: Thu, 16 May 2024 22:38:03 GMT  
		Size: 8.6 MB (8574397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479298b27cc48071809a96a7eb0a5aee7805a0a92aeac4d66913d57e24b296b3`  
		Last Modified: Thu, 16 May 2024 22:38:03 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.in-toto+json
