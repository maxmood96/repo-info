## `adoptopenjdk:11-jdk-hotspot`

```console
$ docker pull adoptopenjdk@sha256:2074d708dda6b095c1f2465cd9f49d67a2ee20e1021d4ec90dc56405fc5fc01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `adoptopenjdk:11-jdk-hotspot` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:0f981f383db5fc6f807983b41069329d88eb2035c67c5c5bf7d51de4c0ac6d52
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240186404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fe1b7f401c8057781b7d91e9ca8760ad7bbc8ed5d1ca7f638931a5670380af`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Oct 2020 17:32:33 GMT
ADD file:435d9776fdd3a1834f344fb82e459dbbb67cd50c71ab5e29b719273888d5bb7c in / 
# Fri, 23 Oct 2020 17:32:34 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 17:32:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 17:32:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 17:32:36 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:19:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:20:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 19:20:02 GMT
ENV JAVA_VERSION=jdk-11.0.9.1+1
# Thu, 19 Nov 2020 19:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e9cea040cdf5d9b0a2986feaf87662e1aef68e876f4d66664cb2be36e26db412';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        armhf|armv7l)          ESUM='871618e96c57ef348fa068ffebf7e935c29c8601d59790a0d08dfd0d5c6f8d66';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d94b6b46a14ab0974b1c1b89661741126d8cf8a0068b471b8f5fa286a71636b1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        s390x)          ESUM='65cc100cc353d77c237f28b24323b647805d30267dcd6505ab7fdb538c16da49';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        amd64|x86_64)          ESUM='e388fd7f3f2503856d0b04fde6e151cbaa91a1df3bcebf1deddfc3729d677ca3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Nov 2020 19:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 19:20:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a5697faee43339ef8e33e3839060252392ad99325a48f7c9d7e93c22db4d4cf`  
		Last Modified: Thu, 08 Oct 2020 15:19:51 GMT  
		Size: 28.6 MB (28558714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba13d3bc422b493440f97a8f148d245e1999cb616cb05876edc3ef29e79852f2`  
		Last Modified: Fri, 23 Oct 2020 17:33:25 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a254829d9e55168306fd80a49e02eb015551facee9c444d9dce3b26d19238b82`  
		Last Modified: Fri, 23 Oct 2020 17:33:25 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03adaffd7e576f90e30e1dede0962fbbb0b58baede693e6375c2c137e506ef92`  
		Last Modified: Wed, 28 Oct 2020 17:37:00 GMT  
		Size: 16.0 MB (16031340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef19bd3e36af7eb5c63bd4ec610eb9b9b20c2319e7113de611242a3dae1ccb4`  
		Last Modified: Thu, 19 Nov 2020 19:26:07 GMT  
		Size: 195.6 MB (195595341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jdk-hotspot` - linux; arm variant v7

```console
$ docker pull adoptopenjdk@sha256:9fcf415a0ba41e644c35f1d3d5466157655f1672531f7dd987de72a69cc66932
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.8 MB (222773822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b4b6402a34c8e5504995d8c89d26b779e7e0a2bbfe49098442ff3608f1ba5f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 25 Nov 2020 22:59:41 GMT
ADD file:b2c2bab174379d89834d816a7519d4758ea075a1aa00c6fe305c329089a15d3d in / 
# Wed, 25 Nov 2020 22:59:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:59:46 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:59:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:59:48 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:18:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 25 Nov 2020 23:18:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:19:34 GMT
ENV JAVA_VERSION=jdk-11.0.9.1+1
# Wed, 25 Nov 2020 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e9cea040cdf5d9b0a2986feaf87662e1aef68e876f4d66664cb2be36e26db412';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        armhf|armv7l)          ESUM='871618e96c57ef348fa068ffebf7e935c29c8601d59790a0d08dfd0d5c6f8d66';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d94b6b46a14ab0974b1c1b89661741126d8cf8a0068b471b8f5fa286a71636b1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        s390x)          ESUM='65cc100cc353d77c237f28b24323b647805d30267dcd6505ab7fdb538c16da49';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        amd64|x86_64)          ESUM='e388fd7f3f2503856d0b04fde6e151cbaa91a1df3bcebf1deddfc3729d677ca3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 25 Nov 2020 23:19:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Nov 2020 23:19:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3a20c5d313f7c8b8e8c7633f51e0ecfd29c87d093315961a38a46da87c3b2be`  
		Last Modified: Fri, 06 Nov 2020 19:09:39 GMT  
		Size: 24.0 MB (24041185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67966bd810cedcb4375094e9af4a7197675edc270d8d16004ab58a8daacbe918`  
		Last Modified: Wed, 25 Nov 2020 23:01:51 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282ed6897607dd46838e55e3fabf03616b42c2275226012a008da3cf081051`  
		Last Modified: Wed, 25 Nov 2020 23:01:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac8cbd0a98818487f6f28b732e1df5a291bc778f42a14ac6be7b4d5eab350bb`  
		Last Modified: Wed, 25 Nov 2020 23:22:35 GMT  
		Size: 14.9 MB (14906111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91073fca729c608de50e13226f3ee7ac87aa02e024f3b7a416db2a39c3111643`  
		Last Modified: Wed, 25 Nov 2020 23:23:52 GMT  
		Size: 183.8 MB (183825486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jdk-hotspot` - linux; arm64 variant v8

```console
$ docker pull adoptopenjdk@sha256:49787bace0362272763d9d3d63a9320bae955a9738d4283da2f825704fe3363a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235347634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf207018d56a308a3b8678f10419a2905eaefb28c62d6b0ab3d177f02daa81f6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 25 Nov 2020 22:43:12 GMT
ADD file:a9ede6466d698f7a9f018b5121f755f98a7322ba320e16ad207aaf3819ea8bc2 in / 
# Wed, 25 Nov 2020 22:43:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:43:17 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:20 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:31:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 25 Nov 2020 23:32:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:32:47 GMT
ENV JAVA_VERSION=jdk-11.0.9.1+1
# Wed, 25 Nov 2020 23:33:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e9cea040cdf5d9b0a2986feaf87662e1aef68e876f4d66664cb2be36e26db412';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        armhf|armv7l)          ESUM='871618e96c57ef348fa068ffebf7e935c29c8601d59790a0d08dfd0d5c6f8d66';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d94b6b46a14ab0974b1c1b89661741126d8cf8a0068b471b8f5fa286a71636b1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        s390x)          ESUM='65cc100cc353d77c237f28b24323b647805d30267dcd6505ab7fdb538c16da49';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        amd64|x86_64)          ESUM='e388fd7f3f2503856d0b04fde6e151cbaa91a1df3bcebf1deddfc3729d677ca3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 25 Nov 2020 23:33:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Nov 2020 23:33:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a970164f39c1a46f71b3615bc9d5b6710832766b530d9179db8e36563f705abb`  
		Last Modified: Fri, 06 Nov 2020 16:25:39 GMT  
		Size: 27.2 MB (27168047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c66f1fb5a2d6587841797a3b0d4c2d0fd0b7ccd867e55a1314cee2e90ad47d`  
		Last Modified: Wed, 25 Nov 2020 22:44:54 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94362ba2c285844f83a1b1e2dac5217b0426427f8bb809af534b5f4d751e298c`  
		Last Modified: Wed, 25 Nov 2020 22:44:54 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1a7a5d722a57ef6dd66ff3b0675957c298d427e78f7796b4d320c04511018a`  
		Last Modified: Wed, 25 Nov 2020 23:35:31 GMT  
		Size: 15.9 MB (15900377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9057135e63e8068d5afd3507863734fc3203088872e1d2e1f4affdc94531f5bf`  
		Last Modified: Wed, 25 Nov 2020 23:36:35 GMT  
		Size: 192.3 MB (192278174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jdk-hotspot` - linux; ppc64le

```console
$ docker pull adoptopenjdk@sha256:97aa6ebd98c266422d020922fbd6bc6ac0b7ee8be892ab9eb6d0bce6c1b414b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228300842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bfacdb60f64f5d054cd87e816cd344fc89b493be0f2a93172dd52a1775e797`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 25 Nov 2020 22:22:45 GMT
ADD file:349669e872fc8d76ff551a3eb05bb336a7d13ef8d99dc4f7604d54fc263a1a40 in / 
# Wed, 25 Nov 2020 22:23:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:23:19 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:23:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:23:34 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 22:44:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 25 Nov 2020 22:46:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:47:29 GMT
ENV JAVA_VERSION=jdk-11.0.9.1+1
# Wed, 25 Nov 2020 22:47:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e9cea040cdf5d9b0a2986feaf87662e1aef68e876f4d66664cb2be36e26db412';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        armhf|armv7l)          ESUM='871618e96c57ef348fa068ffebf7e935c29c8601d59790a0d08dfd0d5c6f8d66';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d94b6b46a14ab0974b1c1b89661741126d8cf8a0068b471b8f5fa286a71636b1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        s390x)          ESUM='65cc100cc353d77c237f28b24323b647805d30267dcd6505ab7fdb538c16da49';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        amd64|x86_64)          ESUM='e388fd7f3f2503856d0b04fde6e151cbaa91a1df3bcebf1deddfc3729d677ca3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 25 Nov 2020 22:47:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Nov 2020 22:48:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0162c086f3047a91e0409b0f80e741887de3c5e5490b9be62d74a5c054c7d6b0`  
		Last Modified: Mon, 09 Nov 2020 19:03:51 GMT  
		Size: 33.3 MB (33278639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61108ece12882b4998d113ea62b7f4d286877fef610d4aae5b2d2f17d68bf8a4`  
		Last Modified: Wed, 25 Nov 2020 22:27:34 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a92bd8a59839464b3f3c73564e77cb7f1868ac3e96fcc07c1a77b85c51ba1b1`  
		Last Modified: Wed, 25 Nov 2020 22:27:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0126056f0b80e5735fc6cef6d439c93c998a81a55e09f213e73e6a7ef1f8cca6`  
		Last Modified: Wed, 25 Nov 2020 23:16:22 GMT  
		Size: 17.2 MB (17210167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac2bc3c759e814f7f1f29fa488951b701351df3913b84df5585971b98c0139`  
		Last Modified: Wed, 25 Nov 2020 23:17:28 GMT  
		Size: 177.8 MB (177810993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jdk-hotspot` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:d35d877b3c73b17b17dec8707aa2f8f20134d5e2824777fcceae1b489afcf650
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213083656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76667ca6fafcdb09e2cab9701f68d55302ab0c309e1441d81c7cdeb67e83bb6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Oct 2020 19:09:19 GMT
ADD file:9b934c86e9ab1dd29cef318d8dd9cd1228b9d92124f434c50ad7d03ede1a5c76 in / 
# Fri, 23 Oct 2020 19:09:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:09:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:09:27 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:09:27 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:41:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:41:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 19:42:24 GMT
ENV JAVA_VERSION=jdk-11.0.9.1+1
# Thu, 19 Nov 2020 19:42:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e9cea040cdf5d9b0a2986feaf87662e1aef68e876f4d66664cb2be36e26db412';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        armhf|armv7l)          ESUM='871618e96c57ef348fa068ffebf7e935c29c8601d59790a0d08dfd0d5c6f8d66';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_arm_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d94b6b46a14ab0974b1c1b89661741126d8cf8a0068b471b8f5fa286a71636b1';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        s390x)          ESUM='65cc100cc353d77c237f28b24323b647805d30267dcd6505ab7fdb538c16da49';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        amd64|x86_64)          ESUM='e388fd7f3f2503856d0b04fde6e151cbaa91a1df3bcebf1deddfc3729d677ca3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.9.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Nov 2020 19:42:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 19:42:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d3e8e1a5d50716d6aabb0cef46599f9e7a722a560910d6f724737aaef0a7d6c3`  
		Last Modified: Mon, 12 Oct 2020 16:45:31 GMT  
		Size: 27.2 MB (27224393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04282efaafb3c9b53bba677fc3c06c478dc1613c1f21939bfa2c113aeef2f99c`  
		Last Modified: Fri, 23 Oct 2020 19:10:20 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6269ae100536d7559ae6ebe6606b4405ebb706c3d963926c5568b6e7fd954582`  
		Last Modified: Fri, 23 Oct 2020 19:10:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cd8065d26d8f90607b2debf915de6242befbe898f8fb305dbd99dc8df92d3a`  
		Last Modified: Wed, 28 Oct 2020 17:59:30 GMT  
		Size: 15.8 MB (15772935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5d2956542b2e766926f5144a6a9647c31652aab2286dc74a60d32be9de5873`  
		Last Modified: Thu, 19 Nov 2020 19:50:03 GMT  
		Size: 170.1 MB (170085294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jdk-hotspot` - windows version 10.0.17763.1577; amd64

```console
$ docker pull adoptopenjdk@sha256:693450b86d7b396940f74d38d961324de794e1bc6892ba753b7cee6085547e7a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2760350142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce52a44700dc2185ade812c8c6f1e44e71c84df14fb8f19e2e40acfa3960fe66`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Nov 2020 19:23:41 GMT
ENV JAVA_VERSION=jdk-11.0.9.1+1
# Thu, 19 Nov 2020 19:26:00 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.9.1_1.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.9.1_1.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (e949c3a7d84e2423f2557e6be3f85058e1c9dc2b5615c8fb6189831e29ee2cd9) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e949c3a7d84e2423f2557e6be3f85058e1c9dc2b5615c8fb6189831e29ee2cd9') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 19 Nov 2020 19:26:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da5a67a9f3a363cb69c8104913a5a58c1c47e8f648a07d057fc28a5f98790e60`  
		Last Modified: Wed, 11 Nov 2020 13:37:50 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b0ae585ffee7c272a7304f97812a23a118cfacd89a5098d3e0309376282185`  
		Last Modified: Thu, 19 Nov 2020 19:51:11 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30eeb8643aa8ec70dbe7e5b11dfe3c0562e86a503439d56eb2e4c8ffc7f08ea3`  
		Last Modified: Thu, 19 Nov 2020 19:51:40 GMT  
		Size: 372.3 MB (372317446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2a95f3bf82cab83369a38bdafb8f521b18ce41a5ad57a2b883301cc68b4724`  
		Last Modified: Thu, 19 Nov 2020 19:51:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-jdk-hotspot` - windows version 10.0.14393.4046; amd64

```console
$ docker pull adoptopenjdk@sha256:9a0eaa3b501e5f6105a68bd728f7436ec364a0ca607b2121174e483aacbd064d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6143674265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f55672821645edcf8a6c822505c1cc79e661e9b41d8974f245fe7f289f717c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Nov 2020 19:26:08 GMT
ENV JAVA_VERSION=jdk-11.0.9.1+1
# Thu, 19 Nov 2020 19:29:09 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.9.1_1.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_windows_hotspot_11.0.9.1_1.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (e949c3a7d84e2423f2557e6be3f85058e1c9dc2b5615c8fb6189831e29ee2cd9) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e949c3a7d84e2423f2557e6be3f85058e1c9dc2b5615c8fb6189831e29ee2cd9') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 19 Nov 2020 19:29:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8043cbf9e851e4bcbf4e51e4dea3d42e40e791f7ff0e729622ac07aa4e8d92f`  
		Last Modified: Thu, 19 Nov 2020 19:51:55 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87972166e27f8ff8673030df123ed4cd0b2485e8b46925486a4bc03ff9e5efc`  
		Last Modified: Thu, 19 Nov 2020 19:52:30 GMT  
		Size: 373.1 MB (373112042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52654af26726c0aec22fdd3e14eac8228ad5cfeb4ef3cfd5239b85db6383778a`  
		Last Modified: Thu, 19 Nov 2020 19:51:55 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
