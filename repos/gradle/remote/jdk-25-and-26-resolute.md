## `gradle:jdk-25-and-26-resolute`

```console
$ docker pull gradle@sha256:657f2aab488284fe7cf038308368b13cdfea59fc79b29aa6fd2a4e1e334258cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:jdk-25-and-26-resolute` - linux; amd64

```console
$ docker pull gradle@sha256:2f622d60c39edbdceb3d56501c390cbbf67cde9a95c62dac9ea028cc1a5d8a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.0 MB (464001965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47b3bd12088431b7a384122476f94f221947b77b377010cdc482be1fa8f8709`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9106.tar --tag 26.04
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9106.tar
# Fri, 19 Jun 2026 01:10:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:10:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:10:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:10:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:10:58 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 19 Jun 2026 01:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Jun 2026 01:11:15 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:14:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Mon, 29 Jun 2026 17:14:13 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Mon, 29 Jun 2026 17:14:13 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Mon, 29 Jun 2026 17:14:13 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Mon, 29 Jun 2026 17:14:13 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:14:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:14:13 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 29 Jun 2026 17:14:13 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:14:13 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:14:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:14:34 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:14:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:14:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:14:37 GMT
USER gradle
# Mon, 29 Jun 2026 17:14:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:14:38 GMT
USER root
```

-	Layers:
	-	`sha256:81e2f2053c8fa702b6863110b55c09e67f6adeb78b4672745958c4d8b3d056c5`  
		Last Modified: Wed, 10 Jun 2026 08:00:11 GMT  
		Size: 41.6 MB (41562239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f56e4c7f2f2a1415c59803638274d488a73b61a8e1f9cbd9cb280327e8d21e`  
		Last Modified: Wed, 10 Jun 2026 08:00:15 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfec58c11de40dd4b26ee63375be80f77405d84e32dc6ab968d4972c8706cbc`  
		Last Modified: Fri, 19 Jun 2026 01:11:35 GMT  
		Size: 16.1 MB (16065873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0d5245cfc4d455fa7d828dd446981f99ca18736f7dcf292439ed50d20fa4e3`  
		Last Modified: Fri, 19 Jun 2026 01:11:37 GMT  
		Size: 92.7 MB (92713181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaa10a6a094940f400995c0e911d15903c5a21c81e534cea489c825167152e6`  
		Last Modified: Fri, 19 Jun 2026 01:11:34 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea88281d21e0b69c22a06494cadd5259cb7303f2f3526dbb1186ed56edd4c17`  
		Last Modified: Mon, 29 Jun 2026 17:15:12 GMT  
		Size: 94.5 MB (94524559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5d15f5420a08ead2ba970e8c36f45e2a4667bfc910c25b201cb07fe54a7750`  
		Last Modified: Mon, 29 Jun 2026 17:15:06 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f30abc4dfdc312746b7c8b9bd68c2cb727e2c4717c6e8d1b32b9aea493c91b`  
		Last Modified: Mon, 29 Jun 2026 17:15:07 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04aa8abb8d58d978731e136ead6c64ff02191bac2dadf561c78e03ca6ed9d742`  
		Last Modified: Mon, 29 Jun 2026 17:15:12 GMT  
		Size: 78.5 MB (78510181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe05e6107a3480c2b03920a13fc114416d866edf8cf67e40660df5225148c49`  
		Last Modified: Mon, 29 Jun 2026 17:15:14 GMT  
		Size: 140.6 MB (140596022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aea846056b5b519ee688ad48d16d69bca93ace2315c44faaf6d11f50d184d24`  
		Last Modified: Mon, 29 Jun 2026 17:15:08 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-26-resolute` - unknown; unknown

```console
$ docker pull gradle@sha256:9e27ce44432410b700319129f839bdbda4d70cca5f2d6b93d0a5274d3d5b251d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9476557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e6fdece0dcbefcdaa5aa5410e9923076ec22f044339693b02b825958245d1`

```dockerfile
```

-	Layers:
	-	`sha256:28d51e1a6524330a4f2e42ad6764f664362ebd8378e90d675b29a54784db8335`  
		Last Modified: Mon, 29 Jun 2026 17:15:07 GMT  
		Size: 9.4 MB (9438949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ed47db826f9228dea1687a73339920eb9a7537d69e6ead20588bc17fbb551f`  
		Last Modified: Mon, 29 Jun 2026 17:15:06 GMT  
		Size: 37.6 KB (37608 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-25-and-26-resolute` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3062f8587a4fa0e44e9481694f2e97a43f992f6d8a84d06992ebb821290f0366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.0 MB (460033404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e0cfe91eb7f186186155079972df81d581ad5242f4fe40bf88d22da367396e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9196.tar --tag 26.04
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9196.tar
# Fri, 19 Jun 2026 01:10:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:10:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:10:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:10:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:10:52 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 19 Jun 2026 01:11:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Jun 2026 01:11:11 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:14:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Mon, 29 Jun 2026 17:14:04 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Mon, 29 Jun 2026 17:14:04 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Mon, 29 Jun 2026 17:14:04 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Mon, 29 Jun 2026 17:14:04 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:14:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:14:04 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 29 Jun 2026 17:14:04 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:14:04 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:14:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:14:25 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:14:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:14:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:14:28 GMT
USER gradle
# Mon, 29 Jun 2026 17:14:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:14:29 GMT
USER root
```

-	Layers:
	-	`sha256:c572f291b2a0cc05a1d523f3dda4d3f1992c3e480debf2e1bc9278aeab115625`  
		Last Modified: Wed, 10 Jun 2026 08:00:25 GMT  
		Size: 40.7 MB (40709186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dda33820b52cf93fd5ff3808c770af252cf0565784b42e52e3dd74e2ebf5b2`  
		Last Modified: Wed, 10 Jun 2026 08:00:29 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986b7a217c59c4a1c6d2f4fc385716e50cd0997c12a644ad1b4a86f7edbe2892`  
		Last Modified: Fri, 19 Jun 2026 01:11:30 GMT  
		Size: 16.1 MB (16078431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f154dea547c648fb8bb2e30a7799e8ca3359b35ce1cfecdbb297e682d27365a5`  
		Last Modified: Fri, 19 Jun 2026 01:11:32 GMT  
		Size: 91.7 MB (91680259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed06bb7d4e7c4d53cafdd06a4846ca28d5eefc4a3dcc8d67ae84956c6dd4658b`  
		Last Modified: Fri, 19 Jun 2026 01:11:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2547ef3ef6c6b42461764a68bd37396340c8e6ffeff179f728f1aca71f5eca5`  
		Last Modified: Mon, 29 Jun 2026 17:15:00 GMT  
		Size: 93.5 MB (93504207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f70e6c6c2550e9b0748eb1f790f345822a596813831d0308166ca44be07552`  
		Last Modified: Mon, 29 Jun 2026 17:14:55 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6b4933e4054a95c0fd6d38b39eb60041a315f4f223bba67aed1809ac8376b6`  
		Last Modified: Mon, 29 Jun 2026 17:14:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045432cd184e2bfb9c0666ca940dce94a730ccf4b5976ec055ebb36f34614cfa`  
		Last Modified: Mon, 29 Jun 2026 17:14:59 GMT  
		Size: 77.4 MB (77431665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f67b9ba82af697c622710dd8c1a4028cb72b55c35f8a84a065e22f661e76976`  
		Last Modified: Mon, 29 Jun 2026 17:15:01 GMT  
		Size: 140.6 MB (140596021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccaea37ed6277b98efa4a0c27f7ab4e9f833126fe4ca92192e43f2e05d57eca`  
		Last Modified: Mon, 29 Jun 2026 17:14:57 GMT  
		Size: 29.3 KB (29338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-26-resolute` - unknown; unknown

```console
$ docker pull gradle@sha256:50c85103344d333c2f4b5f6c3b394970fa885d7e14d651866bb71eedd8bac90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9669947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66599a9f2fddd726cc067d75dca500ac05be2e70e960cd5ee2d7f057d2b16b0`

```dockerfile
```

-	Layers:
	-	`sha256:dfc44d8787d1854ecfac0d88e8366fac5e5917fc8234333f25e435a07aab5efa`  
		Last Modified: Mon, 29 Jun 2026 17:14:56 GMT  
		Size: 9.6 MB (9632005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a139834463c87e80b7b22ce89a6c6d9ccf2f3fe7a962f05c3fdd7f6f9618294b`  
		Last Modified: Mon, 29 Jun 2026 17:14:55 GMT  
		Size: 37.9 KB (37942 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-25-and-26-resolute` - linux; ppc64le

```console
$ docker pull gradle@sha256:f85670efe2afa575d19728115187cb014e7535f0cdb0c5ae239cb9b5a9581ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.1 MB (475120028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206f4afb6adc5f8ed950c1168f9bf1fd27b6ee4656d6b168199ae6f0e8f8df0e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Jun 2026 03:34:08 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9159.tar --tag 26.04
# Wed, 10 Jun 2026 03:34:09 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:34:09 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:34:09 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:34:09 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:34:09.982131+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:34:10 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:34:09.982131+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:34:10 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9159.tar
# Fri, 19 Jun 2026 01:15:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:15:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:15:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:15:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:15:40 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 19 Jun 2026 01:16:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:16:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:16:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:16:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Jun 2026 01:16:24 GMT
CMD ["jshell"]
# Fri, 19 Jun 2026 02:16:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Mon, 29 Jun 2026 17:23:35 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Mon, 29 Jun 2026 17:23:38 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Mon, 29 Jun 2026 17:23:38 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Mon, 29 Jun 2026 17:23:38 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:23:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:23:38 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 29 Jun 2026 17:23:38 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:23:39 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:24:24 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:24:24 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:24:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:24:29 GMT
USER gradle
# Mon, 29 Jun 2026 17:24:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:24:31 GMT
USER root
```

-	Layers:
	-	`sha256:d0ad782fe3317d182d855cc9406d3d23462337de4ab974a6d00a845910465af8`  
		Last Modified: Wed, 10 Jun 2026 08:00:40 GMT  
		Size: 46.6 MB (46593798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8e59391e45c204081dd6a3d3c4682dd0978a8db5fd9745f69792cd691e0624`  
		Last Modified: Wed, 10 Jun 2026 08:00:44 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4625a150716291f3f030b803a3f6c40b9203ae72d188677d7de5d1be8f95cf5b`  
		Last Modified: Fri, 19 Jun 2026 01:17:09 GMT  
		Size: 15.5 MB (15486782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb268e261d29411f1b36f907e043e39da582adfce444b9145fc03ef7a48f7b1a`  
		Last Modified: Fri, 19 Jun 2026 01:17:10 GMT  
		Size: 92.1 MB (92053873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec738335da598bc604b9847a22c08cc96ddf62ca8f6338bb1c14d20d5caa819`  
		Last Modified: Fri, 19 Jun 2026 01:17:08 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f149381dfe7f9a016581c8941c76b77fe8436c0facc983bbd5f0740ce0da328d`  
		Last Modified: Fri, 19 Jun 2026 02:19:15 GMT  
		Size: 93.9 MB (93901867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0670f8f1445037ea74345e6a4f51fce349a537a27a0d2ca33c0318eaf0b76bb3`  
		Last Modified: Mon, 29 Jun 2026 17:25:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e93931c58b56fb6d5936ea2c9f4406b384d6f72a36db91b09e767802d0f946`  
		Last Modified: Mon, 29 Jun 2026 17:25:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e538de353dddf3c21f4c5c1fdd7caed927cb2f9524dfe4e7494abd84dfe93f2`  
		Last Modified: Mon, 29 Jun 2026 17:25:30 GMT  
		Size: 86.5 MB (86483002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7687b3eb62f5a64a182f8cb18a19e9f60d7ffb586c53f83db0b1da1b05079484`  
		Last Modified: Mon, 29 Jun 2026 17:25:31 GMT  
		Size: 140.6 MB (140596023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5c8e7b6c0c3c3b8bb2217d07726cc19c923d1ec480eb9938d856a80187ae76`  
		Last Modified: Mon, 29 Jun 2026 17:25:27 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-26-resolute` - unknown; unknown

```console
$ docker pull gradle@sha256:a2a59b126704f0ce081eef7a23f004cb57dbf434f08d472cbf394f43260ce7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9520941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c580ca93a7eb874361a102d7800f0f877587c8fc73b6dbfd7124c5764816cb4`

```dockerfile
```

-	Layers:
	-	`sha256:ffa8dd39dba59a76088a4dcca8a95031b2b19d74a56975d478c07539f79ce24e`  
		Last Modified: Mon, 29 Jun 2026 17:25:27 GMT  
		Size: 9.5 MB (9483201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5c84653caa6f9b5b7cbb8c3b4cde5f0ec4fa2eb283c093b2f5105fe9275d4f7`  
		Last Modified: Mon, 29 Jun 2026 17:25:26 GMT  
		Size: 37.7 KB (37740 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-25-and-26-resolute` - linux; s390x

```console
$ docker pull gradle@sha256:7db1dbb7aefe1802b12119759c87a1445fab93eb0971dcd7005c16487a8a7e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455484314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4606665019dc6d06aa6931fd35ae6f65bf340650b4326c1bea040037a7ea5c52`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Jun 2026 07:47:21 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9183.tar --tag 26.04
# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T07:47:22.176605+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T07:47:22.176605+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9183.tar
# Fri, 19 Jun 2026 01:10:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:10:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:10:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:10:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:10:49 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 19 Jun 2026 01:11:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Jun 2026 01:11:05 GMT
CMD ["jshell"]
# Fri, 19 Jun 2026 02:11:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Fri, 19 Jun 2026 02:11:54 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Mon, 29 Jun 2026 17:14:02 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Mon, 29 Jun 2026 17:14:02 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Mon, 29 Jun 2026 17:14:02 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:14:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:14:02 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 29 Jun 2026 17:14:02 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:14:02 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:14:19 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:14:19 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:14:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:14:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:14:23 GMT
USER gradle
# Mon, 29 Jun 2026 17:14:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:14:23 GMT
USER root
```

-	Layers:
	-	`sha256:fff40c9207bf9ed5e68aadd6d83ec56f6b350421754c4d815f674a213be1edd8`  
		Last Modified: Wed, 10 Jun 2026 08:01:20 GMT  
		Size: 41.0 MB (40957425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bc0b48de22f57cae536e3f925926b013a50a63629708ed6e139cac57b87e60`  
		Last Modified: Wed, 10 Jun 2026 08:01:23 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d347bd62bcf676f3b8f09ca658938a5984a7c5cd0f684b9efb593210a52ba420`  
		Last Modified: Fri, 19 Jun 2026 01:11:31 GMT  
		Size: 14.6 MB (14639674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31dc0a8913e8a2a2a119a636c61c421c3b3ca506c2b1d443ee99a2e76eb117ed`  
		Last Modified: Fri, 19 Jun 2026 01:11:32 GMT  
		Size: 88.6 MB (88554100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab0c960d7aeab9b51fc6c0bf21b40604b16c565d9cd87b5e3272cac3c30c7a`  
		Last Modified: Fri, 19 Jun 2026 01:11:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d259a5114cc8ea769b2b816cf45eea2c2c25c1c0df3287f16ddc8e2a81fbf`  
		Last Modified: Fri, 19 Jun 2026 02:12:53 GMT  
		Size: 90.5 MB (90536859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355bf16d080460267c8f5fc87f0a73aaf25b9c2627add0fd7d85c508a5b6bd00`  
		Last Modified: Fri, 19 Jun 2026 02:12:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5e01790deec09d7010cb67a291c0184abf831981baa2ae294047a9873eef7f`  
		Last Modified: Mon, 29 Jun 2026 17:15:00 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aa0c487c14604627f3a0624cd236a70b65d987b3ed525ef82c3bed5fe7dae8`  
		Last Modified: Mon, 29 Jun 2026 17:15:02 GMT  
		Size: 80.2 MB (80195567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a845289e14affbe75d0cc18f5ac7ab272c5dd5f857d74981818d14a3c0b27ed2`  
		Last Modified: Mon, 29 Jun 2026 17:15:04 GMT  
		Size: 140.6 MB (140596023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c330acf1ed65e623e212d02d2b5383a89932251f4d908f597a7437f8d6ccae3c`  
		Last Modified: Mon, 29 Jun 2026 17:15:01 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-26-resolute` - unknown; unknown

```console
$ docker pull gradle@sha256:55ecafea3d3f26b63f66db387fc916673d7dc835c5965473249e7e72a5b4a40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9375150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae42d42aaf5c0eae56e6c4ab7449e8530a9e887b7299d09f8077b299547c593`

```dockerfile
```

-	Layers:
	-	`sha256:f6efa52ed0fcdf393232ead26410605e45cd3cf1dabba1245ff840e0a550ce65`  
		Last Modified: Mon, 29 Jun 2026 17:15:00 GMT  
		Size: 9.3 MB (9337544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307f9c3527b99e09516a58121053c06f0ca41514bbb67674649b05fe05e6b76c`  
		Last Modified: Mon, 29 Jun 2026 17:15:00 GMT  
		Size: 37.6 KB (37606 bytes)  
		MIME: application/vnd.in-toto+json
