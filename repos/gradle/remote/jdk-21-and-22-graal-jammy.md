## `gradle:jdk-21-and-22-graal-jammy`

```console
$ docker pull gradle@sha256:e2da653d64204261d0eb07f4aab09245f031f6c6154c7d93bed98441023a5615
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-22-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:f0e19c6dc97df24a51a6c9c008ddfb24f3b388125812e786aa2fc139a3ab1323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.7 MB (903667593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5b90405a5663cd7aa8e8ac5edb22d25f9bcaf3d1ecbfecf9967173d8708c53`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 09 Sep 2024 18:59:34 GMT
ARG RELEASE
# Mon, 09 Sep 2024 18:59:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 18:59:34 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 09 Sep 2024 18:59:34 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Mon, 09 Sep 2024 18:59:34 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm22
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_22_VERSION=22.0.2     && GRAALVM_22_AMD64_DOWNLOAD_SHA256=ebac1dd96a5e0fbcd1dd9804fa58815f146390a40aae966f02a8c26d1974364f     && GRAALVM_22_AARCH64_DOWNLOAD_SHA256=28ca4c815fa68b86141d9dcf1a46c1f58f74dead41de9042de1202337bb014d9     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_22_VERSION}/graalvm-community-jdk-${JAVA_22_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_22_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_22_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm22         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faef84a50d80524022cec846dbcdce0ca7c527f66e3188cc86c1eb83e375aee`  
		Last Modified: Tue, 17 Sep 2024 00:59:49 GMT  
		Size: 4.4 KB (4416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4de56567db156956055da7e222144c0410f8e6632f3d98e35f81e7b8ba04b2`  
		Last Modified: Tue, 17 Sep 2024 00:59:51 GMT  
		Size: 126.4 MB (126374161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd7a983b9f08f6565fea1749dff253a3bfc6d2296bf891ce8df3369c39595d2`  
		Last Modified: Tue, 17 Sep 2024 01:00:01 GMT  
		Size: 611.0 MB (610974334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03064cd18c4fa0ce92f442bffc10afb668cf9c769e7702b4fde511d51242d6d`  
		Last Modified: Tue, 17 Sep 2024 00:59:51 GMT  
		Size: 136.8 MB (136778962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-22-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:1c7a2eff17121f00b08c73adf93bba3d7b6fd875e580072d37f1ede4c93e86f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049365d4657a81a9131b5796ee6cd392fd64864665b7477c3acb03c7cffd134d`

```dockerfile
```

-	Layers:
	-	`sha256:fb632afa4c056cfb4492e06220f4617c03097a82d034be284138782e698b193c`  
		Last Modified: Tue, 17 Sep 2024 00:59:49 GMT  
		Size: 6.5 KB (6531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95415779dcbaa1f0bbdd2ff029b500efbfdda0bdb7802cff0bec7c87e8f92209`  
		Last Modified: Tue, 17 Sep 2024 00:59:49 GMT  
		Size: 33.9 KB (33884 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-22-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:238cdbf657dd05ae589ba3869caa62b40629dfe4ac90193e384fa36b2a3fc2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **863.6 MB (863571327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2317a4ba10889c99cbe5eea0b681401fe388c0f63045b709273eecb804c66da`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 09 Sep 2024 18:59:34 GMT
ARG RELEASE
# Mon, 09 Sep 2024 18:59:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 18:59:34 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 09 Sep 2024 18:59:34 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Mon, 09 Sep 2024 18:59:34 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm22
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_22_VERSION=22.0.2     && GRAALVM_22_AMD64_DOWNLOAD_SHA256=ebac1dd96a5e0fbcd1dd9804fa58815f146390a40aae966f02a8c26d1974364f     && GRAALVM_22_AARCH64_DOWNLOAD_SHA256=28ca4c815fa68b86141d9dcf1a46c1f58f74dead41de9042de1202337bb014d9     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_22_VERSION}/graalvm-community-jdk-${JAVA_22_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_22_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_22_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm22         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea67b2a97619cacf1bc771045a4472fa479c40e504cc1f77687560a5bd83cff`  
		Last Modified: Tue, 17 Sep 2024 02:04:24 GMT  
		Size: 4.4 KB (4418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f245bc1c68d69d191eab9441cea151bedddfb3b734d5c0731df84d2eba51ff`  
		Last Modified: Tue, 17 Sep 2024 02:04:27 GMT  
		Size: 122.4 MB (122440261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9beabb0a63364dcbd39d763ef955dbdf715f0c59f89f7207ea5f0312f4ecc875`  
		Last Modified: Tue, 17 Sep 2024 02:04:42 GMT  
		Size: 577.0 MB (576979946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc132d7270e90a9cf821c88ca8a592c99c8fabdbec0fc19a9b85123387f5a7`  
		Last Modified: Tue, 17 Sep 2024 02:04:28 GMT  
		Size: 136.8 MB (136788341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-22-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:e2dd4550f68b8fb7bc13d6fa5c109c0123d32354f0802141d654664a98961b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8742494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a47af17fea60b1f8344db8544d86c454d9fa1f4a5473b49e96ae473e1a1787d`

```dockerfile
```

-	Layers:
	-	`sha256:911de0464e3a47f5950d79001bf1d26e6217db5efd4fa817c9d72117b6860fbf`  
		Last Modified: Tue, 17 Sep 2024 02:04:25 GMT  
		Size: 8.7 MB (8708166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e157a8970c14d32c353b816c2aa6d3b2faa07e87ab65b1aefc37e5a72f8a76c7`  
		Last Modified: Tue, 17 Sep 2024 02:04:24 GMT  
		Size: 34.3 KB (34328 bytes)  
		MIME: application/vnd.in-toto+json
