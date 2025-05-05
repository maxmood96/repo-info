## `gradle:6-jdk8-jammy`

```console
$ docker pull gradle@sha256:02056ab0c5cb2a1fa516ccd7833b6493923fa4aef7710d11b542ee3cc180d344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:6-jdk8-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:1b31b31104621b9b1833e7f5bf229f5fb6a72d68101a0c1dadbce8600256354c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261505373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ee9ccf402528fe303497be19d7c7bcd596cb5f1a4ae9164f095d1564d38e39`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:19:35 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:19:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Mar 2025 18:19:35 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:19:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:19:35 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_VERSION=6.9.4
# Sun, 30 Mar 2025 18:19:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER gradle
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER root
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcf2be1e50b6eecd7de69e3e91446f571a921ebec66f1cbc9d6de19e4954ac`  
		Last Modified: Mon, 28 Apr 2025 20:07:45 GMT  
		Size: 16.1 MB (16146073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0d6d799645369cea7f9afb2cf27505b86b3759e66b963126773bddd95ad422`  
		Last Modified: Mon, 28 Apr 2025 20:07:46 GMT  
		Size: 54.7 MB (54721288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea6baef7d1a5fca3112d6c7468f6f470e8e5bc65e765b62e60f7796ee330d80`  
		Last Modified: Mon, 28 Apr 2025 20:07:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae24dc7af9228bb0183e25246ac49ab388e163a6b2941491289c9a59ef38662`  
		Last Modified: Mon, 28 Apr 2025 20:07:45 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44591326e8b310b0d5e415055b6200efb1c5f3f2379fe1500f43b614e05d058c`  
		Last Modified: Mon, 28 Apr 2025 21:09:08 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42b03978e38352acb4311d099f4bfc0e6e15117e1092938c33587c3b8f3f106`  
		Last Modified: Mon, 28 Apr 2025 21:09:10 GMT  
		Size: 53.0 MB (52970928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92fc52f684272e424fd008950ab2602fa0c9d2dae31d17d9571a449804384ad`  
		Last Modified: Mon, 28 Apr 2025 21:09:13 GMT  
		Size: 107.7 MB (107696666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316731e8b354fd00f7b8426064c0a146ae3ac8e5a1bdcb6cabc8e6597b5a04a9`  
		Last Modified: Mon, 28 Apr 2025 21:09:08 GMT  
		Size: 431.3 KB (431272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:c137eb1e88c5ee59d909c12e250f380f72adeb0334f69c6713dae85426e7cacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd939e373f4b83028426dcc277285cf6d3af8aef9af86cea1763179b075d91d`

```dockerfile
```

-	Layers:
	-	`sha256:6b5c83680d4b146c2d141345d466606b474233956b213d75bca4cff494d3e728`  
		Last Modified: Mon, 28 Apr 2025 21:09:10 GMT  
		Size: 7.5 MB (7450999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd3ac56622ca075dc6becc82dd6e70ce1130152642946b6d14925b8c33b8ced5`  
		Last Modified: Mon, 28 Apr 2025 21:09:07 GMT  
		Size: 22.3 KB (22295 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:02c4d4bf91ffe96d05103078f7b85e7ec66fa05ea4389a9a445ef6353a3eb41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253548827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8670b794b43ef1886db1acc5bb8a6e6c2f13334f802aff5c63fcecd3b523d9f4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:19:35 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:19:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Mar 2025 18:19:35 GMT
ADD file:0644b965bac173b3de427d73c19d20e4fb61d50785a17a303e350f86b7865f26 in / 
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:19:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:19:35 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_VERSION=6.9.4
# Sun, 30 Mar 2025 18:19:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER gradle
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER root
```

-	Layers:
	-	`sha256:bbd8385a156b4afe216eb6b84f86bc7178bca4ab42ae42bb98f3576ca9f4e17a`  
		Last Modified: Mon, 28 Apr 2025 10:43:57 GMT  
		Size: 26.6 MB (26640827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5c6526ad83b0e90b86594381e1de4dd2faa792f3f23545bc58fab21c751310`  
		Last Modified: Mon, 05 May 2025 16:36:29 GMT  
		Size: 15.9 MB (15890855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1227549b49406bdf1e7ee8c6e2e14a630d8abc84c182e443353a36ab071a36f8`  
		Last Modified: Mon, 05 May 2025 16:36:30 GMT  
		Size: 50.1 MB (50124147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab924c832f4d66bffec44c4e6e6490798bd73c8a33c87d7ada99692544c40c`  
		Last Modified: Mon, 05 May 2025 16:36:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbb2a5ba348a75859e4696496f3e039b3f1a19e4abd9a41be61c637be03bce7`  
		Last Modified: Mon, 05 May 2025 16:36:28 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47628fc366cc095abde72c0b5ca078c9cdcc4c2fac1c47dcf3304385596bcc29`  
		Last Modified: Mon, 05 May 2025 17:08:40 GMT  
		Size: 4.3 KB (4301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6e4f6b67e009f5e6888baf8abdf686d595abc2b833076f64fbd72649d2eb5a`  
		Last Modified: Mon, 05 May 2025 17:08:43 GMT  
		Size: 53.2 MB (53158299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e6c36de32fa3ea071997c50c724c03625451195993cea56ea8803d64ea682e`  
		Last Modified: Mon, 05 May 2025 17:14:18 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ed4a2775b0b91ab7647bf52e1310ce4306c155bd759c6fd601bb544765ed07`  
		Last Modified: Mon, 05 May 2025 17:14:14 GMT  
		Size: 31.3 KB (31267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:3381833f87e69d6cc1818deff4e87127ea78ed6659c31e16a0e82bbddc5cfdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4582aa81de33d14e28af1bbfd4f0e43d3a0dc37416b602e23a388dcaaee3e927`

```dockerfile
```

-	Layers:
	-	`sha256:184e68077005529b7a8b8fbd5150ee18b069c4857f3716b36b57bcbab109b109`  
		Last Modified: Mon, 05 May 2025 17:14:15 GMT  
		Size: 7.5 MB (7453753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8ff355c5177874f9dd7d95e4b57138b42a41ec22920bad0c91ee6a7c570fcb5`  
		Last Modified: Mon, 05 May 2025 17:14:14 GMT  
		Size: 22.4 KB (22427 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3bcb1afe921446bc576623cd5b8943776050cd3bf91a8483fd64ffbedfe530c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257838274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f88daafb8d3738233c98fc337644dd47bb3e31e6d6d892e7e3ab21c3cdc283`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:19:35 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:19:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Mar 2025 18:19:35 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:19:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:19:35 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_VERSION=6.9.4
# Sun, 30 Mar 2025 18:19:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER gradle
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER root
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d988c284109adb0ee08f6d6a95a152f6e364456e1a4853bb6c3ebc58c40f099`  
		Last Modified: Wed, 09 Apr 2025 06:58:01 GMT  
		Size: 16.1 MB (16059566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170bf64b07356b4f10f7d343f35df319a348f741ef64b11fac133c26d5f5e748`  
		Last Modified: Mon, 28 Apr 2025 20:07:43 GMT  
		Size: 53.8 MB (53833721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a4528e4bba6d12ec4efee3b6b8c85b80c55e18350db0904fceaaae99b8acb9`  
		Last Modified: Mon, 28 Apr 2025 20:07:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b1c054a3e19b59c6c32ac2781dbc4878d83606eaaf8cfce95e9a3dceb4f48d`  
		Last Modified: Mon, 28 Apr 2025 20:07:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381801e4cefe7571f9a055ceb529ca0611451c8af6dc4ff7a0acd4d4f108fa4c`  
		Last Modified: Mon, 28 Apr 2025 20:59:43 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8882cd67c323bf521299925a4f17b055dd2fdab4eacb34af7e7d12ac7422df98`  
		Last Modified: Mon, 28 Apr 2025 20:59:45 GMT  
		Size: 52.5 MB (52462290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd78dfbf3d56b70a69269cd2be802927327b5fee8f03d54b0c09d45d16f709`  
		Last Modified: Mon, 28 Apr 2025 21:03:55 GMT  
		Size: 107.7 MB (107696652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ba80db53675d1f0a6523a2e3593af3b3263a23beac7bd53b829e7628469bda`  
		Last Modified: Mon, 28 Apr 2025 21:03:52 GMT  
		Size: 425.0 KB (425030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:9f005e66324049b7b233a6b89cfcbc36dc02aed5fad55031120dd5591f2d0e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd35e83d8f26280e770aeb9bd2ed91a7473d9e4981249a90774e01fac83ea79`

```dockerfile
```

-	Layers:
	-	`sha256:9131431cfd634c123faad718a1498ef6b06fceb32fcbf95a6313c7b27fcfde3c`  
		Last Modified: Mon, 28 Apr 2025 21:03:52 GMT  
		Size: 7.5 MB (7457546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0eddd08ff269153b05daa86eab3110e3bf7241bf998fe8d2a037bfd767659f5`  
		Last Modified: Mon, 28 Apr 2025 21:03:51 GMT  
		Size: 22.5 KB (22470 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:653a143fd4714e9a96079e7ef29807bfeed3f2bb9dbc86b71f161af2ff6fccb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269012502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b7b6975591fd812bf6ae9683264a78ee75fa5db1a81e3aeb43c9b627909e49`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:19:35 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:19:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Mar 2025 18:19:35 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:19:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:19:35 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_VERSION=6.9.4
# Sun, 30 Mar 2025 18:19:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER gradle
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER root
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c38ec2b4ee36ca93f19596eb065a396e648e65a58e52db4e0886be5ded596`  
		Last Modified: Wed, 09 Apr 2025 04:35:13 GMT  
		Size: 17.6 MB (17617815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb0d98af307e249085faddd48e8f4aa5a6038ab49a805959004ee7023d96254`  
		Last Modified: Mon, 28 Apr 2025 20:09:05 GMT  
		Size: 52.2 MB (52168664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e426a38c46a4a8629c3a8aaae8362fae208327c2232380c5e258ae600ad76d6`  
		Last Modified: Mon, 28 Apr 2025 20:09:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a84d408fe9574fde5a2842729cbad669bf7584a830e945b27b5c9beb501c31d`  
		Last Modified: Mon, 28 Apr 2025 20:09:03 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236c73ced6acadf26c82263186f79bb1da505fe2cbe8284f75440f09d930112`  
		Last Modified: Mon, 28 Apr 2025 21:02:17 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d208fc339872eb854192e26774a087a718860ae14d15d04f3ea484764a68d42`  
		Last Modified: Mon, 28 Apr 2025 21:02:21 GMT  
		Size: 57.0 MB (57044896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2a69496fdb992da50e1cae80e7601cef407e6cc3796c2661a5e47ef731afbc`  
		Last Modified: Mon, 28 Apr 2025 21:10:04 GMT  
		Size: 107.7 MB (107696669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050fa88028c8d0ae2a3e24c296ef5556eb45e9a5c46da3ebad3b773a4d0d8602`  
		Last Modified: Mon, 28 Apr 2025 21:10:00 GMT  
		Size: 35.0 KB (34981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:ff36d82c67afdebd7c67c5afceb45a0efc3517f7b1dd09836a0644aa93e3fb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b02e834c5cb4fe3391d151dc2abbbaefeb34d5d5252f247fd562e59204c66fd`

```dockerfile
```

-	Layers:
	-	`sha256:6b216faa4b664db629692399584d955c13e6c31b77e4ec155fb908691d0396cc`  
		Last Modified: Mon, 28 Apr 2025 21:10:00 GMT  
		Size: 7.5 MB (7456880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5477df8fe5f4106fcb6a37d8ad643c3d88b3d59d4a99361b4903e70b7dcb2202`  
		Last Modified: Mon, 28 Apr 2025 21:10:00 GMT  
		Size: 22.4 KB (22357 bytes)  
		MIME: application/vnd.in-toto+json
