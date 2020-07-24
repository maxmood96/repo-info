## `adoptopenjdk:8u262-b10-jdk-hotspot`

```console
$ docker pull adoptopenjdk@sha256:d71a15c00fa273d6190ce590bbfb71efe0871241050539fd1241b12fa2f51f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `adoptopenjdk:8u262-b10-jdk-hotspot` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:9319440f5ca516bfa8550a83163825e316384f13a39b213d1db9ab01aaa6d142
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144345378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab86ecd5bde9c35ae45e2d72691b1cae0b8ef81508b90c4fb67013f02ecf2ca`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 24 Jul 2020 15:17:03 GMT
ENV JAVA_VERSION=jdk8u262-b10
# Fri, 24 Jul 2020 15:17:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7be0b2a4c749a277302a54b456624c076b3a5b990ad502e2a72d803ab31aecab';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u262b10.tar.gz';          ;;        armhf|armv7l)          ESUM='dd85ebb9a64916b4b621a23729e3360adb363d430bf1e99e98f25397834d74bd';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u262b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d2a16915fb85ba851145c91cda5666cb78f06bf4713a2b3bdce813779ff972c2';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u262b10.tar.gz';          ;;        s390x)          ESUM='a504af6924a095cfb6c392653dccd7299925048c91b399d05efa95a094820120';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u262b10.tar.gz';          ;;        amd64|x86_64)          ESUM='733755fd649fad6ae91fc083f7e5a5a0b56410fb6ac1815cff29f744b128b1b1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u262b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 15:17:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:41534844af489a0bc28ed7b1fd06b356e7afee39e0dc17ecdeebdd6b8aa0aff4`  
		Last Modified: Fri, 24 Jul 2020 15:22:58 GMT  
		Size: 103.7 MB (103736366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u262-b10-jdk-hotspot` - linux; arm variant v7

```console
$ docker pull adoptopenjdk@sha256:6b411e24eb6d78b2deb98da7b91c0188c9e9a338f2884e149db7ffe960b52b1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133308889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ce6da3c30a1cdc791520409464c4bd28ef73ecd162b8d47995b4bb929bb341`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 06 Jul 2020 20:07:11 GMT
ADD file:6797f65071d6d263c6466e89bb2db63753b08510aef54a1dc28891fbf2e58799 in / 
# Mon, 06 Jul 2020 20:07:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 20:07:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 20:07:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 20:07:19 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 21:54:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Jul 2020 20:58:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Jul 2020 20:58:24 GMT
ENV JAVA_VERSION=jdk8u262-b10
# Fri, 17 Jul 2020 20:58:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7be0b2a4c749a277302a54b456624c076b3a5b990ad502e2a72d803ab31aecab';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u262b10.tar.gz';          ;;        armhf|armv7l)          ESUM='dd85ebb9a64916b4b621a23729e3360adb363d430bf1e99e98f25397834d74bd';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u262b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d2a16915fb85ba851145c91cda5666cb78f06bf4713a2b3bdce813779ff972c2';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u262b10.tar.gz';          ;;        s390x)          ESUM='a504af6924a095cfb6c392653dccd7299925048c91b399d05efa95a094820120';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u262b10.tar.gz';          ;;        amd64|x86_64)          ESUM='733755fd649fad6ae91fc083f7e5a5a0b56410fb6ac1815cff29f744b128b1b1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u262b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 17 Jul 2020 20:58:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:db182fa07ba527098363444f993730c582b86e361f0ac7ae981ba0e9ca768c84`  
		Last Modified: Mon, 06 Jul 2020 15:46:25 GMT  
		Size: 22.3 MB (22276511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e85650936bd5be5a40db91349e387ede7738f5f7938d6421cb9d64eb021a5a3`  
		Last Modified: Mon, 06 Jul 2020 20:10:21 GMT  
		Size: 35.5 KB (35457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258b890879c48b8d0f50ea632de0a703079d7f5d973ec47338cbe791bb8e30d5`  
		Last Modified: Mon, 06 Jul 2020 20:10:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f858a12ecedcf911e3fea9bb17332b53a888444834a3e3d12cd25be830898d`  
		Last Modified: Mon, 06 Jul 2020 20:10:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cc999ed63826a5b44acb46406a5dc7d80f1604cc4f06927d88bf6c5e79b497`  
		Last Modified: Fri, 17 Jul 2020 21:00:57 GMT  
		Size: 12.8 MB (12816746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb3babd17102cf53f105929187fd553570511c94d4bc3b46b5757b57ea17143`  
		Last Modified: Fri, 17 Jul 2020 21:01:14 GMT  
		Size: 98.2 MB (98179137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u262-b10-jdk-hotspot` - linux; arm64 variant v8

```console
$ docker pull adoptopenjdk@sha256:c482fa7b7736c49ac4bb1cf64ad3ca3b0284f7bc1262b86004d0a9d06b4d9628
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140914576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597553595302f6e5225045a713f3926f7ccb295706440167593d7bba4e519b3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 06 Jul 2020 22:04:54 GMT
ADD file:090a5d48524c4b10f867bf6bb80c106a69bf839c876de86912ed0c633349a1ab in / 
# Mon, 06 Jul 2020 22:04:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:04:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:01 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 01:12:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Jul 2020 20:42:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Jul 2020 20:42:20 GMT
ENV JAVA_VERSION=jdk8u262-b10
# Fri, 17 Jul 2020 20:42:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7be0b2a4c749a277302a54b456624c076b3a5b990ad502e2a72d803ab31aecab';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u262b10.tar.gz';          ;;        armhf|armv7l)          ESUM='dd85ebb9a64916b4b621a23729e3360adb363d430bf1e99e98f25397834d74bd';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u262b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d2a16915fb85ba851145c91cda5666cb78f06bf4713a2b3bdce813779ff972c2';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u262b10.tar.gz';          ;;        s390x)          ESUM='a504af6924a095cfb6c392653dccd7299925048c91b399d05efa95a094820120';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u262b10.tar.gz';          ;;        amd64|x86_64)          ESUM='733755fd649fad6ae91fc083f7e5a5a0b56410fb6ac1815cff29f744b128b1b1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u262b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 17 Jul 2020 20:42:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:68fe03cb170d6a5101858131ae1eac5393a4f018d70abfcd1348fd240ee0ccc5`  
		Last Modified: Tue, 30 Jun 2020 16:25:30 GMT  
		Size: 23.7 MB (23719365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18959295effbb87ec216a036a1821f8b7e183072faaa80a6d7f97aa14b51b2af`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 35.2 KB (35189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51118fb70ce38c0c2e667ecd5fc941590875e2fd9e55dd17c90073f085ba5970`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a5d9eae931d5a3b5a3bcb840e11167c2d3d03ec22258cde67197babf908ed`  
		Last Modified: Mon, 06 Jul 2020 22:06:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5858fe3213ff710f6c318742f085137ce8fcea1e001c321df12f5871e95b09`  
		Last Modified: Fri, 17 Jul 2020 20:45:09 GMT  
		Size: 13.3 MB (13284377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4055bed4357e0db7b73f069b258ba8be8e4a30a1f5d995f6883af964ff8328dc`  
		Last Modified: Fri, 17 Jul 2020 20:45:22 GMT  
		Size: 103.9 MB (103874606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u262-b10-jdk-hotspot` - linux; ppc64le

```console
$ docker pull adoptopenjdk@sha256:377e579b2913e6137ea70ac284974aa2c8f101b99cc8797d102772f83d24f1e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145850328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc22f825fd9803d5ef02e968cfa02e799c22f15551b724130fe12c01f7917c61`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 24 Jul 2020 15:45:32 GMT
ENV JAVA_VERSION=jdk8u262-b10
# Fri, 24 Jul 2020 15:45:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7be0b2a4c749a277302a54b456624c076b3a5b990ad502e2a72d803ab31aecab';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u262b10.tar.gz';          ;;        armhf|armv7l)          ESUM='dd85ebb9a64916b4b621a23729e3360adb363d430bf1e99e98f25397834d74bd';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u262b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d2a16915fb85ba851145c91cda5666cb78f06bf4713a2b3bdce813779ff972c2';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u262b10.tar.gz';          ;;        s390x)          ESUM='a504af6924a095cfb6c392653dccd7299925048c91b399d05efa95a094820120';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u262b10.tar.gz';          ;;        amd64|x86_64)          ESUM='733755fd649fad6ae91fc083f7e5a5a0b56410fb6ac1815cff29f744b128b1b1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u262b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 15:46:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
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
	-	`sha256:9c710c0c49381425da0d6bef2cde1374fd268bb249d5cbee4e621ada1f3f55c9`  
		Last Modified: Fri, 24 Jul 2020 16:19:55 GMT  
		Size: 100.9 MB (100889859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u262-b10-jdk-hotspot` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:ac5b5d8870f3b0dbb7bb29e1cf0efafcdbc0e2323492a1d79e9795356feadc4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137757835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab2fa5bb679cbdd918d0875d66762ad3efaa678f5e44dba696b66c7855b1167`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:07:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jul 2020 15:08:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:08:09 GMT
ENV JAVA_VERSION=jdk8u262-b10
# Fri, 24 Jul 2020 15:08:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7be0b2a4c749a277302a54b456624c076b3a5b990ad502e2a72d803ab31aecab';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u262b10.tar.gz';          ;;        armhf|armv7l)          ESUM='dd85ebb9a64916b4b621a23729e3360adb363d430bf1e99e98f25397834d74bd';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u262b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d2a16915fb85ba851145c91cda5666cb78f06bf4713a2b3bdce813779ff972c2';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u262b10.tar.gz';          ;;        s390x)          ESUM='a504af6924a095cfb6c392653dccd7299925048c91b399d05efa95a094820120';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u262b10.tar.gz';          ;;        amd64|x86_64)          ESUM='733755fd649fad6ae91fc083f7e5a5a0b56410fb6ac1815cff29f744b128b1b1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u262b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 15:08:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebf51d7ec44631141845860c73ae158d9eca8b087d075b3b5c3e7661e8ef437`  
		Last Modified: Fri, 24 Jul 2020 15:18:57 GMT  
		Size: 13.6 MB (13596135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70587dae3bafabe6dd82b7cd04533e51ca89ed1307f5f0202bc2898f5273f93d`  
		Last Modified: Fri, 24 Jul 2020 15:19:09 GMT  
		Size: 98.8 MB (98754967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u262-b10-jdk-hotspot` - windows version 10.0.14393.3808; amd64

```console
$ docker pull adoptopenjdk@sha256:da86a3c75f10fc77c00591e14a516f7944895e9d965d6971b5499bf372543a8e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5939101579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f6fa3e584fcb93ba05bb0ba6e7c7b703fba5bfbec6cb7766f289ab1f9bc044`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jul 2020 13:07:07 GMT
ENV JAVA_VERSION=jdk8u262-b10
# Wed, 22 Jul 2020 13:09:31 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_windows_hotspot_8u262b10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_windows_hotspot_8u262b10.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (251429e9c5ea2d2950aceca10c67e4bf5be3f5f299f2fad4c9757b5ac857cc2c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '251429e9c5ea2d2950aceca10c67e4bf5be3f5f299f2fad4c9757b5ac857cc2c') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370c95b2c779075c70cdf7dc79626aeb314b359ac7544cc6c6d8e27badf5c0f3`  
		Last Modified: Wed, 22 Jul 2020 13:45:03 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9201780d2ba901aa06c2fcb5977e0a190cad4928390cce95a5cfbff41d891e82`  
		Last Modified: Wed, 22 Jul 2020 13:45:21 GMT  
		Size: 201.6 MB (201637206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u262-b10-jdk-hotspot` - windows version 10.0.17763.1339; amd64

```console
$ docker pull adoptopenjdk@sha256:d9d62eed761b6ff26ca5d05ac94e07eb5a7f05a03f2162f64fde3818c4c04c9b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2511182258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b585670b5466b42243884582073c2102225f1306d5adfdd1d8b5acc277cec46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jul 2020 22:28:03 GMT
ENV JAVA_VERSION=jdk8u262-b10
# Fri, 17 Jul 2020 22:29:54 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_windows_hotspot_8u262b10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_windows_hotspot_8u262b10.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (251429e9c5ea2d2950aceca10c67e4bf5be3f5f299f2fad4c9757b5ac857cc2c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '251429e9c5ea2d2950aceca10c67e4bf5be3f5f299f2fad4c9757b5ac857cc2c') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27e43a80b4831dc9da4a0c00301132e0e7a855fc048e9c47bfced4251722fab`  
		Last Modified: Sat, 18 Jul 2020 01:13:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab14fb5144d0debd0b965f74cd8eb552da014431362e8f2b5190a03be848d961`  
		Last Modified: Sat, 18 Jul 2020 01:14:32 GMT  
		Size: 201.0 MB (200987701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
