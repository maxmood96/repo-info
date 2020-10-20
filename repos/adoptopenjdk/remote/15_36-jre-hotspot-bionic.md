## `adoptopenjdk:15_36-jre-hotspot-bionic`

```console
$ docker pull adoptopenjdk@sha256:2a9d7a64fb5856ce56420bfc0163f0c018819506370460234b6f6731a3f70230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `adoptopenjdk:15_36-jre-hotspot-bionic` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:9634b16f4aa67cbc858e8d95b127f5df24ff4944a672d38a2d8721028b50d49f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103438856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f033f2205b2b23a54477050c28bd6458ff48e87b357fd804d943b1853167ffc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:34:27 GMT
ADD file:da80f59399481ffc32f84353830dcf598f31a97785222e75d643bfb8a9aa14e7 in / 
# Fri, 25 Sep 2020 22:34:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:34:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:34:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:34:30 GMT
CMD ["/bin/bash"]
# Fri, 16 Oct 2020 23:19:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Oct 2020 23:20:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Oct 2020 23:21:54 GMT
ENV JAVA_VERSION=jdk-15+36
# Fri, 16 Oct 2020 23:22:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='318f50bae6652d4468ee262ce0fd6569adbc461bea0d1ecce77ce2843efee8d4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_aarch64_linux_hotspot_15_36.tar.gz';          ;;        armhf|armv7l)          ESUM='09c1ba3636e7899d8b43795d7988bcc4b1e1be2919764d94f6d4a1a855ce774f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_arm_linux_hotspot_15_36.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6ea692c7e43bee201a56313bd9f4ddcdea43bed1dfe203c49316ac4d08a4cdd3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_ppc64le_linux_hotspot_15_36.tar.gz';          ;;        s390x)          ESUM='e1e124a29e2bf892d267eb63d00dd136558b4e276bcb6741ea676c995b2fff51';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_s390x_linux_hotspot_15_36.tar.gz';          ;;        amd64|x86_64)          ESUM='230d97a6b16a0735f15013a91f7582a22282ec12bdfaec291ab63274cc075efb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_x64_linux_hotspot_15_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 16 Oct 2020 23:22:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d72e567cc804d0b637182ba23f8b9ffe101e753a39bf52cd4db6b89eb089f13b`  
		Last Modified: Fri, 25 Sep 2020 15:20:50 GMT  
		Size: 28.6 MB (28558050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3630e5ff08d73b6ec0e22736a5c8d2d666e7b568c16f6a4ffadf8c21b9b1ad`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a83d81d1f4f942d37e1f17195d9c519969ed3040fc3e444740b884e44dec33`  
		Last Modified: Fri, 25 Sep 2020 22:36:58 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0c44dfceb587e1c4449c1d73f2490d56882599242350221d746e21daa3c8d0`  
		Last Modified: Fri, 16 Oct 2020 23:38:04 GMT  
		Size: 16.0 MB (16020270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad892fc655d5c81f85266219676c4df605d4189b9562ba7eeaf990dc6c16e43`  
		Last Modified: Fri, 16 Oct 2020 23:41:13 GMT  
		Size: 58.9 MB (58859526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:15_36-jre-hotspot-bionic` - linux; arm variant v7

```console
$ docker pull adoptopenjdk@sha256:275616a5dc9d0a2970d881e02a98c96168331adcde7e326f417032aa6ffff157
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89389681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48ed39417851d9b48e44027fa35826365662abbe10fac4f594aa80750ffa6d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 23:04:32 GMT
ADD file:0ddc5fefae097a5be4c925fdfc09e4a637b74627a8981f0e6fb9890580adc875 in / 
# Fri, 25 Sep 2020 23:04:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:04:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:04:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:04:40 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:23:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 25 Sep 2020 23:23:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 20 Oct 2020 17:01:39 GMT
ENV JAVA_VERSION=jdk-15+36
# Tue, 20 Oct 2020 17:02:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='318f50bae6652d4468ee262ce0fd6569adbc461bea0d1ecce77ce2843efee8d4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_aarch64_linux_hotspot_15_36.tar.gz';          ;;        armhf|armv7l)          ESUM='09c1ba3636e7899d8b43795d7988bcc4b1e1be2919764d94f6d4a1a855ce774f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_arm_linux_hotspot_15_36.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6ea692c7e43bee201a56313bd9f4ddcdea43bed1dfe203c49316ac4d08a4cdd3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_ppc64le_linux_hotspot_15_36.tar.gz';          ;;        s390x)          ESUM='e1e124a29e2bf892d267eb63d00dd136558b4e276bcb6741ea676c995b2fff51';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_s390x_linux_hotspot_15_36.tar.gz';          ;;        amd64|x86_64)          ESUM='230d97a6b16a0735f15013a91f7582a22282ec12bdfaec291ab63274cc075efb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_x64_linux_hotspot_15_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 20 Oct 2020 17:02:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:20e126218ac644f56ef7147c3363108a0814d921e6016af54a1b4c964159f1a9`  
		Last Modified: Fri, 25 Sep 2020 23:06:39 GMT  
		Size: 22.3 MB (22279517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d156c2b31482935ec0363b6e3f1cb6fc56da57e61fc80078914918fe53f8fa5`  
		Last Modified: Fri, 25 Sep 2020 23:06:34 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1a0dbe2162972438aa89d4f90dca5db0e4cee58819ba354ea1c0031101b7a`  
		Last Modified: Fri, 25 Sep 2020 23:06:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b333d1b8f5fe5303d427301eecab31e2fb825ddfe9ed1f96b70bc80a74f9fa44`  
		Last Modified: Fri, 25 Sep 2020 23:27:19 GMT  
		Size: 12.8 MB (12817173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca04f9411fa11c37ece5fc7dc59b3dc49eceb4cc7706827a3f4cdc5177d736`  
		Last Modified: Tue, 20 Oct 2020 17:05:31 GMT  
		Size: 54.3 MB (54291953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:15_36-jre-hotspot-bionic` - linux; arm64 variant v8

```console
$ docker pull adoptopenjdk@sha256:52e7f0417cc7d61fb46bf286007df286ae39269c545686ce40d0bdba981883f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94655475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab9bd29cbd9c7245c39c4d20cf81122ea58e3f4769664f18ae8e12340095a71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:47:32 GMT
ADD file:d2c57bfbb29f6de3b29050a2c50c3806e0c8caa26f6d8dea47f479c923d72e3e in / 
# Fri, 25 Sep 2020 22:47:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:47:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:47:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:47:39 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:06:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 25 Sep 2020 23:06:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 20 Oct 2020 16:40:46 GMT
ENV JAVA_VERSION=jdk-15+36
# Tue, 20 Oct 2020 16:41:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='318f50bae6652d4468ee262ce0fd6569adbc461bea0d1ecce77ce2843efee8d4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_aarch64_linux_hotspot_15_36.tar.gz';          ;;        armhf|armv7l)          ESUM='09c1ba3636e7899d8b43795d7988bcc4b1e1be2919764d94f6d4a1a855ce774f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_arm_linux_hotspot_15_36.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6ea692c7e43bee201a56313bd9f4ddcdea43bed1dfe203c49316ac4d08a4cdd3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_ppc64le_linux_hotspot_15_36.tar.gz';          ;;        s390x)          ESUM='e1e124a29e2bf892d267eb63d00dd136558b4e276bcb6741ea676c995b2fff51';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_s390x_linux_hotspot_15_36.tar.gz';          ;;        amd64|x86_64)          ESUM='230d97a6b16a0735f15013a91f7582a22282ec12bdfaec291ab63274cc075efb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_x64_linux_hotspot_15_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 20 Oct 2020 16:41:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:296c9ad75beec603486f1373addae8e2c509e94c4adda44c1289792c91624acc`  
		Last Modified: Tue, 22 Sep 2020 00:25:11 GMT  
		Size: 23.7 MB (23722853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533d1393025aa8c38e0823a6546a0d4e5dec6b8b670758c25494c35783668d`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11bb34abc87247c6a70c928b7a5ef4cd48093642eb0c4b8121a674d3e278c6`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ba57826dc24dd7e679051972f0a6da7be0dff04d2354108e340a12813e9ff9`  
		Last Modified: Fri, 25 Sep 2020 23:09:59 GMT  
		Size: 13.3 MB (13284869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286e97cf94639c740a0076578ab750ab56dd9d75a45bce46d4826b731c7d738`  
		Last Modified: Tue, 20 Oct 2020 16:48:20 GMT  
		Size: 57.6 MB (57646714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:15_36-jre-hotspot-bionic` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:2af77ba1451d5eab30039cea538b086b979dfeb11390d1dbb1a9e5994fc84bcc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91897653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4924adb7fa0905f887748d7f2e1fd3943adc5253eb6e8cfb9a4a7d0ca7bff69a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:07:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 25 Sep 2020 23:07:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 20 Oct 2020 16:42:16 GMT
ENV JAVA_VERSION=jdk-15+36
# Tue, 20 Oct 2020 16:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='318f50bae6652d4468ee262ce0fd6569adbc461bea0d1ecce77ce2843efee8d4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_aarch64_linux_hotspot_15_36.tar.gz';          ;;        armhf|armv7l)          ESUM='09c1ba3636e7899d8b43795d7988bcc4b1e1be2919764d94f6d4a1a855ce774f';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_arm_linux_hotspot_15_36.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6ea692c7e43bee201a56313bd9f4ddcdea43bed1dfe203c49316ac4d08a4cdd3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_ppc64le_linux_hotspot_15_36.tar.gz';          ;;        s390x)          ESUM='e1e124a29e2bf892d267eb63d00dd136558b4e276bcb6741ea676c995b2fff51';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_s390x_linux_hotspot_15_36.tar.gz';          ;;        amd64|x86_64)          ESUM='230d97a6b16a0735f15013a91f7582a22282ec12bdfaec291ab63274cc075efb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15%2B36/OpenJDK15U-jre_x64_linux_hotspot_15_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 20 Oct 2020 16:42:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eb688908dd55f188cb3c2b3bb83efc30566ace847ab51ba28adbed5d30266b`  
		Last Modified: Fri, 25 Sep 2020 23:12:47 GMT  
		Size: 13.6 MB (13595725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79611366ecdbd8e854009508a25425f8311bc5d7010f71762a8fe4c7d5e576f6`  
		Last Modified: Tue, 20 Oct 2020 16:58:37 GMT  
		Size: 52.9 MB (52928916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
