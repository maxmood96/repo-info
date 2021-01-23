## `gradle:jdk15-hotspot`

```console
$ docker pull gradle@sha256:b48821162b8a78a324158bad11c9297cf209e2f6e121783b9cad4e80fa6babd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jdk15-hotspot` - linux; amd64

```console
$ docker pull gradle@sha256:b1366cd238eb775bcea6ed1d15908a326dfefa99061e16a6a156042661bba99a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.8 MB (420772884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bc96f9798c38c1fda349d2852395993fc0d777fc89e430ca88ff1dcef83d20`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:13:05 GMT
ENV JAVA_VERSION=jdk-15.0.1+9
# Thu, 21 Jan 2021 07:13:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='84398a1566d66ee5a88f3326fb7f0b70504eb510190f8f798bdb386481a3900e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_aarch64_linux_hotspot_15.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='bef5e9f4ab8a87645fa2b3d0ffb9f2b97374caa03cd1296597e8c86e8360d5a2';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_arm_linux_hotspot_15.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bc5347c011025f9830a420f943f52b97ebf0fc642ebff9a25bf465d0a6f3f3b9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_ppc64le_linux_hotspot_15.0.1_9.tar.gz';          ;;        s390x)          ESUM='d402e322841abc3c5c8b0352f08d54d6b5c25b7d6f81716401da266bcb1d1ff0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_s390x_linux_hotspot_15.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='61045ecb9434e3320dbc2c597715f9884586b7a18a56d29851b4d4a4d48a2a5e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_x64_linux_hotspot_15.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Jan 2021 07:13:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Jan 2021 07:13:18 GMT
CMD ["jshell"]
# Sat, 23 Jan 2021 00:24:32 GMT
CMD ["gradle"]
# Sat, 23 Jan 2021 00:24:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 23 Jan 2021 00:24:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 23 Jan 2021 00:24:33 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 23 Jan 2021 00:24:33 GMT
WORKDIR /home/gradle
# Sat, 23 Jan 2021 00:24:55 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Sat, 23 Jan 2021 00:24:56 GMT
ENV GRADLE_VERSION=6.7.1
# Sat, 23 Jan 2021 00:24:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
# Sat, 23 Jan 2021 00:25:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05901bd2c04822802b68afcbb0c5039ac7f895babf1246cc8c8d36c7c35e6d4`  
		Last Modified: Thu, 21 Jan 2021 07:32:29 GMT  
		Size: 207.7 MB (207729343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43f4c60f19553d9e44f95aaa77c7d856c0ef95cb944e286e0a3082e52b83108`  
		Last Modified: Sat, 23 Jan 2021 00:31:15 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9119b483003d29d8450c1a635d75ca8c4885c0984aed66fd92620836bbc3f0`  
		Last Modified: Sat, 23 Jan 2021 00:31:32 GMT  
		Size: 65.6 MB (65583237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2967c35f94e4801030a1b894246baacd2e0b9a8281786dd8879857e966316ae2`  
		Last Modified: Sat, 23 Jan 2021 00:31:23 GMT  
		Size: 102.9 MB (102851377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk15-hotspot` - linux; arm variant v7

```console
$ docker pull gradle@sha256:67e35869f261b33484cf29c1ee095381311c86cd97b92088a81fbc1ae7b26530
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393086517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2487171a7f6358a13f0c7d1d849c36e411841efb3187b1e81510a4d94787eef`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 21 Jan 2021 03:15:51 GMT
ADD file:874b5c952a766aaeff6c0d01f72a2644501ac0c8ab3ea3eef70339f045f09897 in / 
# Thu, 21 Jan 2021 03:15:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:15:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:15:57 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:15:59 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 03:42:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 03:42:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:44:58 GMT
ENV JAVA_VERSION=jdk-15.0.1+9
# Thu, 21 Jan 2021 03:45:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='84398a1566d66ee5a88f3326fb7f0b70504eb510190f8f798bdb386481a3900e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_aarch64_linux_hotspot_15.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='bef5e9f4ab8a87645fa2b3d0ffb9f2b97374caa03cd1296597e8c86e8360d5a2';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_arm_linux_hotspot_15.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bc5347c011025f9830a420f943f52b97ebf0fc642ebff9a25bf465d0a6f3f3b9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_ppc64le_linux_hotspot_15.0.1_9.tar.gz';          ;;        s390x)          ESUM='d402e322841abc3c5c8b0352f08d54d6b5c25b7d6f81716401da266bcb1d1ff0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_s390x_linux_hotspot_15.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='61045ecb9434e3320dbc2c597715f9884586b7a18a56d29851b4d4a4d48a2a5e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_x64_linux_hotspot_15.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Jan 2021 03:45:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Jan 2021 03:45:26 GMT
CMD ["jshell"]
# Sat, 23 Jan 2021 00:04:43 GMT
CMD ["gradle"]
# Sat, 23 Jan 2021 00:04:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 23 Jan 2021 00:04:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 23 Jan 2021 00:04:46 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 23 Jan 2021 00:04:47 GMT
WORKDIR /home/gradle
# Sat, 23 Jan 2021 00:05:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Sat, 23 Jan 2021 00:05:33 GMT
ENV GRADLE_VERSION=6.7.1
# Sat, 23 Jan 2021 00:05:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
# Sat, 23 Jan 2021 00:05:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:f5b689817f397e49f6802d29f6e262a92b16ef6fd29e0dbe7c957ecf60421c1f`  
		Last Modified: Thu, 21 Jan 2021 03:18:26 GMT  
		Size: 24.0 MB (24043427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b105a146cef196c701ff39cc8b99248972b0b02b544bb5fc1346bf37b870383`  
		Last Modified: Thu, 21 Jan 2021 03:18:19 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22943c6e232d1034beb778a2094ae7d8bb94122e5e562c65769abc93a3ab1731`  
		Last Modified: Thu, 21 Jan 2021 03:18:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a004bf3f6fd539a0f81317c01932da5fb822e61204e4a96ad0502e10b7d23f`  
		Last Modified: Thu, 21 Jan 2021 03:46:56 GMT  
		Size: 14.9 MB (14910182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ab9b8cf38627678408ccb309a6702bd958e5d6385c521bcafcc53f0cf44c`  
		Last Modified: Thu, 21 Jan 2021 03:51:04 GMT  
		Size: 191.3 MB (191314103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64d0ffeec417c4babf12342b9bd4726fbfc3bc7289fd5a959761340445a08dc`  
		Last Modified: Sat, 23 Jan 2021 00:08:35 GMT  
		Size: 4.3 KB (4343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08b81185acd6a3cc336b4c01d8c918fef281ff199641e86a1d1024ceda8444b`  
		Last Modified: Sat, 23 Jan 2021 00:08:57 GMT  
		Size: 60.0 MB (59962027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446862cb484465021d919bbe15d54c9ac64575a74a81e45eaa1e5f00754617b`  
		Last Modified: Sat, 23 Jan 2021 00:08:48 GMT  
		Size: 102.9 MB (102851398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk15-hotspot` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5e67a2679f11df500ba1863a239c061645182cd8861e53d0a61a80dca20e14c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.6 MB (416562046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e5f29905b20db710e52a11a43e92007fb25f48008e9fe0ae20bf60309df54b`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:18:25 GMT
ENV JAVA_VERSION=jdk-15.0.1+9
# Thu, 21 Jan 2021 05:18:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='84398a1566d66ee5a88f3326fb7f0b70504eb510190f8f798bdb386481a3900e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_aarch64_linux_hotspot_15.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='bef5e9f4ab8a87645fa2b3d0ffb9f2b97374caa03cd1296597e8c86e8360d5a2';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_arm_linux_hotspot_15.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bc5347c011025f9830a420f943f52b97ebf0fc642ebff9a25bf465d0a6f3f3b9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_ppc64le_linux_hotspot_15.0.1_9.tar.gz';          ;;        s390x)          ESUM='d402e322841abc3c5c8b0352f08d54d6b5c25b7d6f81716401da266bcb1d1ff0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_s390x_linux_hotspot_15.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='61045ecb9434e3320dbc2c597715f9884586b7a18a56d29851b4d4a4d48a2a5e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_x64_linux_hotspot_15.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Jan 2021 05:18:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Jan 2021 05:18:51 GMT
CMD ["jshell"]
# Fri, 22 Jan 2021 23:46:20 GMT
CMD ["gradle"]
# Fri, 22 Jan 2021 23:46:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 Jan 2021 23:46:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 22 Jan 2021 23:46:24 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 Jan 2021 23:46:24 GMT
WORKDIR /home/gradle
# Fri, 22 Jan 2021 23:47:00 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Jan 2021 23:47:02 GMT
ENV GRADLE_VERSION=6.7.1
# Fri, 22 Jan 2021 23:47:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
# Fri, 22 Jan 2021 23:47:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34bdfa7c4589aa88047d99a4692f6cf1c79f1dd21734f09e501d9d0a71e6b16`  
		Last Modified: Thu, 21 Jan 2021 05:24:02 GMT  
		Size: 205.3 MB (205325506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923747016dced179b702c60675b403dc8c02c94ed4c1d46876a88283582c47ac`  
		Last Modified: Fri, 22 Jan 2021 23:52:00 GMT  
		Size: 4.4 KB (4363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f94636ae50e95104f6ed57ed10d6c54acfbf80d497755dd0a1e7a17130cb43`  
		Last Modified: Fri, 22 Jan 2021 23:52:26 GMT  
		Size: 65.3 MB (65301754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6d17c74af3ba27ec3f147096a7bf56498957da6a5e6a096a356c363d48dce`  
		Last Modified: Fri, 22 Jan 2021 23:52:13 GMT  
		Size: 102.9 MB (102851396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk15-hotspot` - linux; ppc64le

```console
$ docker pull gradle@sha256:a0f56cbd3e4ccfbf2d2b4620b45d0ddd48ad4f3922cd84c2230be4859628c7c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.1 MB (417136092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632c548c1d2585ded837a335110273f0d113c2faf72bf69bafd0618355c5b71c`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 21 Jan 2021 03:50:20 GMT
ADD file:49b5be3021a4fb821776e6f80319442aec170cc102d0a654d693b5454690c821 in / 
# Thu, 21 Jan 2021 03:50:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:50:38 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:54 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:32:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 04:34:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:37:29 GMT
ENV JAVA_VERSION=jdk-15.0.1+9
# Thu, 21 Jan 2021 04:37:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='84398a1566d66ee5a88f3326fb7f0b70504eb510190f8f798bdb386481a3900e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_aarch64_linux_hotspot_15.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='bef5e9f4ab8a87645fa2b3d0ffb9f2b97374caa03cd1296597e8c86e8360d5a2';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_arm_linux_hotspot_15.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bc5347c011025f9830a420f943f52b97ebf0fc642ebff9a25bf465d0a6f3f3b9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_ppc64le_linux_hotspot_15.0.1_9.tar.gz';          ;;        s390x)          ESUM='d402e322841abc3c5c8b0352f08d54d6b5c25b7d6f81716401da266bcb1d1ff0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_s390x_linux_hotspot_15.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='61045ecb9434e3320dbc2c597715f9884586b7a18a56d29851b4d4a4d48a2a5e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_x64_linux_hotspot_15.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Jan 2021 04:38:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Jan 2021 04:38:07 GMT
CMD ["jshell"]
# Sat, 23 Jan 2021 00:30:11 GMT
CMD ["gradle"]
# Sat, 23 Jan 2021 00:30:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 23 Jan 2021 00:30:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 23 Jan 2021 00:30:25 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 23 Jan 2021 00:30:27 GMT
WORKDIR /home/gradle
# Sat, 23 Jan 2021 00:32:37 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Sat, 23 Jan 2021 00:32:40 GMT
ENV GRADLE_VERSION=6.7.1
# Sat, 23 Jan 2021 00:32:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
# Sat, 23 Jan 2021 00:33:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:ed91c6e011d4ed173552e8b28be61b946656c0330984b66bbbafa1f5e34f7fda`  
		Last Modified: Thu, 21 Jan 2021 03:55:01 GMT  
		Size: 33.3 MB (33280002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b906af84ca057c8c6651f31329207a1be8db5730495704aa9e38333d794bd3d4`  
		Last Modified: Thu, 21 Jan 2021 03:54:54 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3169ead309f6248d857e6e5c4891d40de8b742b21729c03d465aff49558d9135`  
		Last Modified: Thu, 21 Jan 2021 03:54:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ab13c01c886edd6faaa7b9c76d0d0de3a59132fd56b8b40e93da616dd8c1dc`  
		Last Modified: Thu, 21 Jan 2021 05:03:23 GMT  
		Size: 17.2 MB (17215118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e9e2dca351108fe38b449076f9f2232b0f7d21853aa4293e8c4d811dc8d86d`  
		Last Modified: Thu, 21 Jan 2021 05:17:25 GMT  
		Size: 189.8 MB (189783786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266315b8869968da5d8c50f9ad14768e4b3ffabd4d991bc1ae43ca019fb4022c`  
		Last Modified: Sat, 23 Jan 2021 00:51:53 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05c58b7d48cbaa31f6c4215219d28239761996d3eb363a08a7145978e4d4dc`  
		Last Modified: Sat, 23 Jan 2021 00:52:10 GMT  
		Size: 74.0 MB (74000384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868725cbe1535afb2136b798b0865311278afdaeff2911834a15fbf17eb842cc`  
		Last Modified: Sat, 23 Jan 2021 00:52:11 GMT  
		Size: 102.9 MB (102851398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk15-hotspot` - linux; s390x

```console
$ docker pull gradle@sha256:cddd07d64fc4ab76d6b201d76de5d7d821aa4e26a878476b25b61f52ae1fac71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.4 MB (392429454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbd6c9472037e6bec30506f16ddc26856bb3355c0f69024091f762ce102c09b`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 21 Jan 2021 04:01:09 GMT
ADD file:563ee3423282dfe85d6f542f5274f4fbfb35eabdc30f82580c427458890f099a in / 
# Thu, 21 Jan 2021 04:01:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 04:01:17 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 04:01:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 04:01:20 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:43:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 04:43:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:46:29 GMT
ENV JAVA_VERSION=jdk-15.0.1+9
# Thu, 21 Jan 2021 04:46:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='84398a1566d66ee5a88f3326fb7f0b70504eb510190f8f798bdb386481a3900e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_aarch64_linux_hotspot_15.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='bef5e9f4ab8a87645fa2b3d0ffb9f2b97374caa03cd1296597e8c86e8360d5a2';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_arm_linux_hotspot_15.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bc5347c011025f9830a420f943f52b97ebf0fc642ebff9a25bf465d0a6f3f3b9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_ppc64le_linux_hotspot_15.0.1_9.tar.gz';          ;;        s390x)          ESUM='d402e322841abc3c5c8b0352f08d54d6b5c25b7d6f81716401da266bcb1d1ff0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_s390x_linux_hotspot_15.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='61045ecb9434e3320dbc2c597715f9884586b7a18a56d29851b4d4a4d48a2a5e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.1%2B9/OpenJDK15U-jdk_x64_linux_hotspot_15.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Jan 2021 04:47:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Jan 2021 04:47:04 GMT
CMD ["jshell"]
# Fri, 22 Jan 2021 23:46:04 GMT
CMD ["gradle"]
# Fri, 22 Jan 2021 23:46:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 Jan 2021 23:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 22 Jan 2021 23:46:06 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 Jan 2021 23:46:06 GMT
WORKDIR /home/gradle
# Fri, 22 Jan 2021 23:46:42 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Jan 2021 23:46:53 GMT
ENV GRADLE_VERSION=6.7.1
# Fri, 22 Jan 2021 23:46:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
# Fri, 22 Jan 2021 23:47:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:413f11bd9d503955ec346fcc33cde226866284d10513c27bbbe8a1831e2649a9`  
		Last Modified: Thu, 21 Jan 2021 04:03:37 GMT  
		Size: 27.2 MB (27192128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8381373ef0ee1bc73cf24bd5471bd1d13cf3a5812c2f179d4fe27c969fdffa6`  
		Last Modified: Thu, 21 Jan 2021 04:03:32 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91bc19693304e44a85f335f09c970702b6985f60b1aef345ff1de9a951e89d`  
		Last Modified: Thu, 21 Jan 2021 04:03:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc824387b487764c99064d9c5a4131afb03651d6f120304f7bb31a1d339e9ec2`  
		Last Modified: Thu, 21 Jan 2021 05:07:22 GMT  
		Size: 15.7 MB (15749235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180aede6693a812c8175f058d926d521cbac9532f6db33c7a9ced58e0ad2fd62`  
		Last Modified: Thu, 21 Jan 2021 05:09:42 GMT  
		Size: 181.4 MB (181399148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896da20c92b4c4700b1cbf2a4bea5c0f2c9ae61efde58b890be3cef2a2655fe7`  
		Last Modified: Fri, 22 Jan 2021 23:56:02 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872725afc9aa312c32a1fa46323ab0354efa598ed1666d79fd3e5f95ed624362`  
		Last Modified: Fri, 22 Jan 2021 23:56:14 GMT  
		Size: 65.2 MB (65232128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08cc04781619509d7ffc5ef0cbd51e168adfb6548eedb535230c2c64edd2a99`  
		Last Modified: Fri, 22 Jan 2021 23:56:07 GMT  
		Size: 102.9 MB (102851419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
