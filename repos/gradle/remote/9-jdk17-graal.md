## `gradle:9-jdk17-graal`

```console
$ docker pull gradle@sha256:0c14f5a67049e05ac05aa76c509256d1828d481ab306376f88f99e7593f3f53d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:b19615c6f118fd4836da12f78b024bbf1873cdd442f9383e997599e8971293d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.0 MB (605005278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d93f8f16879425438e79be682ac227cc18b847d6c74c061e5170a611494bfa`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Wed, 29 Oct 2025 17:34:31 GMT
CMD ["gradle"]
# Wed, 29 Oct 2025 17:34:31 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 29 Oct 2025 17:34:31 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 29 Oct 2025 17:34:31 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 29 Oct 2025 17:34:31 GMT
WORKDIR /home/gradle
# Wed, 29 Oct 2025 17:35:04 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 29 Oct 2025 17:35:04 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 29 Oct 2025 17:35:04 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 29 Oct 2025 17:35:12 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 29 Oct 2025 17:35:12 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 29 Oct 2025 17:35:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 29 Oct 2025 17:35:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 29 Oct 2025 17:35:14 GMT
USER gradle
# Wed, 29 Oct 2025 17:35:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 29 Oct 2025 17:35:14 GMT
USER root
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1d4170923f9a416a747d6c86c3f10ff4c7c40a681fe4ced6af6b817ce3df16`  
		Last Modified: Wed, 29 Oct 2025 17:36:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72308357e7b3e6f825bb3db1f8f40e059499655f0648c67e26ba649185638725`  
		Last Modified: Wed, 29 Oct 2025 17:35:57 GMT  
		Size: 148.6 MB (148640241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faee0fbef6ef50b889601f3414ee8dc992a5ea5be242df22e1770364a47242aa`  
		Last Modified: Wed, 29 Oct 2025 17:35:59 GMT  
		Size: 291.1 MB (291064024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e40658f149f2c6dc2b14a050287330bdc959a58177fbd8614a0768681b0c33`  
		Last Modified: Wed, 29 Oct 2025 17:35:56 GMT  
		Size: 135.5 MB (135521656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d953010c3afc7549e5b1eabddcb09180f44a66492a7e3ea97dfb0aa99c894444`  
		Last Modified: Wed, 29 Oct 2025 17:36:05 GMT  
		Size: 54.9 KB (54890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:897afffc0ab0ecf83dd4b96b4435780bc59de36e2b566ef9c5e4ec3c0935d92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9032709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0953a1cff6011cff347dad1a04daa02fbee088f35c436f54623a48fbcfc59e97`

```dockerfile
```

-	Layers:
	-	`sha256:392d0e76bdeebce44afc7a4e9b1e09a1d96070808e2ed24896e3ea6b5a656b43`  
		Last Modified: Wed, 29 Oct 2025 20:23:02 GMT  
		Size: 9.0 MB (9003706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:843e1f7f6c1f28436a2801914e956638663f5ccf98ae3ede9d52ea48adf0d0d5`  
		Last Modified: Wed, 29 Oct 2025 20:23:03 GMT  
		Size: 29.0 KB (29003 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:556168b1433a949103b13714b9f1f5a9121e3fb1bbac932670aaf55f5e1e14cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591685489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922dba36318619a62076605b30b87c2667a94043102552393779b4b133b6f1cf`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Wed, 29 Oct 2025 17:34:17 GMT
CMD ["gradle"]
# Wed, 29 Oct 2025 17:34:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 29 Oct 2025 17:34:17 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 29 Oct 2025 17:34:17 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 29 Oct 2025 17:34:17 GMT
WORKDIR /home/gradle
# Wed, 29 Oct 2025 17:34:54 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 29 Oct 2025 17:34:54 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 29 Oct 2025 17:34:54 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 29 Oct 2025 17:35:03 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 29 Oct 2025 17:35:03 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 29 Oct 2025 17:35:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 29 Oct 2025 17:35:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 29 Oct 2025 17:35:05 GMT
USER gradle
# Wed, 29 Oct 2025 17:35:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 29 Oct 2025 17:35:05 GMT
USER root
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f7b1121502c0e970f7c75542f41f07fa71d235723b16f2f2840236b62f1996`  
		Last Modified: Wed, 29 Oct 2025 17:35:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76cb4f62f3e8e254d739be77f4a2db3c6d65b8dcd4c73fae1f203d78f958319`  
		Last Modified: Wed, 29 Oct 2025 17:35:46 GMT  
		Size: 143.7 MB (143739467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50134f436556f2d8937f95b1ffd115d2cf9eddb3883fedf973644e3bedf9d217`  
		Last Modified: Wed, 29 Oct 2025 17:35:48 GMT  
		Size: 283.5 MB (283501813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f413b72c11b7e8c44f6893907fe5a8e0c3354adea61b5322a323d23a39793c4e`  
		Last Modified: Wed, 29 Oct 2025 17:35:46 GMT  
		Size: 135.5 MB (135521659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a842c568088c5e424d6e1ee59fe34a50ce3086713ea0958b2254e83457a5dd4`  
		Last Modified: Wed, 29 Oct 2025 17:35:54 GMT  
		Size: 59.5 KB (59517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:11182a58791d58900bb24fe873da579b98098f29ce8920e22d6988b50d67fc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9028502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2d0735b49563e8374a41cab8be71b570c01e188f1a9f7bbe1c4cab011ed5ca`

```dockerfile
```

-	Layers:
	-	`sha256:b6b985aa424d099069a6131ed4a62b9408c8ec5029478d806aa46db0a6e78bbb`  
		Last Modified: Wed, 29 Oct 2025 20:23:12 GMT  
		Size: 9.0 MB (8999287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a20a04f1967210eb81bdb02169f075769b44e2498e84575854653faf331d5cd`  
		Last Modified: Wed, 29 Oct 2025 20:23:13 GMT  
		Size: 29.2 KB (29215 bytes)  
		MIME: application/vnd.in-toto+json
