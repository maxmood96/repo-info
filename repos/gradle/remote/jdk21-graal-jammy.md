## `gradle:jdk21-graal-jammy`

```console
$ docker pull gradle@sha256:901ad10ef63c2d30e3dbbfc2c37d9a0cad01531be840b222cf43a4695b367b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk21-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:4c14d730bf47d99525dfd8935fbfb67ac0f76f31aaed87b37840bd7c186ed13b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578792395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df79e7a2858fb2118b624237da6b8d3c561360c79eade08fe09725d9c290f0a8`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:41:22 GMT
CMD ["gradle"]
# Wed, 17 Jan 2024 07:41:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 17 Jan 2024 07:41:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 17 Jan 2024 07:41:23 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 17 Jan 2024 07:41:23 GMT
WORKDIR /home/gradle
# Wed, 17 Jan 2024 07:42:06 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 17 Jan 2024 07:42:07 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 17 Jan 2024 07:43:04 GMT
ENV JAVA_VERSION=21.0.1
# Wed, 17 Jan 2024 07:43:19 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_DOWNLOAD_SHA256=5283EE48A61633F59A49ECDF0EF0AB4C5A8B006C16CE95209DF740BD2AEE73BF     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version
# Wed, 17 Jan 2024 07:43:21 GMT
ENV GRADLE_VERSION=8.5
# Wed, 17 Jan 2024 07:43:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Wed, 17 Jan 2024 07:43:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 17 Jan 2024 07:43:26 GMT
USER gradle
# Wed, 17 Jan 2024 07:43:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 17 Jan 2024 07:43:27 GMT
USER root
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16de0a720d53a335665e945f4b545e18c0d649a2cb63250ae16689a197f4e42`  
		Last Modified: Wed, 17 Jan 2024 07:48:33 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd0c9e1a0eec1007cbed2018eb35de24fc74edde39b125c65605703298df179`  
		Last Modified: Wed, 17 Jan 2024 07:48:51 GMT  
		Size: 126.4 MB (126411524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20da237c370e5aef20f5cf93ecab136e526a2b3f6492adafccceaa873664112`  
		Last Modified: Wed, 17 Jan 2024 07:50:41 GMT  
		Size: 289.4 MB (289384556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423832568d79f6ad8618b0b0f8431404cae7acdc8a0c4488c3bd32b7b357fc3c`  
		Last Modified: Wed, 17 Jan 2024 07:50:25 GMT  
		Size: 132.5 MB (132544672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4064e0da4008636a72ab29bedb969f2d5f2ad8a5cc672c2d7b84c7ee73348b7`  
		Last Modified: Wed, 17 Jan 2024 07:50:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
