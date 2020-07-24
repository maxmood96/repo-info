## `gradle:jdk11`

```console
$ docker pull gradle@sha256:449a6385fa079f420cd7cd4ce34601740e046dfdcaaaf272d6cc5313104859df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `gradle:jdk11` - linux; amd64

```console
$ docker pull gradle@sha256:ac8cd8c09ad618df8ed1fe5f5dc3929a2fb12f52cfd7c0f9e688aec8dbcb1fee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (386038919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b831c3174f2ed4b88389f87bad3697b7813aff25ef74039cbf32907a285d224`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:16:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jul 2020 15:17:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:17:33 GMT
ENV JAVA_VERSION=jdk-11.0.8+10
# Fri, 24 Jul 2020 15:17:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 15:17:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 15:17:48 GMT
CMD ["jshell"]
# Fri, 24 Jul 2020 19:33:12 GMT
CMD ["gradle"]
# Fri, 24 Jul 2020 19:33:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Jul 2020 19:33:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 24 Jul 2020 19:33:13 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Jul 2020 19:33:14 GMT
WORKDIR /home/gradle
# Fri, 24 Jul 2020 19:33:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 19:33:31 GMT
ENV GRADLE_VERSION=6.5.1
# Fri, 24 Jul 2020 19:33:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
# Fri, 24 Jul 2020 19:33:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54d424eaa66f20b7926dbaa13c37d1c7c27c0e3113239f5608b4a57c157c399`  
		Last Modified: Fri, 24 Jul 2020 15:22:49 GMT  
		Size: 13.9 MB (13875512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb68d78371a673636c49ed80c0e1b1a3750491e9b553a0f0bb6747f3ceec9ba`  
		Last Modified: Fri, 24 Jul 2020 15:23:32 GMT  
		Size: 194.3 MB (194266399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14628d9fb80ff5ddcd2d16167d6d711dcc1b06ce5cb6edbc54f373880b7c3e5b`  
		Last Modified: Fri, 24 Jul 2020 19:35:56 GMT  
		Size: 4.5 KB (4496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fe09ba81562d0bef27a168e31533051c8ff539d7a4e190fb0c882170d55138`  
		Last Modified: Fri, 24 Jul 2020 19:36:07 GMT  
		Size: 48.8 MB (48779515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaa805b5928502c8a20483132f93efe61bb76748713168191dfb99202274d87`  
		Last Modified: Fri, 24 Jul 2020 19:36:04 GMT  
		Size: 102.4 MB (102379497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; arm variant v7

```console
$ docker pull gradle@sha256:7f60511d22772fffe71e53dfaa2db18d6e6e98cf10826c298d741b029a52a2ce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364558095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44456d6d2db9cf641c78c57b80915e5e83dbad134a32076aa454ab1e959529b`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jul 2020 16:04:27 GMT
ADD file:934b4bc073556bbba45a5017b40df7ac076a57b031b6b7225919b1ea3c1d89ff in / 
# Fri, 24 Jul 2020 16:04:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:05:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:05:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:05:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:19:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jul 2020 18:20:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:22:30 GMT
ENV JAVA_VERSION=jdk-11.0.8+10
# Fri, 24 Jul 2020 18:23:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 18:23:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 18:23:25 GMT
CMD ["jshell"]
# Fri, 24 Jul 2020 19:57:22 GMT
CMD ["gradle"]
# Fri, 24 Jul 2020 19:57:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Jul 2020 19:57:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 24 Jul 2020 19:57:55 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Jul 2020 19:57:59 GMT
WORKDIR /home/gradle
# Fri, 24 Jul 2020 19:58:53 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 19:58:59 GMT
ENV GRADLE_VERSION=6.5.1
# Fri, 24 Jul 2020 19:59:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
# Fri, 24 Jul 2020 19:59:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:de691405df56c17462a8052d9b88a283d955c448deda7a610d70096a5454ff13`  
		Last Modified: Mon, 13 Jul 2020 15:47:13 GMT  
		Size: 22.3 MB (22277635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a766b93ee2f7ed0525d6d90b71c5e860e5e54d4b5259de86c81e5c49ff120c`  
		Last Modified: Fri, 24 Jul 2020 16:13:28 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c97e104d7363348d21ddc11159cfa859c18d58712fcafc215fefb535baccbae`  
		Last Modified: Fri, 24 Jul 2020 16:13:28 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a97b3bf2bf845ce898abe48aed267cb2a554e220ee512500495c2791ea6ea8`  
		Last Modified: Fri, 24 Jul 2020 16:13:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b94dcf53adc5490aa500e598355308c95d914fd25bb61493b436a89f18e8b9`  
		Last Modified: Fri, 24 Jul 2020 18:29:34 GMT  
		Size: 12.8 MB (12816849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b91860f10686d322770f1a747e9a2125a66a1dbf2beeeda2292197d65269c00`  
		Last Modified: Fri, 24 Jul 2020 18:30:58 GMT  
		Size: 183.3 MB (183306954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288eff7fd4e6b54d0f1aa2d09347bdb1b92dda147b9618c0e1aa253d2d9497f5`  
		Last Modified: Fri, 24 Jul 2020 20:02:48 GMT  
		Size: 4.5 KB (4512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eacafa4548b36cffe5650689bbcc840f3acc698befaf4081e11c4199bf2186`  
		Last Modified: Fri, 24 Jul 2020 20:03:04 GMT  
		Size: 43.7 MB (43736037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a29df2278b4d9e2e9bfd04fdff0d9625cbe7336759547bfe537baf2416c151`  
		Last Modified: Fri, 24 Jul 2020 20:03:03 GMT  
		Size: 102.4 MB (102379605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; ppc64le

```console
$ docker pull gradle@sha256:2879ba70d1a9c6a0af328582daf9caf245eb163e42652530d2d1bb2e6a231e62
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.4 MB (381426261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704b742237dcc5f7cf40fe934db4d2183902c2b3c6a4991d4bb6ac24d55c840f`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jul 2020 14:33:42 GMT
ADD file:d8c73324b090ba968a3efc4afc8af7d913766bd7787fc4cd6e4436895a4e564a in / 
# Fri, 24 Jul 2020 14:34:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:34:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:35:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:35:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:38:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jul 2020 15:45:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:47:49 GMT
ENV JAVA_VERSION=jdk-11.0.8+10
# Fri, 24 Jul 2020 15:48:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 15:49:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 15:49:32 GMT
CMD ["jshell"]
# Fri, 24 Jul 2020 19:39:21 GMT
CMD ["gradle"]
# Fri, 24 Jul 2020 19:39:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Jul 2020 19:39:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 24 Jul 2020 19:39:44 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Jul 2020 19:39:50 GMT
WORKDIR /home/gradle
# Fri, 24 Jul 2020 19:41:52 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 19:42:05 GMT
ENV GRADLE_VERSION=6.5.1
# Fri, 24 Jul 2020 19:42:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
# Fri, 24 Jul 2020 19:42:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:453712c8810fcce792c21167e028047a35328679a3bd4429b8837301315e9103`  
		Last Modified: Mon, 13 Jul 2020 15:47:10 GMT  
		Size: 30.4 MB (30404926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbb4638d99213e93a32d6945492539426ee3616d7ba413462a8b936268a56af`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 35.2 KB (35224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b0bd277b733224c67d835643aa13dd8a9b86bcc10023a393302b3861e9a7b8`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270c2b729d72bf4931bb8d6ccbd100e124e01bac9628380f36c2d0f13bdcc109`  
		Last Modified: Fri, 24 Jul 2020 14:41:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd6970a3a6adb0cbcb037b053a7c0ea9480e9f5edf524c197aea5374c2cf495`  
		Last Modified: Fri, 24 Jul 2020 16:19:35 GMT  
		Size: 14.5 MB (14519278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fe78b7fb95e109d7f6bdaab0b9d4e17d5786667ea34ce4e103fcbb90466ef1`  
		Last Modified: Fri, 24 Jul 2020 16:21:31 GMT  
		Size: 177.3 MB (177275866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc5751dc22f3af3b8f6b837aba2c3789d75425632012be52d3692a68f03ba48`  
		Last Modified: Fri, 24 Jul 2020 19:59:17 GMT  
		Size: 4.5 KB (4532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3c5382ab9f14e626b4dcabf7ef660e509c17da20ba69352c5e5a1d9dac8b14`  
		Last Modified: Fri, 24 Jul 2020 19:59:30 GMT  
		Size: 56.8 MB (56805813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7d3f7da745f4ff764c787ba9f1f8ccfc14d7a74dbc917f977c77773da2c38a`  
		Last Modified: Fri, 24 Jul 2020 19:59:25 GMT  
		Size: 102.4 MB (102379581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
