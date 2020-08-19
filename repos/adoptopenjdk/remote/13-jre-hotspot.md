## `adoptopenjdk:13-jre-hotspot`

```console
$ docker pull adoptopenjdk@sha256:00376365a8c70e0256c3f97677e508ccc794ac782c7b399f9a16133e9ae83ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.14393.3866; amd64
	-	windows version 10.0.17763.1397; amd64

### `adoptopenjdk:13-jre-hotspot` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:bbf932cf9ba5939526f574c06515c41a0dc8b9715dc7bdaebb377ead9151c2bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87046241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5a185d02f7d39a3dd18f318f18a37b19f59e0e6a612b6219b2a24e338140d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:13:50 GMT
ADD file:5c125b7f411566e9daa738d8cb851098f36197810f06488c2609074296f294b2 in / 
# Wed, 19 Aug 2020 21:13:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:13:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:13:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:13:55 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 21:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 19 Aug 2020 21:59:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:59:46 GMT
ENV JAVA_VERSION=jdk-13.0.2+8
# Wed, 19 Aug 2020 22:00:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6c4b69d1609f4c65c576c80d6aa101de80048f8ce5566f890e8fff5349228bae';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.2_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='43d6fb71bdf7b6ad9295087c46dfc9b00bf26db1b5cdcff0c418cbe43b49904a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.2_8.tar.gz';          ;;        s390x)          ESUM='ac07703f9b9aed0676ae751f2b5b2346285566944ba89d0d8833790f83b00163';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_s390x_linux_hotspot_13.0.2_8.tar.gz';          ;;        amd64|x86_64)          ESUM='897f16fe8e056395209e35d2384013bd1ff250e717465769079e3f4793628c34';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_x64_linux_hotspot_13.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 19 Aug 2020 22:00:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:f08d8e2a3ba11bea23cf5c17e8e1c620057412ed05c32d1114640e18d6dd0a43`  
		Last Modified: Sat, 08 Aug 2020 12:21:16 GMT  
		Size: 26.7 MB (26700095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9cb2483bd9c5329a44d9c2fe72535625bbd4308bca95785dd58e72c06365`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e5ff4c0b1526abf77c236655f21c8f67a23313291c8b970fe6b469549d8153`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860925334f940c3145808527480b4f0cba7f01279087fdb27679e4354fba967`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de561dc92760b4e14af6b1ae4b9272bfe502b666e52a04293e7ac88d3d36d5e5`  
		Last Modified: Wed, 19 Aug 2020 22:04:06 GMT  
		Size: 13.3 MB (13312181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dd4883e9705bc4c11d72f99b9b4c732e0cac763dd3c7e4743cd55578774ea2`  
		Last Modified: Wed, 19 Aug 2020 22:04:36 GMT  
		Size: 47.0 MB (46997590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jre-hotspot` - linux; arm64 variant v8

```console
$ docker pull adoptopenjdk@sha256:01ab7bcf71bfa86a22d79cffc398b38c8cf143b3781dde5b842c162882fe9950
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0294df8a5e8ec4db01731cbaa223c782d8151ce2cb3e205b997b1d913ec3515`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:21:15 GMT
ADD file:146b4b3953060bbe623c06f374b3b3798872e4e1ddfef76071c7c4b69a834622 in / 
# Fri, 24 Jul 2020 16:21:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:21:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:23:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:23:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:11:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jul 2020 18:13:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:13:51 GMT
ENV JAVA_VERSION=jdk-13.0.2+8
# Fri, 24 Jul 2020 18:14:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6c4b69d1609f4c65c576c80d6aa101de80048f8ce5566f890e8fff5349228bae';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.2_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='43d6fb71bdf7b6ad9295087c46dfc9b00bf26db1b5cdcff0c418cbe43b49904a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.2_8.tar.gz';          ;;        s390x)          ESUM='ac07703f9b9aed0676ae751f2b5b2346285566944ba89d0d8833790f83b00163';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_s390x_linux_hotspot_13.0.2_8.tar.gz';          ;;        amd64|x86_64)          ESUM='897f16fe8e056395209e35d2384013bd1ff250e717465769079e3f4793628c34';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_x64_linux_hotspot_13.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 18:14:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:a114936b480795ec46632c29c96e126744c314983ee0d83354804dc39d1afb46`  
		Last Modified: Mon, 13 Jul 2020 15:47:08 GMT  
		Size: 23.7 MB (23721122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ecf0d2a869e5d188121e6b38473e481b66599a26d8df24d22c9170f50bfa9`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 35.2 KB (35205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb48eb870f62ec1a7a4a2d753bf2b92dff62a6dbedaeff6db6e41cb33196bc`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f912b9bb20d998fd0f1a2526d5539f35d34a476da71c783d0041b25b78c0af5`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5f4ec4bbde9f5a369741d9fa300ed092ac1fccbc099d1f15d6abd073d6dc7a`  
		Last Modified: Fri, 24 Jul 2020 18:17:09 GMT  
		Size: 12.7 MB (12723464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6202d9abdf2c4b378fd08a35844460951a95670274907d3ccd9c9b05a58462de`  
		Last Modified: Fri, 24 Jul 2020 18:18:06 GMT  
		Size: 45.5 MB (45461350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jre-hotspot` - linux; ppc64le

```console
$ docker pull adoptopenjdk@sha256:4f5d90c0fc016c3870833798128dafc3e811ae666d9e630e58f3ba7831134283
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86511394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a5850e6ed4e4aea18f9f0cbdd63d71aef5722e975b0cf679fc3b18b0265979`
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
# Fri, 24 Jul 2020 15:55:59 GMT
ENV JAVA_VERSION=jdk-13.0.2+8
# Fri, 24 Jul 2020 15:59:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6c4b69d1609f4c65c576c80d6aa101de80048f8ce5566f890e8fff5349228bae';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.2_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='43d6fb71bdf7b6ad9295087c46dfc9b00bf26db1b5cdcff0c418cbe43b49904a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.2_8.tar.gz';          ;;        s390x)          ESUM='ac07703f9b9aed0676ae751f2b5b2346285566944ba89d0d8833790f83b00163';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_s390x_linux_hotspot_13.0.2_8.tar.gz';          ;;        amd64|x86_64)          ESUM='897f16fe8e056395209e35d2384013bd1ff250e717465769079e3f4793628c34';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_x64_linux_hotspot_13.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 16:00:03 GMT
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
	-	`sha256:6574bb84c5b961758d36d667ddfc046d079469e6fcb3d49ecf4e505a4a3444a7`  
		Last Modified: Fri, 24 Jul 2020 16:23:10 GMT  
		Size: 14.0 MB (13956698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debb911b7e1e56690a68c421ed7a427a59e09c0524aaf4d2a8706fc311400670`  
		Last Modified: Fri, 24 Jul 2020 16:24:17 GMT  
		Size: 42.1 MB (42113505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jre-hotspot` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:267135fc82119b5af9c37c6b103b03a238f17a7730cb983aee7cf1182b257d0e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80366398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7590c6e3fbeb7327e27828e349d02fc081a0f47f049f66a82da491c3a98696c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:10:03 GMT
ADD file:1343b5ae7d875bd32e4eac552ae10c9631788fd97b99bcdeb9f6a9b85c230ba2 in / 
# Wed, 19 Aug 2020 21:10:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:10:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:10:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:10:06 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 21:55:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 19 Aug 2020 21:58:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:58:07 GMT
ENV JAVA_VERSION=jdk-13.0.2+8
# Wed, 19 Aug 2020 21:58:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6c4b69d1609f4c65c576c80d6aa101de80048f8ce5566f890e8fff5349228bae';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_aarch64_linux_hotspot_13.0.2_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='43d6fb71bdf7b6ad9295087c46dfc9b00bf26db1b5cdcff0c418cbe43b49904a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_ppc64le_linux_hotspot_13.0.2_8.tar.gz';          ;;        s390x)          ESUM='ac07703f9b9aed0676ae751f2b5b2346285566944ba89d0d8833790f83b00163';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_s390x_linux_hotspot_13.0.2_8.tar.gz';          ;;        amd64|x86_64)          ESUM='897f16fe8e056395209e35d2384013bd1ff250e717465769079e3f4793628c34';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_x64_linux_hotspot_13.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 19 Aug 2020 21:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:25294e13856fd30261115dbfc6dd49e2d854414d32c9ead824b8183a83620e5c`  
		Last Modified: Mon, 10 Aug 2020 15:49:57 GMT  
		Size: 25.4 MB (25371147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4b14541a6306ab7ffae9ed980e3ebac039f590869efecf63c6d745e1cde3c`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4164a02312fb3bccad51789030500218898a262ff17a962d62bb9849c9103d59`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68677136804619b55f0437044d91d7bfe75e0b8013ca953c0d4db40c4d91d6b`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd19ff7cc6600f42206c343a6358578e36a5a3bdbe9b55f996645c07965eda3`  
		Last Modified: Wed, 19 Aug 2020 22:04:01 GMT  
		Size: 13.0 MB (13032981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c52329f7ba8083fbcc31a7aaf4a475b4ebbb17be7c11ee74522c77233dd766`  
		Last Modified: Wed, 19 Aug 2020 22:04:27 GMT  
		Size: 41.9 MB (41925064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jre-hotspot` - windows version 10.0.14393.3866; amd64

```console
$ docker pull adoptopenjdk@sha256:08cd9eb53471a75bc73437e89077ab3a705d61af39699fad46145ee9f5b79126
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5826078385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dd4d9089467769e7ec57e0342a4af23dd48f9f0436da8c70241d4f7de2fba0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 16:45:13 GMT
ENV JAVA_VERSION=jdk-13.0.2+8
# Wed, 12 Aug 2020 16:53:42 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_x64_windows_hotspot_13.0.2_8.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_x64_windows_hotspot_13.0.2_8.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (6fe327787fc81f84ca16296a9edbace713d5b04657234cb9431ab45bda7df2dc) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6fe327787fc81f84ca16296a9edbace713d5b04657234cb9431ab45bda7df2dc') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
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
	-	`sha256:7eef7e7f5dc4713d82fd3b8a61fbd5cb580ebdea982bc1c4f29da20af48df89e`  
		Last Modified: Wed, 12 Aug 2020 17:52:24 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd22bc9157c600d1709c46400be7abc1a43ee6e7f13398416a319ccfd09b5ab8`  
		Last Modified: Wed, 12 Aug 2020 18:01:10 GMT  
		Size: 87.9 MB (87928673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jre-hotspot` - windows version 10.0.17763.1397; amd64

```console
$ docker pull adoptopenjdk@sha256:e17719db993a8f839067a3ea17efe426e8b391a5c614aa76a75b02e57a3e0fb6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2423131249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b804cd636e91143bd18cacd76b00180049799a6a333f4bbe972b4b8b199ca94d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 16:48:39 GMT
ENV JAVA_VERSION=jdk-13.0.2+8
# Wed, 12 Aug 2020 16:55:10 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_x64_windows_hotspot_13.0.2_8.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jre_x64_windows_hotspot_13.0.2_8.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (6fe327787fc81f84ca16296a9edbace713d5b04657234cb9431ab45bda7df2dc) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6fe327787fc81f84ca16296a9edbace713d5b04657234cb9431ab45bda7df2dc') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
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
	-	`sha256:77668552cdd1ff24f36f7a0341ac5eee74353184b2235df085fc4e1232caa59c`  
		Last Modified: Wed, 12 Aug 2020 18:00:05 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea0527b2a80bfa8261d10128ea195f80c8c3dd250e3db595d5250632b0ea084`  
		Last Modified: Wed, 12 Aug 2020 18:01:36 GMT  
		Size: 87.3 MB (87261934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
