## `gradle:8-jdk-21-and-23-graal-jammy`

```console
$ docker pull gradle@sha256:64a51bbc6fe1d90c7ba2d49ebd49d1dc101c5612c2ac8a7cc8904aaa4c85bbfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-21-and-23-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:a19c821da9845cf712865977db715494ed901ee080e80587dee30d1a9269572c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.2 MB (914194458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432e1d1512dc99c17c502e7f37859943849dc4822c559d7ed50d0b0f3637b8a3`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 13 Nov 2024 00:13:30 GMT
CMD ["gradle"]
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Nov 2024 00:13:30 GMT
WORKDIR /home/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm23
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_23_VERSION=23.0.1     && GRAALVM_23_AMD64_DOWNLOAD_SHA256=e26a0a74064b1689c056b5f24d7cc3b271f57f576be063b139d27aafa1322951     && GRAALVM_23_AARCH64_DOWNLOAD_SHA256=5a456db9162a89be5fadd50e703c19313d25ef7f5043b750b639cd0460335e60     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_23_VERSION}/graalvm-community-jdk-${JAVA_23_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_23_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_23_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm23         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_VERSION=8.11
# Wed, 13 Nov 2024 00:13:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c24f26888fcea57a1e71920db1ff5ef7dbbd6efe5a75ca46bb1897b6a28e6e`  
		Last Modified: Wed, 13 Nov 2024 02:08:42 GMT  
		Size: 4.4 KB (4422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db87c9c8737d415bf6e6fb9d9bed625c065c35fa31292519f9f3f931bf72585`  
		Last Modified: Wed, 13 Nov 2024 02:08:44 GMT  
		Size: 126.4 MB (126422883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f56bf26b40db196907800a80b1a6ffedf2cb0b7ad013de30810e3fc7b286c9b`  
		Last Modified: Wed, 13 Nov 2024 02:08:51 GMT  
		Size: 621.3 MB (621252785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb0b2b95d629eb044b0a3664e86b57f7ae4abceb9c8f1e95958a50dbe1b2b9b`  
		Last Modified: Wed, 13 Nov 2024 02:08:44 GMT  
		Size: 137.0 MB (136978648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-23-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:59fc486033fb85eb8958a0d2ee65ea9377167cd6a72279af24c8cb22d81059da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfda88aa07c23ee8727fefabc742d290eaeba54ddaddccf475ac7a858c083b9f`

```dockerfile
```

-	Layers:
	-	`sha256:08789b1abb08c6b93ec6e710a2e006e8004305ee114ec36d77a4df4e639599c1`  
		Last Modified: Wed, 13 Nov 2024 02:08:42 GMT  
		Size: 9.5 MB (9500410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:575d8376fb0c3de0927c19865fa8e4c57df9b36601271c6f7cdbcd10ecb0588a`  
		Last Modified: Wed, 13 Nov 2024 02:08:42 GMT  
		Size: 34.1 KB (34132 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-23-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d127b33801afbf3111be397789e0b942755a48f07c8393dea88acb34fde30fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **874.1 MB (874095805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0365feab5deefebbae0db95ab0b6a086457640d15fb03552663fdd1358585a3`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:51:19 GMT
CMD ["gradle"]
# Wed, 16 Oct 2024 03:51:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 16 Oct 2024 03:51:19 GMT
WORKDIR /home/gradle
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm23
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_23_VERSION=23.0.1     && GRAALVM_23_AMD64_DOWNLOAD_SHA256=e26a0a74064b1689c056b5f24d7cc3b271f57f576be063b139d27aafa1322951     && GRAALVM_23_AARCH64_DOWNLOAD_SHA256=5a456db9162a89be5fadd50e703c19313d25ef7f5043b750b639cd0460335e60     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_23_VERSION}/graalvm-community-jdk-${JAVA_23_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_23_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_23_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm23         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 16 Oct 2024 03:51:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 16 Oct 2024 03:51:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60f8682fb10a6475b7738e85d12e74584ebb61c4b71dbfb59f18a0e09b5e35c`  
		Last Modified: Wed, 16 Oct 2024 22:01:04 GMT  
		Size: 4.4 KB (4421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b4ff64a0b551df6e2000fdfe1584b4cb54839568a4325105ba93d59af51411`  
		Last Modified: Wed, 16 Oct 2024 22:01:07 GMT  
		Size: 122.5 MB (122457537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a84ea875c5ee26be306fff0ebd187d6215274b957057f51b3f7c7a8529f7e1`  
		Last Modified: Wed, 16 Oct 2024 22:01:17 GMT  
		Size: 587.5 MB (587485086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9003628fad3d58c1fdf45f8f2e1280cabdf3162de381adeaa0f01f618f42301`  
		Last Modified: Wed, 16 Oct 2024 22:01:08 GMT  
		Size: 136.8 MB (136790400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-23-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:0cbed909fbef30a4cec10e6ac9dfe753c461120a4a46bfa2c4da2f38b831910a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9407198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc64697b24e850b32676dd993ef808543373835a2a94ff31f110318690706f5f`

```dockerfile
```

-	Layers:
	-	`sha256:9aae25bdbb0368e17b5c18a3e62ab7af8777bb01ad7cfd69a1ef4b0ee99f8ac6`  
		Last Modified: Wed, 16 Oct 2024 22:01:05 GMT  
		Size: 9.4 MB (9372989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a04bf269b8929b8d2bb7ad2d67ce97ab545c776cbc64c175312de3896825e5`  
		Last Modified: Wed, 16 Oct 2024 22:01:04 GMT  
		Size: 34.2 KB (34209 bytes)  
		MIME: application/vnd.in-toto+json
