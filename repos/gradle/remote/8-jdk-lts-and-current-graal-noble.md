## `gradle:8-jdk-lts-and-current-graal-noble`

```console
$ docker pull gradle@sha256:980eefdcdcc6d3ca88a60d140e88d86e21e15e29dd11a6da3678e2918be2830e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-lts-and-current-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:1af2d95661d8ef8706d38cf55944201588a8e8695ffc93e7e30469a631fe30e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.7 MB (941659170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e4ea06448c58dbaa5dea074b6cdd1cb9bf018de3f9736d3d329ab515a82c1e`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
ARG RELEASE
# Sat, 26 Apr 2025 01:26:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 26 Apr 2025 01:26:29 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm24
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_24_VERSION=24.0.1     && GRAALVM_24_AMD64_DOWNLOAD_SHA256=d2c544de672e400476a09c8f1da79ecc6b774a9441e234948542c3b3e6a84bde     && GRAALVM_24_AARCH64_DOWNLOAD_SHA256=a3d1be8fadfb0d3df632252301f79a9b02b47e523da66539d370c62e683d762e     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_24_VERSION}/graalvm-community-jdk-${JAVA_24_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_24_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_24_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm24         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da5306fc2cb1a3705c08ee0611a24133fd146940018ba39679d728c3b49ffd0`  
		Last Modified: Mon, 05 May 2025 16:36:26 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2f969841886d59e16863d045f3c7796fa881bfa58249c3591f7917562582dc`  
		Last Modified: Mon, 05 May 2025 16:36:31 GMT  
		Size: 148.4 MB (148411040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa52bb58b47d3fab01e988f00ac0aa44a450fec37fce3f41924cf49fb387eadd`  
		Last Modified: Mon, 05 May 2025 16:36:44 GMT  
		Size: 626.1 MB (626077958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84f5d60ad77eed92dcf33422edcf6577ec96ee6402fcb3bccb271ff8d045aca`  
		Last Modified: Mon, 05 May 2025 16:36:31 GMT  
		Size: 137.5 MB (137451197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:fc16eec72013dd4fff092d6ffc57bf8950e11bfe97b298ee1d954520df3bcbb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6826255928cd0d01433a13aa056d21f24bd2bea5372ff633c16f88ec6c5c84ff`

```dockerfile
```

-	Layers:
	-	`sha256:ed232e0809aa1b0fdf044c4553ea2a4d2a25356f5f2f3ea7f0470a4508d191a9`  
		Last Modified: Mon, 05 May 2025 16:36:27 GMT  
		Size: 9.1 MB (9116551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bd73850ae847f6295cce31b0675255ee5432c5dc006d69c5b83649266b1d99`  
		Last Modified: Mon, 05 May 2025 16:36:27 GMT  
		Size: 34.7 KB (34702 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-lts-and-current-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5f24ff1ff3dc65302affa4836288f8b168404146e4d94b734d1620f7d40ae55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **901.8 MB (901768407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92acced73a2ad4e6fc658a3794a134b65b06eaa6632c118570725c01e260e1d5`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
ARG RELEASE
# Sat, 26 Apr 2025 01:26:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 26 Apr 2025 01:26:29 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm24
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_24_VERSION=24.0.1     && GRAALVM_24_AMD64_DOWNLOAD_SHA256=d2c544de672e400476a09c8f1da79ecc6b774a9441e234948542c3b3e6a84bde     && GRAALVM_24_AARCH64_DOWNLOAD_SHA256=a3d1be8fadfb0d3df632252301f79a9b02b47e523da66539d370c62e683d762e     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_24_VERSION}/graalvm-community-jdk-${JAVA_24_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_24_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_24_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm24         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29675f4607b33b52e1b9f655b494de2cc4c97fbc6a1335ea5b00f9235cb2728`  
		Last Modified: Mon, 05 May 2025 17:10:36 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e51727a0b21d61ac21875a547d88c99bf5b0f4546a532fd6a991254b2865a41`  
		Last Modified: Mon, 05 May 2025 17:10:40 GMT  
		Size: 143.5 MB (143514637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51ea870831ab709de14fd0cbbd30c1c4ec428313ba05ab3014bf52fae107bbd`  
		Last Modified: Mon, 05 May 2025 17:10:49 GMT  
		Size: 591.9 MB (591948727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e01661fcefe96df04dbd023494757d1d2d88b474a99a5564a7f1425b5f5171`  
		Last Modified: Mon, 05 May 2025 17:10:40 GMT  
		Size: 137.5 MB (137456720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:ef4db277611e4ee683211514977cf53795ee8f9eff2a6c8b8065c545a247697e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9120449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e991cfa5c2c6fef9761266a8888aa2568cc3853bb71036a13a884550251440`

```dockerfile
```

-	Layers:
	-	`sha256:035e6586d6f13c70e03df6f52bd9279be5f8780c2f6b69577fb3a16a46c0c639`  
		Last Modified: Mon, 05 May 2025 17:10:37 GMT  
		Size: 9.1 MB (9085455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34966c0b381bef6b62b140d2037d48f2458c460eb9aa53577bf5b9fc7dea5df8`  
		Last Modified: Mon, 05 May 2025 17:10:36 GMT  
		Size: 35.0 KB (34994 bytes)  
		MIME: application/vnd.in-toto+json
