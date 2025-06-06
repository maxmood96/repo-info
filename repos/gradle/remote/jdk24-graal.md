## `gradle:jdk24-graal`

```console
$ docker pull gradle@sha256:1e223a99974d5bbe39cf3bce1d00c1c57d51cf405b4ecf038ec68319be4c7fc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk24-graal` - linux; amd64

```console
$ docker pull gradle@sha256:71b22420ed1d09c619ff30a65474d1e3d4fb935b99bde21a6277c004410e9fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.8 MB (651832519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb31ce47a35f4a64ccc30639865461287c5833b6b3fd6f8546e5b1d9b56e6d8`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 05 Jun 2025 16:04:16 GMT
ENV JAVA_VERSION=24.0.1
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=d2c544de672e400476a09c8f1da79ecc6b774a9441e234948542c3b3e6a84bde     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a3d1be8fadfb0d3df632252301f79a9b02b47e523da66539d370c62e683d762e     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea378672d1b559a43772d39b544760f2ebc8b3c34a8acd842ef88040653bf437`  
		Last Modified: Thu, 05 Jun 2025 20:08:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99afd69e1acb342ade1974418e4d2f86492f5c2620da5985cfc11537cec89099`  
		Last Modified: Thu, 05 Jun 2025 23:02:47 GMT  
		Size: 148.6 MB (148554266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23250f5c752f9dd03f99664cecc3404228238c84183127f404026f5eab07ca1d`  
		Last Modified: Thu, 05 Jun 2025 23:03:02 GMT  
		Size: 336.1 MB (336111193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1d52b30e9e8215044bcbc8d079368cfd835f6dec0e548f754e1170adb1228`  
		Last Modified: Thu, 05 Jun 2025 23:02:50 GMT  
		Size: 137.4 MB (137395505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193b87d6205e6e6f927a4cd2d7ac36dcdad58b1f0527daab7fbd50a95a7145ca`  
		Last Modified: Thu, 05 Jun 2025 20:09:01 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:ff0787ac9df1cbc267fb2c6fa74587a89e0082ac7c4a1db9239fc2138bd05f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8834221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1097e0c42a7388e2876df8896bfe0bdcec9661536c46a677d8e32a083d35e7b`

```dockerfile
```

-	Layers:
	-	`sha256:bffb8f70c93499ec9fd2a6096dbf39440d7535539b2113ca21c7ce2b6dea1e02`  
		Last Modified: Thu, 05 Jun 2025 20:21:51 GMT  
		Size: 8.8 MB (8805323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e75ca77fda1f8b6acefc849cf7c775b1f13461776b27358b87b586be6144e4a2`  
		Last Modified: Thu, 05 Jun 2025 20:21:52 GMT  
		Size: 28.9 KB (28898 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:aa7dff7634b1b94a721bb2338913797a4875e3ee7ff1ee109dde3301bdd18e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.3 MB (620276269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26c702d41bbe36d429594bf72b0424b06fc50df751c45679cb4a475ebabe47`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 05 Jun 2025 16:04:16 GMT
ENV JAVA_VERSION=24.0.1
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=d2c544de672e400476a09c8f1da79ecc6b774a9441e234948542c3b3e6a84bde     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a3d1be8fadfb0d3df632252301f79a9b02b47e523da66539d370c62e683d762e     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a084dbc9b7efa126554be6b387c36437dd79574d6672a7d118b4ec83c3f0d72`  
		Last Modified: Wed, 04 Jun 2025 05:33:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22900b68b25711552ba19e9c1d789101c568031c82e0d748f01f2ee09135990c`  
		Last Modified: Thu, 05 Jun 2025 02:21:05 GMT  
		Size: 143.7 MB (143678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9e695b1e88a3bad084d40f80a1059c47a75513f5b299602f3f34b8666cf1d1`  
		Last Modified: Fri, 06 Jun 2025 02:08:19 GMT  
		Size: 310.3 MB (310289982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b69c4f276fe01a5a1ed83eba21d9a9b72c52d4115d7e40dae7dc39f27a1226a`  
		Last Modified: Fri, 06 Jun 2025 02:08:09 GMT  
		Size: 137.4 MB (137395510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb826b3aaaa33be496f4c51eb40ad03b4459117b1b0b9578d35eadcd44637805`  
		Last Modified: Thu, 05 Jun 2025 20:27:56 GMT  
		Size: 59.5 KB (59536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:d157e92ae2f8680871946caaeb1f2049a187988d3b565c04ddff3f2a3355fe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cbace2b7375dc79d359972a7c3134702164b2206d9d5ff948bd63ca217dee8`

```dockerfile
```

-	Layers:
	-	`sha256:9bf4e2adc26ac8a2f4233ad682892000bca45ef65ec0ca44ca899fafc97ea571`  
		Last Modified: Thu, 05 Jun 2025 23:23:06 GMT  
		Size: 8.8 MB (8800254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8349e8d46959270488b0226a002e7b8ee143662b81c7bcb9dc47f9fb35b9438e`  
		Last Modified: Thu, 05 Jun 2025 23:23:07 GMT  
		Size: 29.1 KB (29110 bytes)  
		MIME: application/vnd.in-toto+json
