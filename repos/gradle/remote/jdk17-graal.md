## `gradle:jdk17-graal`

```console
$ docker pull gradle@sha256:779815c578b15936137582d51945d82dd55ee232ddac92764afe73bb1b9b4830
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:4e6acd865b7ed5d58e457a26646962df0614b51ec9ac8b000fea4f33668df0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.8 MB (583775330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7d2e788d81c4fb87050c4ea9e13f51456a4f8b8192d63635c8b6c33c9fe5db`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["gradle"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Aug 2024 06:00:50 GMT
WORKDIR /home/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_VERSION=8.10
# Thu, 15 Aug 2024 06:00:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER gradle
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER root
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b29dab5ea7ab5661f2f5eb5e6f0f00349fa6afe863720675301dfd066c5800`  
		Last Modified: Thu, 15 Aug 2024 17:59:23 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517d56b0d821739ae2b084ea9b2f32ca610d9e48ef951700aded0249ae3b9717`  
		Last Modified: Thu, 15 Aug 2024 17:59:25 GMT  
		Size: 126.4 MB (126389582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5652bd2c83492c6e783874dbf597dbfd255daa9f88210f2c98da02b90b19ed33`  
		Last Modified: Thu, 15 Aug 2024 17:59:27 GMT  
		Size: 291.1 MB (291064103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7355d233201eb09262fc915e4fc321f94076350f5bef073a0434208ffc2232cf`  
		Last Modified: Thu, 15 Aug 2024 17:59:25 GMT  
		Size: 136.7 MB (136728340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736213752a492cc5b974ddc4a2069de38d4ae79039f989547ce6217d9060cc2d`  
		Last Modified: Thu, 15 Aug 2024 17:59:24 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:600c5acae19d5d251fef96ee1cb23c5487a2dcb4c5909e9f7229522f1879ea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8738614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f042146aa05414a14a3680ba14bdc30c1eb6d77b4cf3145566259f06f6a8a772`

```dockerfile
```

-	Layers:
	-	`sha256:3a894321cecc354fb02a0d96bf9e0a1c7d87f35668b64cd684d3e7e544aa44bb`  
		Last Modified: Thu, 15 Aug 2024 17:59:23 GMT  
		Size: 8.7 MB (8706839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5b81fab09c7a27ebd42876b54e257a8c73581567fb7442ad96d5968564a7a6`  
		Last Modified: Thu, 15 Aug 2024 17:59:23 GMT  
		Size: 31.8 KB (31775 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:dfbf097f65f2f92678b54cdb35c9798715f9c192fdb31057897fb8c847f51a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.1 MB (570115499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580ddd123872c9398ead7f8545425923d60df1bfcd38127aeeb75ebb670fb221`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["gradle"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Aug 2024 06:00:50 GMT
WORKDIR /home/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_VERSION=8.10
# Thu, 15 Aug 2024 06:00:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER gradle
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER root
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afebaaaad32a669174efd9ba758e15ca0a65de1414ece0841ce39d34251014c3`  
		Last Modified: Sat, 17 Aug 2024 02:20:30 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0252fdf7ef52cdef41fcc48dfbf3dbb075614dd4a419a029e00aaacd6cc84f`  
		Last Modified: Sat, 17 Aug 2024 02:20:34 GMT  
		Size: 122.5 MB (122462567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f516dc565377d1207afa80ada07a34bb8098f80cb3a459ba2b53f3c338008030`  
		Last Modified: Sat, 17 Aug 2024 02:20:37 GMT  
		Size: 283.5 MB (283502045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476b28eced1d332bf7b05945cc6b866ca77f4b25e34ad38d59e3beab7c82ccb`  
		Last Modified: Sat, 17 Aug 2024 02:20:34 GMT  
		Size: 136.7 MB (136728339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8707b9accad6dd073061911a4a253ed4d076a662992982125bb3614c58be77b7`  
		Last Modified: Sat, 17 Aug 2024 02:20:31 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:57d83d2b12e4e05d2d50f3f1e82ef180435d39d23d2b14cd8b6e720cc876a3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8732502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0567ae91209983489911adf428e854898f010c403dfc8e66030ba5702d7e6834`

```dockerfile
```

-	Layers:
	-	`sha256:705beedbf449aeb4d9d24a61f89ecca338a9aa9f99488dee7ddc67890d245291`  
		Last Modified: Sat, 17 Aug 2024 02:20:31 GMT  
		Size: 8.7 MB (8700187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:278678dc97407924bb24d5ffbee02ae23137c5017fb40278439484407433d0f7`  
		Last Modified: Sat, 17 Aug 2024 02:20:30 GMT  
		Size: 32.3 KB (32315 bytes)  
		MIME: application/vnd.in-toto+json
