## `adoptopenjdk:13-jre-openj9`

```console
$ docker pull adoptopenjdk@sha256:82623f974233d125206c9f1a684b9e601c08e3876686a978f6adc7e54ed5fc49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.14393.3866; amd64
	-	windows version 10.0.17763.1397; amd64

### `adoptopenjdk:13-jre-openj9` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:1172f2559d9f7d5f55afa55e53e4f4c70ddf9531ceb131a011f820a947ef1a6e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82193177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4ef12a97ee36c2b6fba122c4e569e683082c15cf0c413252888fbb4382670a`
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
# Fri, 24 Jul 2020 15:18:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:20:38 GMT
ENV JAVA_VERSION=jdk-13.0.2+8_openj9-0.18.0
# Fri, 24 Jul 2020 15:21:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='7bf8dc4c3b95e87b154f7bc2f9388a6539413fe76d49b362bba878217ccb7ed7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_ppc64le_linux_openj9_13.0.2_8_openj9-0.18.0.tar.gz';          ;;        s390x)          ESUM='d3051351ead072a19225427b83f71b5efe8ceb1133bbdff6c19ec7a380b70cbc';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_s390x_linux_openj9_13.0.2_8_openj9-0.18.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a0ab38607811e282f64082edc68a2dea3fa6a5113391efb124a6d7d02883110a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_x64_linux_openj9_13.0.2_8_openj9-0.18.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 15:21:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 15:21:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
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
	-	`sha256:a9ba6ced65f28cc40fd6f16e78bf56908a7f0c33325033060d477581d40935f0`  
		Last Modified: Fri, 24 Jul 2020 15:23:55 GMT  
		Size: 13.3 MB (13312034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355dc712d47228390858c0e88f3952b7d47cc3246b7c56254107ef909882f38d`  
		Last Modified: Fri, 24 Jul 2020 15:27:38 GMT  
		Size: 42.1 MB (42147643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jre-openj9` - linux; ppc64le

```console
$ docker pull adoptopenjdk@sha256:0a8c1dff8b284f68c6df8ac7fcb88c37291e2ed87fdea6211fe037fba9bf2b37
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86892099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1cd62600e59aff84deb6e579160e87f46e82f5528bef639201c6bad79eb3bb`
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
# Fri, 24 Jul 2020 15:55:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:12:35 GMT
ENV JAVA_VERSION=jdk-13.0.2+8_openj9-0.18.0
# Fri, 24 Jul 2020 16:14:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='7bf8dc4c3b95e87b154f7bc2f9388a6539413fe76d49b362bba878217ccb7ed7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_ppc64le_linux_openj9_13.0.2_8_openj9-0.18.0.tar.gz';          ;;        s390x)          ESUM='d3051351ead072a19225427b83f71b5efe8ceb1133bbdff6c19ec7a380b70cbc';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_s390x_linux_openj9_13.0.2_8_openj9-0.18.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a0ab38607811e282f64082edc68a2dea3fa6a5113391efb124a6d7d02883110a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_x64_linux_openj9_13.0.2_8_openj9-0.18.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 16:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 16:14:54 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
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
	-	`sha256:6574bb84c5b961758d36d667ddfc046d079469e6fcb3d49ecf4e505a4a3444a7`  
		Last Modified: Fri, 24 Jul 2020 16:23:10 GMT  
		Size: 14.0 MB (13956698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aca5fd4dc2334dc4fbd20f2937068b83237824f590a42b8a91fbd6533dda2de`  
		Last Modified: Fri, 24 Jul 2020 16:31:24 GMT  
		Size: 42.5 MB (42494210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jre-openj9` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:a9ebe6ee6620a373756a9d24c27be55b17e552ec8a33bf73f253f2d6b90b92a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80728230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f310d684966222014663291417eb2031c08b27d339b4f4fa6487a8c6a03bffcf`
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
# Fri, 24 Jul 2020 15:10:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:15:44 GMT
ENV JAVA_VERSION=jdk-13.0.2+8_openj9-0.18.0
# Fri, 24 Jul 2020 15:16:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='7bf8dc4c3b95e87b154f7bc2f9388a6539413fe76d49b362bba878217ccb7ed7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_ppc64le_linux_openj9_13.0.2_8_openj9-0.18.0.tar.gz';          ;;        s390x)          ESUM='d3051351ead072a19225427b83f71b5efe8ceb1133bbdff6c19ec7a380b70cbc';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_s390x_linux_openj9_13.0.2_8_openj9-0.18.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a0ab38607811e282f64082edc68a2dea3fa6a5113391efb124a6d7d02883110a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_x64_linux_openj9_13.0.2_8_openj9-0.18.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 15:16:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 15:16:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
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
	-	`sha256:6c3fceaa64b515859a04865d8afd801e3f3f196775b901d41018423649f652de`  
		Last Modified: Fri, 24 Jul 2020 15:20:02 GMT  
		Size: 13.0 MB (13033302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfd7c123102267e9ad6cb0ad7ad1fc48c18089c2dcd345e2f0626cb0c80a77c`  
		Last Modified: Fri, 24 Jul 2020 15:23:14 GMT  
		Size: 42.3 MB (42288195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jre-openj9` - windows version 10.0.14393.3866; amd64

```console
$ docker pull adoptopenjdk@sha256:cacfa0a0abb6464c1ba683d589b73d9602061a762b2c46eb28c311fcb2eced41
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5819269433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21517d3d3103c78984310288b4079f86a39d6f06afb615f63bc8b83a9a7ca735`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 17:24:35 GMT
ENV JAVA_VERSION=jdk-13.0.2+8_openj9-0.18.0
# Wed, 12 Aug 2020 17:32:40 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (c27a5f69d41058773e4ccf8bfd5b247b50f57cab0a65a540fcc25984b5eafadc) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c27a5f69d41058773e4ccf8bfd5b247b50f57cab0a65a540fcc25984b5eafadc') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 12 Aug 2020 17:32:41 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:32838d9637dc39d4acee78700b0f93d6c8c9d2db755f12c8009c1b51687d3fbd`  
		Last Modified: Tue, 11 Aug 2020 20:54:28 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e7485d500533b371ac7eaf275b04c493504ae39a32e0e881643aae31d41e2b`  
		Last Modified: Wed, 12 Aug 2020 18:09:55 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684b6d8097b8193e4a56f6c65969aef7c8e12063250ad862eeb8446730f6a4a0`  
		Last Modified: Wed, 12 Aug 2020 18:12:41 GMT  
		Size: 81.1 MB (81118639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887edb6a9a1cc8d556c53dba08c579ead235d2f0915eae5bd60fceaf257084e3`  
		Last Modified: Wed, 12 Aug 2020 18:12:30 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jre-openj9` - windows version 10.0.17763.1397; amd64

```console
$ docker pull adoptopenjdk@sha256:711dd31402328b380558d5d79017071f6b36cfaf23010fa0529d37e93bcd60d9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2416326390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06eda1132fd6baf815278fea4b7eeb4b174aa3079e784ceacbc0cb2aef445991`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 17:28:03 GMT
ENV JAVA_VERSION=jdk-13.0.2+8_openj9-0.18.0
# Wed, 12 Aug 2020 17:34:14 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8_openj9-0.18.0/OpenJDK13U-jre_x64_windows_openj9_13.0.2_8_openj9-0.18.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (c27a5f69d41058773e4ccf8bfd5b247b50f57cab0a65a540fcc25984b5eafadc) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c27a5f69d41058773e4ccf8bfd5b247b50f57cab0a65a540fcc25984b5eafadc') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 12 Aug 2020 17:34:15 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19af971fbf7bf05b9c6c98103587a1ab985dc991618438baee88c0eb2073043b`  
		Last Modified: Wed, 12 Aug 2020 18:11:39 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6018ce57e906ae63edaff21c88ad1c6e96cf12a6dea7dec7d9f6419fa00dd7bd`  
		Last Modified: Wed, 12 Aug 2020 18:13:04 GMT  
		Size: 80.5 MB (80455988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a96192b750877c01519771b7c05c4d8db196cbafaa4423cb9e695337a1e711`  
		Last Modified: Wed, 12 Aug 2020 18:12:52 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
