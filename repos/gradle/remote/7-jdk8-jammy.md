## `gradle:7-jdk8-jammy`

```console
$ docker pull gradle@sha256:24d721d6864d6b30a72c57c57a8269eace080631297be1af4ec1d5d876c4336b
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

### `gradle:7-jdk8-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:9c236af21f5dbeae39fd6f7eb3bd10a11e16c486923e2977a048cd091bc06698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279714918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9f8340c69ab116b922f2fdcf2601c4feac342fceceece6c56e9661f0d91172`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
ARG RELEASE
# Sun, 27 Apr 2025 20:21:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 27 Apr 2025 20:21:59 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Jun 2025 15:28:43 GMT
CMD ["gradle"]
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Jun 2025 15:28:43 GMT
WORKDIR /home/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_VERSION=7.6.5
# Wed, 04 Jun 2025 15:28:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER gradle
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER root
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2589b3c98f0015ba28d6da3f6a1951846d6f66c1f03d6e31dd4c0215f3101f`  
		Last Modified: Tue, 03 Jun 2025 13:30:56 GMT  
		Size: 16.1 MB (16146418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c768cbce2b07b93b907fef0a47898da4894ac81422ea8a5774c5787a7d2e76`  
		Last Modified: Tue, 03 Jun 2025 13:31:59 GMT  
		Size: 54.7 MB (54721257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214aa749b90778cd712b02013e92fb8a0ffc8e80f8683ed9d2eeedade97bf33d`  
		Last Modified: Tue, 03 Jun 2025 13:30:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99d3bf18543373561fc760e586b299a0226fd6c31786ac5747c6013d4da5d1`  
		Last Modified: Tue, 03 Jun 2025 13:30:56 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ac0bc0668a8d296c5638c3b94795c3838b6d8c140cd8a7c0498a6b6c27827d`  
		Last Modified: Wed, 04 Jun 2025 18:04:02 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9099f4d307dff08f7a31a659749f1c7b99d3121be95bf361823573f38e844b83`  
		Last Modified: Wed, 04 Jun 2025 18:04:12 GMT  
		Size: 50.8 MB (50782654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0ff202345dc200e87604e1d828223cbc5d54a8b3b49c9ea7c638671b255095`  
		Last Modified: Wed, 04 Jun 2025 20:31:34 GMT  
		Size: 128.5 MB (128469906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271dfddf50b5cd71a0f73d34ddf5b0fe27dd3826312001ea7e97c27fb0835e5b`  
		Last Modified: Wed, 04 Jun 2025 18:04:02 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:da91e37660f37d59f981b9c115dacc860597b87f6ecf09e39f27ef1afeaa5662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7538362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389798aea537824148072ec12ed49d5e6c32ceed12a079ed04d72fceb2eedb2f`

```dockerfile
```

-	Layers:
	-	`sha256:31b56077da2000728a83e7226cdf4b50a6f137fdb518529e59a1f29b101c0e4e`  
		Last Modified: Wed, 04 Jun 2025 20:19:17 GMT  
		Size: 7.5 MB (7514537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7999c3bfd8d93e896c4d5e5f686565795bdae61519d0d0b609f47eef4660fab`  
		Last Modified: Wed, 04 Jun 2025 20:19:19 GMT  
		Size: 23.8 KB (23825 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:13c1c1f64f2cd209471f1b8f8ab787c2624122d11cbe1c3f37a66ade33b453d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268690900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769a052291b65ee0fe280fa3ec38091cac9c119d6775f9b440b096f799c18ef4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
ARG RELEASE
# Sun, 27 Apr 2025 20:21:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 27 Apr 2025 20:21:59 GMT
ADD file:a68d8d0994670732edac30efcee96eec3850856e5c33c1c7fee7fdc59173ac3d in / 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Jun 2025 18:03:22 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:03:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:03:22 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 02 Jun 2025 18:03:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 02 Jun 2025 18:03:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
USER gradle
# Mon, 02 Jun 2025 18:03:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
USER root
```

-	Layers:
	-	`sha256:f35c50ead1843adba7d4d13281d31bc17c201a55b8bd1a3961e1bcfd131b762d`  
		Last Modified: Tue, 03 Jun 2025 13:42:56 GMT  
		Size: 26.6 MB (26640475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c869906112a22f8bcfcd7276bcc7d904f46535968a6e8d65eb57940c3ac442`  
		Last Modified: Tue, 03 Jun 2025 14:52:52 GMT  
		Size: 15.9 MB (15890981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb92e17db77649b2e9966ab72a3e8017929c3934a51883552eecfaf73cca2af`  
		Last Modified: Wed, 04 Jun 2025 01:00:49 GMT  
		Size: 50.1 MB (50124122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0e79694c6f93b9a692dc11ccae9ec592433af279a534650d04b69f16cb71cb`  
		Last Modified: Wed, 04 Jun 2025 01:00:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9b1883afd722a6ef042aeea6b3f8a2c7686b04c4b278525c2552c7c46259a1`  
		Last Modified: Wed, 04 Jun 2025 01:00:54 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a93cc83d3696df839cf9d5121dc59f00e76118c37729dba8170672a900d604`  
		Last Modified: Tue, 03 Jun 2025 05:20:34 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4df7f52435638f2b4488fa0130a2df5d8186c904f33ce2ce95252f0b3890b92`  
		Last Modified: Tue, 03 Jun 2025 05:20:36 GMT  
		Size: 53.3 MB (53266745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f020c0a1ee14f8005ced5b3c52a3863454871e72dc42cb9806d03002791a4e65`  
		Last Modified: Tue, 03 Jun 2025 05:24:11 GMT  
		Size: 122.7 MB (122730529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2797e61d583eb3bd974a82fbffc36c44d478ad862ac255950b9d81ebf8336935`  
		Last Modified: Tue, 03 Jun 2025 05:24:07 GMT  
		Size: 31.3 KB (31289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:891acd0c18f95a6d12ff35a090a898b6aa6b2ad281f7bd3b76b770a961c3cf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7535049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ab01a4f0d20c78d5c79a49bebd78079c5514c0786b0bd6d58a3c47dcdd5a49`

```dockerfile
```

-	Layers:
	-	`sha256:ffb4fd26a05044b0a7b2c33d4526d7060a13e2c3f8bc37d35f2436461debddad`  
		Last Modified: Wed, 04 Jun 2025 20:19:25 GMT  
		Size: 7.5 MB (7511093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3248c51cc45de05e6b239ccc65a8d4003641b96e3ae4f995025f3f92053ced19`  
		Last Modified: Wed, 04 Jun 2025 20:19:27 GMT  
		Size: 24.0 KB (23956 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9ae79c1e04f338b7641bc2a9040d100782aee9ef5c5cd2d5b1808a6828e21cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270374743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4c5c7d06f6958b384f61793f5d1b26a95c2338a7e12930cbdeaa739cf083cc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
ARG RELEASE
# Sun, 27 Apr 2025 20:21:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 27 Apr 2025 20:21:59 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Jun 2025 18:03:22 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:03:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:03:22 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 02 Jun 2025 18:03:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 02 Jun 2025 18:03:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
USER gradle
# Mon, 02 Jun 2025 18:03:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
USER root
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cfe0c2e8be99f8d950a6958a0c910d4d550d66bf0da03d2cb05a26a4ba8061`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 16.1 MB (16059839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa7e6721661644b410badf233b52acdc5ce44bccb8a03c4e7bf1ed3e2cd3480`  
		Last Modified: Tue, 03 Jun 2025 13:38:14 GMT  
		Size: 53.8 MB (53833676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199dc0076a55858a60007e9d117ba00a84f6ea72b8130dcb0ccc582231a8e505`  
		Last Modified: Tue, 03 Jun 2025 13:38:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc06c820b3485eae674f224801928330c00a9a5cd6d1673ae29508ef9180e091`  
		Last Modified: Tue, 03 Jun 2025 13:38:00 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ebe324668faf76f9d5b67c6ce2097db3e058f2f9ef24d97e50228ea84b6f14`  
		Last Modified: Tue, 03 Jun 2025 13:37:58 GMT  
		Size: 4.3 KB (4325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabea37013f33dd9ab32c3c72830cd74f43f166875e8f0e62a8e2fe8352b5186`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 50.3 MB (50328815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74abc8a10b6305390522b0277894c9226755dbe9de6380732a32483923a6c81e`  
		Last Modified: Wed, 04 Jun 2025 05:46:28 GMT  
		Size: 122.7 MB (122730526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cdcdc110ca8d0977020741aa2b2c9ba7cd9dd6633b90116aae02999c8ae16d`  
		Last Modified: Wed, 04 Jun 2025 05:24:06 GMT  
		Size: 59.5 KB (59514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:62bc8aba8ae887053ea0738e63c5d44c9dbb51fb7f0b64c55255dbc51fa69c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7538589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbf0c2a159f0091c3379c92b4f265b3ddfbb5bdc61de332f6e99385d742937d`

```dockerfile
```

-	Layers:
	-	`sha256:101af78ea3e7691fcc7e47b86c445fb651cc9d738ec8c5a587e9d679eb45238e`  
		Last Modified: Wed, 04 Jun 2025 20:19:33 GMT  
		Size: 7.5 MB (7514592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768fdacd1f1d888de8ccc1055d9098e1749ad7f6a69331feffb5c5c0f32025b2`  
		Last Modified: Wed, 04 Jun 2025 20:19:34 GMT  
		Size: 24.0 KB (23997 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:8ab5372db4808fefeffc07f9ac79217e33a69b4bf0f28b7d9beaf12ebfe76e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281751276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa824e2f3b674bd57eb914bd8780d8df243be72d52a48d53d86867773ea83fb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
ARG RELEASE
# Sun, 27 Apr 2025 20:21:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 27 Apr 2025 20:21:59 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Jun 2025 18:03:22 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:03:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:03:22 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:03:22 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 02 Jun 2025 18:03:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 02 Jun 2025 18:03:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
USER gradle
# Mon, 02 Jun 2025 18:03:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:03:22 GMT
USER root
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00de0e8a8949ec849c4e2d822052efc995cbfd8901f78e2be800be3fd9735154`  
		Last Modified: Tue, 03 Jun 2025 14:13:03 GMT  
		Size: 17.6 MB (17618370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1b641cc171e1687d997b7f6f2b89e9c24437cfaef8f0a8f5609e92c6c2c10`  
		Last Modified: Tue, 03 Jun 2025 15:28:50 GMT  
		Size: 52.2 MB (52168624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4a1edce742c7e651c02e9bac66fdfeb5d7841797b010477ae23b430ee2d1d`  
		Last Modified: Tue, 03 Jun 2025 15:28:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399f24cd581aba4871fe1b4e653a69858b7a481d2e8c2a220f485fa4c75721bc`  
		Last Modified: Tue, 03 Jun 2025 15:28:50 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8240a0287207a66d72428d10916e3e77a73b0141306282848692ca47b54ffe`  
		Last Modified: Wed, 04 Jun 2025 20:53:00 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81f7dbe55528b6e4fec27e0886769b915f32544e75feefc483c046c6dde0613`  
		Last Modified: Tue, 03 Jun 2025 06:47:47 GMT  
		Size: 54.8 MB (54751609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc4f8fb8a69b5f0dfb96a64ca6a2627802a17a9b1069dd1992f655549fb5995`  
		Last Modified: Tue, 03 Jun 2025 06:56:35 GMT  
		Size: 122.7 MB (122730530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d20182662ddb80d911cc96ba4ebcc47b1bb2e891af47fa57f603701549c08`  
		Last Modified: Tue, 03 Jun 2025 06:56:30 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:99a585a256452618d30ad3729d480b6ff743bd6ff0fb048abcb5d455b917fba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7538001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30c28f01dc1b5a3f8a699a20ad6751ee5c77f4cc711f2d63aee23e46e63fe59`

```dockerfile
```

-	Layers:
	-	`sha256:57893198a054ffce8ac55f383a3e345618746e33112e8fb50308fa25f113221d`  
		Last Modified: Wed, 04 Jun 2025 20:19:42 GMT  
		Size: 7.5 MB (7514114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2e1b914423bcd52780b4ff6447c206a919fc4e2b4aecf5a8e070738c73a98c`  
		Last Modified: Wed, 04 Jun 2025 20:19:43 GMT  
		Size: 23.9 KB (23887 bytes)  
		MIME: application/vnd.in-toto+json
