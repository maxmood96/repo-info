## `gradle:9-jdk21-graal`

```console
$ docker pull gradle@sha256:7060c07a823179688455c43cdc9d1c7b1dd890a5b1fb50f376761ad1d0f66f16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-graal` - linux; amd64

```console
$ docker pull gradle@sha256:ca1f1fb65b6f4528cfb6e1d87714172a65394c23b21a93fad812ab10b5ddcc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.4 MB (606373657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b3adf12c56e0141433f6d57a6799004d98fe96fd39f7a7d7f489d94fcc04a2`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:53:03 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:53:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:53:03 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:53:03 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:53:03 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:53:42 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:53:42 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:53:42 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 07 Apr 2026 01:53:51 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:53:51 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 07 Apr 2026 01:53:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 07 Apr 2026 01:53:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:53:53 GMT
USER gradle
# Tue, 07 Apr 2026 01:53:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 07 Apr 2026 01:53:54 GMT
USER root
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3421e00ed84a32bec04e2413cf4fe81311670ba7237cfbbbe151fe36c8afce75`  
		Last Modified: Tue, 07 Apr 2026 01:54:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476eff79a09602fa7e438c1d60b159159475d3c3cec12d24a95ab7e3bd5fc522`  
		Last Modified: Tue, 07 Apr 2026 01:54:36 GMT  
		Size: 148.8 MB (148819006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a919cb4450c9f25d24d2474cfd47304f4156b5a57a4bac6312c8c432803005fc`  
		Last Modified: Tue, 07 Apr 2026 01:54:38 GMT  
		Size: 290.0 MB (289985938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2d9865bc36393545891adadbf7f13d3c4c23e3c1649b3c2371c8c5819fdda5`  
		Last Modified: Tue, 07 Apr 2026 01:54:36 GMT  
		Size: 137.8 MB (137808327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7d9b51c3f247339150e25fe7a6b467c6c312b29f51dbcac806bf56acb492ab`  
		Last Modified: Tue, 07 Apr 2026 01:54:30 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:50b677d35158705079fc5c7d00fcb8e7c1cf469cbe6ac2f07fd956c9ad9feae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9001398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843a94b6389726bf3d6393d78841a7c6af342ab8b834d8f3fa2b66c08847c575`

```dockerfile
```

-	Layers:
	-	`sha256:04886f61891a148b707d0c3a64f1d6c0d6b4ca8bfe911d7a76324870cfa8adbb`  
		Last Modified: Tue, 07 Apr 2026 01:54:29 GMT  
		Size: 9.0 MB (8972450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ba9191cc87cf877097e94c41cb8a2c2d76fe5b1fa97e3f10a4182fe5780a039`  
		Last Modified: Tue, 07 Apr 2026 01:54:28 GMT  
		Size: 28.9 KB (28948 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:be7c53095e28e9dcbf10b3cae0fd52210f66b3234cbcfa959f0ffe3f6d4225ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.3 MB (592298228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925f33e039bef981be3b6d37049a38ef953f92d53d7f7d74c0a817ad2cb6a01f`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:56:31 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:56:31 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:56:31 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:56:31 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:56:31 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:57:05 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:57:05 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:57:05 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 07 Apr 2026 01:57:16 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:57:16 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 07 Apr 2026 01:57:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 07 Apr 2026 01:57:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:57:18 GMT
USER gradle
# Tue, 07 Apr 2026 01:57:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 07 Apr 2026 01:57:18 GMT
USER root
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d55ea8c3503af27ede52829d42b6d7586f7ab4ecedc907e81e69ff83af1bc38`  
		Last Modified: Tue, 07 Apr 2026 01:57:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fae00c68274786863144a3ec1540850bc90267912b5dc510ec369a0896daf4`  
		Last Modified: Tue, 07 Apr 2026 01:57:59 GMT  
		Size: 143.9 MB (143918874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85455d3f60c1b84bf712f00cd2e3082173bd1b00bac58d20b990bf3eecccbcf8`  
		Last Modified: Tue, 07 Apr 2026 01:58:02 GMT  
		Size: 281.7 MB (281666306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93e2412833d54117ed45b35d21e962f03c9d4a653589f425e8d120e9c61c88`  
		Last Modified: Tue, 07 Apr 2026 01:57:59 GMT  
		Size: 137.8 MB (137808327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa7730c9f83efb785b5be02b152fa576009cf87b4806317508f52afd2a791f`  
		Last Modified: Tue, 07 Apr 2026 01:57:53 GMT  
		Size: 29.3 KB (29328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:442335562d9d56e9b06a2843a84062cf986037b60389de19f08f6a89ecff3225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8997189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecac6e05beeb773402f8d6b071b9684a416f648845f6ebb80ebc854dfda2cdd`

```dockerfile
```

-	Layers:
	-	`sha256:0c671825ba5e11b8dc4f31dea98eb359ef426baebaeb89fa7ccb5890d09ad4ed`  
		Last Modified: Tue, 07 Apr 2026 01:57:53 GMT  
		Size: 9.0 MB (8968031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61099f30084b4cfaf5cbd494b7000381a02193df1f38ff270adab27244e4e616`  
		Last Modified: Tue, 07 Apr 2026 01:57:52 GMT  
		Size: 29.2 KB (29158 bytes)  
		MIME: application/vnd.in-toto+json
