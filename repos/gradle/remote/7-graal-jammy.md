## `gradle:7-graal-jammy`

```console
$ docker pull gradle@sha256:7705e1d01805e42c27446fa432105f8c5d9aa01d12ecaa78e5bf19707ecc1ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:972d49d3358af6bc7c169e03a178fc26f35175ebe504175d78869f7dd2b6a370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.7 MB (575683121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccba4c76f99eb4d053c2a9b7a1e7bb543236520ac5c646f29fd0919b4d059f5a`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=17.0.9
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f879215ef6319ad8ba15c6ca12e6979df1025e89e891f42601dc758badbdb3`  
		Last Modified: Tue, 02 Sep 2025 00:27:42 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bab99c57763ceced93028ffd224e5c34f92a2f29dac963781217da06afafee2`  
		Last Modified: Tue, 02 Sep 2025 00:27:55 GMT  
		Size: 126.6 MB (126553277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3f5df1f90486d482ee4addcd476a3cee5c4b07bc3935861805e738d3c3fd49`  
		Last Modified: Tue, 02 Sep 2025 02:25:51 GMT  
		Size: 291.1 MB (291064254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deab5e306ac7b32969ed7fd87b1563f3a54a41e9f2de2181f465fb309d524dd0`  
		Last Modified: Tue, 02 Sep 2025 02:26:00 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9536b41e83699e6284654264e1b0320bc23b72bf2f733a6eb26c07b275e7d98f`  
		Last Modified: Tue, 02 Sep 2025 00:27:42 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:16498cf47879b090703e6d05c12de948fede8e410de33d6c3cfb6f1f414abc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137818f8adeee799e4660e4e5a7959ccd4d43f57356bcd5eecb473c87bcb57bd`

```dockerfile
```

-	Layers:
	-	`sha256:14eaa6a99b6452cc0d00b755fb96fee1e8c1a582ef065546130b7bb5165e6d27`  
		Last Modified: Tue, 02 Sep 2025 02:18:58 GMT  
		Size: 9.3 MB (9315598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dafe75f133e97b9de409cd85da7b34b48671ffc9900dfc4b6b260f136e41438`  
		Last Modified: Tue, 02 Sep 2025 02:18:59 GMT  
		Size: 29.1 KB (29077 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:58f415f0187298ae2252671c3e4cba09dd7239ae4a4a6b5911b2cecf156dede0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562056658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6aa59f859ee2b715b278c69da3322391905d1d7524309023111dd7e51238f8c`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Sep 2025 15:37:00 GMT
ARG RELEASE
# Tue, 23 Sep 2025 15:37:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 15:37:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 15:37:00 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Sep 2025 15:37:00 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:37:00 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 23 Sep 2025 15:37:00 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 23 Sep 2025 15:37:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER gradle
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER root
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3846ebe76bd4e821503cacefdc4add97336d2f94a9cc3801330ddfe69b46df14`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d431378859af9c7243826f55ffccdd284524d5c8e1a1fab163b29dcde6e4c9`  
		Last Modified: Thu, 02 Oct 2025 01:21:30 GMT  
		Size: 122.6 MB (122638365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fed16c214332f65001ae0ace2034831aa2606a0898ea9f0a4f8d59950b157f`  
		Last Modified: Thu, 02 Oct 2025 01:21:34 GMT  
		Size: 283.5 MB (283501913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e96c974694017ddd68c8f345caa8ce8e77a4546b1dd603d39b140845a7e37c5`  
		Last Modified: Thu, 02 Oct 2025 01:21:30 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58d4b1bcf5e8ce918c6739ad99904bee016f428d0d8d658c922ce9daf64b68a`  
		Last Modified: Thu, 02 Oct 2025 02:04:31 GMT  
		Size: 59.5 KB (59515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:8ea1ccbe6b7f66d620ee656076cadee1e82e7daf48ad8fdefef552860505df9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9313715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8a445aaf43e218830c1ffa112926a21d7caa23e5d9542d28f842c51e0ee85c`

```dockerfile
```

-	Layers:
	-	`sha256:c8327d9fe5a9960669eff9f0cb7f6326b3b8ec274cc41aa376ffb11eafcfd541`  
		Last Modified: Thu, 02 Oct 2025 05:19:23 GMT  
		Size: 9.3 MB (9284414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d6e915f629518a01d0ff99d6e6c0c1f73fbb46503738243f6ed4ee6c1ca823`  
		Last Modified: Thu, 02 Oct 2025 05:19:28 GMT  
		Size: 29.3 KB (29301 bytes)  
		MIME: application/vnd.in-toto+json
