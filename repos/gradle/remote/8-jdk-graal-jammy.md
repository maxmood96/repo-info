## `gradle:8-jdk-graal-jammy`

```console
$ docker pull gradle@sha256:c4825e162af80a8e2062be617f77f6f8f88535a57eb81cca033794bec4a22be8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:fbe6406aba51f40a0a8622440618196dd3243d10606603e70bf4431acb68c5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584588886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005e7be840f8275495f5ac1d2db5596f28eb9868c5c7095dc8afe5cc6c0cfb44`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:33 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:16:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:16:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:16:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:16:33 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:16:57 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:16:57 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 15 May 2026 21:16:57 GMT
ENV JAVA_VERSION=21.0.2
# Fri, 15 May 2026 21:17:06 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 15 May 2026 21:17:06 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 15 May 2026 21:17:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 15 May 2026 21:17:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:17:09 GMT
USER gradle
# Fri, 15 May 2026 21:17:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:17:09 GMT
USER root
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3455f8a1d348adc5fd19f2e44b9d0a34540138216e63647888fb207aa76550`  
		Last Modified: Fri, 15 May 2026 21:17:42 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf03e37f55ccc9931a21523f9c07fe3a6655d0d433bdc926f61c5133c5705939`  
		Last Modified: Fri, 15 May 2026 21:17:49 GMT  
		Size: 126.7 MB (126737541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61b750d80536485882431b7a65eda18bb3a3cdbb22f38b9095b7a24f2f6e596`  
		Last Modified: Fri, 15 May 2026 21:17:53 GMT  
		Size: 290.0 MB (289986836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e90331db781dc7e7bb417908e38dca88efdcd0055c0f868aef5f9ef1c69b25a`  
		Last Modified: Fri, 15 May 2026 21:17:50 GMT  
		Size: 138.1 MB (138068579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8beb5866d4a61aa9246b580a8be1b2a4d62d6b4b0ec962a8b9deacbcd460e9b`  
		Last Modified: Fri, 15 May 2026 21:17:43 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:58c1c5ecf7ef2d8082a36619d6974ca6e48ff5321fc21d109c228459aa24a219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9411129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6dc73c4deee641b587c810c662fa4884635c990b284d98d71c8884b69143f3`

```dockerfile
```

-	Layers:
	-	`sha256:6d0b189bcb42d56d275d53c653db32e0919d6903ac2109daa92b36e7ef050831`  
		Last Modified: Fri, 15 May 2026 21:17:43 GMT  
		Size: 9.4 MB (9382058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:552d7e841732f379e61c1469510974b54b2042bce09c4a8e2097b14774e69a05`  
		Last Modified: Fri, 15 May 2026 21:17:42 GMT  
		Size: 29.1 KB (29071 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c50c107cf5196f84a134117f4562578d392a2c33aa3016d354672ca0ec86d210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570274817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3feaf289ec33872ea0a8b332fa37fc4748aac32671cde805a4036a8c63514c7d`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:49 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:16:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:16:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:16:49 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:16:49 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:17:21 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:17:21 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 15 May 2026 21:17:21 GMT
ENV JAVA_VERSION=21.0.2
# Fri, 15 May 2026 21:17:30 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 15 May 2026 21:17:30 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 15 May 2026 21:17:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 15 May 2026 21:17:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:17:33 GMT
USER gradle
# Fri, 15 May 2026 21:17:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:17:33 GMT
USER root
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff55b15fd9eb15d0c80d12e8a4c52d93f147dd74c22615cfb6aea96928549fc`  
		Last Modified: Fri, 15 May 2026 21:18:05 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b718e3a04f1426631246402ef09743550cab7ff96b08b21b653c3a8e9b18de5b`  
		Last Modified: Fri, 15 May 2026 21:18:11 GMT  
		Size: 122.9 MB (122869566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949a2d9e5eb4c33778966334d75cdd607d8112951b4521aa9adfa3b738c621b4`  
		Last Modified: Fri, 15 May 2026 21:18:14 GMT  
		Size: 281.7 MB (281666221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100a0c50bb8c03acafd1c1270c86ad808d009cae18db756076f0af62eb35ab2a`  
		Last Modified: Fri, 15 May 2026 21:18:13 GMT  
		Size: 138.1 MB (138068535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23425d950daa0699bddb2020992d16bd315dc345d113294f979a699ff7cc9e12`  
		Last Modified: Fri, 15 May 2026 21:18:06 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:7cf634dc9c86b3a3e54c674cb47cb5e1256b60f0cecebe1f083e860a0af385c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9380173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191ee5db6fe18aa7d3e22f69630857e79127e0a0803b81ea3061c1c8a622df94`

```dockerfile
```

-	Layers:
	-	`sha256:80ad8db6269d7ad8b683238f4643d8012334a4e358de8d36f868f4e336aea616`  
		Last Modified: Fri, 15 May 2026 21:18:05 GMT  
		Size: 9.4 MB (9350878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3e854f9894d05dbc9f45de90ca65299a6f574e1be66844f396667f39eecc4d`  
		Last Modified: Fri, 15 May 2026 21:18:04 GMT  
		Size: 29.3 KB (29295 bytes)  
		MIME: application/vnd.in-toto+json
