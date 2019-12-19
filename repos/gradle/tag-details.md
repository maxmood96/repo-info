<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `gradle`

-	[`gradle:6.0`](#gradle60)
-	[`gradle:6.0.1`](#gradle601)
-	[`gradle:6.0.1-jdk`](#gradle601-jdk)
-	[`gradle:6.0.1-jdk11`](#gradle601-jdk11)
-	[`gradle:6.0.1-jdk13`](#gradle601-jdk13)
-	[`gradle:6.0.1-jdk8`](#gradle601-jdk8)
-	[`gradle:6.0.1-jre`](#gradle601-jre)
-	[`gradle:6.0.1-jre11`](#gradle601-jre11)
-	[`gradle:6.0.1-jre13`](#gradle601-jre13)
-	[`gradle:6.0.1-jre8`](#gradle601-jre8)
-	[`gradle:6.0-jdk`](#gradle60-jdk)
-	[`gradle:6.0-jdk11`](#gradle60-jdk11)
-	[`gradle:6.0-jdk13`](#gradle60-jdk13)
-	[`gradle:6.0-jdk8`](#gradle60-jdk8)
-	[`gradle:6.0-jre`](#gradle60-jre)
-	[`gradle:6.0-jre11`](#gradle60-jre11)
-	[`gradle:6.0-jre13`](#gradle60-jre13)
-	[`gradle:6.0-jre8`](#gradle60-jre8)
-	[`gradle:jdk`](#gradlejdk)
-	[`gradle:jdk11`](#gradlejdk11)
-	[`gradle:jdk13`](#gradlejdk13)
-	[`gradle:jdk8`](#gradlejdk8)
-	[`gradle:jre`](#gradlejre)
-	[`gradle:jre11`](#gradlejre11)
-	[`gradle:jre13`](#gradlejre13)
-	[`gradle:jre8`](#gradlejre8)
-	[`gradle:latest`](#gradlelatest)

## `gradle:6.0`

```console
$ docker pull gradle@sha256:8ba20b563ed5c90f4e16705a0590d469190362fffc02dbbe308f05b81a16506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0` - linux; amd64

```console
$ docker pull gradle@sha256:e5496a08fead0e48822aa86087b9d5f278795586a8588528bc289f0406e8d235
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288889902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc47c2ea2852e1ae6d6756cae8c568b3b255e198d589f81be8835390c6740a2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:56:27 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:56:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:56:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:56:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:56:29 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:56:57 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:56:57 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:56:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596d6c23adc7886652eea636e0c856146cc51d2da380a735645fad034dfe5069`  
		Last Modified: Thu, 19 Dec 2019 06:47:29 GMT  
		Size: 105.1 MB (105052689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07313090020e2216012e1a247dd3e9fce45ffac5a07713c234c1f02718a91a8`  
		Last Modified: Thu, 19 Dec 2019 10:59:36 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d786c8e5ce8bd8e0a4bdfc0ecbde07e01b6607161798b7c5a1f68fd0673aea`  
		Last Modified: Thu, 19 Dec 2019 10:59:47 GMT  
		Size: 48.6 MB (48646474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84476db4b1ac2fc5e552d5bdb3d8247691ea1d57ccbddf9bc83c28455f012d3`  
		Last Modified: Thu, 19 Dec 2019 10:59:43 GMT  
		Size: 95.1 MB (95137274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0` - linux; ppc64le

```console
$ docker pull gradle@sha256:de97c2794be05db81624dc748d5f0bf6f774b3746b07e662593263f523fa126e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298448560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229fbb404cae0f708aa5d31816a664d221d3bf69c7a3d1450ba375ef51a3a708`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:18:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:18:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:07:19 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:07:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:07:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:07:41 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:07:44 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:09:21 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:16:56 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:16:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11691fec336d2f0ecf12299c6a2258179b6a03f37e8596ace4bdcf8340a84210`  
		Last Modified: Fri, 08 Nov 2019 02:26:43 GMT  
		Size: 102.2 MB (102223730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9315d5888c26e44dda21265c0782bd2458f9275e893dda525156726db64fd`  
		Last Modified: Fri, 08 Nov 2019 03:18:05 GMT  
		Size: 4.5 KB (4526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f9984d68d74068dfbcdb0f0ec1b51ba5716b1cca72aa6813cfbaae8f333f`  
		Last Modified: Fri, 08 Nov 2019 03:18:18 GMT  
		Size: 56.7 MB (56678368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b2332b39dc868b3d267bf94fca2afd107122993c7dec787be0f95aa7adf3a9`  
		Last Modified: Wed, 20 Nov 2019 00:19:42 GMT  
		Size: 95.1 MB (95137355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0` - linux; s390x

```console
$ docker pull gradle@sha256:271543f903e154259439857a293709a845db5d56bed51bb86dc75d8bdc27f92b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614cb05338d916b421497a72794e78adae51687596d0ce1ee3eb69b1ce6d7ab2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:41:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:16:40 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:16:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:16:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:16:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:16:43 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:17:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:33 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75a894e76562f7781c6919af4bc9ab7ff662d7e916f0e18fe1261def191dec`  
		Last Modified: Fri, 08 Nov 2019 02:44:32 GMT  
		Size: 100.7 MB (100734555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b0f50dfaf38af9bcb739cda10fb6a0c7e8610af129e4285b00e833cf63be05`  
		Last Modified: Fri, 08 Nov 2019 03:19:04 GMT  
		Size: 4.5 KB (4497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5fff2ffc2e2c8a9e323c3696a7eacf9842b928e684dfa7cb4b2b577fab52d`  
		Last Modified: Fri, 08 Nov 2019 03:19:14 GMT  
		Size: 48.1 MB (48095072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1a287aa214edc225ccf89f9627b82a3b65d511ae9ffb5a99235667c5c1438d`  
		Last Modified: Tue, 19 Nov 2019 23:42:29 GMT  
		Size: 95.1 MB (95137322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0.1`

```console
$ docker pull gradle@sha256:8ba20b563ed5c90f4e16705a0590d469190362fffc02dbbe308f05b81a16506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0.1` - linux; amd64

```console
$ docker pull gradle@sha256:e5496a08fead0e48822aa86087b9d5f278795586a8588528bc289f0406e8d235
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288889902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc47c2ea2852e1ae6d6756cae8c568b3b255e198d589f81be8835390c6740a2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:56:27 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:56:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:56:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:56:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:56:29 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:56:57 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:56:57 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:56:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596d6c23adc7886652eea636e0c856146cc51d2da380a735645fad034dfe5069`  
		Last Modified: Thu, 19 Dec 2019 06:47:29 GMT  
		Size: 105.1 MB (105052689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07313090020e2216012e1a247dd3e9fce45ffac5a07713c234c1f02718a91a8`  
		Last Modified: Thu, 19 Dec 2019 10:59:36 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d786c8e5ce8bd8e0a4bdfc0ecbde07e01b6607161798b7c5a1f68fd0673aea`  
		Last Modified: Thu, 19 Dec 2019 10:59:47 GMT  
		Size: 48.6 MB (48646474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84476db4b1ac2fc5e552d5bdb3d8247691ea1d57ccbddf9bc83c28455f012d3`  
		Last Modified: Thu, 19 Dec 2019 10:59:43 GMT  
		Size: 95.1 MB (95137274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1` - linux; ppc64le

```console
$ docker pull gradle@sha256:de97c2794be05db81624dc748d5f0bf6f774b3746b07e662593263f523fa126e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298448560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229fbb404cae0f708aa5d31816a664d221d3bf69c7a3d1450ba375ef51a3a708`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:18:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:18:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:07:19 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:07:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:07:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:07:41 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:07:44 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:09:21 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:16:56 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:16:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11691fec336d2f0ecf12299c6a2258179b6a03f37e8596ace4bdcf8340a84210`  
		Last Modified: Fri, 08 Nov 2019 02:26:43 GMT  
		Size: 102.2 MB (102223730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9315d5888c26e44dda21265c0782bd2458f9275e893dda525156726db64fd`  
		Last Modified: Fri, 08 Nov 2019 03:18:05 GMT  
		Size: 4.5 KB (4526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f9984d68d74068dfbcdb0f0ec1b51ba5716b1cca72aa6813cfbaae8f333f`  
		Last Modified: Fri, 08 Nov 2019 03:18:18 GMT  
		Size: 56.7 MB (56678368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b2332b39dc868b3d267bf94fca2afd107122993c7dec787be0f95aa7adf3a9`  
		Last Modified: Wed, 20 Nov 2019 00:19:42 GMT  
		Size: 95.1 MB (95137355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1` - linux; s390x

```console
$ docker pull gradle@sha256:271543f903e154259439857a293709a845db5d56bed51bb86dc75d8bdc27f92b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614cb05338d916b421497a72794e78adae51687596d0ce1ee3eb69b1ce6d7ab2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:41:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:16:40 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:16:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:16:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:16:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:16:43 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:17:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:33 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75a894e76562f7781c6919af4bc9ab7ff662d7e916f0e18fe1261def191dec`  
		Last Modified: Fri, 08 Nov 2019 02:44:32 GMT  
		Size: 100.7 MB (100734555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b0f50dfaf38af9bcb739cda10fb6a0c7e8610af129e4285b00e833cf63be05`  
		Last Modified: Fri, 08 Nov 2019 03:19:04 GMT  
		Size: 4.5 KB (4497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5fff2ffc2e2c8a9e323c3696a7eacf9842b928e684dfa7cb4b2b577fab52d`  
		Last Modified: Fri, 08 Nov 2019 03:19:14 GMT  
		Size: 48.1 MB (48095072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1a287aa214edc225ccf89f9627b82a3b65d511ae9ffb5a99235667c5c1438d`  
		Last Modified: Tue, 19 Nov 2019 23:42:29 GMT  
		Size: 95.1 MB (95137322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0.1-jdk`

```console
$ docker pull gradle@sha256:8ba20b563ed5c90f4e16705a0590d469190362fffc02dbbe308f05b81a16506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0.1-jdk` - linux; amd64

```console
$ docker pull gradle@sha256:e5496a08fead0e48822aa86087b9d5f278795586a8588528bc289f0406e8d235
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288889902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc47c2ea2852e1ae6d6756cae8c568b3b255e198d589f81be8835390c6740a2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:56:27 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:56:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:56:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:56:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:56:29 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:56:57 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:56:57 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:56:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596d6c23adc7886652eea636e0c856146cc51d2da380a735645fad034dfe5069`  
		Last Modified: Thu, 19 Dec 2019 06:47:29 GMT  
		Size: 105.1 MB (105052689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07313090020e2216012e1a247dd3e9fce45ffac5a07713c234c1f02718a91a8`  
		Last Modified: Thu, 19 Dec 2019 10:59:36 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d786c8e5ce8bd8e0a4bdfc0ecbde07e01b6607161798b7c5a1f68fd0673aea`  
		Last Modified: Thu, 19 Dec 2019 10:59:47 GMT  
		Size: 48.6 MB (48646474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84476db4b1ac2fc5e552d5bdb3d8247691ea1d57ccbddf9bc83c28455f012d3`  
		Last Modified: Thu, 19 Dec 2019 10:59:43 GMT  
		Size: 95.1 MB (95137274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jdk` - linux; ppc64le

```console
$ docker pull gradle@sha256:de97c2794be05db81624dc748d5f0bf6f774b3746b07e662593263f523fa126e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298448560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229fbb404cae0f708aa5d31816a664d221d3bf69c7a3d1450ba375ef51a3a708`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:18:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:18:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:07:19 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:07:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:07:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:07:41 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:07:44 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:09:21 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:16:56 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:16:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11691fec336d2f0ecf12299c6a2258179b6a03f37e8596ace4bdcf8340a84210`  
		Last Modified: Fri, 08 Nov 2019 02:26:43 GMT  
		Size: 102.2 MB (102223730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9315d5888c26e44dda21265c0782bd2458f9275e893dda525156726db64fd`  
		Last Modified: Fri, 08 Nov 2019 03:18:05 GMT  
		Size: 4.5 KB (4526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f9984d68d74068dfbcdb0f0ec1b51ba5716b1cca72aa6813cfbaae8f333f`  
		Last Modified: Fri, 08 Nov 2019 03:18:18 GMT  
		Size: 56.7 MB (56678368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b2332b39dc868b3d267bf94fca2afd107122993c7dec787be0f95aa7adf3a9`  
		Last Modified: Wed, 20 Nov 2019 00:19:42 GMT  
		Size: 95.1 MB (95137355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jdk` - linux; s390x

```console
$ docker pull gradle@sha256:271543f903e154259439857a293709a845db5d56bed51bb86dc75d8bdc27f92b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614cb05338d916b421497a72794e78adae51687596d0ce1ee3eb69b1ce6d7ab2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:41:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:16:40 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:16:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:16:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:16:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:16:43 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:17:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:33 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75a894e76562f7781c6919af4bc9ab7ff662d7e916f0e18fe1261def191dec`  
		Last Modified: Fri, 08 Nov 2019 02:44:32 GMT  
		Size: 100.7 MB (100734555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b0f50dfaf38af9bcb739cda10fb6a0c7e8610af129e4285b00e833cf63be05`  
		Last Modified: Fri, 08 Nov 2019 03:19:04 GMT  
		Size: 4.5 KB (4497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5fff2ffc2e2c8a9e323c3696a7eacf9842b928e684dfa7cb4b2b577fab52d`  
		Last Modified: Fri, 08 Nov 2019 03:19:14 GMT  
		Size: 48.1 MB (48095072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1a287aa214edc225ccf89f9627b82a3b65d511ae9ffb5a99235667c5c1438d`  
		Last Modified: Tue, 19 Nov 2019 23:42:29 GMT  
		Size: 95.1 MB (95137322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0.1-jdk11`

```console
$ docker pull gradle@sha256:3774e8b27b3904f5b3f776a64fc1641eff6e2a1d7b978ab981dbfd498c84a219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `gradle:6.0.1-jdk11` - linux; amd64

```console
$ docker pull gradle@sha256:88e93f9ef304868cb3ea2925a88631e0574418ee0d85822251c6fb07d2ba5956
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381659710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8041b3ebdc74d94f6cac12012aa7f93d34116255d4352c5c49e9a3c6660b325`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:33 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 06:44:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        armhf)          ESUM='c6b1fda3f8807028cbfcc34a4ded2e8a5a6b6239d2bcc1f06673ea6b1530df94';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.5_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d763481ddc29ac0bdefb24216b3a0bf9afbb058552682567a075f9c0f7da5814';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6dd0c9c8a740e6c19149e98034fba8e368fd9aa16ab417aa636854d40db1a161';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 06:44:47 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 10:57:35 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:57:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:57:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:57:36 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:57:37 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:57:54 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:57:54 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:57:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a5601342fdc19041e774599a3a5f0e49e747e6ff8a02429de43656a48d5790`  
		Last Modified: Thu, 19 Dec 2019 06:48:02 GMT  
		Size: 197.8 MB (197822308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e5f7405ee8015ba4c6a300bf711cdc06c5b4b9c71a4b41890a17408451813`  
		Last Modified: Thu, 19 Dec 2019 11:00:16 GMT  
		Size: 4.5 KB (4491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164260929f249d04eaee3c0c3d0a6530550b0c72731b5a9b7564ab31358d5130`  
		Last Modified: Thu, 19 Dec 2019 11:00:26 GMT  
		Size: 48.6 MB (48646663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867d15ff716dddc670529f5289c20650d5708565c28a30a91fad40531ad252a`  
		Last Modified: Thu, 19 Dec 2019 11:00:29 GMT  
		Size: 95.1 MB (95137275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jdk11` - linux; arm variant v7

```console
$ docker pull gradle@sha256:2d416ac5679ae159bb258e207a11965a562483073dfb108e704ca6cd1f4ad5a9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.7 MB (357653302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63f695b83024fd8f844edaee0188f9014f8d87dd9e58fa62d0d4f9851354cf7`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:34:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 07:34:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:34:55 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 07:35:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        armhf)          ESUM='c6b1fda3f8807028cbfcc34a4ded2e8a5a6b6239d2bcc1f06673ea6b1530df94';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.5_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d763481ddc29ac0bdefb24216b3a0bf9afbb058552682567a075f9c0f7da5814';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6dd0c9c8a740e6c19149e98034fba8e368fd9aa16ab417aa636854d40db1a161';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 07:35:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 07:35:19 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 08:29:10 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 08:29:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 08:29:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 08:29:13 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 08:29:14 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 08:29:48 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:29:50 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 08:29:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 08:30:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70980651c174a0c8207979963c952c66f259507ea151d864bb0642811e77ea`  
		Last Modified: Thu, 19 Dec 2019 07:36:36 GMT  
		Size: 12.3 MB (12267151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fc6791bb8979c7816db2ca64a3b2b4f705b9f8d486ddadc04d4f431aec1f41`  
		Last Modified: Thu, 19 Dec 2019 07:37:06 GMT  
		Size: 184.3 MB (184320655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d8b0c49dae07b6dcf7975dffdcf649ba126faee348d1957e51c5c2e3feaa3d`  
		Last Modified: Thu, 19 Dec 2019 08:31:51 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83a60961b742b02200015d811be575856b3fcf4b5a7153d934be4243a44c4c0`  
		Last Modified: Thu, 19 Dec 2019 08:32:07 GMT  
		Size: 43.6 MB (43611824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4319335b5d5deacb263a647021099fabbab28248a74309fd20207dc884d746a`  
		Last Modified: Thu, 19 Dec 2019 08:32:05 GMT  
		Size: 95.1 MB (95137346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jdk11` - linux; ppc64le

```console
$ docker pull gradle@sha256:70f12a1f674aee3feefbfc2d284b7e703bd68ecf42cd32c737b12b8163691bf9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.4 MB (378437452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05047db2933933dd16087337a9b2310acca4b75687f5312358df5b09f7c0f29f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:19:15 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Fri, 08 Nov 2019 02:19:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        armhf)          ESUM='c6b1fda3f8807028cbfcc34a4ded2e8a5a6b6239d2bcc1f06673ea6b1530df94';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.5_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d763481ddc29ac0bdefb24216b3a0bf9afbb058552682567a075f9c0f7da5814';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6dd0c9c8a740e6c19149e98034fba8e368fd9aa16ab417aa636854d40db1a161';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:19:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 02:19:47 GMT
CMD ["jshell"]
# Fri, 08 Nov 2019 03:12:46 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:12:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:13:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:13:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:13:06 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:14:27 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:17:41 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:17:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0c5021ee48efdfa117eddc0926b74496b28d6472e9baf8355b8e1eab79a960`  
		Last Modified: Fri, 08 Nov 2019 02:27:38 GMT  
		Size: 182.2 MB (182211824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446da082f980cca1cf6accaacf7be5ad870535a7aca6b0bf62924012968da1fb`  
		Last Modified: Fri, 08 Nov 2019 03:19:25 GMT  
		Size: 4.5 KB (4528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bbfbd2811f7e2747a094ab15b3606c9361356d7ebae852dc928a082e6c69c9`  
		Last Modified: Fri, 08 Nov 2019 03:19:40 GMT  
		Size: 56.7 MB (56679199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3aaf4968493c29fb31e5a50e332bd946d937edf2ebf6a53e32fa633b40753d0`  
		Last Modified: Wed, 20 Nov 2019 00:20:51 GMT  
		Size: 95.1 MB (95137320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0.1-jdk13`

```console
$ docker pull gradle@sha256:61e0df286a33ca5bc7e7ae8c3efd352ee15155957cec0389111e8668b4807090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0.1-jdk13` - linux; amd64

```console
$ docker pull gradle@sha256:11954dd10166447cb4bb840f35694c420682ff07e1569041063eac0a5d5a2bc4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.4 MB (392389674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d189a62ff78094fc5e611566a7e7a6370123b2310b68d3472d0af348b8cb8e1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:45:02 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 06:45:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:45:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 06:45:15 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 10:58:32 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:58:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:58:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:58:33 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:58:33 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:58:50 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:58:51 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:58:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:58:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742105205d26a48c4efc794ff9c1727510deda216fdbee70057555daf34604fd`  
		Last Modified: Thu, 19 Dec 2019 06:48:40 GMT  
		Size: 208.6 MB (208552263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8182b82c24e3e5440732e5974f7df0f24f31d634ca694f21a5fb226cfd1cb8`  
		Last Modified: Thu, 19 Dec 2019 11:00:50 GMT  
		Size: 4.5 KB (4491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f925699a0ffe096f0c9c3334f72eed242bae1a1d221d696e5eee915e942b240`  
		Last Modified: Thu, 19 Dec 2019 11:01:00 GMT  
		Size: 48.6 MB (48646666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32be832b61beea577d22980e821aaf75261907d23acf17a858c2cf825658193`  
		Last Modified: Thu, 19 Dec 2019 11:00:57 GMT  
		Size: 95.1 MB (95137281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jdk13` - linux; arm variant v7

```console
$ docker pull gradle@sha256:d8c21bd9a0e57601722b85fcf651268f5ed8b7dcf348b6dd94fd81345ecb467f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366027908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f66c02d7e23a7d370a0778f598e7137897c6bb5b6cf00218790e810bf40655a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:34:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 07:34:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:35:35 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 07:36:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 07:36:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 07:36:16 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 08:30:15 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 08:30:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 08:30:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 08:30:18 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 08:30:19 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 08:31:15 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:31:19 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 08:31:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 08:31:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70980651c174a0c8207979963c952c66f259507ea151d864bb0642811e77ea`  
		Last Modified: Thu, 19 Dec 2019 07:36:36 GMT  
		Size: 12.3 MB (12267151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ea41660b072f1d696ee3eb5e298effdb694ce10c48fcf047fa5c0df2ca5b98`  
		Last Modified: Thu, 19 Dec 2019 07:37:52 GMT  
		Size: 192.7 MB (192694921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270ee4394edc3df6ef7229ddb68d18bf9c520ce8a6bfc008c62c8a69802b113b`  
		Last Modified: Thu, 19 Dec 2019 08:32:15 GMT  
		Size: 4.5 KB (4514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc63704c32cd7ac29da21066502204d5cdf4a0b694358d565e17d7a73bd7b26`  
		Last Modified: Thu, 19 Dec 2019 08:32:31 GMT  
		Size: 43.6 MB (43612152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc3cd42f671600010a75eae9d678051d4563a761e981d50a2cbc68509315882`  
		Last Modified: Thu, 19 Dec 2019 08:32:29 GMT  
		Size: 95.1 MB (95137348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jdk13` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3ac4f5084a175ae3e80beea60ad3db627e8391b8bb01f033a07c118b3cb308c9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.8 MB (384796356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca0a836b8bf140190f5a67b462b6cdcf09e5d2f1968f9471304d34440a811`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:05:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 08:06:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:06:33 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 08:06:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 08:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 08:06:53 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 09:53:11 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 09:53:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 09:53:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 09:53:15 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 09:53:16 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 09:53:53 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:53:56 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 09:53:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 09:54:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f68c9bd344e83976e79975d3e4d867b348f38c6faa51b6a4d5c114ca23134d8`  
		Last Modified: Thu, 19 Dec 2019 08:07:33 GMT  
		Size: 12.7 MB (12732128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c3a85665587cae3d2f91c7df4ac8fffea83ccf3a8ffb7d12b944bc2d914b2`  
		Last Modified: Thu, 19 Dec 2019 08:08:01 GMT  
		Size: 207.0 MB (206970493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d7bb931f919772e247dc0761a62616610b150f87e337757aa31e57bdb09519`  
		Last Modified: Thu, 19 Dec 2019 09:55:22 GMT  
		Size: 4.5 KB (4533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2ee296cb883493cd4794c0e2fa2cb5dd7fea5602eefb9ab93ba077f4cfa74c`  
		Last Modified: Thu, 19 Dec 2019 09:55:36 GMT  
		Size: 46.2 MB (46196943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da117fd38f6ce03f273494eb8d016d4d36520e6279750164688b2aad1728dbb3`  
		Last Modified: Thu, 19 Dec 2019 09:55:33 GMT  
		Size: 95.1 MB (95137307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jdk13` - linux; ppc64le

```console
$ docker pull gradle@sha256:f8508376250fbb0ede28217652d3b900f9e9cc3e5f53ad0165504e9562b755b8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 MB (387317150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e8c445ffd1fb3b19607455199233163d5ae4a8b088be18313771075c7e585`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:20:24 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:20:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 02:20:54 GMT
CMD ["jshell"]
# Tue, 12 Nov 2019 02:04:23 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 02:04:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 02:04:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 02:04:34 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 02:04:38 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 02:06:06 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:18:26 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:18:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:18:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7829f1f9068dd6677f84b0dcb76e331dc711fcb88fb8e11a86489ba3a44144`  
		Last Modified: Fri, 08 Nov 2019 02:28:37 GMT  
		Size: 191.1 MB (191091672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6f52194782c2d3a80798266515900d4e09d7d2e58fdbb54ded2d2412cf9fc1`  
		Last Modified: Tue, 12 Nov 2019 02:11:05 GMT  
		Size: 4.5 KB (4531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777efb823cf8e517eac3a94a3c60ee57cc3d9f7d486408b0c6f6fd59dd3cd975`  
		Last Modified: Tue, 12 Nov 2019 02:11:20 GMT  
		Size: 56.7 MB (56679068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79f7b059907fcfcd7d0fc552d42ffe7e3d305c941f879a5d3b5b1ec07a95968`  
		Last Modified: Wed, 20 Nov 2019 00:21:37 GMT  
		Size: 95.1 MB (95137298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jdk13` - linux; s390x

```console
$ docker pull gradle@sha256:5b817101f77f442cbec9a23ca8877fcc2f6b00078c9943a860a5f7776abd073b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367227784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afe48fdb5418150055e6eaa1370f0276d4b578696994ebb3befd7a61cf9c3eb`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:42:17 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:42:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 02:42:29 GMT
CMD ["jshell"]
# Tue, 12 Nov 2019 00:42:27 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 00:42:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 00:42:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 00:42:29 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 00:42:29 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 00:42:52 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:42:00 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:42:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:42:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0468f77333e3f6ba95c46ae196080bc38eb20b0c14ef070380ec24354e735a8c`  
		Last Modified: Fri, 08 Nov 2019 02:45:08 GMT  
		Size: 185.5 MB (185546389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e871332d1942f2b085cb5a9047c15122420acdc371aca57c7b0c5975fc1ac8`  
		Last Modified: Tue, 12 Nov 2019 00:44:33 GMT  
		Size: 4.5 KB (4499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1ddb84107e1c7c7bac5e70e6a6aeba3f03bcd96cb34ba7921693fc1a54b5a7`  
		Last Modified: Tue, 12 Nov 2019 00:44:43 GMT  
		Size: 48.1 MB (48096956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9818de0a85a705ed4c3390b8bd0854e7c989e7bd2da3080304a2b46eb5eaee`  
		Last Modified: Tue, 19 Nov 2019 23:43:11 GMT  
		Size: 95.1 MB (95137278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0.1-jdk8`

```console
$ docker pull gradle@sha256:8ba20b563ed5c90f4e16705a0590d469190362fffc02dbbe308f05b81a16506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0.1-jdk8` - linux; amd64

```console
$ docker pull gradle@sha256:e5496a08fead0e48822aa86087b9d5f278795586a8588528bc289f0406e8d235
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288889902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc47c2ea2852e1ae6d6756cae8c568b3b255e198d589f81be8835390c6740a2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:56:27 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:56:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:56:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:56:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:56:29 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:56:57 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:56:57 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:56:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596d6c23adc7886652eea636e0c856146cc51d2da380a735645fad034dfe5069`  
		Last Modified: Thu, 19 Dec 2019 06:47:29 GMT  
		Size: 105.1 MB (105052689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07313090020e2216012e1a247dd3e9fce45ffac5a07713c234c1f02718a91a8`  
		Last Modified: Thu, 19 Dec 2019 10:59:36 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d786c8e5ce8bd8e0a4bdfc0ecbde07e01b6607161798b7c5a1f68fd0673aea`  
		Last Modified: Thu, 19 Dec 2019 10:59:47 GMT  
		Size: 48.6 MB (48646474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84476db4b1ac2fc5e552d5bdb3d8247691ea1d57ccbddf9bc83c28455f012d3`  
		Last Modified: Thu, 19 Dec 2019 10:59:43 GMT  
		Size: 95.1 MB (95137274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jdk8` - linux; ppc64le

```console
$ docker pull gradle@sha256:de97c2794be05db81624dc748d5f0bf6f774b3746b07e662593263f523fa126e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298448560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229fbb404cae0f708aa5d31816a664d221d3bf69c7a3d1450ba375ef51a3a708`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:18:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:18:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:07:19 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:07:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:07:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:07:41 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:07:44 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:09:21 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:16:56 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:16:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11691fec336d2f0ecf12299c6a2258179b6a03f37e8596ace4bdcf8340a84210`  
		Last Modified: Fri, 08 Nov 2019 02:26:43 GMT  
		Size: 102.2 MB (102223730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9315d5888c26e44dda21265c0782bd2458f9275e893dda525156726db64fd`  
		Last Modified: Fri, 08 Nov 2019 03:18:05 GMT  
		Size: 4.5 KB (4526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f9984d68d74068dfbcdb0f0ec1b51ba5716b1cca72aa6813cfbaae8f333f`  
		Last Modified: Fri, 08 Nov 2019 03:18:18 GMT  
		Size: 56.7 MB (56678368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b2332b39dc868b3d267bf94fca2afd107122993c7dec787be0f95aa7adf3a9`  
		Last Modified: Wed, 20 Nov 2019 00:19:42 GMT  
		Size: 95.1 MB (95137355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jdk8` - linux; s390x

```console
$ docker pull gradle@sha256:271543f903e154259439857a293709a845db5d56bed51bb86dc75d8bdc27f92b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614cb05338d916b421497a72794e78adae51687596d0ce1ee3eb69b1ce6d7ab2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:41:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:16:40 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:16:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:16:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:16:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:16:43 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:17:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:33 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75a894e76562f7781c6919af4bc9ab7ff662d7e916f0e18fe1261def191dec`  
		Last Modified: Fri, 08 Nov 2019 02:44:32 GMT  
		Size: 100.7 MB (100734555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b0f50dfaf38af9bcb739cda10fb6a0c7e8610af129e4285b00e833cf63be05`  
		Last Modified: Fri, 08 Nov 2019 03:19:04 GMT  
		Size: 4.5 KB (4497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5fff2ffc2e2c8a9e323c3696a7eacf9842b928e684dfa7cb4b2b577fab52d`  
		Last Modified: Fri, 08 Nov 2019 03:19:14 GMT  
		Size: 48.1 MB (48095072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1a287aa214edc225ccf89f9627b82a3b65d511ae9ffb5a99235667c5c1438d`  
		Last Modified: Tue, 19 Nov 2019 23:42:29 GMT  
		Size: 95.1 MB (95137322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0.1-jre`

```console
$ docker pull gradle@sha256:9cc6f3cd0b060375ab2275d2d9009c4f0afdcff215295fe83960c155bdf83ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0.1-jre` - linux; amd64

```console
$ docker pull gradle@sha256:252c4aa523ce210f1384b4c1dbff1833888d54d2ddbc6bc1166907fa53d359bc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225153278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69106a8f82ff8683ecfcdb1fd02a0b14c6c8d7f145ea0efcf5fd6085b5f3263a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:57:07 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:57:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:57:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:57:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:57:08 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:57:26 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:57:26 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:57:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90bb5798781d7d972ceffbb8a018b8d4a6209e6ebffef84b49ae3eb603b83b3`  
		Last Modified: Thu, 19 Dec 2019 06:47:39 GMT  
		Size: 41.3 MB (41315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566cc78d89ca54deaef6f31921a9a0cf09937e4fe868206170480b1ac77f7cba`  
		Last Modified: Thu, 19 Dec 2019 10:59:56 GMT  
		Size: 4.5 KB (4490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52cba128b83aaed76d8e263f0b092bbc645fcebb37d69492f15e17ff3c8dad9`  
		Last Modified: Thu, 19 Dec 2019 11:00:07 GMT  
		Size: 48.6 MB (48646581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc26c95e2e9c68317162517ec85ea42b4c61a7d9068b8e7907d606971e74d56`  
		Last Modified: Thu, 19 Dec 2019 11:00:05 GMT  
		Size: 95.1 MB (95137279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jre` - linux; ppc64le

```console
$ docker pull gradle@sha256:4fb399803b5d67a4e672cfbcb06aefaa2f6e3309ef2e312e5bb320a5a4d7f26b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236621590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ccc6ec0d066910e82f75882d759c6fa535b780ead3c224e7bfad63eda8d8b1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:19:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:10:02 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:10:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:10:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:10:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:10:32 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:11:58 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:17:19 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:17:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ba113a58c3754d98a4cd77c5c3298e88b288fbbc6396e224d48f14a2051737`  
		Last Modified: Fri, 08 Nov 2019 02:27:06 GMT  
		Size: 40.4 MB (40395973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5215135253fc66c5e436a1c7cf0dfca107c7c2efb89e0c36aac6a44180c12616`  
		Last Modified: Fri, 08 Nov 2019 03:18:48 GMT  
		Size: 4.5 KB (4531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450733ab5d7b8c356095a70730cc5719812f0e8e98c7df2a6356d42c00c7e2f4`  
		Last Modified: Fri, 08 Nov 2019 03:19:03 GMT  
		Size: 56.7 MB (56679157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6a148705e89eea028591a3864b03e403b433637492bc5fe9b4f775d5423ecc`  
		Last Modified: Wed, 20 Nov 2019 00:20:21 GMT  
		Size: 95.1 MB (95137348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jre` - linux; s390x

```console
$ docker pull gradle@sha256:991ee619cc20d42a5c55a8c7a5ea05149e41de96f4745c29b69eb370b4155c79
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220684522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3531bbf861e7d285f38a4f9e9adc6b86e12729f7cd94c7ec623d3dee874eba1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:42:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:17:47 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:17:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:17:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:17:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:17:49 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:18:19 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:42 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33c44ac698abb009f50d3e585414a474039b681a90428ee2f4b108705725618`  
		Last Modified: Fri, 08 Nov 2019 02:44:46 GMT  
		Size: 39.0 MB (39004827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b31bf9feb646bd1283f25648587844e48832ba5cf55088429e39cc7de67d8f`  
		Last Modified: Fri, 08 Nov 2019 03:19:28 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f319e5024bfd448efb861ced63b58bcfaf2af7249978af930ef82734bef3e1fb`  
		Last Modified: Fri, 08 Nov 2019 03:19:38 GMT  
		Size: 48.1 MB (48095225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9197ffe30daa470cb2b2d989f05e49aa02894c024920d824aaa6f57b03a13840`  
		Last Modified: Tue, 19 Nov 2019 23:42:46 GMT  
		Size: 95.1 MB (95137300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0.1-jre11`

```console
$ docker pull gradle@sha256:4ef02a0dcc0f9286b920e96502cdc8f736d5dd8238ea0743124082003af8a98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0.1-jre11` - linux; amd64

```console
$ docker pull gradle@sha256:a6ff0139ad814a4440d5625fb62cebde5af4f005c4622cc84bed6079cb116b53
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226690960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294f7c2a658c17259f51748b39df06221cbcd7a902af543f27a32733dbce62e7`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:33 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 06:44:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='2e5343f2046844673f88a4297f5e5796979acb9880b291f965b4c9fa33201d78';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='2f08c469c9a8adea1b6ee3444ba2a8242a7e99d87976a077faf037a9eb7f884b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:58:03 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:58:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:58:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:58:04 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:58:05 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:58:22 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:58:22 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:58:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:58:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8c6504c719a3a083869f0711720d4ad964c9dd22968979cbd6e6155b355c3`  
		Last Modified: Thu, 19 Dec 2019 06:48:16 GMT  
		Size: 42.9 MB (42853646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9a88e172fca720ef5e1c1be9d4ec1ccddb7244cd3f7a149639024c442ad748`  
		Last Modified: Thu, 19 Dec 2019 11:00:34 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6731489a22f40676f442ac3acaf06be19d51ec0a9602093b70ef35f61478f918`  
		Last Modified: Thu, 19 Dec 2019 11:00:45 GMT  
		Size: 48.6 MB (48646554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff73ce0d214daa7269ef8676f2183330965052befaaacefccd9e5d5cb152040d`  
		Last Modified: Thu, 19 Dec 2019 11:00:43 GMT  
		Size: 95.1 MB (95137295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jre11` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7a36234ba72755b3f6e36e8de770aec23ae4c32fed9e62dfae185a36419938eb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219608547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b169fa10c8a26c4773e8751e23d0a72a8086162c90924eba02c7b8c1a8cd98d8`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:58:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Oct 2019 22:59:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 22:59:31 GMT
ENV JAVA_VERSION=jdk-11.0.4+11
# Thu, 31 Oct 2019 22:59:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5f7b5c110fc0f344a549cb11784a6d76838061a2b6f654f7841f60e0cd286c6a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.4_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5da5f86f250eeb26719ba06ae1a1133eb75933fad7b9cf1624d743fafd7a7e2b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.4_11.tar.gz';          ;;        s390x)          ESUM='274036da66b150050e23dfc87a4c0ab5331fa6f0d0804b8016621aedf8d1a1e1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.4_11.tar.gz';          ;;        amd64|x86_64)          ESUM='70d2cc675155476f1d8516a7ae6729d44681e4fad5a6fc8dfa65cab36a67b7e0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.4_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Oct 2019 22:59:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Nov 2019 23:44:27 GMT
CMD ["gradle"]
# Wed, 13 Nov 2019 23:44:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Nov 2019 23:44:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 13 Nov 2019 23:44:31 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Nov 2019 23:44:31 GMT
WORKDIR /home/gradle
# Wed, 13 Nov 2019 23:45:10 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 01:08:50 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 01:08:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 01:09:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb929685f4a20d12d37720cde265d3c645d4ec19fbad4db50c81055be5dc25`  
		Last Modified: Thu, 31 Oct 2019 23:01:25 GMT  
		Size: 10.3 MB (10302431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403ce56eaf5b3e8f6d958819de2613191ecb8d22c81a84c9a17ec1c423b7d4c`  
		Last Modified: Thu, 31 Oct 2019 23:02:56 GMT  
		Size: 41.8 MB (41805533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2f85d224d63a93cc5db3bd7b0d341a81e670c3f42324a2c582ec35b67db249`  
		Last Modified: Wed, 13 Nov 2019 23:47:49 GMT  
		Size: 4.5 KB (4525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d9bc1e8992ab73a596b584cc0566486ad47e2cbfbb1eea0f041b57f96cae07`  
		Last Modified: Wed, 13 Nov 2019 23:48:06 GMT  
		Size: 48.6 MB (48604121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd45752872dacbd1e3a15b33b4fc65c3308b9dadb474d4162ee1b57a6f6f7bde`  
		Last Modified: Wed, 20 Nov 2019 01:10:15 GMT  
		Size: 95.1 MB (95137303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jre11` - linux; ppc64le

```console
$ docker pull gradle@sha256:a8a84eed38970fa312c9dc5699613c1cb7b2888718312466f183f1cebbf6dc95
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235727564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7bcc7c40466cc06f9025d70db225ea78252c1a186233f28ee6fa5be8e2d877`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:19:15 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Fri, 08 Nov 2019 02:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='2e5343f2046844673f88a4297f5e5796979acb9880b291f965b4c9fa33201d78';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='2f08c469c9a8adea1b6ee3444ba2a8242a7e99d87976a077faf037a9eb7f884b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:15:11 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:15:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:15:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:15:28 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:15:29 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:16:55 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:18:04 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:18:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:18:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f71bc3c769bd80c7987467a5821fc6f00e294fb811fe979e0db9e54f56f923`  
		Last Modified: Fri, 08 Nov 2019 02:28:03 GMT  
		Size: 39.5 MB (39502141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7335b89bbecfa0b3d341c3f2560562602ec80820e2f75eafd33703414a9b39`  
		Last Modified: Fri, 08 Nov 2019 03:20:01 GMT  
		Size: 4.5 KB (4519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2fc8ba596f232efb90bfd809db33c9369fae793a2c7d4f384bd9f53d21a5d`  
		Last Modified: Fri, 08 Nov 2019 03:20:15 GMT  
		Size: 56.7 MB (56679024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822497c407117226c58230b2d73ff6f50a0802f0a8c6ca18b84fe87353c65490`  
		Last Modified: Wed, 20 Nov 2019 00:21:14 GMT  
		Size: 95.1 MB (95137299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jre11` - linux; s390x

```console
$ docker pull gradle@sha256:58efd9b105c6804d3aa7bb054918ec3363d37216a46a1abebe14f94927a33a0a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220802607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4146c763017a89f0885c0655fe0f00caf775d5c5fe1b45c39866784d69215fc`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Oct 2019 23:00:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:01:04 GMT
ENV JAVA_VERSION=jdk-11.0.4+11
# Thu, 31 Oct 2019 23:01:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5f7b5c110fc0f344a549cb11784a6d76838061a2b6f654f7841f60e0cd286c6a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.4_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5da5f86f250eeb26719ba06ae1a1133eb75933fad7b9cf1624d743fafd7a7e2b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.4_11.tar.gz';          ;;        s390x)          ESUM='274036da66b150050e23dfc87a4c0ab5331fa6f0d0804b8016621aedf8d1a1e1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.4_11.tar.gz';          ;;        amd64|x86_64)          ESUM='70d2cc675155476f1d8516a7ae6729d44681e4fad5a6fc8dfa65cab36a67b7e0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.4_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Oct 2019 23:01:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2019 00:06:03 GMT
CMD ["gradle"]
# Fri, 01 Nov 2019 00:06:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 01 Nov 2019 00:06:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 01 Nov 2019 00:06:07 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 01 Nov 2019 00:06:12 GMT
WORKDIR /home/gradle
# Fri, 01 Nov 2019 00:07:00 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:51 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d6516ebe93aefa5d84bd151472231fda34a88c02a0c5b2ebdfa62a362ffdb3`  
		Last Modified: Thu, 31 Oct 2019 23:05:58 GMT  
		Size: 10.6 MB (10552908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b8346f33b7a78720e7cd5172e7b4f38a024424cb9dc5daba2b93de5544ff30`  
		Last Modified: Thu, 31 Oct 2019 23:07:19 GMT  
		Size: 39.1 MB (39140065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805900cc5865bfc68379f7c6d998a52143a8dfdd4b0fcf1b01bec462b3e10ef7`  
		Last Modified: Fri, 01 Nov 2019 00:11:20 GMT  
		Size: 4.5 KB (4487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc2b2d13feddb7c6fbb064377df74103abbff926f507978ec46e4bf50eaef0e`  
		Last Modified: Fri, 01 Nov 2019 00:11:32 GMT  
		Size: 50.6 MB (50566020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17211c185452fb28b459fbf936cab64009a4f24441c630e3b25ebb2740d2bca7`  
		Last Modified: Tue, 19 Nov 2019 23:43:00 GMT  
		Size: 95.1 MB (95137301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0.1-jre13`

```console
$ docker pull gradle@sha256:7e5d8822ae3ecd5d5bda18e15d76e05b53cdd97b7828b199f7c7cc7d40efb381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0.1-jre13` - linux; amd64

```console
$ docker pull gradle@sha256:eb2899a8dc83ed1d71b3ea46b8f7712d4a51aecb0c5f51ef794fcbf5c142b022
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230867584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1597227d3129c534858de02c7345ff021f32eae7b81160b38128b14922cab7`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:45:02 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 06:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:58:59 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:59:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:59:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:59:01 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:59:01 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:59:18 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:59:19 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:59:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:59:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c602e7de7b4dc2b103089415bc7f2bcfeb6cef5bce65e56697171f4c28fb0db`  
		Last Modified: Thu, 19 Dec 2019 06:48:54 GMT  
		Size: 47.0 MB (47030224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7591b3257d32942bd82b92ff47965ea3fa268726bc77bae899ccdc1a8b151664`  
		Last Modified: Thu, 19 Dec 2019 11:01:06 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177500b750cd88e2e6ba43c86ceb35e0a07d82399537e8c3ed8092ea1facedcf`  
		Last Modified: Thu, 19 Dec 2019 11:01:16 GMT  
		Size: 48.6 MB (48646601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94567a87645fe8a72aab33f449987caa46f296c200b856261a8eb44c62c9c4cd`  
		Last Modified: Thu, 19 Dec 2019 11:01:12 GMT  
		Size: 95.1 MB (95137294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jre13` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:908295cbe4551c884489890ad453853948016d17973588579a9b0e1adf072b86
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223295867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e3c174b4152a9b26e69e909bbee35e5552d0fbe4ad5d4845e79906765d7dd4`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:05:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 08:06:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:06:33 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 08:07:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 08:07:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 09:54:15 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 09:54:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 09:54:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 09:54:19 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 09:54:20 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 09:54:52 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:54:55 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 09:54:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 09:55:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f68c9bd344e83976e79975d3e4d867b348f38c6faa51b6a4d5c114ca23134d8`  
		Last Modified: Thu, 19 Dec 2019 08:07:33 GMT  
		Size: 12.7 MB (12732128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33f535ea89f1b9ee2d722880cd9fc4e675b0e393fcff76d1e2e723b4697270c`  
		Last Modified: Thu, 19 Dec 2019 08:08:24 GMT  
		Size: 45.5 MB (45469630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612afd22e5bc153b5bc5be67897c663e05529e6b69ae192eecb6c1bae6fbc1ee`  
		Last Modified: Thu, 19 Dec 2019 09:55:44 GMT  
		Size: 4.5 KB (4523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9326b1786a92e9b0f8acfb4668819f54c944a85fae60b64d10dd5b915d5c46`  
		Last Modified: Thu, 19 Dec 2019 09:55:59 GMT  
		Size: 46.2 MB (46197288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af98ba96798f0abc1f4f1b481e1b592e41597a277680066ca9bbf17496bf308`  
		Last Modified: Thu, 19 Dec 2019 09:55:56 GMT  
		Size: 95.1 MB (95137346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jre13` - linux; ppc64le

```console
$ docker pull gradle@sha256:02db8e97c98d331e6c1489d6fab1cc316bb571f8aad5ea6ceaae8d5f7c55e21c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238328456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650fc2a86145ca41cc7d3e70417360c13456f969ee0219009b842b9552657240`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:20:24 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:21:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2019 02:06:50 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 02:06:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 02:06:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 02:07:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 02:07:02 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 02:08:06 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:18:48 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:18:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:19:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37d97458785efed876bd376e84f425f759cc4d9dd81bca6177d094e62f2e371`  
		Last Modified: Fri, 08 Nov 2019 02:29:02 GMT  
		Size: 42.1 MB (42103092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a789ce2eb06d8e276d2e7417fa0f0223b92a0b19717d9bef0ee543d179957eb`  
		Last Modified: Tue, 12 Nov 2019 02:11:33 GMT  
		Size: 4.5 KB (4523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025163cce798cf3ca3e392896fd7713a7a327a74c71eebcb81ac726810bb39e4`  
		Last Modified: Tue, 12 Nov 2019 02:11:53 GMT  
		Size: 56.7 MB (56678908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feec192277bf2d7b06e673409f3e9feffa288ea648c36de641863e54c7fd688c`  
		Last Modified: Wed, 20 Nov 2019 00:22:01 GMT  
		Size: 95.1 MB (95137352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jre13` - linux; s390x

```console
$ docker pull gradle@sha256:66c7c5e1e32191ab79416e3b68e4b75641a47b8351eb09b4f7b9cee6a64102b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223596116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea5359512eced13d27bccd2fb4b47b4dce80c9ce54ac6a06cade6c749a97438`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:42:17 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:42:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2019 00:43:02 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 00:43:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 00:43:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 00:43:03 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 00:43:03 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 00:43:27 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:42:08 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:42:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:42:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1574b9d2915ca440a8df6067210b8b08a83fa5e1b26a947456fe7ce51ac62c79`  
		Last Modified: Fri, 08 Nov 2019 02:45:24 GMT  
		Size: 41.9 MB (41916656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51f59d9f4e9a794f0a5819eb266ba17ab3e031ee74ce4b07f6e0e9f992a9b16`  
		Last Modified: Tue, 12 Nov 2019 00:44:55 GMT  
		Size: 4.5 KB (4499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c9182a8c3317e15fea9b4554a082a526c2c6b2dbe466b8e793e51c1b2ac0c3`  
		Last Modified: Tue, 12 Nov 2019 00:45:06 GMT  
		Size: 48.1 MB (48094976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309103460d533b426ed0b8b98731c7b01e2ed5b2b03792081b92af72e99b9a29`  
		Last Modified: Tue, 19 Nov 2019 23:43:40 GMT  
		Size: 95.1 MB (95137323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0.1-jre8`

```console
$ docker pull gradle@sha256:9cc6f3cd0b060375ab2275d2d9009c4f0afdcff215295fe83960c155bdf83ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0.1-jre8` - linux; amd64

```console
$ docker pull gradle@sha256:252c4aa523ce210f1384b4c1dbff1833888d54d2ddbc6bc1166907fa53d359bc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225153278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69106a8f82ff8683ecfcdb1fd02a0b14c6c8d7f145ea0efcf5fd6085b5f3263a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:57:07 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:57:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:57:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:57:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:57:08 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:57:26 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:57:26 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:57:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90bb5798781d7d972ceffbb8a018b8d4a6209e6ebffef84b49ae3eb603b83b3`  
		Last Modified: Thu, 19 Dec 2019 06:47:39 GMT  
		Size: 41.3 MB (41315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566cc78d89ca54deaef6f31921a9a0cf09937e4fe868206170480b1ac77f7cba`  
		Last Modified: Thu, 19 Dec 2019 10:59:56 GMT  
		Size: 4.5 KB (4490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52cba128b83aaed76d8e263f0b092bbc645fcebb37d69492f15e17ff3c8dad9`  
		Last Modified: Thu, 19 Dec 2019 11:00:07 GMT  
		Size: 48.6 MB (48646581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc26c95e2e9c68317162517ec85ea42b4c61a7d9068b8e7907d606971e74d56`  
		Last Modified: Thu, 19 Dec 2019 11:00:05 GMT  
		Size: 95.1 MB (95137279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jre8` - linux; ppc64le

```console
$ docker pull gradle@sha256:4fb399803b5d67a4e672cfbcb06aefaa2f6e3309ef2e312e5bb320a5a4d7f26b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236621590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ccc6ec0d066910e82f75882d759c6fa535b780ead3c224e7bfad63eda8d8b1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:19:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:10:02 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:10:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:10:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:10:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:10:32 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:11:58 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:17:19 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:17:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ba113a58c3754d98a4cd77c5c3298e88b288fbbc6396e224d48f14a2051737`  
		Last Modified: Fri, 08 Nov 2019 02:27:06 GMT  
		Size: 40.4 MB (40395973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5215135253fc66c5e436a1c7cf0dfca107c7c2efb89e0c36aac6a44180c12616`  
		Last Modified: Fri, 08 Nov 2019 03:18:48 GMT  
		Size: 4.5 KB (4531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450733ab5d7b8c356095a70730cc5719812f0e8e98c7df2a6356d42c00c7e2f4`  
		Last Modified: Fri, 08 Nov 2019 03:19:03 GMT  
		Size: 56.7 MB (56679157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6a148705e89eea028591a3864b03e403b433637492bc5fe9b4f775d5423ecc`  
		Last Modified: Wed, 20 Nov 2019 00:20:21 GMT  
		Size: 95.1 MB (95137348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0.1-jre8` - linux; s390x

```console
$ docker pull gradle@sha256:991ee619cc20d42a5c55a8c7a5ea05149e41de96f4745c29b69eb370b4155c79
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220684522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3531bbf861e7d285f38a4f9e9adc6b86e12729f7cd94c7ec623d3dee874eba1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:42:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:17:47 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:17:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:17:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:17:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:17:49 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:18:19 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:42 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33c44ac698abb009f50d3e585414a474039b681a90428ee2f4b108705725618`  
		Last Modified: Fri, 08 Nov 2019 02:44:46 GMT  
		Size: 39.0 MB (39004827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b31bf9feb646bd1283f25648587844e48832ba5cf55088429e39cc7de67d8f`  
		Last Modified: Fri, 08 Nov 2019 03:19:28 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f319e5024bfd448efb861ced63b58bcfaf2af7249978af930ef82734bef3e1fb`  
		Last Modified: Fri, 08 Nov 2019 03:19:38 GMT  
		Size: 48.1 MB (48095225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9197ffe30daa470cb2b2d989f05e49aa02894c024920d824aaa6f57b03a13840`  
		Last Modified: Tue, 19 Nov 2019 23:42:46 GMT  
		Size: 95.1 MB (95137300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0-jdk`

```console
$ docker pull gradle@sha256:8ba20b563ed5c90f4e16705a0590d469190362fffc02dbbe308f05b81a16506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0-jdk` - linux; amd64

```console
$ docker pull gradle@sha256:e5496a08fead0e48822aa86087b9d5f278795586a8588528bc289f0406e8d235
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288889902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc47c2ea2852e1ae6d6756cae8c568b3b255e198d589f81be8835390c6740a2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:56:27 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:56:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:56:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:56:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:56:29 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:56:57 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:56:57 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:56:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596d6c23adc7886652eea636e0c856146cc51d2da380a735645fad034dfe5069`  
		Last Modified: Thu, 19 Dec 2019 06:47:29 GMT  
		Size: 105.1 MB (105052689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07313090020e2216012e1a247dd3e9fce45ffac5a07713c234c1f02718a91a8`  
		Last Modified: Thu, 19 Dec 2019 10:59:36 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d786c8e5ce8bd8e0a4bdfc0ecbde07e01b6607161798b7c5a1f68fd0673aea`  
		Last Modified: Thu, 19 Dec 2019 10:59:47 GMT  
		Size: 48.6 MB (48646474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84476db4b1ac2fc5e552d5bdb3d8247691ea1d57ccbddf9bc83c28455f012d3`  
		Last Modified: Thu, 19 Dec 2019 10:59:43 GMT  
		Size: 95.1 MB (95137274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jdk` - linux; ppc64le

```console
$ docker pull gradle@sha256:de97c2794be05db81624dc748d5f0bf6f774b3746b07e662593263f523fa126e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298448560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229fbb404cae0f708aa5d31816a664d221d3bf69c7a3d1450ba375ef51a3a708`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:18:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:18:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:07:19 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:07:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:07:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:07:41 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:07:44 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:09:21 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:16:56 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:16:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11691fec336d2f0ecf12299c6a2258179b6a03f37e8596ace4bdcf8340a84210`  
		Last Modified: Fri, 08 Nov 2019 02:26:43 GMT  
		Size: 102.2 MB (102223730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9315d5888c26e44dda21265c0782bd2458f9275e893dda525156726db64fd`  
		Last Modified: Fri, 08 Nov 2019 03:18:05 GMT  
		Size: 4.5 KB (4526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f9984d68d74068dfbcdb0f0ec1b51ba5716b1cca72aa6813cfbaae8f333f`  
		Last Modified: Fri, 08 Nov 2019 03:18:18 GMT  
		Size: 56.7 MB (56678368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b2332b39dc868b3d267bf94fca2afd107122993c7dec787be0f95aa7adf3a9`  
		Last Modified: Wed, 20 Nov 2019 00:19:42 GMT  
		Size: 95.1 MB (95137355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jdk` - linux; s390x

```console
$ docker pull gradle@sha256:271543f903e154259439857a293709a845db5d56bed51bb86dc75d8bdc27f92b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614cb05338d916b421497a72794e78adae51687596d0ce1ee3eb69b1ce6d7ab2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:41:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:16:40 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:16:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:16:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:16:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:16:43 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:17:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:33 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75a894e76562f7781c6919af4bc9ab7ff662d7e916f0e18fe1261def191dec`  
		Last Modified: Fri, 08 Nov 2019 02:44:32 GMT  
		Size: 100.7 MB (100734555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b0f50dfaf38af9bcb739cda10fb6a0c7e8610af129e4285b00e833cf63be05`  
		Last Modified: Fri, 08 Nov 2019 03:19:04 GMT  
		Size: 4.5 KB (4497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5fff2ffc2e2c8a9e323c3696a7eacf9842b928e684dfa7cb4b2b577fab52d`  
		Last Modified: Fri, 08 Nov 2019 03:19:14 GMT  
		Size: 48.1 MB (48095072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1a287aa214edc225ccf89f9627b82a3b65d511ae9ffb5a99235667c5c1438d`  
		Last Modified: Tue, 19 Nov 2019 23:42:29 GMT  
		Size: 95.1 MB (95137322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0-jdk11`

```console
$ docker pull gradle@sha256:3774e8b27b3904f5b3f776a64fc1641eff6e2a1d7b978ab981dbfd498c84a219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `gradle:6.0-jdk11` - linux; amd64

```console
$ docker pull gradle@sha256:88e93f9ef304868cb3ea2925a88631e0574418ee0d85822251c6fb07d2ba5956
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381659710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8041b3ebdc74d94f6cac12012aa7f93d34116255d4352c5c49e9a3c6660b325`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:33 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 06:44:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        armhf)          ESUM='c6b1fda3f8807028cbfcc34a4ded2e8a5a6b6239d2bcc1f06673ea6b1530df94';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.5_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d763481ddc29ac0bdefb24216b3a0bf9afbb058552682567a075f9c0f7da5814';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6dd0c9c8a740e6c19149e98034fba8e368fd9aa16ab417aa636854d40db1a161';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 06:44:47 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 10:57:35 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:57:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:57:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:57:36 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:57:37 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:57:54 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:57:54 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:57:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a5601342fdc19041e774599a3a5f0e49e747e6ff8a02429de43656a48d5790`  
		Last Modified: Thu, 19 Dec 2019 06:48:02 GMT  
		Size: 197.8 MB (197822308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e5f7405ee8015ba4c6a300bf711cdc06c5b4b9c71a4b41890a17408451813`  
		Last Modified: Thu, 19 Dec 2019 11:00:16 GMT  
		Size: 4.5 KB (4491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164260929f249d04eaee3c0c3d0a6530550b0c72731b5a9b7564ab31358d5130`  
		Last Modified: Thu, 19 Dec 2019 11:00:26 GMT  
		Size: 48.6 MB (48646663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867d15ff716dddc670529f5289c20650d5708565c28a30a91fad40531ad252a`  
		Last Modified: Thu, 19 Dec 2019 11:00:29 GMT  
		Size: 95.1 MB (95137275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jdk11` - linux; arm variant v7

```console
$ docker pull gradle@sha256:2d416ac5679ae159bb258e207a11965a562483073dfb108e704ca6cd1f4ad5a9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.7 MB (357653302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63f695b83024fd8f844edaee0188f9014f8d87dd9e58fa62d0d4f9851354cf7`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:34:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 07:34:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:34:55 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 07:35:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        armhf)          ESUM='c6b1fda3f8807028cbfcc34a4ded2e8a5a6b6239d2bcc1f06673ea6b1530df94';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.5_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d763481ddc29ac0bdefb24216b3a0bf9afbb058552682567a075f9c0f7da5814';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6dd0c9c8a740e6c19149e98034fba8e368fd9aa16ab417aa636854d40db1a161';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 07:35:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 07:35:19 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 08:29:10 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 08:29:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 08:29:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 08:29:13 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 08:29:14 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 08:29:48 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:29:50 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 08:29:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 08:30:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70980651c174a0c8207979963c952c66f259507ea151d864bb0642811e77ea`  
		Last Modified: Thu, 19 Dec 2019 07:36:36 GMT  
		Size: 12.3 MB (12267151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fc6791bb8979c7816db2ca64a3b2b4f705b9f8d486ddadc04d4f431aec1f41`  
		Last Modified: Thu, 19 Dec 2019 07:37:06 GMT  
		Size: 184.3 MB (184320655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d8b0c49dae07b6dcf7975dffdcf649ba126faee348d1957e51c5c2e3feaa3d`  
		Last Modified: Thu, 19 Dec 2019 08:31:51 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83a60961b742b02200015d811be575856b3fcf4b5a7153d934be4243a44c4c0`  
		Last Modified: Thu, 19 Dec 2019 08:32:07 GMT  
		Size: 43.6 MB (43611824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4319335b5d5deacb263a647021099fabbab28248a74309fd20207dc884d746a`  
		Last Modified: Thu, 19 Dec 2019 08:32:05 GMT  
		Size: 95.1 MB (95137346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jdk11` - linux; ppc64le

```console
$ docker pull gradle@sha256:70f12a1f674aee3feefbfc2d284b7e703bd68ecf42cd32c737b12b8163691bf9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.4 MB (378437452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05047db2933933dd16087337a9b2310acca4b75687f5312358df5b09f7c0f29f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:19:15 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Fri, 08 Nov 2019 02:19:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        armhf)          ESUM='c6b1fda3f8807028cbfcc34a4ded2e8a5a6b6239d2bcc1f06673ea6b1530df94';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.5_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d763481ddc29ac0bdefb24216b3a0bf9afbb058552682567a075f9c0f7da5814';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6dd0c9c8a740e6c19149e98034fba8e368fd9aa16ab417aa636854d40db1a161';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:19:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 02:19:47 GMT
CMD ["jshell"]
# Fri, 08 Nov 2019 03:12:46 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:12:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:13:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:13:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:13:06 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:14:27 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:17:41 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:17:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0c5021ee48efdfa117eddc0926b74496b28d6472e9baf8355b8e1eab79a960`  
		Last Modified: Fri, 08 Nov 2019 02:27:38 GMT  
		Size: 182.2 MB (182211824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446da082f980cca1cf6accaacf7be5ad870535a7aca6b0bf62924012968da1fb`  
		Last Modified: Fri, 08 Nov 2019 03:19:25 GMT  
		Size: 4.5 KB (4528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bbfbd2811f7e2747a094ab15b3606c9361356d7ebae852dc928a082e6c69c9`  
		Last Modified: Fri, 08 Nov 2019 03:19:40 GMT  
		Size: 56.7 MB (56679199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3aaf4968493c29fb31e5a50e332bd946d937edf2ebf6a53e32fa633b40753d0`  
		Last Modified: Wed, 20 Nov 2019 00:20:51 GMT  
		Size: 95.1 MB (95137320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0-jdk13`

```console
$ docker pull gradle@sha256:61e0df286a33ca5bc7e7ae8c3efd352ee15155957cec0389111e8668b4807090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0-jdk13` - linux; amd64

```console
$ docker pull gradle@sha256:11954dd10166447cb4bb840f35694c420682ff07e1569041063eac0a5d5a2bc4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.4 MB (392389674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d189a62ff78094fc5e611566a7e7a6370123b2310b68d3472d0af348b8cb8e1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:45:02 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 06:45:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:45:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 06:45:15 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 10:58:32 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:58:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:58:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:58:33 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:58:33 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:58:50 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:58:51 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:58:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:58:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742105205d26a48c4efc794ff9c1727510deda216fdbee70057555daf34604fd`  
		Last Modified: Thu, 19 Dec 2019 06:48:40 GMT  
		Size: 208.6 MB (208552263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8182b82c24e3e5440732e5974f7df0f24f31d634ca694f21a5fb226cfd1cb8`  
		Last Modified: Thu, 19 Dec 2019 11:00:50 GMT  
		Size: 4.5 KB (4491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f925699a0ffe096f0c9c3334f72eed242bae1a1d221d696e5eee915e942b240`  
		Last Modified: Thu, 19 Dec 2019 11:01:00 GMT  
		Size: 48.6 MB (48646666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32be832b61beea577d22980e821aaf75261907d23acf17a858c2cf825658193`  
		Last Modified: Thu, 19 Dec 2019 11:00:57 GMT  
		Size: 95.1 MB (95137281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jdk13` - linux; arm variant v7

```console
$ docker pull gradle@sha256:d8c21bd9a0e57601722b85fcf651268f5ed8b7dcf348b6dd94fd81345ecb467f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366027908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f66c02d7e23a7d370a0778f598e7137897c6bb5b6cf00218790e810bf40655a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:34:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 07:34:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:35:35 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 07:36:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 07:36:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 07:36:16 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 08:30:15 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 08:30:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 08:30:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 08:30:18 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 08:30:19 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 08:31:15 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:31:19 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 08:31:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 08:31:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70980651c174a0c8207979963c952c66f259507ea151d864bb0642811e77ea`  
		Last Modified: Thu, 19 Dec 2019 07:36:36 GMT  
		Size: 12.3 MB (12267151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ea41660b072f1d696ee3eb5e298effdb694ce10c48fcf047fa5c0df2ca5b98`  
		Last Modified: Thu, 19 Dec 2019 07:37:52 GMT  
		Size: 192.7 MB (192694921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270ee4394edc3df6ef7229ddb68d18bf9c520ce8a6bfc008c62c8a69802b113b`  
		Last Modified: Thu, 19 Dec 2019 08:32:15 GMT  
		Size: 4.5 KB (4514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc63704c32cd7ac29da21066502204d5cdf4a0b694358d565e17d7a73bd7b26`  
		Last Modified: Thu, 19 Dec 2019 08:32:31 GMT  
		Size: 43.6 MB (43612152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc3cd42f671600010a75eae9d678051d4563a761e981d50a2cbc68509315882`  
		Last Modified: Thu, 19 Dec 2019 08:32:29 GMT  
		Size: 95.1 MB (95137348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jdk13` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3ac4f5084a175ae3e80beea60ad3db627e8391b8bb01f033a07c118b3cb308c9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.8 MB (384796356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca0a836b8bf140190f5a67b462b6cdcf09e5d2f1968f9471304d34440a811`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:05:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 08:06:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:06:33 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 08:06:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 08:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 08:06:53 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 09:53:11 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 09:53:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 09:53:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 09:53:15 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 09:53:16 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 09:53:53 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:53:56 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 09:53:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 09:54:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f68c9bd344e83976e79975d3e4d867b348f38c6faa51b6a4d5c114ca23134d8`  
		Last Modified: Thu, 19 Dec 2019 08:07:33 GMT  
		Size: 12.7 MB (12732128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c3a85665587cae3d2f91c7df4ac8fffea83ccf3a8ffb7d12b944bc2d914b2`  
		Last Modified: Thu, 19 Dec 2019 08:08:01 GMT  
		Size: 207.0 MB (206970493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d7bb931f919772e247dc0761a62616610b150f87e337757aa31e57bdb09519`  
		Last Modified: Thu, 19 Dec 2019 09:55:22 GMT  
		Size: 4.5 KB (4533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2ee296cb883493cd4794c0e2fa2cb5dd7fea5602eefb9ab93ba077f4cfa74c`  
		Last Modified: Thu, 19 Dec 2019 09:55:36 GMT  
		Size: 46.2 MB (46196943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da117fd38f6ce03f273494eb8d016d4d36520e6279750164688b2aad1728dbb3`  
		Last Modified: Thu, 19 Dec 2019 09:55:33 GMT  
		Size: 95.1 MB (95137307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jdk13` - linux; ppc64le

```console
$ docker pull gradle@sha256:f8508376250fbb0ede28217652d3b900f9e9cc3e5f53ad0165504e9562b755b8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 MB (387317150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e8c445ffd1fb3b19607455199233163d5ae4a8b088be18313771075c7e585`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:20:24 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:20:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 02:20:54 GMT
CMD ["jshell"]
# Tue, 12 Nov 2019 02:04:23 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 02:04:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 02:04:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 02:04:34 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 02:04:38 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 02:06:06 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:18:26 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:18:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:18:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7829f1f9068dd6677f84b0dcb76e331dc711fcb88fb8e11a86489ba3a44144`  
		Last Modified: Fri, 08 Nov 2019 02:28:37 GMT  
		Size: 191.1 MB (191091672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6f52194782c2d3a80798266515900d4e09d7d2e58fdbb54ded2d2412cf9fc1`  
		Last Modified: Tue, 12 Nov 2019 02:11:05 GMT  
		Size: 4.5 KB (4531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777efb823cf8e517eac3a94a3c60ee57cc3d9f7d486408b0c6f6fd59dd3cd975`  
		Last Modified: Tue, 12 Nov 2019 02:11:20 GMT  
		Size: 56.7 MB (56679068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79f7b059907fcfcd7d0fc552d42ffe7e3d305c941f879a5d3b5b1ec07a95968`  
		Last Modified: Wed, 20 Nov 2019 00:21:37 GMT  
		Size: 95.1 MB (95137298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jdk13` - linux; s390x

```console
$ docker pull gradle@sha256:5b817101f77f442cbec9a23ca8877fcc2f6b00078c9943a860a5f7776abd073b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367227784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afe48fdb5418150055e6eaa1370f0276d4b578696994ebb3befd7a61cf9c3eb`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:42:17 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:42:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 02:42:29 GMT
CMD ["jshell"]
# Tue, 12 Nov 2019 00:42:27 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 00:42:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 00:42:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 00:42:29 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 00:42:29 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 00:42:52 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:42:00 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:42:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:42:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0468f77333e3f6ba95c46ae196080bc38eb20b0c14ef070380ec24354e735a8c`  
		Last Modified: Fri, 08 Nov 2019 02:45:08 GMT  
		Size: 185.5 MB (185546389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e871332d1942f2b085cb5a9047c15122420acdc371aca57c7b0c5975fc1ac8`  
		Last Modified: Tue, 12 Nov 2019 00:44:33 GMT  
		Size: 4.5 KB (4499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1ddb84107e1c7c7bac5e70e6a6aeba3f03bcd96cb34ba7921693fc1a54b5a7`  
		Last Modified: Tue, 12 Nov 2019 00:44:43 GMT  
		Size: 48.1 MB (48096956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9818de0a85a705ed4c3390b8bd0854e7c989e7bd2da3080304a2b46eb5eaee`  
		Last Modified: Tue, 19 Nov 2019 23:43:11 GMT  
		Size: 95.1 MB (95137278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0-jdk8`

```console
$ docker pull gradle@sha256:8ba20b563ed5c90f4e16705a0590d469190362fffc02dbbe308f05b81a16506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0-jdk8` - linux; amd64

```console
$ docker pull gradle@sha256:e5496a08fead0e48822aa86087b9d5f278795586a8588528bc289f0406e8d235
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288889902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc47c2ea2852e1ae6d6756cae8c568b3b255e198d589f81be8835390c6740a2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:56:27 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:56:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:56:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:56:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:56:29 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:56:57 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:56:57 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:56:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596d6c23adc7886652eea636e0c856146cc51d2da380a735645fad034dfe5069`  
		Last Modified: Thu, 19 Dec 2019 06:47:29 GMT  
		Size: 105.1 MB (105052689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07313090020e2216012e1a247dd3e9fce45ffac5a07713c234c1f02718a91a8`  
		Last Modified: Thu, 19 Dec 2019 10:59:36 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d786c8e5ce8bd8e0a4bdfc0ecbde07e01b6607161798b7c5a1f68fd0673aea`  
		Last Modified: Thu, 19 Dec 2019 10:59:47 GMT  
		Size: 48.6 MB (48646474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84476db4b1ac2fc5e552d5bdb3d8247691ea1d57ccbddf9bc83c28455f012d3`  
		Last Modified: Thu, 19 Dec 2019 10:59:43 GMT  
		Size: 95.1 MB (95137274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jdk8` - linux; ppc64le

```console
$ docker pull gradle@sha256:de97c2794be05db81624dc748d5f0bf6f774b3746b07e662593263f523fa126e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298448560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229fbb404cae0f708aa5d31816a664d221d3bf69c7a3d1450ba375ef51a3a708`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:18:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:18:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:07:19 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:07:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:07:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:07:41 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:07:44 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:09:21 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:16:56 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:16:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11691fec336d2f0ecf12299c6a2258179b6a03f37e8596ace4bdcf8340a84210`  
		Last Modified: Fri, 08 Nov 2019 02:26:43 GMT  
		Size: 102.2 MB (102223730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9315d5888c26e44dda21265c0782bd2458f9275e893dda525156726db64fd`  
		Last Modified: Fri, 08 Nov 2019 03:18:05 GMT  
		Size: 4.5 KB (4526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f9984d68d74068dfbcdb0f0ec1b51ba5716b1cca72aa6813cfbaae8f333f`  
		Last Modified: Fri, 08 Nov 2019 03:18:18 GMT  
		Size: 56.7 MB (56678368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b2332b39dc868b3d267bf94fca2afd107122993c7dec787be0f95aa7adf3a9`  
		Last Modified: Wed, 20 Nov 2019 00:19:42 GMT  
		Size: 95.1 MB (95137355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jdk8` - linux; s390x

```console
$ docker pull gradle@sha256:271543f903e154259439857a293709a845db5d56bed51bb86dc75d8bdc27f92b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614cb05338d916b421497a72794e78adae51687596d0ce1ee3eb69b1ce6d7ab2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:41:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:16:40 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:16:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:16:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:16:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:16:43 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:17:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:33 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75a894e76562f7781c6919af4bc9ab7ff662d7e916f0e18fe1261def191dec`  
		Last Modified: Fri, 08 Nov 2019 02:44:32 GMT  
		Size: 100.7 MB (100734555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b0f50dfaf38af9bcb739cda10fb6a0c7e8610af129e4285b00e833cf63be05`  
		Last Modified: Fri, 08 Nov 2019 03:19:04 GMT  
		Size: 4.5 KB (4497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5fff2ffc2e2c8a9e323c3696a7eacf9842b928e684dfa7cb4b2b577fab52d`  
		Last Modified: Fri, 08 Nov 2019 03:19:14 GMT  
		Size: 48.1 MB (48095072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1a287aa214edc225ccf89f9627b82a3b65d511ae9ffb5a99235667c5c1438d`  
		Last Modified: Tue, 19 Nov 2019 23:42:29 GMT  
		Size: 95.1 MB (95137322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0-jre`

```console
$ docker pull gradle@sha256:9cc6f3cd0b060375ab2275d2d9009c4f0afdcff215295fe83960c155bdf83ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0-jre` - linux; amd64

```console
$ docker pull gradle@sha256:252c4aa523ce210f1384b4c1dbff1833888d54d2ddbc6bc1166907fa53d359bc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225153278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69106a8f82ff8683ecfcdb1fd02a0b14c6c8d7f145ea0efcf5fd6085b5f3263a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:57:07 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:57:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:57:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:57:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:57:08 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:57:26 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:57:26 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:57:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90bb5798781d7d972ceffbb8a018b8d4a6209e6ebffef84b49ae3eb603b83b3`  
		Last Modified: Thu, 19 Dec 2019 06:47:39 GMT  
		Size: 41.3 MB (41315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566cc78d89ca54deaef6f31921a9a0cf09937e4fe868206170480b1ac77f7cba`  
		Last Modified: Thu, 19 Dec 2019 10:59:56 GMT  
		Size: 4.5 KB (4490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52cba128b83aaed76d8e263f0b092bbc645fcebb37d69492f15e17ff3c8dad9`  
		Last Modified: Thu, 19 Dec 2019 11:00:07 GMT  
		Size: 48.6 MB (48646581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc26c95e2e9c68317162517ec85ea42b4c61a7d9068b8e7907d606971e74d56`  
		Last Modified: Thu, 19 Dec 2019 11:00:05 GMT  
		Size: 95.1 MB (95137279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jre` - linux; ppc64le

```console
$ docker pull gradle@sha256:4fb399803b5d67a4e672cfbcb06aefaa2f6e3309ef2e312e5bb320a5a4d7f26b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236621590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ccc6ec0d066910e82f75882d759c6fa535b780ead3c224e7bfad63eda8d8b1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:19:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:10:02 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:10:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:10:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:10:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:10:32 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:11:58 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:17:19 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:17:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ba113a58c3754d98a4cd77c5c3298e88b288fbbc6396e224d48f14a2051737`  
		Last Modified: Fri, 08 Nov 2019 02:27:06 GMT  
		Size: 40.4 MB (40395973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5215135253fc66c5e436a1c7cf0dfca107c7c2efb89e0c36aac6a44180c12616`  
		Last Modified: Fri, 08 Nov 2019 03:18:48 GMT  
		Size: 4.5 KB (4531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450733ab5d7b8c356095a70730cc5719812f0e8e98c7df2a6356d42c00c7e2f4`  
		Last Modified: Fri, 08 Nov 2019 03:19:03 GMT  
		Size: 56.7 MB (56679157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6a148705e89eea028591a3864b03e403b433637492bc5fe9b4f775d5423ecc`  
		Last Modified: Wed, 20 Nov 2019 00:20:21 GMT  
		Size: 95.1 MB (95137348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jre` - linux; s390x

```console
$ docker pull gradle@sha256:991ee619cc20d42a5c55a8c7a5ea05149e41de96f4745c29b69eb370b4155c79
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220684522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3531bbf861e7d285f38a4f9e9adc6b86e12729f7cd94c7ec623d3dee874eba1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:42:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:17:47 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:17:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:17:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:17:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:17:49 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:18:19 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:42 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33c44ac698abb009f50d3e585414a474039b681a90428ee2f4b108705725618`  
		Last Modified: Fri, 08 Nov 2019 02:44:46 GMT  
		Size: 39.0 MB (39004827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b31bf9feb646bd1283f25648587844e48832ba5cf55088429e39cc7de67d8f`  
		Last Modified: Fri, 08 Nov 2019 03:19:28 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f319e5024bfd448efb861ced63b58bcfaf2af7249978af930ef82734bef3e1fb`  
		Last Modified: Fri, 08 Nov 2019 03:19:38 GMT  
		Size: 48.1 MB (48095225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9197ffe30daa470cb2b2d989f05e49aa02894c024920d824aaa6f57b03a13840`  
		Last Modified: Tue, 19 Nov 2019 23:42:46 GMT  
		Size: 95.1 MB (95137300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0-jre11`

```console
$ docker pull gradle@sha256:4ef02a0dcc0f9286b920e96502cdc8f736d5dd8238ea0743124082003af8a98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0-jre11` - linux; amd64

```console
$ docker pull gradle@sha256:a6ff0139ad814a4440d5625fb62cebde5af4f005c4622cc84bed6079cb116b53
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226690960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294f7c2a658c17259f51748b39df06221cbcd7a902af543f27a32733dbce62e7`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:33 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 06:44:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='2e5343f2046844673f88a4297f5e5796979acb9880b291f965b4c9fa33201d78';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='2f08c469c9a8adea1b6ee3444ba2a8242a7e99d87976a077faf037a9eb7f884b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:58:03 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:58:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:58:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:58:04 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:58:05 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:58:22 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:58:22 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:58:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:58:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8c6504c719a3a083869f0711720d4ad964c9dd22968979cbd6e6155b355c3`  
		Last Modified: Thu, 19 Dec 2019 06:48:16 GMT  
		Size: 42.9 MB (42853646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9a88e172fca720ef5e1c1be9d4ec1ccddb7244cd3f7a149639024c442ad748`  
		Last Modified: Thu, 19 Dec 2019 11:00:34 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6731489a22f40676f442ac3acaf06be19d51ec0a9602093b70ef35f61478f918`  
		Last Modified: Thu, 19 Dec 2019 11:00:45 GMT  
		Size: 48.6 MB (48646554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff73ce0d214daa7269ef8676f2183330965052befaaacefccd9e5d5cb152040d`  
		Last Modified: Thu, 19 Dec 2019 11:00:43 GMT  
		Size: 95.1 MB (95137295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jre11` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7a36234ba72755b3f6e36e8de770aec23ae4c32fed9e62dfae185a36419938eb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219608547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b169fa10c8a26c4773e8751e23d0a72a8086162c90924eba02c7b8c1a8cd98d8`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:58:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Oct 2019 22:59:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 22:59:31 GMT
ENV JAVA_VERSION=jdk-11.0.4+11
# Thu, 31 Oct 2019 22:59:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5f7b5c110fc0f344a549cb11784a6d76838061a2b6f654f7841f60e0cd286c6a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.4_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5da5f86f250eeb26719ba06ae1a1133eb75933fad7b9cf1624d743fafd7a7e2b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.4_11.tar.gz';          ;;        s390x)          ESUM='274036da66b150050e23dfc87a4c0ab5331fa6f0d0804b8016621aedf8d1a1e1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.4_11.tar.gz';          ;;        amd64|x86_64)          ESUM='70d2cc675155476f1d8516a7ae6729d44681e4fad5a6fc8dfa65cab36a67b7e0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.4_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Oct 2019 22:59:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Nov 2019 23:44:27 GMT
CMD ["gradle"]
# Wed, 13 Nov 2019 23:44:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Nov 2019 23:44:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 13 Nov 2019 23:44:31 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Nov 2019 23:44:31 GMT
WORKDIR /home/gradle
# Wed, 13 Nov 2019 23:45:10 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 01:08:50 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 01:08:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 01:09:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb929685f4a20d12d37720cde265d3c645d4ec19fbad4db50c81055be5dc25`  
		Last Modified: Thu, 31 Oct 2019 23:01:25 GMT  
		Size: 10.3 MB (10302431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403ce56eaf5b3e8f6d958819de2613191ecb8d22c81a84c9a17ec1c423b7d4c`  
		Last Modified: Thu, 31 Oct 2019 23:02:56 GMT  
		Size: 41.8 MB (41805533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2f85d224d63a93cc5db3bd7b0d341a81e670c3f42324a2c582ec35b67db249`  
		Last Modified: Wed, 13 Nov 2019 23:47:49 GMT  
		Size: 4.5 KB (4525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d9bc1e8992ab73a596b584cc0566486ad47e2cbfbb1eea0f041b57f96cae07`  
		Last Modified: Wed, 13 Nov 2019 23:48:06 GMT  
		Size: 48.6 MB (48604121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd45752872dacbd1e3a15b33b4fc65c3308b9dadb474d4162ee1b57a6f6f7bde`  
		Last Modified: Wed, 20 Nov 2019 01:10:15 GMT  
		Size: 95.1 MB (95137303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jre11` - linux; ppc64le

```console
$ docker pull gradle@sha256:a8a84eed38970fa312c9dc5699613c1cb7b2888718312466f183f1cebbf6dc95
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235727564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7bcc7c40466cc06f9025d70db225ea78252c1a186233f28ee6fa5be8e2d877`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:19:15 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Fri, 08 Nov 2019 02:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='2e5343f2046844673f88a4297f5e5796979acb9880b291f965b4c9fa33201d78';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='2f08c469c9a8adea1b6ee3444ba2a8242a7e99d87976a077faf037a9eb7f884b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:15:11 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:15:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:15:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:15:28 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:15:29 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:16:55 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:18:04 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:18:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:18:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f71bc3c769bd80c7987467a5821fc6f00e294fb811fe979e0db9e54f56f923`  
		Last Modified: Fri, 08 Nov 2019 02:28:03 GMT  
		Size: 39.5 MB (39502141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7335b89bbecfa0b3d341c3f2560562602ec80820e2f75eafd33703414a9b39`  
		Last Modified: Fri, 08 Nov 2019 03:20:01 GMT  
		Size: 4.5 KB (4519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2fc8ba596f232efb90bfd809db33c9369fae793a2c7d4f384bd9f53d21a5d`  
		Last Modified: Fri, 08 Nov 2019 03:20:15 GMT  
		Size: 56.7 MB (56679024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822497c407117226c58230b2d73ff6f50a0802f0a8c6ca18b84fe87353c65490`  
		Last Modified: Wed, 20 Nov 2019 00:21:14 GMT  
		Size: 95.1 MB (95137299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jre11` - linux; s390x

```console
$ docker pull gradle@sha256:58efd9b105c6804d3aa7bb054918ec3363d37216a46a1abebe14f94927a33a0a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220802607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4146c763017a89f0885c0655fe0f00caf775d5c5fe1b45c39866784d69215fc`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Oct 2019 23:00:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:01:04 GMT
ENV JAVA_VERSION=jdk-11.0.4+11
# Thu, 31 Oct 2019 23:01:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5f7b5c110fc0f344a549cb11784a6d76838061a2b6f654f7841f60e0cd286c6a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.4_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5da5f86f250eeb26719ba06ae1a1133eb75933fad7b9cf1624d743fafd7a7e2b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.4_11.tar.gz';          ;;        s390x)          ESUM='274036da66b150050e23dfc87a4c0ab5331fa6f0d0804b8016621aedf8d1a1e1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.4_11.tar.gz';          ;;        amd64|x86_64)          ESUM='70d2cc675155476f1d8516a7ae6729d44681e4fad5a6fc8dfa65cab36a67b7e0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.4_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Oct 2019 23:01:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2019 00:06:03 GMT
CMD ["gradle"]
# Fri, 01 Nov 2019 00:06:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 01 Nov 2019 00:06:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 01 Nov 2019 00:06:07 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 01 Nov 2019 00:06:12 GMT
WORKDIR /home/gradle
# Fri, 01 Nov 2019 00:07:00 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:51 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d6516ebe93aefa5d84bd151472231fda34a88c02a0c5b2ebdfa62a362ffdb3`  
		Last Modified: Thu, 31 Oct 2019 23:05:58 GMT  
		Size: 10.6 MB (10552908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b8346f33b7a78720e7cd5172e7b4f38a024424cb9dc5daba2b93de5544ff30`  
		Last Modified: Thu, 31 Oct 2019 23:07:19 GMT  
		Size: 39.1 MB (39140065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805900cc5865bfc68379f7c6d998a52143a8dfdd4b0fcf1b01bec462b3e10ef7`  
		Last Modified: Fri, 01 Nov 2019 00:11:20 GMT  
		Size: 4.5 KB (4487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc2b2d13feddb7c6fbb064377df74103abbff926f507978ec46e4bf50eaef0e`  
		Last Modified: Fri, 01 Nov 2019 00:11:32 GMT  
		Size: 50.6 MB (50566020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17211c185452fb28b459fbf936cab64009a4f24441c630e3b25ebb2740d2bca7`  
		Last Modified: Tue, 19 Nov 2019 23:43:00 GMT  
		Size: 95.1 MB (95137301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0-jre13`

```console
$ docker pull gradle@sha256:7e5d8822ae3ecd5d5bda18e15d76e05b53cdd97b7828b199f7c7cc7d40efb381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0-jre13` - linux; amd64

```console
$ docker pull gradle@sha256:eb2899a8dc83ed1d71b3ea46b8f7712d4a51aecb0c5f51ef794fcbf5c142b022
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230867584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1597227d3129c534858de02c7345ff021f32eae7b81160b38128b14922cab7`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:45:02 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 06:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:58:59 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:59:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:59:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:59:01 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:59:01 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:59:18 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:59:19 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:59:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:59:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c602e7de7b4dc2b103089415bc7f2bcfeb6cef5bce65e56697171f4c28fb0db`  
		Last Modified: Thu, 19 Dec 2019 06:48:54 GMT  
		Size: 47.0 MB (47030224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7591b3257d32942bd82b92ff47965ea3fa268726bc77bae899ccdc1a8b151664`  
		Last Modified: Thu, 19 Dec 2019 11:01:06 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177500b750cd88e2e6ba43c86ceb35e0a07d82399537e8c3ed8092ea1facedcf`  
		Last Modified: Thu, 19 Dec 2019 11:01:16 GMT  
		Size: 48.6 MB (48646601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94567a87645fe8a72aab33f449987caa46f296c200b856261a8eb44c62c9c4cd`  
		Last Modified: Thu, 19 Dec 2019 11:01:12 GMT  
		Size: 95.1 MB (95137294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jre13` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:908295cbe4551c884489890ad453853948016d17973588579a9b0e1adf072b86
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223295867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e3c174b4152a9b26e69e909bbee35e5552d0fbe4ad5d4845e79906765d7dd4`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:05:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 08:06:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:06:33 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 08:07:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 08:07:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 09:54:15 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 09:54:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 09:54:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 09:54:19 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 09:54:20 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 09:54:52 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:54:55 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 09:54:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 09:55:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f68c9bd344e83976e79975d3e4d867b348f38c6faa51b6a4d5c114ca23134d8`  
		Last Modified: Thu, 19 Dec 2019 08:07:33 GMT  
		Size: 12.7 MB (12732128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33f535ea89f1b9ee2d722880cd9fc4e675b0e393fcff76d1e2e723b4697270c`  
		Last Modified: Thu, 19 Dec 2019 08:08:24 GMT  
		Size: 45.5 MB (45469630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612afd22e5bc153b5bc5be67897c663e05529e6b69ae192eecb6c1bae6fbc1ee`  
		Last Modified: Thu, 19 Dec 2019 09:55:44 GMT  
		Size: 4.5 KB (4523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9326b1786a92e9b0f8acfb4668819f54c944a85fae60b64d10dd5b915d5c46`  
		Last Modified: Thu, 19 Dec 2019 09:55:59 GMT  
		Size: 46.2 MB (46197288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af98ba96798f0abc1f4f1b481e1b592e41597a277680066ca9bbf17496bf308`  
		Last Modified: Thu, 19 Dec 2019 09:55:56 GMT  
		Size: 95.1 MB (95137346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jre13` - linux; ppc64le

```console
$ docker pull gradle@sha256:02db8e97c98d331e6c1489d6fab1cc316bb571f8aad5ea6ceaae8d5f7c55e21c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238328456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650fc2a86145ca41cc7d3e70417360c13456f969ee0219009b842b9552657240`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:20:24 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:21:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2019 02:06:50 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 02:06:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 02:06:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 02:07:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 02:07:02 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 02:08:06 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:18:48 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:18:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:19:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37d97458785efed876bd376e84f425f759cc4d9dd81bca6177d094e62f2e371`  
		Last Modified: Fri, 08 Nov 2019 02:29:02 GMT  
		Size: 42.1 MB (42103092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a789ce2eb06d8e276d2e7417fa0f0223b92a0b19717d9bef0ee543d179957eb`  
		Last Modified: Tue, 12 Nov 2019 02:11:33 GMT  
		Size: 4.5 KB (4523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025163cce798cf3ca3e392896fd7713a7a327a74c71eebcb81ac726810bb39e4`  
		Last Modified: Tue, 12 Nov 2019 02:11:53 GMT  
		Size: 56.7 MB (56678908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feec192277bf2d7b06e673409f3e9feffa288ea648c36de641863e54c7fd688c`  
		Last Modified: Wed, 20 Nov 2019 00:22:01 GMT  
		Size: 95.1 MB (95137352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jre13` - linux; s390x

```console
$ docker pull gradle@sha256:66c7c5e1e32191ab79416e3b68e4b75641a47b8351eb09b4f7b9cee6a64102b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223596116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea5359512eced13d27bccd2fb4b47b4dce80c9ce54ac6a06cade6c749a97438`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:42:17 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:42:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2019 00:43:02 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 00:43:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 00:43:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 00:43:03 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 00:43:03 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 00:43:27 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:42:08 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:42:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:42:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1574b9d2915ca440a8df6067210b8b08a83fa5e1b26a947456fe7ce51ac62c79`  
		Last Modified: Fri, 08 Nov 2019 02:45:24 GMT  
		Size: 41.9 MB (41916656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51f59d9f4e9a794f0a5819eb266ba17ab3e031ee74ce4b07f6e0e9f992a9b16`  
		Last Modified: Tue, 12 Nov 2019 00:44:55 GMT  
		Size: 4.5 KB (4499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c9182a8c3317e15fea9b4554a082a526c2c6b2dbe466b8e793e51c1b2ac0c3`  
		Last Modified: Tue, 12 Nov 2019 00:45:06 GMT  
		Size: 48.1 MB (48094976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309103460d533b426ed0b8b98731c7b01e2ed5b2b03792081b92af72e99b9a29`  
		Last Modified: Tue, 19 Nov 2019 23:43:40 GMT  
		Size: 95.1 MB (95137323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:6.0-jre8`

```console
$ docker pull gradle@sha256:9cc6f3cd0b060375ab2275d2d9009c4f0afdcff215295fe83960c155bdf83ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6.0-jre8` - linux; amd64

```console
$ docker pull gradle@sha256:252c4aa523ce210f1384b4c1dbff1833888d54d2ddbc6bc1166907fa53d359bc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225153278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69106a8f82ff8683ecfcdb1fd02a0b14c6c8d7f145ea0efcf5fd6085b5f3263a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:57:07 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:57:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:57:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:57:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:57:08 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:57:26 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:57:26 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:57:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90bb5798781d7d972ceffbb8a018b8d4a6209e6ebffef84b49ae3eb603b83b3`  
		Last Modified: Thu, 19 Dec 2019 06:47:39 GMT  
		Size: 41.3 MB (41315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566cc78d89ca54deaef6f31921a9a0cf09937e4fe868206170480b1ac77f7cba`  
		Last Modified: Thu, 19 Dec 2019 10:59:56 GMT  
		Size: 4.5 KB (4490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52cba128b83aaed76d8e263f0b092bbc645fcebb37d69492f15e17ff3c8dad9`  
		Last Modified: Thu, 19 Dec 2019 11:00:07 GMT  
		Size: 48.6 MB (48646581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc26c95e2e9c68317162517ec85ea42b4c61a7d9068b8e7907d606971e74d56`  
		Last Modified: Thu, 19 Dec 2019 11:00:05 GMT  
		Size: 95.1 MB (95137279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jre8` - linux; ppc64le

```console
$ docker pull gradle@sha256:4fb399803b5d67a4e672cfbcb06aefaa2f6e3309ef2e312e5bb320a5a4d7f26b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236621590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ccc6ec0d066910e82f75882d759c6fa535b780ead3c224e7bfad63eda8d8b1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:19:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:10:02 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:10:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:10:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:10:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:10:32 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:11:58 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:17:19 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:17:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ba113a58c3754d98a4cd77c5c3298e88b288fbbc6396e224d48f14a2051737`  
		Last Modified: Fri, 08 Nov 2019 02:27:06 GMT  
		Size: 40.4 MB (40395973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5215135253fc66c5e436a1c7cf0dfca107c7c2efb89e0c36aac6a44180c12616`  
		Last Modified: Fri, 08 Nov 2019 03:18:48 GMT  
		Size: 4.5 KB (4531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450733ab5d7b8c356095a70730cc5719812f0e8e98c7df2a6356d42c00c7e2f4`  
		Last Modified: Fri, 08 Nov 2019 03:19:03 GMT  
		Size: 56.7 MB (56679157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6a148705e89eea028591a3864b03e403b433637492bc5fe9b4f775d5423ecc`  
		Last Modified: Wed, 20 Nov 2019 00:20:21 GMT  
		Size: 95.1 MB (95137348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6.0-jre8` - linux; s390x

```console
$ docker pull gradle@sha256:991ee619cc20d42a5c55a8c7a5ea05149e41de96f4745c29b69eb370b4155c79
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220684522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3531bbf861e7d285f38a4f9e9adc6b86e12729f7cd94c7ec623d3dee874eba1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:42:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:17:47 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:17:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:17:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:17:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:17:49 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:18:19 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:42 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33c44ac698abb009f50d3e585414a474039b681a90428ee2f4b108705725618`  
		Last Modified: Fri, 08 Nov 2019 02:44:46 GMT  
		Size: 39.0 MB (39004827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b31bf9feb646bd1283f25648587844e48832ba5cf55088429e39cc7de67d8f`  
		Last Modified: Fri, 08 Nov 2019 03:19:28 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f319e5024bfd448efb861ced63b58bcfaf2af7249978af930ef82734bef3e1fb`  
		Last Modified: Fri, 08 Nov 2019 03:19:38 GMT  
		Size: 48.1 MB (48095225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9197ffe30daa470cb2b2d989f05e49aa02894c024920d824aaa6f57b03a13840`  
		Last Modified: Tue, 19 Nov 2019 23:42:46 GMT  
		Size: 95.1 MB (95137300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:jdk`

```console
$ docker pull gradle@sha256:8ba20b563ed5c90f4e16705a0590d469190362fffc02dbbe308f05b81a16506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jdk` - linux; amd64

```console
$ docker pull gradle@sha256:e5496a08fead0e48822aa86087b9d5f278795586a8588528bc289f0406e8d235
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288889902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc47c2ea2852e1ae6d6756cae8c568b3b255e198d589f81be8835390c6740a2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:56:27 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:56:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:56:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:56:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:56:29 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:56:57 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:56:57 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:56:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596d6c23adc7886652eea636e0c856146cc51d2da380a735645fad034dfe5069`  
		Last Modified: Thu, 19 Dec 2019 06:47:29 GMT  
		Size: 105.1 MB (105052689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07313090020e2216012e1a247dd3e9fce45ffac5a07713c234c1f02718a91a8`  
		Last Modified: Thu, 19 Dec 2019 10:59:36 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d786c8e5ce8bd8e0a4bdfc0ecbde07e01b6607161798b7c5a1f68fd0673aea`  
		Last Modified: Thu, 19 Dec 2019 10:59:47 GMT  
		Size: 48.6 MB (48646474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84476db4b1ac2fc5e552d5bdb3d8247691ea1d57ccbddf9bc83c28455f012d3`  
		Last Modified: Thu, 19 Dec 2019 10:59:43 GMT  
		Size: 95.1 MB (95137274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk` - linux; ppc64le

```console
$ docker pull gradle@sha256:de97c2794be05db81624dc748d5f0bf6f774b3746b07e662593263f523fa126e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298448560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229fbb404cae0f708aa5d31816a664d221d3bf69c7a3d1450ba375ef51a3a708`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:18:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:18:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:07:19 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:07:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:07:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:07:41 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:07:44 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:09:21 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:16:56 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:16:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11691fec336d2f0ecf12299c6a2258179b6a03f37e8596ace4bdcf8340a84210`  
		Last Modified: Fri, 08 Nov 2019 02:26:43 GMT  
		Size: 102.2 MB (102223730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9315d5888c26e44dda21265c0782bd2458f9275e893dda525156726db64fd`  
		Last Modified: Fri, 08 Nov 2019 03:18:05 GMT  
		Size: 4.5 KB (4526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f9984d68d74068dfbcdb0f0ec1b51ba5716b1cca72aa6813cfbaae8f333f`  
		Last Modified: Fri, 08 Nov 2019 03:18:18 GMT  
		Size: 56.7 MB (56678368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b2332b39dc868b3d267bf94fca2afd107122993c7dec787be0f95aa7adf3a9`  
		Last Modified: Wed, 20 Nov 2019 00:19:42 GMT  
		Size: 95.1 MB (95137355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk` - linux; s390x

```console
$ docker pull gradle@sha256:271543f903e154259439857a293709a845db5d56bed51bb86dc75d8bdc27f92b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614cb05338d916b421497a72794e78adae51687596d0ce1ee3eb69b1ce6d7ab2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:41:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:16:40 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:16:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:16:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:16:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:16:43 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:17:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:33 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75a894e76562f7781c6919af4bc9ab7ff662d7e916f0e18fe1261def191dec`  
		Last Modified: Fri, 08 Nov 2019 02:44:32 GMT  
		Size: 100.7 MB (100734555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b0f50dfaf38af9bcb739cda10fb6a0c7e8610af129e4285b00e833cf63be05`  
		Last Modified: Fri, 08 Nov 2019 03:19:04 GMT  
		Size: 4.5 KB (4497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5fff2ffc2e2c8a9e323c3696a7eacf9842b928e684dfa7cb4b2b577fab52d`  
		Last Modified: Fri, 08 Nov 2019 03:19:14 GMT  
		Size: 48.1 MB (48095072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1a287aa214edc225ccf89f9627b82a3b65d511ae9ffb5a99235667c5c1438d`  
		Last Modified: Tue, 19 Nov 2019 23:42:29 GMT  
		Size: 95.1 MB (95137322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:jdk11`

```console
$ docker pull gradle@sha256:3774e8b27b3904f5b3f776a64fc1641eff6e2a1d7b978ab981dbfd498c84a219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `gradle:jdk11` - linux; amd64

```console
$ docker pull gradle@sha256:88e93f9ef304868cb3ea2925a88631e0574418ee0d85822251c6fb07d2ba5956
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381659710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8041b3ebdc74d94f6cac12012aa7f93d34116255d4352c5c49e9a3c6660b325`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:33 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 06:44:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        armhf)          ESUM='c6b1fda3f8807028cbfcc34a4ded2e8a5a6b6239d2bcc1f06673ea6b1530df94';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.5_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d763481ddc29ac0bdefb24216b3a0bf9afbb058552682567a075f9c0f7da5814';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6dd0c9c8a740e6c19149e98034fba8e368fd9aa16ab417aa636854d40db1a161';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 06:44:47 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 10:57:35 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:57:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:57:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:57:36 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:57:37 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:57:54 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:57:54 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:57:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a5601342fdc19041e774599a3a5f0e49e747e6ff8a02429de43656a48d5790`  
		Last Modified: Thu, 19 Dec 2019 06:48:02 GMT  
		Size: 197.8 MB (197822308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250e5f7405ee8015ba4c6a300bf711cdc06c5b4b9c71a4b41890a17408451813`  
		Last Modified: Thu, 19 Dec 2019 11:00:16 GMT  
		Size: 4.5 KB (4491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164260929f249d04eaee3c0c3d0a6530550b0c72731b5a9b7564ab31358d5130`  
		Last Modified: Thu, 19 Dec 2019 11:00:26 GMT  
		Size: 48.6 MB (48646663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867d15ff716dddc670529f5289c20650d5708565c28a30a91fad40531ad252a`  
		Last Modified: Thu, 19 Dec 2019 11:00:29 GMT  
		Size: 95.1 MB (95137275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; arm variant v7

```console
$ docker pull gradle@sha256:2d416ac5679ae159bb258e207a11965a562483073dfb108e704ca6cd1f4ad5a9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.7 MB (357653302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63f695b83024fd8f844edaee0188f9014f8d87dd9e58fa62d0d4f9851354cf7`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:34:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 07:34:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:34:55 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 07:35:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        armhf)          ESUM='c6b1fda3f8807028cbfcc34a4ded2e8a5a6b6239d2bcc1f06673ea6b1530df94';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.5_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d763481ddc29ac0bdefb24216b3a0bf9afbb058552682567a075f9c0f7da5814';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6dd0c9c8a740e6c19149e98034fba8e368fd9aa16ab417aa636854d40db1a161';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 07:35:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 07:35:19 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 08:29:10 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 08:29:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 08:29:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 08:29:13 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 08:29:14 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 08:29:48 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:29:50 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 08:29:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 08:30:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70980651c174a0c8207979963c952c66f259507ea151d864bb0642811e77ea`  
		Last Modified: Thu, 19 Dec 2019 07:36:36 GMT  
		Size: 12.3 MB (12267151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fc6791bb8979c7816db2ca64a3b2b4f705b9f8d486ddadc04d4f431aec1f41`  
		Last Modified: Thu, 19 Dec 2019 07:37:06 GMT  
		Size: 184.3 MB (184320655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d8b0c49dae07b6dcf7975dffdcf649ba126faee348d1957e51c5c2e3feaa3d`  
		Last Modified: Thu, 19 Dec 2019 08:31:51 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83a60961b742b02200015d811be575856b3fcf4b5a7153d934be4243a44c4c0`  
		Last Modified: Thu, 19 Dec 2019 08:32:07 GMT  
		Size: 43.6 MB (43611824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4319335b5d5deacb263a647021099fabbab28248a74309fd20207dc884d746a`  
		Last Modified: Thu, 19 Dec 2019 08:32:05 GMT  
		Size: 95.1 MB (95137346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk11` - linux; ppc64le

```console
$ docker pull gradle@sha256:70f12a1f674aee3feefbfc2d284b7e703bd68ecf42cd32c737b12b8163691bf9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.4 MB (378437452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05047db2933933dd16087337a9b2310acca4b75687f5312358df5b09f7c0f29f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:19:15 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Fri, 08 Nov 2019 02:19:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        armhf)          ESUM='c6b1fda3f8807028cbfcc34a4ded2e8a5a6b6239d2bcc1f06673ea6b1530df94';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.5_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d763481ddc29ac0bdefb24216b3a0bf9afbb058552682567a075f9c0f7da5814';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6dd0c9c8a740e6c19149e98034fba8e368fd9aa16ab417aa636854d40db1a161';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:19:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 02:19:47 GMT
CMD ["jshell"]
# Fri, 08 Nov 2019 03:12:46 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:12:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:13:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:13:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:13:06 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:14:27 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:17:41 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:17:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0c5021ee48efdfa117eddc0926b74496b28d6472e9baf8355b8e1eab79a960`  
		Last Modified: Fri, 08 Nov 2019 02:27:38 GMT  
		Size: 182.2 MB (182211824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446da082f980cca1cf6accaacf7be5ad870535a7aca6b0bf62924012968da1fb`  
		Last Modified: Fri, 08 Nov 2019 03:19:25 GMT  
		Size: 4.5 KB (4528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bbfbd2811f7e2747a094ab15b3606c9361356d7ebae852dc928a082e6c69c9`  
		Last Modified: Fri, 08 Nov 2019 03:19:40 GMT  
		Size: 56.7 MB (56679199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3aaf4968493c29fb31e5a50e332bd946d937edf2ebf6a53e32fa633b40753d0`  
		Last Modified: Wed, 20 Nov 2019 00:20:51 GMT  
		Size: 95.1 MB (95137320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:jdk13`

```console
$ docker pull gradle@sha256:61e0df286a33ca5bc7e7ae8c3efd352ee15155957cec0389111e8668b4807090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jdk13` - linux; amd64

```console
$ docker pull gradle@sha256:11954dd10166447cb4bb840f35694c420682ff07e1569041063eac0a5d5a2bc4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.4 MB (392389674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d189a62ff78094fc5e611566a7e7a6370123b2310b68d3472d0af348b8cb8e1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:45:02 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 06:45:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:45:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 06:45:15 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 10:58:32 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:58:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:58:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:58:33 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:58:33 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:58:50 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:58:51 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:58:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:58:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742105205d26a48c4efc794ff9c1727510deda216fdbee70057555daf34604fd`  
		Last Modified: Thu, 19 Dec 2019 06:48:40 GMT  
		Size: 208.6 MB (208552263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8182b82c24e3e5440732e5974f7df0f24f31d634ca694f21a5fb226cfd1cb8`  
		Last Modified: Thu, 19 Dec 2019 11:00:50 GMT  
		Size: 4.5 KB (4491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f925699a0ffe096f0c9c3334f72eed242bae1a1d221d696e5eee915e942b240`  
		Last Modified: Thu, 19 Dec 2019 11:01:00 GMT  
		Size: 48.6 MB (48646666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32be832b61beea577d22980e821aaf75261907d23acf17a858c2cf825658193`  
		Last Modified: Thu, 19 Dec 2019 11:00:57 GMT  
		Size: 95.1 MB (95137281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk13` - linux; arm variant v7

```console
$ docker pull gradle@sha256:d8c21bd9a0e57601722b85fcf651268f5ed8b7dcf348b6dd94fd81345ecb467f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366027908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f66c02d7e23a7d370a0778f598e7137897c6bb5b6cf00218790e810bf40655a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:34:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 07:34:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:35:35 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 07:36:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 07:36:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 07:36:16 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 08:30:15 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 08:30:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 08:30:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 08:30:18 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 08:30:19 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 08:31:15 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:31:19 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 08:31:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 08:31:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70980651c174a0c8207979963c952c66f259507ea151d864bb0642811e77ea`  
		Last Modified: Thu, 19 Dec 2019 07:36:36 GMT  
		Size: 12.3 MB (12267151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ea41660b072f1d696ee3eb5e298effdb694ce10c48fcf047fa5c0df2ca5b98`  
		Last Modified: Thu, 19 Dec 2019 07:37:52 GMT  
		Size: 192.7 MB (192694921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270ee4394edc3df6ef7229ddb68d18bf9c520ce8a6bfc008c62c8a69802b113b`  
		Last Modified: Thu, 19 Dec 2019 08:32:15 GMT  
		Size: 4.5 KB (4514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc63704c32cd7ac29da21066502204d5cdf4a0b694358d565e17d7a73bd7b26`  
		Last Modified: Thu, 19 Dec 2019 08:32:31 GMT  
		Size: 43.6 MB (43612152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc3cd42f671600010a75eae9d678051d4563a761e981d50a2cbc68509315882`  
		Last Modified: Thu, 19 Dec 2019 08:32:29 GMT  
		Size: 95.1 MB (95137348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk13` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3ac4f5084a175ae3e80beea60ad3db627e8391b8bb01f033a07c118b3cb308c9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.8 MB (384796356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca0a836b8bf140190f5a67b462b6cdcf09e5d2f1968f9471304d34440a811`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:05:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 08:06:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:06:33 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 08:06:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 08:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 08:06:53 GMT
CMD ["jshell"]
# Thu, 19 Dec 2019 09:53:11 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 09:53:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 09:53:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 09:53:15 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 09:53:16 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 09:53:53 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:53:56 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 09:53:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 09:54:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f68c9bd344e83976e79975d3e4d867b348f38c6faa51b6a4d5c114ca23134d8`  
		Last Modified: Thu, 19 Dec 2019 08:07:33 GMT  
		Size: 12.7 MB (12732128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c3a85665587cae3d2f91c7df4ac8fffea83ccf3a8ffb7d12b944bc2d914b2`  
		Last Modified: Thu, 19 Dec 2019 08:08:01 GMT  
		Size: 207.0 MB (206970493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d7bb931f919772e247dc0761a62616610b150f87e337757aa31e57bdb09519`  
		Last Modified: Thu, 19 Dec 2019 09:55:22 GMT  
		Size: 4.5 KB (4533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2ee296cb883493cd4794c0e2fa2cb5dd7fea5602eefb9ab93ba077f4cfa74c`  
		Last Modified: Thu, 19 Dec 2019 09:55:36 GMT  
		Size: 46.2 MB (46196943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da117fd38f6ce03f273494eb8d016d4d36520e6279750164688b2aad1728dbb3`  
		Last Modified: Thu, 19 Dec 2019 09:55:33 GMT  
		Size: 95.1 MB (95137307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk13` - linux; ppc64le

```console
$ docker pull gradle@sha256:f8508376250fbb0ede28217652d3b900f9e9cc3e5f53ad0165504e9562b755b8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 MB (387317150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e8c445ffd1fb3b19607455199233163d5ae4a8b088be18313771075c7e585`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:20:24 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:20:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 02:20:54 GMT
CMD ["jshell"]
# Tue, 12 Nov 2019 02:04:23 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 02:04:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 02:04:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 02:04:34 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 02:04:38 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 02:06:06 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:18:26 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:18:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:18:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7829f1f9068dd6677f84b0dcb76e331dc711fcb88fb8e11a86489ba3a44144`  
		Last Modified: Fri, 08 Nov 2019 02:28:37 GMT  
		Size: 191.1 MB (191091672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6f52194782c2d3a80798266515900d4e09d7d2e58fdbb54ded2d2412cf9fc1`  
		Last Modified: Tue, 12 Nov 2019 02:11:05 GMT  
		Size: 4.5 KB (4531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777efb823cf8e517eac3a94a3c60ee57cc3d9f7d486408b0c6f6fd59dd3cd975`  
		Last Modified: Tue, 12 Nov 2019 02:11:20 GMT  
		Size: 56.7 MB (56679068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79f7b059907fcfcd7d0fc552d42ffe7e3d305c941f879a5d3b5b1ec07a95968`  
		Last Modified: Wed, 20 Nov 2019 00:21:37 GMT  
		Size: 95.1 MB (95137298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk13` - linux; s390x

```console
$ docker pull gradle@sha256:5b817101f77f442cbec9a23ca8877fcc2f6b00078c9943a860a5f7776abd073b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367227784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afe48fdb5418150055e6eaa1370f0276d4b578696994ebb3befd7a61cf9c3eb`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:42:17 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:42:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f0cfd0d807a10e6128cf1b0ead1e8ae3702ac702d9b4d13914bbce2be06947bb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        armhf)          ESUM='6d0a31bda85e2fc4d52aa7be7b2e1a0a8fd392465ebb42b05fd59a993cca460c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_arm_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f8ea316dac57453d06163d4d706d601c355ba0c56a426eadd075e1e281370f4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='334604f0ae9f36265ddde9e98060be929c35654d5e78b8e9f2998f0964ef04b4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='2226366d7dffb3eb4ec3d14101f4ddb4259195aa43bb319a93810447b8384930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jdk_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 02:42:29 GMT
CMD ["jshell"]
# Tue, 12 Nov 2019 00:42:27 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 00:42:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 00:42:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 00:42:29 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 00:42:29 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 00:42:52 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:42:00 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:42:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:42:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0468f77333e3f6ba95c46ae196080bc38eb20b0c14ef070380ec24354e735a8c`  
		Last Modified: Fri, 08 Nov 2019 02:45:08 GMT  
		Size: 185.5 MB (185546389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e871332d1942f2b085cb5a9047c15122420acdc371aca57c7b0c5975fc1ac8`  
		Last Modified: Tue, 12 Nov 2019 00:44:33 GMT  
		Size: 4.5 KB (4499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1ddb84107e1c7c7bac5e70e6a6aeba3f03bcd96cb34ba7921693fc1a54b5a7`  
		Last Modified: Tue, 12 Nov 2019 00:44:43 GMT  
		Size: 48.1 MB (48096956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9818de0a85a705ed4c3390b8bd0854e7c989e7bd2da3080304a2b46eb5eaee`  
		Last Modified: Tue, 19 Nov 2019 23:43:11 GMT  
		Size: 95.1 MB (95137278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:jdk8`

```console
$ docker pull gradle@sha256:8ba20b563ed5c90f4e16705a0590d469190362fffc02dbbe308f05b81a16506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jdk8` - linux; amd64

```console
$ docker pull gradle@sha256:e5496a08fead0e48822aa86087b9d5f278795586a8588528bc289f0406e8d235
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288889902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc47c2ea2852e1ae6d6756cae8c568b3b255e198d589f81be8835390c6740a2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:56:27 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:56:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:56:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:56:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:56:29 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:56:57 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:56:57 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:56:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596d6c23adc7886652eea636e0c856146cc51d2da380a735645fad034dfe5069`  
		Last Modified: Thu, 19 Dec 2019 06:47:29 GMT  
		Size: 105.1 MB (105052689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07313090020e2216012e1a247dd3e9fce45ffac5a07713c234c1f02718a91a8`  
		Last Modified: Thu, 19 Dec 2019 10:59:36 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d786c8e5ce8bd8e0a4bdfc0ecbde07e01b6607161798b7c5a1f68fd0673aea`  
		Last Modified: Thu, 19 Dec 2019 10:59:47 GMT  
		Size: 48.6 MB (48646474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84476db4b1ac2fc5e552d5bdb3d8247691ea1d57ccbddf9bc83c28455f012d3`  
		Last Modified: Thu, 19 Dec 2019 10:59:43 GMT  
		Size: 95.1 MB (95137274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; ppc64le

```console
$ docker pull gradle@sha256:de97c2794be05db81624dc748d5f0bf6f774b3746b07e662593263f523fa126e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298448560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229fbb404cae0f708aa5d31816a664d221d3bf69c7a3d1450ba375ef51a3a708`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:18:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:18:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:07:19 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:07:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:07:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:07:41 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:07:44 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:09:21 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:16:56 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:16:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11691fec336d2f0ecf12299c6a2258179b6a03f37e8596ace4bdcf8340a84210`  
		Last Modified: Fri, 08 Nov 2019 02:26:43 GMT  
		Size: 102.2 MB (102223730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9315d5888c26e44dda21265c0782bd2458f9275e893dda525156726db64fd`  
		Last Modified: Fri, 08 Nov 2019 03:18:05 GMT  
		Size: 4.5 KB (4526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f9984d68d74068dfbcdb0f0ec1b51ba5716b1cca72aa6813cfbaae8f333f`  
		Last Modified: Fri, 08 Nov 2019 03:18:18 GMT  
		Size: 56.7 MB (56678368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b2332b39dc868b3d267bf94fca2afd107122993c7dec787be0f95aa7adf3a9`  
		Last Modified: Wed, 20 Nov 2019 00:19:42 GMT  
		Size: 95.1 MB (95137355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk8` - linux; s390x

```console
$ docker pull gradle@sha256:271543f903e154259439857a293709a845db5d56bed51bb86dc75d8bdc27f92b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614cb05338d916b421497a72794e78adae51687596d0ce1ee3eb69b1ce6d7ab2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:41:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:16:40 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:16:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:16:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:16:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:16:43 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:17:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:33 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75a894e76562f7781c6919af4bc9ab7ff662d7e916f0e18fe1261def191dec`  
		Last Modified: Fri, 08 Nov 2019 02:44:32 GMT  
		Size: 100.7 MB (100734555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b0f50dfaf38af9bcb739cda10fb6a0c7e8610af129e4285b00e833cf63be05`  
		Last Modified: Fri, 08 Nov 2019 03:19:04 GMT  
		Size: 4.5 KB (4497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5fff2ffc2e2c8a9e323c3696a7eacf9842b928e684dfa7cb4b2b577fab52d`  
		Last Modified: Fri, 08 Nov 2019 03:19:14 GMT  
		Size: 48.1 MB (48095072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1a287aa214edc225ccf89f9627b82a3b65d511ae9ffb5a99235667c5c1438d`  
		Last Modified: Tue, 19 Nov 2019 23:42:29 GMT  
		Size: 95.1 MB (95137322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:jre`

```console
$ docker pull gradle@sha256:9cc6f3cd0b060375ab2275d2d9009c4f0afdcff215295fe83960c155bdf83ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jre` - linux; amd64

```console
$ docker pull gradle@sha256:252c4aa523ce210f1384b4c1dbff1833888d54d2ddbc6bc1166907fa53d359bc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225153278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69106a8f82ff8683ecfcdb1fd02a0b14c6c8d7f145ea0efcf5fd6085b5f3263a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:57:07 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:57:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:57:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:57:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:57:08 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:57:26 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:57:26 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:57:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90bb5798781d7d972ceffbb8a018b8d4a6209e6ebffef84b49ae3eb603b83b3`  
		Last Modified: Thu, 19 Dec 2019 06:47:39 GMT  
		Size: 41.3 MB (41315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566cc78d89ca54deaef6f31921a9a0cf09937e4fe868206170480b1ac77f7cba`  
		Last Modified: Thu, 19 Dec 2019 10:59:56 GMT  
		Size: 4.5 KB (4490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52cba128b83aaed76d8e263f0b092bbc645fcebb37d69492f15e17ff3c8dad9`  
		Last Modified: Thu, 19 Dec 2019 11:00:07 GMT  
		Size: 48.6 MB (48646581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc26c95e2e9c68317162517ec85ea42b4c61a7d9068b8e7907d606971e74d56`  
		Last Modified: Thu, 19 Dec 2019 11:00:05 GMT  
		Size: 95.1 MB (95137279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre` - linux; ppc64le

```console
$ docker pull gradle@sha256:4fb399803b5d67a4e672cfbcb06aefaa2f6e3309ef2e312e5bb320a5a4d7f26b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236621590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ccc6ec0d066910e82f75882d759c6fa535b780ead3c224e7bfad63eda8d8b1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:19:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:10:02 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:10:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:10:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:10:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:10:32 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:11:58 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:17:19 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:17:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ba113a58c3754d98a4cd77c5c3298e88b288fbbc6396e224d48f14a2051737`  
		Last Modified: Fri, 08 Nov 2019 02:27:06 GMT  
		Size: 40.4 MB (40395973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5215135253fc66c5e436a1c7cf0dfca107c7c2efb89e0c36aac6a44180c12616`  
		Last Modified: Fri, 08 Nov 2019 03:18:48 GMT  
		Size: 4.5 KB (4531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450733ab5d7b8c356095a70730cc5719812f0e8e98c7df2a6356d42c00c7e2f4`  
		Last Modified: Fri, 08 Nov 2019 03:19:03 GMT  
		Size: 56.7 MB (56679157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6a148705e89eea028591a3864b03e403b433637492bc5fe9b4f775d5423ecc`  
		Last Modified: Wed, 20 Nov 2019 00:20:21 GMT  
		Size: 95.1 MB (95137348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre` - linux; s390x

```console
$ docker pull gradle@sha256:991ee619cc20d42a5c55a8c7a5ea05149e41de96f4745c29b69eb370b4155c79
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220684522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3531bbf861e7d285f38a4f9e9adc6b86e12729f7cd94c7ec623d3dee874eba1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:42:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:17:47 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:17:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:17:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:17:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:17:49 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:18:19 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:42 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33c44ac698abb009f50d3e585414a474039b681a90428ee2f4b108705725618`  
		Last Modified: Fri, 08 Nov 2019 02:44:46 GMT  
		Size: 39.0 MB (39004827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b31bf9feb646bd1283f25648587844e48832ba5cf55088429e39cc7de67d8f`  
		Last Modified: Fri, 08 Nov 2019 03:19:28 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f319e5024bfd448efb861ced63b58bcfaf2af7249978af930ef82734bef3e1fb`  
		Last Modified: Fri, 08 Nov 2019 03:19:38 GMT  
		Size: 48.1 MB (48095225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9197ffe30daa470cb2b2d989f05e49aa02894c024920d824aaa6f57b03a13840`  
		Last Modified: Tue, 19 Nov 2019 23:42:46 GMT  
		Size: 95.1 MB (95137300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:jre11`

```console
$ docker pull gradle@sha256:4ef02a0dcc0f9286b920e96502cdc8f736d5dd8238ea0743124082003af8a98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jre11` - linux; amd64

```console
$ docker pull gradle@sha256:a6ff0139ad814a4440d5625fb62cebde5af4f005c4622cc84bed6079cb116b53
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226690960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294f7c2a658c17259f51748b39df06221cbcd7a902af543f27a32733dbce62e7`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:33 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Thu, 19 Dec 2019 06:44:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='2e5343f2046844673f88a4297f5e5796979acb9880b291f965b4c9fa33201d78';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='2f08c469c9a8adea1b6ee3444ba2a8242a7e99d87976a077faf037a9eb7f884b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:58:03 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:58:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:58:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:58:04 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:58:05 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:58:22 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:58:22 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:58:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:58:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8c6504c719a3a083869f0711720d4ad964c9dd22968979cbd6e6155b355c3`  
		Last Modified: Thu, 19 Dec 2019 06:48:16 GMT  
		Size: 42.9 MB (42853646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9a88e172fca720ef5e1c1be9d4ec1ccddb7244cd3f7a149639024c442ad748`  
		Last Modified: Thu, 19 Dec 2019 11:00:34 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6731489a22f40676f442ac3acaf06be19d51ec0a9602093b70ef35f61478f918`  
		Last Modified: Thu, 19 Dec 2019 11:00:45 GMT  
		Size: 48.6 MB (48646554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff73ce0d214daa7269ef8676f2183330965052befaaacefccd9e5d5cb152040d`  
		Last Modified: Thu, 19 Dec 2019 11:00:43 GMT  
		Size: 95.1 MB (95137295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre11` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7a36234ba72755b3f6e36e8de770aec23ae4c32fed9e62dfae185a36419938eb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219608547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b169fa10c8a26c4773e8751e23d0a72a8086162c90924eba02c7b8c1a8cd98d8`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:58:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Oct 2019 22:59:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 22:59:31 GMT
ENV JAVA_VERSION=jdk-11.0.4+11
# Thu, 31 Oct 2019 22:59:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5f7b5c110fc0f344a549cb11784a6d76838061a2b6f654f7841f60e0cd286c6a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.4_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5da5f86f250eeb26719ba06ae1a1133eb75933fad7b9cf1624d743fafd7a7e2b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.4_11.tar.gz';          ;;        s390x)          ESUM='274036da66b150050e23dfc87a4c0ab5331fa6f0d0804b8016621aedf8d1a1e1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.4_11.tar.gz';          ;;        amd64|x86_64)          ESUM='70d2cc675155476f1d8516a7ae6729d44681e4fad5a6fc8dfa65cab36a67b7e0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.4_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Oct 2019 22:59:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Nov 2019 23:44:27 GMT
CMD ["gradle"]
# Wed, 13 Nov 2019 23:44:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Nov 2019 23:44:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 13 Nov 2019 23:44:31 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Nov 2019 23:44:31 GMT
WORKDIR /home/gradle
# Wed, 13 Nov 2019 23:45:10 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 01:08:50 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 01:08:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 01:09:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb929685f4a20d12d37720cde265d3c645d4ec19fbad4db50c81055be5dc25`  
		Last Modified: Thu, 31 Oct 2019 23:01:25 GMT  
		Size: 10.3 MB (10302431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403ce56eaf5b3e8f6d958819de2613191ecb8d22c81a84c9a17ec1c423b7d4c`  
		Last Modified: Thu, 31 Oct 2019 23:02:56 GMT  
		Size: 41.8 MB (41805533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2f85d224d63a93cc5db3bd7b0d341a81e670c3f42324a2c582ec35b67db249`  
		Last Modified: Wed, 13 Nov 2019 23:47:49 GMT  
		Size: 4.5 KB (4525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d9bc1e8992ab73a596b584cc0566486ad47e2cbfbb1eea0f041b57f96cae07`  
		Last Modified: Wed, 13 Nov 2019 23:48:06 GMT  
		Size: 48.6 MB (48604121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd45752872dacbd1e3a15b33b4fc65c3308b9dadb474d4162ee1b57a6f6f7bde`  
		Last Modified: Wed, 20 Nov 2019 01:10:15 GMT  
		Size: 95.1 MB (95137303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre11` - linux; ppc64le

```console
$ docker pull gradle@sha256:a8a84eed38970fa312c9dc5699613c1cb7b2888718312466f183f1cebbf6dc95
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235727564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7bcc7c40466cc06f9025d70db225ea78252c1a186233f28ee6fa5be8e2d877`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:19:15 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Fri, 08 Nov 2019 02:20:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='2e5343f2046844673f88a4297f5e5796979acb9880b291f965b4c9fa33201d78';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.5_10.tar.gz';          ;;        amd64|x86_64)          ESUM='2f08c469c9a8adea1b6ee3444ba2a8242a7e99d87976a077faf037a9eb7f884b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.5_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:15:11 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:15:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:15:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:15:28 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:15:29 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:16:55 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:18:04 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:18:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:18:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f71bc3c769bd80c7987467a5821fc6f00e294fb811fe979e0db9e54f56f923`  
		Last Modified: Fri, 08 Nov 2019 02:28:03 GMT  
		Size: 39.5 MB (39502141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7335b89bbecfa0b3d341c3f2560562602ec80820e2f75eafd33703414a9b39`  
		Last Modified: Fri, 08 Nov 2019 03:20:01 GMT  
		Size: 4.5 KB (4519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc2fc8ba596f232efb90bfd809db33c9369fae793a2c7d4f384bd9f53d21a5d`  
		Last Modified: Fri, 08 Nov 2019 03:20:15 GMT  
		Size: 56.7 MB (56679024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822497c407117226c58230b2d73ff6f50a0802f0a8c6ca18b84fe87353c65490`  
		Last Modified: Wed, 20 Nov 2019 00:21:14 GMT  
		Size: 95.1 MB (95137299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre11` - linux; s390x

```console
$ docker pull gradle@sha256:58efd9b105c6804d3aa7bb054918ec3363d37216a46a1abebe14f94927a33a0a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220802607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4146c763017a89f0885c0655fe0f00caf775d5c5fe1b45c39866784d69215fc`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Oct 2019 23:00:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:01:04 GMT
ENV JAVA_VERSION=jdk-11.0.4+11
# Thu, 31 Oct 2019 23:01:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5f7b5c110fc0f344a549cb11784a6d76838061a2b6f654f7841f60e0cd286c6a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.4_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5da5f86f250eeb26719ba06ae1a1133eb75933fad7b9cf1624d743fafd7a7e2b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.4_11.tar.gz';          ;;        s390x)          ESUM='274036da66b150050e23dfc87a4c0ab5331fa6f0d0804b8016621aedf8d1a1e1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.4_11.tar.gz';          ;;        amd64|x86_64)          ESUM='70d2cc675155476f1d8516a7ae6729d44681e4fad5a6fc8dfa65cab36a67b7e0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.4%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.4_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 31 Oct 2019 23:01:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2019 00:06:03 GMT
CMD ["gradle"]
# Fri, 01 Nov 2019 00:06:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 01 Nov 2019 00:06:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 01 Nov 2019 00:06:07 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 01 Nov 2019 00:06:12 GMT
WORKDIR /home/gradle
# Fri, 01 Nov 2019 00:07:00 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:51 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d6516ebe93aefa5d84bd151472231fda34a88c02a0c5b2ebdfa62a362ffdb3`  
		Last Modified: Thu, 31 Oct 2019 23:05:58 GMT  
		Size: 10.6 MB (10552908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b8346f33b7a78720e7cd5172e7b4f38a024424cb9dc5daba2b93de5544ff30`  
		Last Modified: Thu, 31 Oct 2019 23:07:19 GMT  
		Size: 39.1 MB (39140065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805900cc5865bfc68379f7c6d998a52143a8dfdd4b0fcf1b01bec462b3e10ef7`  
		Last Modified: Fri, 01 Nov 2019 00:11:20 GMT  
		Size: 4.5 KB (4487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc2b2d13feddb7c6fbb064377df74103abbff926f507978ec46e4bf50eaef0e`  
		Last Modified: Fri, 01 Nov 2019 00:11:32 GMT  
		Size: 50.6 MB (50566020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17211c185452fb28b459fbf936cab64009a4f24441c630e3b25ebb2740d2bca7`  
		Last Modified: Tue, 19 Nov 2019 23:43:00 GMT  
		Size: 95.1 MB (95137301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:jre13`

```console
$ docker pull gradle@sha256:7e5d8822ae3ecd5d5bda18e15d76e05b53cdd97b7828b199f7c7cc7d40efb381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jre13` - linux; amd64

```console
$ docker pull gradle@sha256:eb2899a8dc83ed1d71b3ea46b8f7712d4a51aecb0c5f51ef794fcbf5c142b022
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230867584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1597227d3129c534858de02c7345ff021f32eae7b81160b38128b14922cab7`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:45:02 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 06:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:58:59 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:59:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:59:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:59:01 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:59:01 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:59:18 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:59:19 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:59:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:59:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c602e7de7b4dc2b103089415bc7f2bcfeb6cef5bce65e56697171f4c28fb0db`  
		Last Modified: Thu, 19 Dec 2019 06:48:54 GMT  
		Size: 47.0 MB (47030224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7591b3257d32942bd82b92ff47965ea3fa268726bc77bae899ccdc1a8b151664`  
		Last Modified: Thu, 19 Dec 2019 11:01:06 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177500b750cd88e2e6ba43c86ceb35e0a07d82399537e8c3ed8092ea1facedcf`  
		Last Modified: Thu, 19 Dec 2019 11:01:16 GMT  
		Size: 48.6 MB (48646601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94567a87645fe8a72aab33f449987caa46f296c200b856261a8eb44c62c9c4cd`  
		Last Modified: Thu, 19 Dec 2019 11:01:12 GMT  
		Size: 95.1 MB (95137294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre13` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:908295cbe4551c884489890ad453853948016d17973588579a9b0e1adf072b86
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223295867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e3c174b4152a9b26e69e909bbee35e5552d0fbe4ad5d4845e79906765d7dd4`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:05:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 08:06:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:06:33 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Thu, 19 Dec 2019 08:07:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 08:07:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 09:54:15 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 09:54:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 09:54:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 09:54:19 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 09:54:20 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 09:54:52 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:54:55 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 09:54:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 09:55:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f68c9bd344e83976e79975d3e4d867b348f38c6faa51b6a4d5c114ca23134d8`  
		Last Modified: Thu, 19 Dec 2019 08:07:33 GMT  
		Size: 12.7 MB (12732128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33f535ea89f1b9ee2d722880cd9fc4e675b0e393fcff76d1e2e723b4697270c`  
		Last Modified: Thu, 19 Dec 2019 08:08:24 GMT  
		Size: 45.5 MB (45469630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612afd22e5bc153b5bc5be67897c663e05529e6b69ae192eecb6c1bae6fbc1ee`  
		Last Modified: Thu, 19 Dec 2019 09:55:44 GMT  
		Size: 4.5 KB (4523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9326b1786a92e9b0f8acfb4668819f54c944a85fae60b64d10dd5b915d5c46`  
		Last Modified: Thu, 19 Dec 2019 09:55:59 GMT  
		Size: 46.2 MB (46197288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af98ba96798f0abc1f4f1b481e1b592e41597a277680066ca9bbf17496bf308`  
		Last Modified: Thu, 19 Dec 2019 09:55:56 GMT  
		Size: 95.1 MB (95137346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre13` - linux; ppc64le

```console
$ docker pull gradle@sha256:02db8e97c98d331e6c1489d6fab1cc316bb571f8aad5ea6ceaae8d5f7c55e21c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238328456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650fc2a86145ca41cc7d3e70417360c13456f969ee0219009b842b9552657240`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:20:24 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:21:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2019 02:06:50 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 02:06:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 02:06:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 02:07:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 02:07:02 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 02:08:06 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:18:48 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:18:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:19:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37d97458785efed876bd376e84f425f759cc4d9dd81bca6177d094e62f2e371`  
		Last Modified: Fri, 08 Nov 2019 02:29:02 GMT  
		Size: 42.1 MB (42103092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a789ce2eb06d8e276d2e7417fa0f0223b92a0b19717d9bef0ee543d179957eb`  
		Last Modified: Tue, 12 Nov 2019 02:11:33 GMT  
		Size: 4.5 KB (4523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025163cce798cf3ca3e392896fd7713a7a327a74c71eebcb81ac726810bb39e4`  
		Last Modified: Tue, 12 Nov 2019 02:11:53 GMT  
		Size: 56.7 MB (56678908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feec192277bf2d7b06e673409f3e9feffa288ea648c36de641863e54c7fd688c`  
		Last Modified: Wed, 20 Nov 2019 00:22:01 GMT  
		Size: 95.1 MB (95137352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre13` - linux; s390x

```console
$ docker pull gradle@sha256:66c7c5e1e32191ab79416e3b68e4b75641a47b8351eb09b4f7b9cee6a64102b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223596116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea5359512eced13d27bccd2fb4b47b4dce80c9ce54ac6a06cade6c749a97438`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:42:17 GMT
ENV JAVA_VERSION=jdk-13.0.1+9
# Fri, 08 Nov 2019 02:42:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='58e841a26c1b3a0cf15f052797e5a6a91f8b65c78d0eb84e4eb6310b3af5b9ec';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c6258058557fd0ec6f0426c4671ad78e7b665cf8d487e5d07b690e792121b2f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.1_9.tar.gz';          ;;        s390x)          ESUM='e866aa35889358bb134675a079510b0cc279737c3fb26f30e229a69726833f5b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_s390x_linux_hotspot_13.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5bd06d9df1f76d953658fbe36812809b43e2d9dd00093e023aded64846f7af5a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.1%2B9/OpenJDK13U-jre_x64_linux_hotspot_13.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2019 00:43:02 GMT
CMD ["gradle"]
# Tue, 12 Nov 2019 00:43:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 Nov 2019 00:43:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 12 Nov 2019 00:43:03 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 Nov 2019 00:43:03 GMT
WORKDIR /home/gradle
# Tue, 12 Nov 2019 00:43:27 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:42:08 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:42:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:42:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1574b9d2915ca440a8df6067210b8b08a83fa5e1b26a947456fe7ce51ac62c79`  
		Last Modified: Fri, 08 Nov 2019 02:45:24 GMT  
		Size: 41.9 MB (41916656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51f59d9f4e9a794f0a5819eb266ba17ab3e031ee74ce4b07f6e0e9f992a9b16`  
		Last Modified: Tue, 12 Nov 2019 00:44:55 GMT  
		Size: 4.5 KB (4499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c9182a8c3317e15fea9b4554a082a526c2c6b2dbe466b8e793e51c1b2ac0c3`  
		Last Modified: Tue, 12 Nov 2019 00:45:06 GMT  
		Size: 48.1 MB (48094976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309103460d533b426ed0b8b98731c7b01e2ed5b2b03792081b92af72e99b9a29`  
		Last Modified: Tue, 19 Nov 2019 23:43:40 GMT  
		Size: 95.1 MB (95137323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:jre8`

```console
$ docker pull gradle@sha256:9cc6f3cd0b060375ab2275d2d9009c4f0afdcff215295fe83960c155bdf83ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jre8` - linux; amd64

```console
$ docker pull gradle@sha256:252c4aa523ce210f1384b4c1dbff1833888d54d2ddbc6bc1166907fa53d359bc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225153278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69106a8f82ff8683ecfcdb1fd02a0b14c6c8d7f145ea0efcf5fd6085b5f3263a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:57:07 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:57:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:57:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:57:08 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:57:08 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:57:26 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:57:26 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:57:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90bb5798781d7d972ceffbb8a018b8d4a6209e6ebffef84b49ae3eb603b83b3`  
		Last Modified: Thu, 19 Dec 2019 06:47:39 GMT  
		Size: 41.3 MB (41315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566cc78d89ca54deaef6f31921a9a0cf09937e4fe868206170480b1ac77f7cba`  
		Last Modified: Thu, 19 Dec 2019 10:59:56 GMT  
		Size: 4.5 KB (4490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52cba128b83aaed76d8e263f0b092bbc645fcebb37d69492f15e17ff3c8dad9`  
		Last Modified: Thu, 19 Dec 2019 11:00:07 GMT  
		Size: 48.6 MB (48646581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc26c95e2e9c68317162517ec85ea42b4c61a7d9068b8e7907d606971e74d56`  
		Last Modified: Thu, 19 Dec 2019 11:00:05 GMT  
		Size: 95.1 MB (95137279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre8` - linux; ppc64le

```console
$ docker pull gradle@sha256:4fb399803b5d67a4e672cfbcb06aefaa2f6e3309ef2e312e5bb320a5a4d7f26b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236621590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ccc6ec0d066910e82f75882d759c6fa535b780ead3c224e7bfad63eda8d8b1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:19:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:10:02 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:10:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:10:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:10:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:10:32 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:11:58 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:17:19 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:17:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ba113a58c3754d98a4cd77c5c3298e88b288fbbc6396e224d48f14a2051737`  
		Last Modified: Fri, 08 Nov 2019 02:27:06 GMT  
		Size: 40.4 MB (40395973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5215135253fc66c5e436a1c7cf0dfca107c7c2efb89e0c36aac6a44180c12616`  
		Last Modified: Fri, 08 Nov 2019 03:18:48 GMT  
		Size: 4.5 KB (4531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450733ab5d7b8c356095a70730cc5719812f0e8e98c7df2a6356d42c00c7e2f4`  
		Last Modified: Fri, 08 Nov 2019 03:19:03 GMT  
		Size: 56.7 MB (56679157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6a148705e89eea028591a3864b03e403b433637492bc5fe9b4f775d5423ecc`  
		Last Modified: Wed, 20 Nov 2019 00:20:21 GMT  
		Size: 95.1 MB (95137348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre8` - linux; s390x

```console
$ docker pull gradle@sha256:991ee619cc20d42a5c55a8c7a5ea05149e41de96f4745c29b69eb370b4155c79
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220684522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3531bbf861e7d285f38a4f9e9adc6b86e12729f7cd94c7ec623d3dee874eba1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:42:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='3a82861b74fb8c8a7910ce46482c5f7b1c239f5c52512729791b22760663c06e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='0d8ac42ca397376e7a437a28355143d2dcabf27729349c88714b4a8006871cb3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='bd06b84a1fc10e0a555431bc49a84e86df45de0be93c8ee4d09d13513219843b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:17:47 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:17:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:17:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:17:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:17:49 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:18:19 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:42 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33c44ac698abb009f50d3e585414a474039b681a90428ee2f4b108705725618`  
		Last Modified: Fri, 08 Nov 2019 02:44:46 GMT  
		Size: 39.0 MB (39004827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b31bf9feb646bd1283f25648587844e48832ba5cf55088429e39cc7de67d8f`  
		Last Modified: Fri, 08 Nov 2019 03:19:28 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f319e5024bfd448efb861ced63b58bcfaf2af7249978af930ef82734bef3e1fb`  
		Last Modified: Fri, 08 Nov 2019 03:19:38 GMT  
		Size: 48.1 MB (48095225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9197ffe30daa470cb2b2d989f05e49aa02894c024920d824aaa6f57b03a13840`  
		Last Modified: Tue, 19 Nov 2019 23:42:46 GMT  
		Size: 95.1 MB (95137300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gradle:latest`

```console
$ docker pull gradle@sha256:8ba20b563ed5c90f4e16705a0590d469190362fffc02dbbe308f05b81a16506d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `gradle:latest` - linux; amd64

```console
$ docker pull gradle@sha256:e5496a08fead0e48822aa86087b9d5f278795586a8588528bc289f0406e8d235
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288889902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc47c2ea2852e1ae6d6756cae8c568b3b255e198d589f81be8835390c6740a2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Dec 2019 06:44:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:44:09 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Thu, 19 Dec 2019 06:44:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Dec 2019 06:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:56:27 GMT
CMD ["gradle"]
# Thu, 19 Dec 2019 10:56:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 19 Dec 2019 10:56:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 19 Dec 2019 10:56:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 19 Dec 2019 10:56:29 GMT
WORKDIR /home/gradle
# Thu, 19 Dec 2019 10:56:57 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 10:56:57 GMT
ENV GRADLE_VERSION=6.0.1
# Thu, 19 Dec 2019 10:56:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Thu, 19 Dec 2019 10:57:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff21ce7d875874bffbded53d145025fc53273ed43e60390bfb159ce785b0aa`  
		Last Modified: Thu, 19 Dec 2019 06:47:19 GMT  
		Size: 13.3 MB (13323051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596d6c23adc7886652eea636e0c856146cc51d2da380a735645fad034dfe5069`  
		Last Modified: Thu, 19 Dec 2019 06:47:29 GMT  
		Size: 105.1 MB (105052689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07313090020e2216012e1a247dd3e9fce45ffac5a07713c234c1f02718a91a8`  
		Last Modified: Thu, 19 Dec 2019 10:59:36 GMT  
		Size: 4.5 KB (4492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d786c8e5ce8bd8e0a4bdfc0ecbde07e01b6607161798b7c5a1f68fd0673aea`  
		Last Modified: Thu, 19 Dec 2019 10:59:47 GMT  
		Size: 48.6 MB (48646474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84476db4b1ac2fc5e552d5bdb3d8247691ea1d57ccbddf9bc83c28455f012d3`  
		Last Modified: Thu, 19 Dec 2019 10:59:43 GMT  
		Size: 95.1 MB (95137274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:latest` - linux; ppc64le

```console
$ docker pull gradle@sha256:de97c2794be05db81624dc748d5f0bf6f774b3746b07e662593263f523fa126e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298448560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229fbb404cae0f708aa5d31816a664d221d3bf69c7a3d1450ba375ef51a3a708`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:21 GMT
ADD file:30ef96089560e5d0fd15cedc8abbf9dca4595d7a2e1c0b0ece79285e113362ae in / 
# Thu, 31 Oct 2019 22:20:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:39 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 22:39:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:18:19 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:18:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:18:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:07:19 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:07:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:07:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:07:41 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:07:44 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:09:21 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Nov 2019 00:16:56 GMT
ENV GRADLE_VERSION=6.0.1
# Wed, 20 Nov 2019 00:16:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Wed, 20 Nov 2019 00:17:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0df5667a7bd66c236484948884a4d4a0042007c89a7eed91d9a16f53e5b71bff`  
		Last Modified: Thu, 31 Oct 2019 22:23:11 GMT  
		Size: 30.4 MB (30399392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41e27fecb7f57b1fb0cdeac211f333f83d41762c7cda0d671d7aa78ff5b6b`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 35.2 KB (35209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f44d704e37f5d554db70eeefaa29a43e989b1e23e0006dccc091a663d57702`  
		Last Modified: Thu, 31 Oct 2019 22:23:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f86326bc71646eaa81919ef8752c4ade9ee718c562d8aa3d38338ffd9018a6`  
		Last Modified: Thu, 31 Oct 2019 22:23:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d843402600aecbd7872bf82eb97cdf645e7508c114773493c802cb7cc204d298`  
		Last Modified: Fri, 08 Nov 2019 02:26:32 GMT  
		Size: 14.0 MB (13968943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11691fec336d2f0ecf12299c6a2258179b6a03f37e8596ace4bdcf8340a84210`  
		Last Modified: Fri, 08 Nov 2019 02:26:43 GMT  
		Size: 102.2 MB (102223730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9315d5888c26e44dda21265c0782bd2458f9275e893dda525156726db64fd`  
		Last Modified: Fri, 08 Nov 2019 03:18:05 GMT  
		Size: 4.5 KB (4526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f9984d68d74068dfbcdb0f0ec1b51ba5716b1cca72aa6813cfbaae8f333f`  
		Last Modified: Fri, 08 Nov 2019 03:18:18 GMT  
		Size: 56.7 MB (56678368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b2332b39dc868b3d267bf94fca2afd107122993c7dec787be0f95aa7adf3a9`  
		Last Modified: Wed, 20 Nov 2019 00:19:42 GMT  
		Size: 95.1 MB (95137355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:latest` - linux; s390x

```console
$ docker pull gradle@sha256:271543f903e154259439857a293709a845db5d56bed51bb86dc75d8bdc27f92b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614cb05338d916b421497a72794e78adae51687596d0ce1ee3eb69b1ce6d7ab2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 Nov 2019 02:41:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Nov 2019 02:41:48 GMT
ENV JAVA_VERSION=jdk8u232-b09
# Fri, 08 Nov 2019 02:41:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='da87bdc04b47477b42afc76066dbd96efa35ad967238be03a0081f8840e893a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u232b09.tar.gz';          ;;        s390x)          ESUM='bd20cb8bf4cfab9d3e2b2ccfb9a6f9eda1e4e67b4103b9975d29de12c05ad1f5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_s390x_linux_hotspot_8u232b09.tar.gz';          ;;        amd64|x86_64)          ESUM='7b7884f2eb2ba2d47f4c0bf3bb1a2a95b73a3a7734bd47ebf9798483a7bcc423';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 08 Nov 2019 02:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Nov 2019 03:16:40 GMT
CMD ["gradle"]
# Fri, 08 Nov 2019 03:16:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 Nov 2019 03:16:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 08 Nov 2019 03:16:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 Nov 2019 03:16:43 GMT
WORKDIR /home/gradle
# Fri, 08 Nov 2019 03:17:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Nov 2019 23:41:33 GMT
ENV GRADLE_VERSION=6.0.1
# Tue, 19 Nov 2019 23:41:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
# Tue, 19 Nov 2019 23:41:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d364b7098b9f2e58579a3603dc0a12a1991353ac58ed339316e6762b21efba44
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b19c0383ed91f9b1804ed41cac85c7d675628ede6f1b32b27d54b75a6f40aa`  
		Last Modified: Fri, 08 Nov 2019 02:44:24 GMT  
		Size: 13.0 MB (13040836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75a894e76562f7781c6919af4bc9ab7ff662d7e916f0e18fe1261def191dec`  
		Last Modified: Fri, 08 Nov 2019 02:44:32 GMT  
		Size: 100.7 MB (100734555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b0f50dfaf38af9bcb739cda10fb6a0c7e8610af129e4285b00e833cf63be05`  
		Last Modified: Fri, 08 Nov 2019 03:19:04 GMT  
		Size: 4.5 KB (4497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5fff2ffc2e2c8a9e323c3696a7eacf9842b928e684dfa7cb4b2b577fab52d`  
		Last Modified: Fri, 08 Nov 2019 03:19:14 GMT  
		Size: 48.1 MB (48095072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1a287aa214edc225ccf89f9627b82a3b65d511ae9ffb5a99235667c5c1438d`  
		Last Modified: Tue, 19 Nov 2019 23:42:29 GMT  
		Size: 95.1 MB (95137322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
