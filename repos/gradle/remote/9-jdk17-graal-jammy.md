## `gradle:9-jdk17-graal-jammy`

```console
$ docker pull gradle@sha256:d703991e8fe9851a72b4a4a5667e38bc2a1bfc395519bd18b12b06b21bb8b343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:e0574a55f443b24d2c524025b893abd0c180f731c422e13c96fdc395ca23b478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.4 MB (585376246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87673cb2b8e1551e9295996762db4216d714d117d1f6d352d071bfe3f2fc27d5`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:35:46 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 20:35:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 20:35:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 20:35:46 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 20:35:47 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 20:36:16 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 20:36:16 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 15 Apr 2026 20:36:16 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 15 Apr 2026 20:36:26 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 15 Apr 2026 20:36:26 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 15 Apr 2026 20:36:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 15 Apr 2026 20:36:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 20:36:28 GMT
USER gradle
# Wed, 15 Apr 2026 20:36:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 15 Apr 2026 20:36:29 GMT
USER root
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863567381a1056f573b79a366eee5806e8c22bc8914b0a9993069a2a65dcedb8`  
		Last Modified: Wed, 15 Apr 2026 20:37:01 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbb7f396bc718b6bb9a518d8c933e56574194b9433a4ddfd413d5b451a7cf8d`  
		Last Modified: Wed, 15 Apr 2026 20:37:08 GMT  
		Size: 126.7 MB (126737370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d143dfb0f9fd78d5b1b1110e772223029eb24967f934210790a374e516ee21f`  
		Last Modified: Wed, 15 Apr 2026 20:37:12 GMT  
		Size: 291.1 MB (291064099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457bbb1092d08afb789ea7e7e08b8b71b8ff56a89356ef6970351f2ac5fd190`  
		Last Modified: Wed, 15 Apr 2026 20:37:09 GMT  
		Size: 137.8 MB (137808328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73db9575f9ff5b92497c19f55464967f83bb3a4b9cc1250e961c321ad2187fe`  
		Last Modified: Wed, 15 Apr 2026 20:37:01 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:e337b6772cd35273d381f605c47dd7d4518e5b5be149464f294d48dda4d676b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9416701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd436f7e2e6dab00c07145db052dfaa058e3f2b0f09616f9942b74c7eff0d50`

```dockerfile
```

-	Layers:
	-	`sha256:bccc3c243b0f342ff1571d4ab8b1a92ebbcb3a3eb2715d429f549fbd95ac9a57`  
		Last Modified: Wed, 15 Apr 2026 20:37:01 GMT  
		Size: 9.4 MB (9389144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb1614adc93f049c842e055c7d30ee8030880913315f4356abfc71cdc4ea9eb`  
		Last Modified: Wed, 15 Apr 2026 20:37:01 GMT  
		Size: 27.6 KB (27557 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:088210ad5988f4199d860abed95d402f848eff839ecd749a9cc7ea39ffa86178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.8 MB (571838363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def8a2999c95eec76eb94a817cf077754498d3aaf221929af79e736fd8f23517`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:36:01 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 20:36:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 20:36:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 20:36:01 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 20:36:02 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 20:36:37 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 20:36:37 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 15 Apr 2026 20:36:37 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 15 Apr 2026 20:36:48 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 15 Apr 2026 20:36:48 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 15 Apr 2026 20:36:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 15 Apr 2026 20:36:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 20:36:51 GMT
USER gradle
# Wed, 15 Apr 2026 20:36:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 15 Apr 2026 20:36:51 GMT
USER root
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9768e1e0321606787b915fd3478c9bfec31b0365c3a0c632ecc917f6d0a197e0`  
		Last Modified: Wed, 15 Apr 2026 20:37:23 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b56046d92987f933e8588b82be325ec3c33ac3b9bac49cfe6eb9ca23d9c75b`  
		Last Modified: Wed, 15 Apr 2026 20:37:31 GMT  
		Size: 122.9 MB (122887867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0fd2b126224b6cbf2f7fe61db166578b05b284d20bee66e2c689ad1c05c3ed`  
		Last Modified: Wed, 15 Apr 2026 20:37:34 GMT  
		Size: 283.5 MB (283501946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208fdeaa3a1931a2cbd86f26dfc89a81c8dcb163d4ea4ee0f5a57cdb2bd305df`  
		Last Modified: Wed, 15 Apr 2026 20:37:31 GMT  
		Size: 137.8 MB (137808330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e791b9f2e61185facac95b2c8efb72696c50116ce7d4eb35af97061e7a7ca38`  
		Last Modified: Wed, 15 Apr 2026 20:37:25 GMT  
		Size: 29.3 KB (29331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:8dac9774d4eeddc6cb42c63498faad97b4a7e618e84915a7af9ebcb7d2b441df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9385621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a907647f50fa4c02b8a7b26fb80f77269bf5a19b240b38e3ca14b3cb20ff38af`

```dockerfile
```

-	Layers:
	-	`sha256:102a84fd8100b28747a471c88994246701e0369cca18021cda31abbe010624b2`  
		Last Modified: Wed, 15 Apr 2026 20:37:24 GMT  
		Size: 9.4 MB (9357900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f78be8ec93cd89289e57fea536ceedf4ce0e7add0e22ec90b6655f44d148245`  
		Last Modified: Wed, 15 Apr 2026 20:37:23 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json
