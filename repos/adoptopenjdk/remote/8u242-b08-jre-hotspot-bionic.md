## `adoptopenjdk:8u242-b08-jre-hotspot-bionic`

```console
$ docker pull adoptopenjdk@sha256:cd1082c55187517aa4cec58e4cb39502817228985df46cf151d5180e523c5ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm64 variant v8
	-	linux; s390x

### `adoptopenjdk:8u242-b08-jre-hotspot-bionic` - linux; arm64 variant v8

```console
$ docker pull adoptopenjdk@sha256:350c0cd4f8d1a31bd4046cb899a119d5c4f9e5471f703027843ba6279a9f68c0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77882880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b9c69aaf3d7fa23f4097ac88a45e3411efe95e0c4da206d5aa4a346f6dd28b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:41:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 21 Feb 2020 22:42:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 04:50:34 GMT
ENV JAVA_VERSION=jdk8u242-b08
# Thu, 27 Feb 2020 04:51:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='178b0b18ed8ca7552ee26848b417f0ef5ceababc56823aaf522e78c19579d751';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_aarch64_linux_hotspot_jdk8u242-b08.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='0b34b855a205d7c00b6625075884b48f6b9fafe3288397116896c39a39220b74';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u242b08.tar.gz';          ;;        s390x)          ESUM='a0e122c7ecd1cb8968cb4000923292db210fc7463f2ba4d764912de2e2489d15';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_s390x_linux_hotspot_8u242b08.tar.gz';          ;;        amd64|x86_64)          ESUM='5edfaefdbb0469d8b24d61c8aef80c076611053b1738029c0232b9a632fe2708';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_x64_linux_hotspot_8u242b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 27 Feb 2020 04:51:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b5eadacd92003b0f840ccaa2c2b09ea51d298126dd647d280a6de60720a3d4`  
		Last Modified: Fri, 21 Feb 2020 22:44:36 GMT  
		Size: 12.7 MB (12732441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47753d70ca6a96019c2cb57b05eaa8e2b6ef93607c79861f7542fb7cd4919f0a`  
		Last Modified: Thu, 27 Feb 2020 04:52:59 GMT  
		Size: 41.4 MB (41393060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u242-b08-jre-hotspot-bionic` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:f0d3e795a94f1f254be9600c8d82334a46a5ceadfdf41cd84cdac22749660ec7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77494378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7146dadc9875be83868e4a537fa04629205e3a4393397a1d517f79a80877a825`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:53:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 21 Feb 2020 22:53:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 22:41:36 GMT
ENV JAVA_VERSION=jdk8u242-b08
# Wed, 26 Feb 2020 22:42:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='178b0b18ed8ca7552ee26848b417f0ef5ceababc56823aaf522e78c19579d751';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_aarch64_linux_hotspot_jdk8u242-b08.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='0b34b855a205d7c00b6625075884b48f6b9fafe3288397116896c39a39220b74';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u242b08.tar.gz';          ;;        s390x)          ESUM='a0e122c7ecd1cb8968cb4000923292db210fc7463f2ba4d764912de2e2489d15';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_s390x_linux_hotspot_8u242b08.tar.gz';          ;;        amd64|x86_64)          ESUM='5edfaefdbb0469d8b24d61c8aef80c076611053b1738029c0232b9a632fe2708';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_x64_linux_hotspot_8u242b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 26 Feb 2020 22:42:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ced1901bd9234160acb28fbd10c7976df2447abc6646ddb64edbaac80b17c7`  
		Last Modified: Fri, 21 Feb 2020 23:01:29 GMT  
		Size: 13.0 MB (13042538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c084e5e48298a3b20e8f38a6643bc6c05d362cb4c018acbbb811eb920372070d`  
		Last Modified: Wed, 26 Feb 2020 22:43:54 GMT  
		Size: 39.0 MB (39048947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
