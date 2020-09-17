## `adoptopenjdk:8u262-b10-jdk-openj9-0.21.0-bionic`

```console
$ docker pull adoptopenjdk@sha256:13f1e763eb0eb33386eff9021f967625727d6ccd1ebe9eb387c08cce1c88bbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `adoptopenjdk:8u262-b10-jdk-openj9-0.21.0-bionic` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:752ed58a8ce81db69d0f6ae36806f52f005f086918723b289f04fb2ff5184ff5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155932347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f39785689a709375b1c898f099bae963885327f6e058dc2a61057030182d15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:34:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Sep 2020 23:35:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:38:04 GMT
ENV JAVA_VERSION=jdk8u262-b10_openj9-0.21.0
# Wed, 16 Sep 2020 23:38:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='8659c84c5c5d94ffed4789f06f2be401e59020b83e95fd45e71992f425483a13';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_ppc64le_linux_openj9_8u262b10_openj9-0.21.0.tar.gz';          ;;        s390x)          ESUM='37fe91840b1d8fa98bc6a859ef29b28e0b2187cd926c9d58743f7022640f8d8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_s390x_linux_openj9_8u262b10_openj9-0.21.0.tar.gz';          ;;        amd64|x86_64)          ESUM='bdeab95a04462ae48df1dc1c53c833f86bfa34bd3a86c65c7adad7c096a1dbce';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_x64_linux_openj9_8u262b10_openj9-0.21.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 16 Sep 2020 23:38:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Sep 2020 23:38:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1854bb447e96b1e5e1051bef627b6167e587e689da45e38caada1a12fd195061`  
		Last Modified: Wed, 16 Sep 2020 23:41:46 GMT  
		Size: 13.9 MB (13875245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693fff1667b1c9a691bae3aa5cb0efcd5134bc7546cc66435ac0a9a7117cb5d3`  
		Last Modified: Wed, 16 Sep 2020 23:44:44 GMT  
		Size: 115.4 MB (115356480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u262-b10-jdk-openj9-0.21.0-bionic` - linux; ppc64le

```console
$ docker pull adoptopenjdk@sha256:69919696211998a68f6b3a6968b8783e623bab7a0d833f4b0ab5830be9327d64
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160881066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39a471cd108cb6e4275d2b8125b0f29f9cce73f8934890a1dfc27216b74be53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 23:54:24 GMT
ADD file:8f9c69dc1466e3fa3f47ef42daa366ad93d6a34e816768fb8dd35e541e61b9af in / 
# Wed, 16 Sep 2020 23:54:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:54:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:55:02 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:55:04 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:08:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Sep 2020 00:09:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:17:41 GMT
ENV JAVA_VERSION=jdk8u262-b10_openj9-0.21.0
# Thu, 17 Sep 2020 00:18:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='8659c84c5c5d94ffed4789f06f2be401e59020b83e95fd45e71992f425483a13';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_ppc64le_linux_openj9_8u262b10_openj9-0.21.0.tar.gz';          ;;        s390x)          ESUM='37fe91840b1d8fa98bc6a859ef29b28e0b2187cd926c9d58743f7022640f8d8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_s390x_linux_openj9_8u262b10_openj9-0.21.0.tar.gz';          ;;        amd64|x86_64)          ESUM='bdeab95a04462ae48df1dc1c53c833f86bfa34bd3a86c65c7adad7c096a1dbce';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_x64_linux_openj9_8u262b10_openj9-0.21.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Sep 2020 00:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Sep 2020 00:18:27 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:cab4317aedcc40ff2a2f72b253d06e717095a7e3cf1c28ab1ede6b2ee2113c28`  
		Last Modified: Mon, 07 Sep 2020 15:50:42 GMT  
		Size: 30.4 MB (30407200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62ab144e14fcd18dc307805290e556f638df374f6647d94816e4aa11f2c014a`  
		Last Modified: Thu, 17 Sep 2020 00:01:25 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab01c61d5c7930829a28ce67f84f50f322fbb587f8c867af94413ae163e19c`  
		Last Modified: Thu, 17 Sep 2020 00:01:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9979d7fedd70abf0a194bac264009b81e45db4df709a1facde8ae8ab2efdf0ba`  
		Last Modified: Thu, 17 Sep 2020 00:25:41 GMT  
		Size: 14.5 MB (14518581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343171a36736a77d4d86986eb05c4416c2d6fd87dc9b4a5c5328020f852c4329`  
		Last Modified: Thu, 17 Sep 2020 00:29:54 GMT  
		Size: 116.0 MB (115954243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u262-b10-jdk-openj9-0.21.0-bionic` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:3be109f985e7fbd484772b54236f09d632b28d37d3981b23a800b810fc6d8e10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153995744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5891dc60b578c4c90ec81ce78efbfea0ed5734e7f63565c6845f8846c4072153`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:51:22 GMT
ADD file:835d62b9e8aa5985cb778cef4129baec4d3688713202ad55a1fa54bb9daf136e in / 
# Wed, 16 Sep 2020 22:51:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:51:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:51:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:51:26 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:13:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Sep 2020 23:13:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:15:44 GMT
ENV JAVA_VERSION=jdk8u262-b10_openj9-0.21.0
# Wed, 16 Sep 2020 23:15:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='8659c84c5c5d94ffed4789f06f2be401e59020b83e95fd45e71992f425483a13';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_ppc64le_linux_openj9_8u262b10_openj9-0.21.0.tar.gz';          ;;        s390x)          ESUM='37fe91840b1d8fa98bc6a859ef29b28e0b2187cd926c9d58743f7022640f8d8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_s390x_linux_openj9_8u262b10_openj9-0.21.0.tar.gz';          ;;        amd64|x86_64)          ESUM='bdeab95a04462ae48df1dc1c53c833f86bfa34bd3a86c65c7adad7c096a1dbce';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_x64_linux_openj9_8u262b10_openj9-0.21.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 16 Sep 2020 23:15:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Sep 2020 23:15:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:cedb15d27487fa2e085bee049ff12636f8ba01e63c3bbdc094088e8bb7d8b641`  
		Last Modified: Mon, 07 Sep 2020 15:51:50 GMT  
		Size: 25.4 MB (25370945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4002d8c6f20fd20eb7aa7e91bfa01443724872a214bb07ad9cf86a810c86ed`  
		Last Modified: Wed, 16 Sep 2020 22:52:22 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4b15c73b5f07d5d69927632e5a59fb80805da20bc1fabc30f973b5b2ff5805`  
		Last Modified: Wed, 16 Sep 2020 22:52:22 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e9b0ab5887bff45bcb68bdc19ff28f198af83c3c03d9e85a75ae6214c8dade`  
		Last Modified: Wed, 16 Sep 2020 23:18:16 GMT  
		Size: 13.6 MB (13595571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8207780b48dc4013c06ef84f8f270ad1f90263a8f153cbadcd238489acfeaf9`  
		Last Modified: Wed, 16 Sep 2020 23:20:26 GMT  
		Size: 115.0 MB (115028191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
