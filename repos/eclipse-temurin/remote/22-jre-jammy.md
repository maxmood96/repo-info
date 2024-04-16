## `eclipse-temurin:22-jre-jammy`

```console
$ docker pull eclipse-temurin@sha256:dde6121143bc017026d14b0e55df87a47ef1b8b6c404da9d97415a30b751068c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:22-jre-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4bc5f546cf3fb1727ba54add3b9ea8ad3238144698e13d62e94bd8f80be14d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95697492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88e62e240e1a2aac6aab59aaf0553ff5b014e41d741036029dd048f4cddae86`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4748e5024eb0251ddf0f576e4c56d21270b1f2186f62b25fc1d89c888d742ed4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='faceda94ffd16e177cb674471f29789e48378f9f190eac8523713a0cb3324be9';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e1cce04600b388777a1a278dda572a664db14cea034dc131155b3da5e6e885e5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5f02755dd723eca151979d5b1d20885668ba65b8d52a1ce6fda5f36f2f371e`  
		Last Modified: Tue, 16 Apr 2024 04:08:15 GMT  
		Size: 11.8 MB (11794676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74c3a2791be75ee21e82a339fd6c05a385f7af39b3c3ed61154b1e5194c3050`  
		Last Modified: Tue, 16 Apr 2024 04:08:19 GMT  
		Size: 53.5 MB (53462176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b96deb9a6fbedd137d6b957b9fd052e9d22628bdfc27def4a7c3e0176e9e467`  
		Last Modified: Tue, 16 Apr 2024 04:08:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fa0599380ccc2c6826bc40f38fd572d464311adc1e73fcce42daf79c3af087`  
		Last Modified: Tue, 16 Apr 2024 04:08:12 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:04280b85ecad740f8f291851b8260295fc4735fdcf4f72cddce81b5aab470f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92652557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10288990143cfdbb71a8f64fd41c77f4cc2061cd95830f2f6782e73ebff4ed83`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4748e5024eb0251ddf0f576e4c56d21270b1f2186f62b25fc1d89c888d742ed4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='faceda94ffd16e177cb674471f29789e48378f9f190eac8523713a0cb3324be9';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e1cce04600b388777a1a278dda572a664db14cea034dc131155b3da5e6e885e5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71980d0334b80d8fb30049294c1306a6b4a3bb5734998ee63706a8ef1894936a`  
		Last Modified: Tue, 16 Apr 2024 02:59:43 GMT  
		Size: 11.7 MB (11740400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28446be91e4f150ff6ac1151697ca5146b300205ea7571806726bb6171f1ceab`  
		Last Modified: Tue, 16 Apr 2024 02:59:47 GMT  
		Size: 52.5 MB (52510997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984fa202f01548e3df788657649f09e5bbd1bc09ef78ab09fbad114078b99a97`  
		Last Modified: Tue, 16 Apr 2024 02:59:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1958c77dbab0096e6fe2f8baf51ed74a133fe581d2147f2ff22acc2b7ab5db`  
		Last Modified: Tue, 16 Apr 2024 02:59:41 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f9b582e7611807b411268d6d837a6f4d6fe33440524cb19dd69b75c7fb37fde3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101067371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8973028a7ed5ae76c6f97767bd7269958041affcc5f0f9c52e59b156682709`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4748e5024eb0251ddf0f576e4c56d21270b1f2186f62b25fc1d89c888d742ed4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='faceda94ffd16e177cb674471f29789e48378f9f190eac8523713a0cb3324be9';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e1cce04600b388777a1a278dda572a664db14cea034dc131155b3da5e6e885e5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08418e3a8d90552f6252aa06d99a4344552d80cc8cdc1ee7f3ef482a40e449f4`  
		Last Modified: Tue, 16 Apr 2024 02:55:03 GMT  
		Size: 12.4 MB (12370989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31a9af7327e943e830fbc6f782b5a43fe1ab42a5f958208922b5f646aa3fa11`  
		Last Modified: Tue, 16 Apr 2024 02:55:08 GMT  
		Size: 53.1 MB (53108269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c4109e3a11663bd13fdea09fef71875887dae25a378da9336b18ded827c732`  
		Last Modified: Tue, 16 Apr 2024 02:54:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d419f93a96313ba2564a634a2122b349fb517b02596332781e070aa0a32cb2da`  
		Last Modified: Tue, 16 Apr 2024 02:54:57 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
