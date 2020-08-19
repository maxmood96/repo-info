## `adoptopenjdk:13-jdk-hotspot-bionic`

```console
$ docker pull adoptopenjdk@sha256:cb0b5860ad69e135503d5e5057038ef1746ac2908db2e3065c79e792a00ce767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `adoptopenjdk:13-jdk-hotspot-bionic` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:a92e9d461abbd7c94b4a68dd2e40ec111194f7d3c5367dc310f27b5c39c30737
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248551156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c3a84822c4fa3a68b935769dd3a58fe7d9ba9616db14b62c421e5d32aa44a3`
-	Default Command: `["jshell"]`

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
# Wed, 19 Aug 2020 21:59:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0e6081cb51f8a6f3062bef4f4c45dbe1fccfd3f3b4b5d52522a3edb76581e3af';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.2_8.tar.gz';          ;;        armhf|armv7l)          ESUM='9beec080f2b2a7f6883b024272f4e8d5a0b027325e83647be318215781af1d1a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_arm_linux_hotspot_13.0.2_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='fb3362e34aac091a4682394d20dcdc3daea51995d369d62c28424573e0fc04aa';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.2_8.tar.gz';          ;;        s390x)          ESUM='1b9e7cd7fdde10fe3534988ef58c36f132b12f814503a034461c95735057467f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.2_8.tar.gz';          ;;        amd64|x86_64)          ESUM='9ccc063569f19899fd08e41466f8c4cd4e05058abdb5178fa374cb365dcf5998';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_x64_linux_hotspot_13.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 19 Aug 2020 21:59:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Aug 2020 21:59:58 GMT
CMD ["jshell"]
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
	-	`sha256:89098a37699b808bbdb43bfc23b7dbc5945cb6e5a7649cc45d3189d47a2b70fc`  
		Last Modified: Wed, 19 Aug 2020 22:04:22 GMT  
		Size: 208.5 MB (208502505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jdk-hotspot-bionic` - linux; arm variant v7

```console
$ docker pull adoptopenjdk@sha256:856e8eb1abe47bab5594913b26a8b621b7c3ea61ea183cd21f8da21bb72a5105
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227293905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641d34c77bf6371130f4fde794c1bf1c76f7aa6c079a57f1eae321c28d169345`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Aug 2020 21:45:03 GMT
ADD file:8369fef9339cb0f1b2b9660d860a6cbf4a5cd6c5e173fbb8cdf8b9485e56aaf4 in / 
# Wed, 19 Aug 2020 21:45:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:45:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:45:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:45:12 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:12:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 19 Aug 2020 22:14:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:14:39 GMT
ENV JAVA_VERSION=jdk-13.0.2+8
# Wed, 19 Aug 2020 22:15:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0e6081cb51f8a6f3062bef4f4c45dbe1fccfd3f3b4b5d52522a3edb76581e3af';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.2_8.tar.gz';          ;;        armhf|armv7l)          ESUM='9beec080f2b2a7f6883b024272f4e8d5a0b027325e83647be318215781af1d1a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_arm_linux_hotspot_13.0.2_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='fb3362e34aac091a4682394d20dcdc3daea51995d369d62c28424573e0fc04aa';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.2_8.tar.gz';          ;;        s390x)          ESUM='1b9e7cd7fdde10fe3534988ef58c36f132b12f814503a034461c95735057467f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.2_8.tar.gz';          ;;        amd64|x86_64)          ESUM='9ccc063569f19899fd08e41466f8c4cd4e05058abdb5178fa374cb365dcf5998';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_x64_linux_hotspot_13.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 19 Aug 2020 22:15:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Aug 2020 22:15:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:854ab59e811f2c269687884c4899a5de08a5f65b6489dffdb58754086f21e5fc`  
		Last Modified: Mon, 10 Aug 2020 14:29:24 GMT  
		Size: 22.3 MB (22278969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996b7ca18b137080bed3caae4f18c24a2ae9b41a0bd9279d21fe013600e6dbf6`  
		Last Modified: Wed, 19 Aug 2020 21:47:13 GMT  
		Size: 35.5 KB (35458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a08dcf8afcac65e6356d202299b593954a299f9ebdb2db237496025225c8f2`  
		Last Modified: Wed, 19 Aug 2020 21:47:13 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34a2e7cb38ebbe96765deedfead50764f5a482a67ca440de7e9e660db464be7`  
		Last Modified: Wed, 19 Aug 2020 21:47:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362efddcbf0ecc420f5a765f69f36c9ceea340dccb55eda598db6a2ad79650fa`  
		Last Modified: Wed, 19 Aug 2020 22:18:22 GMT  
		Size: 12.3 MB (12254025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246944f6c588836f46d0ac048b53608baad3a374bd5e65da496a296509067e6e`  
		Last Modified: Wed, 19 Aug 2020 22:18:50 GMT  
		Size: 192.7 MB (192724412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jdk-hotspot-bionic` - linux; arm64 variant v8

```console
$ docker pull adoptopenjdk@sha256:83a68c0a18e2c17561020c7a58adbb29890e508d80b1c4c8277f1b547a7b0423
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243453281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4672a28aaa01e6502f55971b52e97e120aeee9cbf661959519a77ffd3fa2b5`
-	Default Command: `["jshell"]`

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
# Fri, 24 Jul 2020 18:14:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0e6081cb51f8a6f3062bef4f4c45dbe1fccfd3f3b4b5d52522a3edb76581e3af';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.2_8.tar.gz';          ;;        armhf|armv7l)          ESUM='9beec080f2b2a7f6883b024272f4e8d5a0b027325e83647be318215781af1d1a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_arm_linux_hotspot_13.0.2_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='fb3362e34aac091a4682394d20dcdc3daea51995d369d62c28424573e0fc04aa';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.2_8.tar.gz';          ;;        s390x)          ESUM='1b9e7cd7fdde10fe3534988ef58c36f132b12f814503a034461c95735057467f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.2_8.tar.gz';          ;;        amd64|x86_64)          ESUM='9ccc063569f19899fd08e41466f8c4cd4e05058abdb5178fa374cb365dcf5998';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_x64_linux_hotspot_13.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 18:14:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 18:14:12 GMT
CMD ["jshell"]
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
	-	`sha256:c436be02188ae4fa35acd34496045cbecc57bd04a0a41e586310afb707c4bc15`  
		Last Modified: Fri, 24 Jul 2020 18:17:37 GMT  
		Size: 207.0 MB (206972453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jdk-hotspot-bionic` - linux; ppc64le

```console
$ docker pull adoptopenjdk@sha256:df0a935c767e322ff3d43d911ca945f5f3bcb00013462d33eec01d1ebc11fe2b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235510558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a303e91f914b49eee6f4378aa653bc99a8e7fa4473ad3d22df79cedae98105de`
-	Default Command: `["jshell"]`

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
# Fri, 24 Jul 2020 15:56:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0e6081cb51f8a6f3062bef4f4c45dbe1fccfd3f3b4b5d52522a3edb76581e3af';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.2_8.tar.gz';          ;;        armhf|armv7l)          ESUM='9beec080f2b2a7f6883b024272f4e8d5a0b027325e83647be318215781af1d1a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_arm_linux_hotspot_13.0.2_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='fb3362e34aac091a4682394d20dcdc3daea51995d369d62c28424573e0fc04aa';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.2_8.tar.gz';          ;;        s390x)          ESUM='1b9e7cd7fdde10fe3534988ef58c36f132b12f814503a034461c95735057467f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.2_8.tar.gz';          ;;        amd64|x86_64)          ESUM='9ccc063569f19899fd08e41466f8c4cd4e05058abdb5178fa374cb365dcf5998';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_x64_linux_hotspot_13.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Jul 2020 15:57:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 15:57:39 GMT
CMD ["jshell"]
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
	-	`sha256:c0be2f37e2ae7b29a57e47b357153aee07c1865cad254a491bc2b78d655b7fb9`  
		Last Modified: Fri, 24 Jul 2020 16:23:39 GMT  
		Size: 191.1 MB (191112669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:13-jdk-hotspot-bionic` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:b2641f6fca76e6478cd55213a8f82868e82c716a557801480cfc7aed6bc86ea3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224010598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11da763c2b0ef60504f827776ab0744ac5bcc073379148bb556be413e13fc204`
-	Default Command: `["jshell"]`

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
# Wed, 19 Aug 2020 21:58:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0e6081cb51f8a6f3062bef4f4c45dbe1fccfd3f3b4b5d52522a3edb76581e3af';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_aarch64_linux_hotspot_13.0.2_8.tar.gz';          ;;        armhf|armv7l)          ESUM='9beec080f2b2a7f6883b024272f4e8d5a0b027325e83647be318215781af1d1a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_arm_linux_hotspot_13.0.2_8.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='fb3362e34aac091a4682394d20dcdc3daea51995d369d62c28424573e0fc04aa';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_ppc64le_linux_hotspot_13.0.2_8.tar.gz';          ;;        s390x)          ESUM='1b9e7cd7fdde10fe3534988ef58c36f132b12f814503a034461c95735057467f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_s390x_linux_hotspot_13.0.2_8.tar.gz';          ;;        amd64|x86_64)          ESUM='9ccc063569f19899fd08e41466f8c4cd4e05058abdb5178fa374cb365dcf5998';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk13-binaries/releases/download/jdk-13.0.2%2B8/OpenJDK13U-jdk_x64_linux_hotspot_13.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 19 Aug 2020 21:58:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Aug 2020 21:58:31 GMT
CMD ["jshell"]
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
	-	`sha256:f7997be8d05ffff17168ce8825bcadd5379f306f106aa9709e9b0e0364e88be5`  
		Last Modified: Wed, 19 Aug 2020 22:04:12 GMT  
		Size: 185.6 MB (185569264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
