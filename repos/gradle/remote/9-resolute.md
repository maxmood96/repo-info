## `gradle:9-resolute`

```console
$ docker pull gradle@sha256:8de3543f1772bb66be3b275893e5977b6d8bd2b0d25551faa5846a821d1f0600
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

### `gradle:9-resolute` - linux; amd64

```console
$ docker pull gradle@sha256:c41ef9ec84d88c0884fd66aa0557662b003a71f19d73474d60c90e5e939eef14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366465433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38376604a10856ee9a9f442c0cc34a0c427ddda08591274e99162367315f9404`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Fri, 08 May 2026 00:00:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:48 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 08 May 2026 00:01:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:01:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:01:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:01:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:01:06 GMT
CMD ["jshell"]
# Tue, 19 May 2026 18:52:20 GMT
CMD ["gradle"]
# Tue, 19 May 2026 18:52:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 19 May 2026 18:52:20 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 19 May 2026 18:52:20 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 19 May 2026 18:52:20 GMT
WORKDIR /home/gradle
# Tue, 19 May 2026 18:52:37 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 19 May 2026 18:52:37 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 19 May 2026 18:52:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 19 May 2026 18:52:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 19 May 2026 18:52:39 GMT
USER gradle
# Tue, 19 May 2026 18:52:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 19 May 2026 18:52:40 GMT
USER root
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566da077aa0452dcc3bf94ac4d5699d6e18e1aa1150db1829181d29237d0fe96`  
		Last Modified: Fri, 08 May 2026 00:01:25 GMT  
		Size: 16.1 MB (16113938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d819569f447cfbb2ec0e9f707214447f716f504b5476b0c0f6dec75218ce8d`  
		Last Modified: Fri, 08 May 2026 00:01:27 GMT  
		Size: 92.7 MB (92712873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1ad4588d336b2cb341c23ab4a48914e151921f642c9ffc6b75aeb684909cbe`  
		Last Modified: Fri, 08 May 2026 00:01:24 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f45e7030c6a7e606f9a3c2e3d89a7076c7f4bec71302a3f957bb39d6756bce2`  
		Last Modified: Tue, 19 May 2026 18:53:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aed1162db59881d5ef2316ab9fe4c4e57285dea28be63af40c8245b7af8f79e`  
		Last Modified: Tue, 19 May 2026 18:53:06 GMT  
		Size: 75.8 MB (75817172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01929d3be052f273f74fd9eb6266ebf754830f5def685f23b876bd554ed0ed9c`  
		Last Modified: Tue, 19 May 2026 18:53:07 GMT  
		Size: 140.2 MB (140236948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07fbdf3d7a1cda4638a00479c9f37bbb1f3523884f0b5124b72e01acb0096f4`  
		Last Modified: Tue, 19 May 2026 18:53:03 GMT  
		Size: 25.6 KB (25616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-resolute` - unknown; unknown

```console
$ docker pull gradle@sha256:a250385f4dd4250e9118ad4667b04622b75050adbe045d41a61a5652b7cdf6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9354810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb5abbde543e77c6493010189641e4a0ac6fc6a8094da97b999bc392ebd0fb1`

```dockerfile
```

-	Layers:
	-	`sha256:07e66d9de753e01571e4faf86a618fb34baf46f800103ca9acdf1b881e0b7255`  
		Last Modified: Tue, 19 May 2026 18:53:03 GMT  
		Size: 9.3 MB (9324106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bce200de041a14d6e6410d29f348a62479093525fc8144aa9a54aeed1c47a1ff`  
		Last Modified: Tue, 19 May 2026 18:53:03 GMT  
		Size: 30.7 KB (30704 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-resolute` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f3223a18b9902731b9a0fa5d75caced594365d1f718cc094594116c614d183da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363601118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c2cfa630d255422a90da86cc7ac28741b06cedf298e3d673bf50698ddcd6a0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Fri, 08 May 2026 00:00:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:31 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 08 May 2026 00:00:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:00:48 GMT
CMD ["jshell"]
# Tue, 19 May 2026 18:52:09 GMT
CMD ["gradle"]
# Tue, 19 May 2026 18:52:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 19 May 2026 18:52:09 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 19 May 2026 18:52:09 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 19 May 2026 18:52:09 GMT
WORKDIR /home/gradle
# Tue, 19 May 2026 18:52:29 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 19 May 2026 18:52:29 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 19 May 2026 18:52:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 19 May 2026 18:52:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 19 May 2026 18:52:36 GMT
USER gradle
# Tue, 19 May 2026 18:52:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 19 May 2026 18:52:37 GMT
USER root
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110e723aaf118849c4c7d8e1952fcf284fd25538affe28e6e48aace0c3f6b886`  
		Last Modified: Fri, 08 May 2026 00:01:08 GMT  
		Size: 16.1 MB (16123002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e650a32c4230af2f102ab8950d796c1030516cbc0e9f9b6a45a763df80bfd0f5`  
		Last Modified: Fri, 08 May 2026 00:01:10 GMT  
		Size: 91.7 MB (91680620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c857dd63485cd7c0d156e8a0315a86a40b3b7f2d4815826cc0baa24d217102f`  
		Last Modified: Fri, 08 May 2026 00:01:07 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19ca8c39a022df99c86d01ff31449bf2ca6e9e7c7d4206012f9d8a389d7c2b7`  
		Last Modified: Tue, 19 May 2026 18:53:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37e622a7145b3e43bd81f1c8af3199d0408de5b5ced65b2e6b87fccbf0fbacf`  
		Last Modified: Tue, 19 May 2026 18:53:05 GMT  
		Size: 74.8 MB (74798193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ebb6fceca2f81fb69050f0c14eb5daa71c09cbb1340ada5d5e77f6ac751470`  
		Last Modified: Tue, 19 May 2026 18:53:06 GMT  
		Size: 140.2 MB (140236984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfffc07d03e88f2cbcb050702c7604ce0e685f95d0edd27cda90c36c5c130e0`  
		Last Modified: Tue, 19 May 2026 18:53:02 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-resolute` - unknown; unknown

```console
$ docker pull gradle@sha256:c8c3211eac2f43d732b1f966ba693a079fdac817f3e1bd9a17dd10f6be68681c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9548974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c1fd50a29f04ee09af7f2ca492fdb553adf19ea64c80b811ab982ee5e45a34`

```dockerfile
```

-	Layers:
	-	`sha256:1ff9269bd5ac692645c2d6dc751467a56cb74de46764405b5d5cb449c4adfccf`  
		Last Modified: Tue, 19 May 2026 18:53:02 GMT  
		Size: 9.5 MB (9517881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49c42f7dabc7aca12970ae093b003758713dbe978bf9e3424eabdb8f8240475f`  
		Last Modified: Tue, 19 May 2026 18:53:02 GMT  
		Size: 31.1 KB (31093 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-resolute` - linux; ppc64le

```console
$ docker pull gradle@sha256:8be7a43eb3c53783c6189bb9ec4a000ed244cfa3c8244575fe6de5740d82c706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.9 MB (377933760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9be711e5a47e6d967ffe4e3223d8a0a9ea25a9b230e6edadb8442ddaedf98aa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 21 Apr 2026 15:28:41 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4397.tar --tag 26.04
# Tue, 21 Apr 2026 15:28:42 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:28:42 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:28:42 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:28:42 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:28:42.218648+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:28:42 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:28:42.218648+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:28:42 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4397.tar
# Fri, 08 May 2026 00:15:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:15:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:15:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:15:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:15:06 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 08 May 2026 00:15:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:15:41 GMT
CMD ["jshell"]
# Tue, 19 May 2026 19:01:07 GMT
CMD ["gradle"]
# Tue, 19 May 2026 19:01:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 19 May 2026 19:01:07 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 19 May 2026 19:01:07 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 19 May 2026 19:01:07 GMT
WORKDIR /home/gradle
# Tue, 19 May 2026 19:03:04 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 19 May 2026 19:03:04 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 19 May 2026 19:03:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 19 May 2026 19:03:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 19 May 2026 19:03:10 GMT
USER gradle
# Tue, 19 May 2026 19:03:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 19 May 2026 19:03:12 GMT
USER root
```

-	Layers:
	-	`sha256:6778ea4a0df31759938f6ad86a00ccbec8f6fb3a87cc23d066b75b8797f38133`  
		Last Modified: Tue, 21 Apr 2026 18:49:54 GMT  
		Size: 46.6 MB (46597071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a61592fadf77f9bc7cdabb18c478369fa8e8f607c5bded0b7b60eb646761e`  
		Last Modified: Tue, 21 Apr 2026 18:49:56 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a29ae4533931757f78fd02c1aa171f628542b261123a01361818392fa760c6`  
		Last Modified: Fri, 08 May 2026 00:16:20 GMT  
		Size: 15.5 MB (15533621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aaf9e3a1f2f7f1c0055eba11acda8286c05bf1171cd6a4836f2f02f8c9f71f`  
		Last Modified: Fri, 08 May 2026 00:16:22 GMT  
		Size: 92.1 MB (92054095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6b5b6153b07375b1d50c37bc7ef168e72202d357fd2b2710d9419a90476273`  
		Last Modified: Fri, 08 May 2026 00:16:19 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeeb99bbf6bc00cf594546e8e8d2cc32137588695ce081f3fbde01f1c49193b`  
		Last Modified: Tue, 19 May 2026 19:04:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac9aa3aae2f196bbf5acb5194254199f65f23cbaa17989e9aa24ec5a2b89af`  
		Last Modified: Tue, 19 May 2026 19:04:23 GMT  
		Size: 83.5 MB (83507586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51a3b0400035d02339199a879a21bec3e316e1c03d3e93d32dd2d96b4bd81bc`  
		Last Modified: Tue, 19 May 2026 19:04:24 GMT  
		Size: 140.2 MB (140236990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5931edbed7042bd3dfad2ad8aaf05e737928fd8b5529fc192c34d5af8312bb9a`  
		Last Modified: Tue, 19 May 2026 19:04:19 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-resolute` - unknown; unknown

```console
$ docker pull gradle@sha256:8f7b394849586aea0b6e3760ad9dfda114c86eb743cc345d6e34b0c1d9bd4f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9417939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7a5b0768a29bdc69cbec0fd61d03a1815a4912e6eec13bed66968039aab1f6`

```dockerfile
```

-	Layers:
	-	`sha256:45acfe2a7b20f4c856a945cc95a9ab5223ed4601268c19e6dd4a1a5efdf4e696`  
		Last Modified: Tue, 19 May 2026 19:04:19 GMT  
		Size: 9.4 MB (9387067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c41bb3f425cf66ff4a5440c4ff2aa897c7676c1340fbf47eb108b80504d3ff84`  
		Last Modified: Tue, 19 May 2026 19:04:19 GMT  
		Size: 30.9 KB (30872 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-resolute` - linux; s390x

```console
$ docker pull gradle@sha256:ef36e1c78130ce595b10c43759175fd2950bb736143c7ff111b7611248c87f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361714574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8e387fa5df01c2619ffa15b225ccd675a1cf0738138d7c7cfcc961de0e4959`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:34 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4463.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:35 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:35 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:35 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:35 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:35.069505+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:35 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:35.069505+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:35 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4463.tar
# Fri, 08 May 2026 00:05:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:05:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:05:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:05:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:05:54 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 08 May 2026 00:06:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:06:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:06:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:06:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:06:10 GMT
CMD ["jshell"]
# Tue, 19 May 2026 18:47:57 GMT
CMD ["gradle"]
# Tue, 19 May 2026 18:47:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 19 May 2026 18:47:57 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 19 May 2026 18:47:57 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 19 May 2026 18:47:57 GMT
WORKDIR /home/gradle
# Tue, 19 May 2026 18:48:40 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 19 May 2026 18:48:40 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 19 May 2026 18:48:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 19 May 2026 18:48:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 19 May 2026 18:48:45 GMT
USER gradle
# Tue, 19 May 2026 18:48:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 19 May 2026 18:48:46 GMT
USER root
```

-	Layers:
	-	`sha256:03dae6861127cd7f8db2f8a92a08f2d51871f69916247da38f9039679fd7a1da`  
		Last Modified: Tue, 21 Apr 2026 18:50:24 GMT  
		Size: 41.0 MB (40952193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b357ff8099f61a0e764119efc1c055b34bf5652e64e5c5955f88387a724676b6`  
		Last Modified: Tue, 21 Apr 2026 18:50:26 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dee4d0237a8a1ed6fa42dc59593d2d780268305c6c8fd5a445f70fb02b5f6c`  
		Last Modified: Fri, 08 May 2026 00:06:38 GMT  
		Size: 14.7 MB (14686126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ac8a359c00c52293aa314f85bbe803fa910f0847ef4a00b63b5a541f898580`  
		Last Modified: Fri, 08 May 2026 00:06:40 GMT  
		Size: 88.6 MB (88554419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd557b7677228be2fb1f7a941401dc3f88203e58f533ed8178be607820b517c`  
		Last Modified: Fri, 08 May 2026 00:06:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80580100b3ceac9d0317197274d9d1fcb708596cd298cdaae0d6f14aac20070`  
		Last Modified: Tue, 19 May 2026 18:49:29 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec72626540aad47daaa15ef77d3cb4c724790423942a7fb0f9ab04963c81f6b`  
		Last Modified: Tue, 19 May 2026 18:49:32 GMT  
		Size: 77.3 MB (77280455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3464b0ff0b1c2e3926f8eb0938edef98db50dca14b55a0b9007f7a15f215a5`  
		Last Modified: Tue, 19 May 2026 18:49:36 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7cb765a45512ba44ee88b217994c7358999088ffc3ad735c0cc0d2636de873`  
		Last Modified: Tue, 19 May 2026 18:49:29 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-resolute` - unknown; unknown

```console
$ docker pull gradle@sha256:28108f4bff47cecb8ee803c941a1d0ed2798ce900c2b41ca6b6291a08fbc6cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9273299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43634ddb9e36232122cd8a9248a6b5530ef1a9d231de329466c3163a8df1de0c`

```dockerfile
```

-	Layers:
	-	`sha256:4caa2f706bcb91c0c660ca0b060a02facc1015459c1dd8f380eb702e201f83fe`  
		Last Modified: Tue, 19 May 2026 18:49:30 GMT  
		Size: 9.2 MB (9242597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009031b3908afa9ef74c5766dfd36669c6edc895cbc537e02ab38e67ff81f3e9`  
		Last Modified: Tue, 19 May 2026 18:49:29 GMT  
		Size: 30.7 KB (30702 bytes)  
		MIME: application/vnd.in-toto+json
