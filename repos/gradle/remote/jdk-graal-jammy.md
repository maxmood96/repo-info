## `gradle:jdk-graal-jammy`

```console
$ docker pull gradle@sha256:67eaeb2ffd6d08ad73950b4d86d4e3c6088828902e93a7d37ee622957ae67f3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:3f123b077885c935f64bb8fe5d0414adead97093d68acf03ccd674e6be58acdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.0 MB (582975029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d23ea6ff3be205f644ecf10e49e7143cee531b574d0521e5b4a36430aeae50`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Mar 2025 21:20:39 GMT
ARG RELEASE
# Thu, 27 Mar 2025 21:20:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 21:20:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 21:20:39 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Mar 2025 21:20:39 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Thu, 27 Mar 2025 21:20:39 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 21:20:39 GMT
CMD ["gradle"]
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 27 Mar 2025 21:20:39 GMT
WORKDIR /home/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 27 Mar 2025 21:20:39 GMT
ENV JAVA_VERSION=21.0.2
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_VERSION=8.13
# Thu, 27 Mar 2025 21:20:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER gradle
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER root
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acb240e89498a5413b00641681a52f6e86ba89a57ea98770abdac95c39eafdb`  
		Last Modified: Wed, 09 Apr 2025 01:17:27 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa8b996488fb2279554ff396b7014ec7e1d4273bb30e75c4ba2dbd2904a5b2e`  
		Last Modified: Wed, 09 Apr 2025 01:17:29 GMT  
		Size: 126.4 MB (126408410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0aea3980e62a0472eac8249ad8af64115afb18acb45733a112d20a82dc870c`  
		Last Modified: Wed, 09 Apr 2025 01:17:33 GMT  
		Size: 290.0 MB (289986841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13770d022c5f841818ad7cad575942c72c6673d747dddbe5bacc200c7a4bf12`  
		Last Modified: Wed, 09 Apr 2025 01:17:30 GMT  
		Size: 137.0 MB (136988178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b894c40fd6dd22789822c3d7baedef7b131459cf1493812717c762e74711e3`  
		Last Modified: Wed, 09 Apr 2025 01:17:28 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:37b392f6c12d59531f67da710edc007e8366a55eca60846135164b9f8a78b6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9142370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cc760bd715ea15930fb51dc78951b8e377df7d58279777349c7fbafdce3390`

```dockerfile
```

-	Layers:
	-	`sha256:be31d731a83247885b42d11b6f77373c785beaceb97d26bfdd9e19b9ec93bc0b`  
		Last Modified: Wed, 09 Apr 2025 01:17:28 GMT  
		Size: 9.1 MB (9114170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e61a8773724c3781ecff64795ae3e9a76b3a8043852f739a9cb3bc3e221407`  
		Last Modified: Wed, 09 Apr 2025 01:17:27 GMT  
		Size: 28.2 KB (28200 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:23a3de13b6821e582148e841e9dd1facf62faecf0290aa29ec35b1dd95342ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.6 MB (572613286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6486441bef664b9e4009f1c09f5cbc8bf000b61b290f421178f10ffc9b16d4`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d406c588a0b7d6239ca09d12f957b9772c3561dfa4e7248c1645e5ffadafeda5`  
		Last Modified: Wed, 05 Mar 2025 22:50:09 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b914410e039d2c8574aad8f89ea90d80c3a3ded864e64204588e7a97564236b`  
		Last Modified: Wed, 05 Mar 2025 22:50:12 GMT  
		Size: 126.5 MB (126536813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552e780cca06c409b6b1e664c670fc309d68761da6c20d63db113486b82ae1a`  
		Last Modified: Wed, 05 Mar 2025 22:50:16 GMT  
		Size: 281.7 MB (281666234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e293fb3ef35097f0ce5f0dc8312da479b226dca753179600b7d54431c78fa33b`  
		Last Modified: Wed, 05 Mar 2025 22:50:13 GMT  
		Size: 137.0 MB (136988181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f31a8f01f244b76dd431f7dfc8aec22f3242e6894707827c4b029764f9017c3`  
		Last Modified: Wed, 05 Mar 2025 22:50:10 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:2c46f9e3f58f03ebe6a9403dd0df2b1f9c21984a75102d7fd450a69db18a0e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9110812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01873ff243319d68cbd67f25fdcab061c4ab94e60a6e5e182582f4c72acae632`

```dockerfile
```

-	Layers:
	-	`sha256:d17a5ce505d129799c302089c2e4a0e3fc1fe8d68e87b986fa34b6183a5dfbd7`  
		Last Modified: Wed, 05 Mar 2025 22:50:10 GMT  
		Size: 9.1 MB (9083374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3712c093795e574eae17d05cec00025b443c4dca3f38211698da47246164e1f2`  
		Last Modified: Wed, 05 Mar 2025 22:50:09 GMT  
		Size: 27.4 KB (27438 bytes)  
		MIME: application/vnd.in-toto+json
