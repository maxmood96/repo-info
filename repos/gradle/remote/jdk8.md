## `gradle:jdk8`

```console
$ docker pull gradle@sha256:ee49f45d231a8dd265deccd53b964a43478e0d3cb78624e885a556c1ad44fb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jdk8` - linux; amd64

```console
$ docker pull gradle@sha256:cdd97089ba537fde544d2e4d894c7e7923e68db5aad81d3a3ef000e2533339b2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293765393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c26c0d58309c695a8191a4e70fd63cf1d1a6ade7d22aaf2d45e175f4223e0d`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 01:46:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jun 2020 01:46:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:46:25 GMT
ENV JAVA_VERSION=jdk8u252-b09
# Wed, 17 Jun 2020 01:46:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='536bf397d98174b376da9ed49d2f659d65c7310318d8211444f4b7ba7c15e453';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u252b09.tar.gz';          ;;        armhf|armv7l)          ESUM='5b401ad3c9b246281bd6df34b1abaf75e10e5cad9c6b26b55232b016e90e411a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u252b09.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='55f0453b1d28812154138cf52b17b7acd93b9e55263f1f508f559795d31b2671';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u252b09.tar.gz';          ;;        s390x)          ESUM='db39932666c37718b1c3c62a1adb4f8e9c33258cf15a85ddf9b4d71199edfb1d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u252b09.tar.gz';          ;;        amd64|x86_64)          ESUM='2b59b5282ff32bce7abba8ad6b9fde34c15a98f949ad8ae43e789bbd78fc8862';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u252b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 17 Jun 2020 01:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2020 06:17:40 GMT
CMD ["gradle"]
# Wed, 17 Jun 2020 06:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 17 Jun 2020 06:17:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 17 Jun 2020 06:17:42 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 17 Jun 2020 06:17:42 GMT
WORKDIR /home/gradle
# Wed, 17 Jun 2020 06:18:06 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Jul 2020 19:19:48 GMT
ENV GRADLE_VERSION=6.5.1
# Wed, 01 Jul 2020 19:19:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
# Wed, 01 Jul 2020 19:19:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205a7ec514d2cd428757163aacefd82b2947b6a557973f9bf6587fe2bc31e3b8`  
		Last Modified: Wed, 17 Jun 2020 01:50:17 GMT  
		Size: 13.3 MB (13311450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c375e6cae508b3d8bbbad22144a73a10427951e1d9bcb8b88b0603b26ac26b`  
		Last Modified: Wed, 17 Jun 2020 01:50:24 GMT  
		Size: 102.7 MB (102690067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e63078ed7e2966b576f7a983002f24552bc1f7727ad2249e0e7688fe9f3c3f3`  
		Last Modified: Wed, 17 Jun 2020 06:20:55 GMT  
		Size: 4.5 KB (4487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3181381bb6204eb5be5bdf959ae2533d4086dfa2a48fbcfcc1136e20595e2b38`  
		Last Modified: Wed, 17 Jun 2020 06:21:06 GMT  
		Size: 48.7 MB (48654729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc225e194d117941691d4868a9291ca85b1fc2dd51d70728600e41dcc39840ee`  
		Last Modified: Wed, 01 Jul 2020 19:21:01 GMT  
		Size: 102.4 MB (102379566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; ppc64le

```console
$ docker pull gradle@sha256:9e10c9ec92eab69106801f4ba9f36d5afdf57327e9c64fe6aba0deba5c169b74
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303334386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fcbb96a50fd123cad78d3deda304348098300d85784988960586f74cf47100b`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Jun 2020 01:23:28 GMT
ADD file:3d8a4167931b708419d8f212295ee2e69c2e17523d93de0f36af7c8b7adaf6b0 in / 
# Wed, 17 Jun 2020 01:23:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:23:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:23:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:23:59 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:25:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jun 2020 03:26:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:27:02 GMT
ENV JAVA_VERSION=jdk8u252-b09
# Wed, 17 Jun 2020 03:27:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='536bf397d98174b376da9ed49d2f659d65c7310318d8211444f4b7ba7c15e453';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u252b09.tar.gz';          ;;        armhf|armv7l)          ESUM='5b401ad3c9b246281bd6df34b1abaf75e10e5cad9c6b26b55232b016e90e411a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u252b09.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='55f0453b1d28812154138cf52b17b7acd93b9e55263f1f508f559795d31b2671';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u252b09.tar.gz';          ;;        s390x)          ESUM='db39932666c37718b1c3c62a1adb4f8e9c33258cf15a85ddf9b4d71199edfb1d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u252b09.tar.gz';          ;;        amd64|x86_64)          ESUM='2b59b5282ff32bce7abba8ad6b9fde34c15a98f949ad8ae43e789bbd78fc8862';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u252b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 17 Jun 2020 03:27:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2020 05:21:21 GMT
CMD ["gradle"]
# Wed, 17 Jun 2020 05:21:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 17 Jun 2020 05:21:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 17 Jun 2020 05:21:46 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 17 Jun 2020 05:21:53 GMT
WORKDIR /home/gradle
# Wed, 17 Jun 2020 05:24:03 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Jul 2020 19:17:39 GMT
ENV GRADLE_VERSION=6.5.1
# Wed, 01 Jul 2020 19:17:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
# Wed, 01 Jul 2020 19:18:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:c82758296165adcddbc1b265a621d9938f9c807decd8469ae7f939d875188bf5`  
		Last Modified: Sat, 30 May 2020 05:26:15 GMT  
		Size: 30.4 MB (30400411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740d34e8b0154512b13d50a28cb641b322092ef53e5681dd77102035104fbffe`  
		Last Modified: Wed, 17 Jun 2020 01:28:15 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e49637d96cd01435b847808eee898f2f13837bf3034497154962bb88ef0416b`  
		Last Modified: Wed, 17 Jun 2020 01:28:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042abc2d98a7172c5b211cb1f6be22813334814c096e94c8fbf0a7972587d765`  
		Last Modified: Wed, 17 Jun 2020 01:28:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a910ee11e6ad058caab92c085018fc0da3bfc7f3d1bb0c650f7aa3eb0c7d7c`  
		Last Modified: Wed, 17 Jun 2020 03:39:07 GMT  
		Size: 14.0 MB (13955963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9198446323d367afd056fa17ad3a4c6719915a9064a366920715f9d01e8b16`  
		Last Modified: Wed, 17 Jun 2020 03:39:16 GMT  
		Size: 99.9 MB (99866987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48403e1d01998cf0b50f3deb86a66cfed0790c2def2f73cecdf94353f3b06d4a`  
		Last Modified: Wed, 17 Jun 2020 05:48:16 GMT  
		Size: 4.5 KB (4535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeefba1582ec04645132828cb5f16ec1e8be6f8a8a167937851debb131cba5d`  
		Last Modified: Wed, 17 Jun 2020 05:48:30 GMT  
		Size: 56.7 MB (56690649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c975b1fc38d71b686d98ec97610826a7f4fedf58749660f99571b48992f886d`  
		Last Modified: Wed, 01 Jul 2020 19:22:32 GMT  
		Size: 102.4 MB (102379603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; s390x

```console
$ docker pull gradle@sha256:d8a28dc1d9dba19a146f4cadeac7c6fe661dc5078fec2e752262e7e909f1f4e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287327325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ec8e3d88cfe3c5d6a7cc106b4ef5b0a5c3b9e00f618eb2fceac66c93b9953a`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:57:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jun 2020 02:58:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:58:01 GMT
ENV JAVA_VERSION=jdk8u252-b09
# Wed, 17 Jun 2020 02:58:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='536bf397d98174b376da9ed49d2f659d65c7310318d8211444f4b7ba7c15e453';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u252b09.tar.gz';          ;;        armhf|armv7l)          ESUM='5b401ad3c9b246281bd6df34b1abaf75e10e5cad9c6b26b55232b016e90e411a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u252b09.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='55f0453b1d28812154138cf52b17b7acd93b9e55263f1f508f559795d31b2671';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u252b09.tar.gz';          ;;        s390x)          ESUM='db39932666c37718b1c3c62a1adb4f8e9c33258cf15a85ddf9b4d71199edfb1d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u252b09.tar.gz';          ;;        amd64|x86_64)          ESUM='2b59b5282ff32bce7abba8ad6b9fde34c15a98f949ad8ae43e789bbd78fc8862';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u252b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 17 Jun 2020 02:58:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2020 03:49:45 GMT
CMD ["gradle"]
# Wed, 17 Jun 2020 03:49:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 17 Jun 2020 03:49:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 17 Jun 2020 03:49:46 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 17 Jun 2020 03:49:47 GMT
WORKDIR /home/gradle
# Wed, 17 Jun 2020 03:50:06 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Jul 2020 19:41:38 GMT
ENV GRADLE_VERSION=6.5.1
# Wed, 01 Jul 2020 19:41:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
# Wed, 01 Jul 2020 19:41:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=50a7d30529fa939721fe9268a0205142f3f2302bcac5fb45b27a3902e58db54a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed532570dcab9ebdbb790d8ffbc4d7efd4d3032c37c5279da2aff135f7a2514`  
		Last Modified: Wed, 17 Jun 2020 03:02:51 GMT  
		Size: 13.0 MB (13032315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42bdb7a6bc4fe637f1e7e7d4f7973466c7e9449cdc334234739d5a6739481a5`  
		Last Modified: Wed, 17 Jun 2020 03:03:02 GMT  
		Size: 98.4 MB (98388178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b90dd6c8df1cf76473d2f2b7060ff33a4cde2e294ecfee76c8c19430eb12aa`  
		Last Modified: Wed, 17 Jun 2020 04:05:19 GMT  
		Size: 4.5 KB (4522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014ca68d1724591574e70796d89a3d8e06cc6e6549761b15db9c4b1179115639`  
		Last Modified: Wed, 17 Jun 2020 04:05:27 GMT  
		Size: 48.1 MB (48119664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aacf4265f5fc166aa31b30efecd6c92e021448157c2dbaa7089228a6c2f3b2d`  
		Last Modified: Wed, 01 Jul 2020 19:43:07 GMT  
		Size: 102.4 MB (102379600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
