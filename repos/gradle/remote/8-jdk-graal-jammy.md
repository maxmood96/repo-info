## `gradle:8-jdk-graal-jammy`

```console
$ docker pull gradle@sha256:cc0d2372b0d22fce33980687f71a0adaa19b8e587903f0906fc3652aa89168e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:4dd33f9ec90baf6824f5e15f3151fcfcf89527ea3df4dd59819887729ed3540b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583515551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790f6c1d8ea80fb937596acd2b4537a74bfd8a66dd18c5a8c1b49fc1a764a67e`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:23:02 GMT
CMD ["gradle"]
# Thu, 13 Nov 2025 23:23:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 13 Nov 2025 23:23:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 13 Nov 2025 23:23:02 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 13 Nov 2025 23:23:02 GMT
WORKDIR /home/gradle
# Thu, 13 Nov 2025 23:23:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 13 Nov 2025 23:23:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 13 Nov 2025 23:23:29 GMT
ENV JAVA_VERSION=21.0.2
# Thu, 13 Nov 2025 23:23:38 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 13 Nov 2025 23:23:38 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 13 Nov 2025 23:23:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 13 Nov 2025 23:23:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 13 Nov 2025 23:23:41 GMT
USER gradle
# Thu, 13 Nov 2025 23:23:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 13 Nov 2025 23:23:41 GMT
USER root
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87ce04f1d9892c33dd1187ec5d41c50a4324d59e68183d3ec78624eac35656b`  
		Last Modified: Thu, 13 Nov 2025 23:24:34 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cfcc62854763b31a1c170fbafba3bed91c611e545a6fe017286d9739f030f3`  
		Last Modified: Thu, 13 Nov 2025 23:24:43 GMT  
		Size: 126.5 MB (126538204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a0a3561439a32eacf0da8df553a1c48b2e37e441faa6556ec4130eeab60752`  
		Last Modified: Thu, 13 Nov 2025 23:24:27 GMT  
		Size: 290.0 MB (289986106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adff9191975fd1016995c474c157f8ad61d35a9a7539b45bdc1760e6d2709289`  
		Last Modified: Thu, 13 Nov 2025 23:24:23 GMT  
		Size: 137.4 MB (137395202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe88c7a99e07ca58a905a94078bcd8b95628e8debf1074d5abb7c403af7c803`  
		Last Modified: Thu, 13 Nov 2025 23:24:34 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:5dec93a5260de574cab768373eab953f22fd42bbd072a92e6400f0efe0510d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9411025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1d0473c695a3acf42a0026a8877ce8195633f3227a3121fb32460a9992cd03`

```dockerfile
```

-	Layers:
	-	`sha256:c6d8541684ecb6ffce0e7055dad585a14a2ea663a04fe031ecfde00c6037b5af`  
		Last Modified: Fri, 14 Nov 2025 03:25:57 GMT  
		Size: 9.4 MB (9382078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f689bda3b4ccca020cdadcf767fe6495d83f5cf05e50a422eae2dca104d9a0`  
		Last Modified: Fri, 14 Nov 2025 03:25:58 GMT  
		Size: 28.9 KB (28947 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d0e51de691824f41dff18e9dee951c1b4c6f080e519043039a402167b2ae2193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.1 MB (569144278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70a453536f9dc3ea9c539ffb0cff1c7750b07268c10ddcefff9a243bb6193bb`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:22:53 GMT
CMD ["gradle"]
# Thu, 13 Nov 2025 23:22:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 13 Nov 2025 23:22:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 13 Nov 2025 23:22:53 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 13 Nov 2025 23:22:53 GMT
WORKDIR /home/gradle
# Thu, 13 Nov 2025 23:23:21 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 13 Nov 2025 23:23:21 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 13 Nov 2025 23:23:21 GMT
ENV JAVA_VERSION=21.0.2
# Thu, 13 Nov 2025 23:23:30 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 13 Nov 2025 23:23:30 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 13 Nov 2025 23:23:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 13 Nov 2025 23:23:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 13 Nov 2025 23:23:33 GMT
USER gradle
# Thu, 13 Nov 2025 23:23:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 13 Nov 2025 23:23:33 GMT
USER root
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af22a9ee974ffe39396477aa03334b0a71d2e1590d5f25c0baf8276f0ffb1b2f`  
		Last Modified: Thu, 13 Nov 2025 23:24:20 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c261ede4f6483fb76b5d05aae026ec48418bdf71a435314a0c2458f498e366a6`  
		Last Modified: Thu, 13 Nov 2025 23:24:31 GMT  
		Size: 122.6 MB (122634917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d30d47221580496727ed41a972fe284a4cc5c2b9198fa0a64d211da9b52abc`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 281.7 MB (281666420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945efc5f1aff9874a61befbb63651bb053dc07e5ff6773d7ec8c30be11dd3e3b`  
		Last Modified: Thu, 13 Nov 2025 23:24:13 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70364980ec220979a34ccd17aeeaf086dbdf1320bb12eb28aae7a38a1a790c8d`  
		Last Modified: Thu, 13 Nov 2025 23:24:21 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:8afee9983edacd3d3e65660e6256df9d0edba93939c33824c85417099ffb12f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9380070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb54a67f1fbe9eac7bd59d250c8717ee6350fcbd908745f97996bd0bf0783002`

```dockerfile
```

-	Layers:
	-	`sha256:475b1aa865ebb9f7d06878b622c0fc2f7edf0336d2536799d0964ce15a8e4012`  
		Last Modified: Fri, 14 Nov 2025 03:26:05 GMT  
		Size: 9.4 MB (9350898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23b33eb4b78af66a13bb60c41b2b21389cd6c620ff9a811a3e769ec3da4e9ff6`  
		Last Modified: Fri, 14 Nov 2025 03:26:06 GMT  
		Size: 29.2 KB (29172 bytes)  
		MIME: application/vnd.in-toto+json
