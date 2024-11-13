## `gradle:jdk17-graal-jammy`

```console
$ docker pull gradle@sha256:7d05785961c4214998a0c26f9515ccd6864b6e52db70a666e1f2e7559c6d9141
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:50b2eead3dcba05a96c660b659c37933bc5d0ab22349e8bc00cc08accceeaa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.0 MB (584004113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9e32a9051edeb75953c6fc87637e41f70642529ea5ff3cf278af602fbf210d`
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
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Nov 2024 00:13:30 GMT
WORKDIR /home/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_VERSION=8.11
# Wed, 13 Nov 2024 00:13:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER gradle
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER root
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6136b1d5218335321eb2909473a0ec39e775b534e171f4a4a9ebe4ca7c0f9c9`  
		Last Modified: Wed, 13 Nov 2024 02:08:05 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5851a35dbc0422fd01ef396b85b6cdd939e99b00e303b652c3ea0a556cdb1`  
		Last Modified: Wed, 13 Nov 2024 02:08:07 GMT  
		Size: 126.4 MB (126421709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94562c1069bb70d9951d0e240662d6d9e693c82f80746acb78cbfb4eebb01a7f`  
		Last Modified: Wed, 13 Nov 2024 02:08:10 GMT  
		Size: 291.1 MB (291064063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30124dbe17bcfda4da0a0d17f157be2122a03aeec57340217f7180935932ce9b`  
		Last Modified: Wed, 13 Nov 2024 02:08:07 GMT  
		Size: 136.9 MB (136923410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c44336d2f570dc143d83af832e400f8b88ba8c0db82a1a3eb44698fc38d440b`  
		Last Modified: Wed, 13 Nov 2024 02:08:06 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:e9e458c656c7e660ad9186cd549dc5dcd4f343a0b9f45aeb6b8e0cafb8843271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9186889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbbb22b0816e0e380411a6022035abc0b28bba891d91508ceddb921e685bd31`

```dockerfile
```

-	Layers:
	-	`sha256:f43515c3ef742b59be18554522770897fa51c09a67262f2a51e7ee1a8f826d67`  
		Last Modified: Wed, 13 Nov 2024 02:08:05 GMT  
		Size: 9.2 MB (9154860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21209797d856130ee3781770abb9fc7ec623515b4b40fa147f4c6fd4eb1d7df1`  
		Last Modified: Wed, 13 Nov 2024 02:08:05 GMT  
		Size: 32.0 KB (32029 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8200b8e27b728c52e14085f07b6a841a722d5414573a78acebc43bc4c0d8ae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570322790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8260d8d7bff35ead1498a4b90a61f96f1df0a32540845e7449fc926a3d220cd`
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
# Wed, 13 Nov 2024 00:13:30 GMT
CMD ["gradle"]
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Nov 2024 00:13:30 GMT
WORKDIR /home/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 13 Nov 2024 00:13:30 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_VERSION=8.11
# Wed, 13 Nov 2024 00:13:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER gradle
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER root
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11196b4936e1bb43d24d5b3c735201e3ac221765499426a4a4646b89f370c8`  
		Last Modified: Wed, 13 Nov 2024 08:25:49 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071742355ead2080c6ab133df3fbc0900f8addf779400f9e0046db19eccc960e`  
		Last Modified: Wed, 13 Nov 2024 08:25:53 GMT  
		Size: 122.5 MB (122475229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86bde1fe1ad3980348fd8fc2b0f8afdb9a48032bd067a99082ea5fb3d3e8c7b`  
		Last Modified: Wed, 13 Nov 2024 08:25:56 GMT  
		Size: 283.5 MB (283501927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4a962a85e559e429fb57890f10ca1f5c7df45208a780f6172c04c39d338ef6`  
		Last Modified: Wed, 13 Nov 2024 08:25:53 GMT  
		Size: 136.9 MB (136923436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded2ef7da9d4901f3eea4b93f24a16790a8b6d7956e4a312f97c61f395222c51`  
		Last Modified: Wed, 13 Nov 2024 08:25:50 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:8b14f259d4637c2a9b5e83b0a6ff67b9846f69b7a40224f46366595fc9ac533d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9156237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff795777e727f770f5b5f559cac2387940163d5c51c1df270db6f3fbe32a081`

```dockerfile
```

-	Layers:
	-	`sha256:4537741fc25d9141afd7076e0e91069e1a5025aed0cf9237e681ee4f98df5644`  
		Last Modified: Wed, 13 Nov 2024 08:25:50 GMT  
		Size: 9.1 MB (9123804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e2e733dacd9731f7a438e3a74e08db140d3a7f3e9833620a9b4f82f53fc23a`  
		Last Modified: Wed, 13 Nov 2024 08:25:49 GMT  
		Size: 32.4 KB (32433 bytes)  
		MIME: application/vnd.in-toto+json
