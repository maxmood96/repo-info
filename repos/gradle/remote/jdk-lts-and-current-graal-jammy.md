## `gradle:jdk-lts-and-current-graal-jammy`

```console
$ docker pull gradle@sha256:4f585c8ac1982a1f3fbc352269453c1b96e566bcd4c1851bc401a68cfef2358a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:35699d17723d990a2244ebd75f2afc0a82f51f105ffd3057d8773d430fb86aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **913.8 MB (913811388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a22f7c2df08dbe29dabf8dcca36b81b0ecc4232f7f043df831ec43468bf73f`
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
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm23
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_23_VERSION=23.0.1     && GRAALVM_23_AMD64_DOWNLOAD_SHA256=e26a0a74064b1689c056b5f24d7cc3b271f57f576be063b139d27aafa1322951     && GRAALVM_23_AARCH64_DOWNLOAD_SHA256=5a456db9162a89be5fadd50e703c19313d25ef7f5043b750b639cd0460335e60     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_23_VERSION}/graalvm-community-jdk-${JAVA_23_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_23_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_23_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm23         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95e4621b38e18a704bfe9b02f7bffd24f022565d273d8887d27bb188aa33df2`  
		Last Modified: Fri, 20 Dec 2024 21:37:54 GMT  
		Size: 4.4 KB (4418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3037523f763bd88f0fff7ff3d63a9dd42f0ae2ca0886eb6a26f8a292cbaf7223`  
		Size: 126.4 MB (126406265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d27612807b6866c2914336c6134076418971fedf349fdddcdd9ec56938a8a4`  
		Size: 621.3 MB (621252811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d29d3a2c928f9b263ce4a61def67117c227d00a7e65d45001bd6f199072d91e`  
		Last Modified: Fri, 20 Dec 2024 21:37:58 GMT  
		Size: 136.6 MB (136612174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:6b2cae06662df346ec22a06e3dbd49ce12978e3c192da60c5fdd35511d2bc100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9516177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f8f686a129203d3ebe93ca1af5b784c4f6fc3c55510f3ded60c766dc7522f8`

```dockerfile
```

-	Layers:
	-	`sha256:b08933aa33d2396ca5651f80362af67932ae0ef4530046b3ed0bd92a0c98636c`  
		Last Modified: Fri, 20 Dec 2024 21:37:55 GMT  
		Size: 9.5 MB (9482045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977b98b5bc2ff5162c44ea2a2f466c1c7cdd4cab6ec5aef9ed1b9337e8d6c197`  
		Last Modified: Fri, 20 Dec 2024 21:37:54 GMT  
		Size: 34.1 KB (34132 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:25ea2406574beefaf1a9985f9b995884d1e0082c6f03d755c0f644cd5d327474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.9 MB (873931649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38dac0a5fe290cdeed70549e965acfd0bf35b979b4e693ea5370f323371385b`
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
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm23
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_23_VERSION=23.0.1     && GRAALVM_23_AMD64_DOWNLOAD_SHA256=e26a0a74064b1689c056b5f24d7cc3b271f57f576be063b139d27aafa1322951     && GRAALVM_23_AARCH64_DOWNLOAD_SHA256=5a456db9162a89be5fadd50e703c19313d25ef7f5043b750b639cd0460335e60     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_23_VERSION}/graalvm-community-jdk-${JAVA_23_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_23_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_23_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm23         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29284703b255abec0a30277e5fcf84a30a0bb8981aa0bdf0c3b11adaccc6023a`  
		Last Modified: Sat, 21 Dec 2024 00:41:37 GMT  
		Size: 4.4 KB (4422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20451a6b2abf3b39c94f7e57dd6ceb9709180d492e00ed0a56f30ed85491b19a`  
		Last Modified: Sat, 21 Dec 2024 00:41:41 GMT  
		Size: 122.5 MB (122462021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31b179fbbe9ffe374a636d1dc26701045381ab3f1683736a9bc907cac2920e`  
		Last Modified: Sat, 21 Dec 2024 00:41:53 GMT  
		Size: 587.5 MB (587485131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9554ceae31f466879d62c79320e27962c95250a361d807b56535b81ac6d514b8`  
		Last Modified: Sat, 21 Dec 2024 00:41:41 GMT  
		Size: 136.6 MB (136621714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:575757671de8b4a63a86232f817b22190a02a3571dffee6bbe7cf6523196c955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9457037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1fc3aa566e54c655a523aea3062d929844ff88936ad9110c579c35c6cb00c8`

```dockerfile
```

-	Layers:
	-	`sha256:f587c7dfae536e29afca9956956797763a49e4c28f2eded33440df2e8953a363`  
		Last Modified: Sat, 21 Dec 2024 00:41:38 GMT  
		Size: 9.4 MB (9422612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8e6f512c9b6f7fbdaa2dbb0ed9548d7949cbc0e92f20ff80b75d65c076a9fc`  
		Size: 34.4 KB (34425 bytes)  
		MIME: application/vnd.in-toto+json
