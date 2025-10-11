## `gradle:9-graal-noble`

```console
$ docker pull gradle@sha256:a8d80a73f5a1633dbc29a65e4cf583f13ea9060319b87cadb32ab407a1778957
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:7789119d1c7cb91a3f59252635bad7c6c5576d19d88a123d0be58f9e8af7c2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.5 MB (653493138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75973eb9d9a1489b63185bca638cd3ac1fd96fa3460ad17e0260d6a891c500b`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 30 Sep 2025 09:31:25 GMT
ARG RELEASE
# Tue, 30 Sep 2025 09:31:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 09:31:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 09:31:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 09:31:25 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_VERSION=25.0.0
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=1862f2ce97387a303cae4c512cb21baf36fafd2457c3cbbc10d87db94b89d3dd     && GRAALVM_AARCH64_DOWNLOAD_SHA256=6c3c8b7617006c5d174d9cf7d357ccfb4bae77a4df1294ee28084fcb6eea8921     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf13a9f8b5fa15537c1c1275f1f91cfc887ea57e1d6ec1adaa2b2777de0f103`  
		Last Modified: Thu, 09 Oct 2025 21:16:09 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca29de4fd9457ac2c1c80b87af2111102d77810493f6e3d01b88e3200507e56`  
		Last Modified: Thu, 09 Oct 2025 22:28:29 GMT  
		Size: 148.6 MB (148628500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dd470daf593656c9567342fecea32d51ef4e169743559cf2779aa0732085dc`  
		Last Modified: Thu, 09 Oct 2025 22:18:47 GMT  
		Size: 340.6 MB (340570531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96556e2998195ab8431bf77057d03b3395776353b350d432afe2d06c8da76715`  
		Last Modified: Thu, 09 Oct 2025 22:18:26 GMT  
		Size: 134.5 MB (134514745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2511702431d6c2594d28ab5ffdf828ca59a151879accd381e702fdcfa6502fd0`  
		Last Modified: Thu, 09 Oct 2025 21:16:08 GMT  
		Size: 54.9 KB (54896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:103b2bdb312dc3282421b8bf9e203287aef3c463f39b7c18b209ba262ccf2055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9056698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f40a9a172aac13b7119d464a295f0c2c600ec26663737620cc92c0bde3ea8d`

```dockerfile
```

-	Layers:
	-	`sha256:b0cf84e4993125937554cf65fc901dac413630836e1a6ca227436aef81aa0bcf`  
		Last Modified: Thu, 09 Oct 2025 23:24:34 GMT  
		Size: 9.0 MB (9022764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0b4b2418834b7b3aaf116329ab23a9b463f7acd9f182bdb45cece274a6d69d7`  
		Last Modified: Thu, 09 Oct 2025 23:24:35 GMT  
		Size: 33.9 KB (33934 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:64a1309d69d7c3cea7056f7a55464c220a174de4317e04862898f18f74424110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.8 MB (622801999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b5b91f31cab9fe6ac8e395d6d668ba7fb94ff44cb72d25d5108cf6841ea34b`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 30 Sep 2025 09:31:25 GMT
ARG RELEASE
# Tue, 30 Sep 2025 09:31:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 09:31:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 09:31:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 09:31:25 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_VERSION=25.0.0
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=1862f2ce97387a303cae4c512cb21baf36fafd2457c3cbbc10d87db94b89d3dd     && GRAALVM_AARCH64_DOWNLOAD_SHA256=6c3c8b7617006c5d174d9cf7d357ccfb4bae77a4df1294ee28084fcb6eea8921     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cb43f23e9cfddfae81efc4f90e5d128c2c064f2cbcc23271270b3adef90f10`  
		Last Modified: Thu, 09 Oct 2025 21:16:17 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650b44e63b7dcd3f84a27bb8bc207eedd3dee320043b1f26da76fcdda9bab0e1`  
		Last Modified: Fri, 10 Oct 2025 04:37:00 GMT  
		Size: 143.7 MB (143736844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b3be2df1fdc2d572de5e06346e5e2ff78817dcce9f565e266d562199e9e37`  
		Last Modified: Fri, 10 Oct 2025 04:37:56 GMT  
		Size: 315.6 MB (315627952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9baf56f9d6760bd1bc072c1121b9dbc37f2b2d749aae783502594f9ae60ec1e`  
		Last Modified: Fri, 10 Oct 2025 04:37:52 GMT  
		Size: 134.5 MB (134514660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf9825eac4e54d4ed7acfe62f31481daf810e03f701ecab5ad7f104f4ce1459`  
		Last Modified: Thu, 09 Oct 2025 21:16:17 GMT  
		Size: 59.5 KB (59513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:5f4478ad2c7140fdbc7004947b1ec274b83934da883a73ba05485fdedc8c4a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9052242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f64f4e032da0fe51457f727438c188c37ac5bdd1b1331f1cbf921f57f6b6869`

```dockerfile
```

-	Layers:
	-	`sha256:b932d37081d8a7f359f138957de47adf3a4345cfc28680a2a78ac245263b08a5`  
		Last Modified: Thu, 09 Oct 2025 23:25:10 GMT  
		Size: 9.0 MB (9017904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb96239530fe054fdb8f2aef00884c5eac42cbc988870809be2069db427591b`  
		Last Modified: Thu, 09 Oct 2025 23:25:12 GMT  
		Size: 34.3 KB (34338 bytes)  
		MIME: application/vnd.in-toto+json
