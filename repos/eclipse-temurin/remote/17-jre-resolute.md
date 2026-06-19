## `eclipse-temurin:17-jre-resolute`

```console
$ docker pull eclipse-temurin@sha256:b958f60e3a7b1813ae00d53879d8e9a36136e086a13d8f0668620a8e69274546
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:17-jre-resolute` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:759adfa3787ccf9e00d7c2fcbe162399ed79d272ab1fd8ddab384c2519d7a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109252870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b129737e59d3bb26f15c70beb0052af475930bb847fdfd4966ed287f88513b2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9106.tar --tag 26.04
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9106.tar
# Fri, 19 Jun 2026 01:11:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:11:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:11:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:11:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:02 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 19 Jun 2026 01:11:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:81e2f2053c8fa702b6863110b55c09e67f6adeb78b4672745958c4d8b3d056c5`  
		Last Modified: Wed, 10 Jun 2026 08:00:11 GMT  
		Size: 41.6 MB (41562239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f56e4c7f2f2a1415c59803638274d488a73b61a8e1f9cbd9cb280327e8d21e`  
		Last Modified: Wed, 10 Jun 2026 08:00:15 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1138b4ddaebefb926b2bb70b8296bd150a43391ea36a04f36d55bdc3a68e569`  
		Last Modified: Fri, 19 Jun 2026 01:11:21 GMT  
		Size: 20.1 MB (20122690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd847706531f17812ea38d3e6717105036f2184210b5e942a5ca2760298dac31`  
		Last Modified: Fri, 19 Jun 2026 01:11:22 GMT  
		Size: 47.6 MB (47565111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf746862a74256590bd014a64101d7baddc9869a06970f8e2b84de3abc84c78`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98099d09b5ac43d29e938945236d40d88a10a18f07b7885b3ba09e38a51ed1e`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:aaf178bd66178bdced1b5730d636a7381541765508f2d564d32a84ffcb740683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc359f253ce9287807b9628da72a89ecf4e94ecd8a3d8206134291883d23e156`

```dockerfile
```

-	Layers:
	-	`sha256:124e3e108911ccd53674a18ae25ac9686a504a4bf1cee7d0ba85ec9d582fa113`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 5.1 MB (5097764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f0e48087c099fc51afa63d266963e2d537f32234be1460e0f037770e0ef2a1c`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 24.8 KB (24772 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-resolute` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:2144a1bcf5b195359f704a4967bd74425f7bacc0c3af6c4298166787f75e9568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102967774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef2045dab4d85d5ec1597dd231ab336326daa81c92e54d266aa836a56b69f69`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 10 Jun 2026 03:33:33 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9272.tar --tag 26.04
# Wed, 10 Jun 2026 03:33:34 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:33:34 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:33:34 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:33:34 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:33:34.480095+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:34 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:33:34.480095+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:34 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9272.tar
# Fri, 19 Jun 2026 01:11:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:11:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:11:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:11:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:01 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 19 Jun 2026 01:11:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3afcfc6322f1b6ea07a2fb9b031f643f9af38c2bf4625ad357d711767538dbf8`  
		Last Modified: Wed, 10 Jun 2026 08:00:56 GMT  
		Size: 38.7 MB (38703143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c279c504cbdcf584210eab38c9b6180e5f540e26a0d226b9601877512d72bbf5`  
		Last Modified: Wed, 10 Jun 2026 08:00:59 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50f66bce57ed81d8a2923be8a357f9dc0f74717d2a4adcfd36b1655f5258ce`  
		Last Modified: Fri, 19 Jun 2026 01:11:21 GMT  
		Size: 19.1 MB (19129812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97573213e8f759296ed18915c5747b68304c49eb5f1c5f95a2ca296b9f83955`  
		Last Modified: Fri, 19 Jun 2026 01:11:22 GMT  
		Size: 45.1 MB (45131989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179fb8f708a30574eed08f939c085a93e94f457478f55aa5266c92f60747ef33`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d41a00fb5e1f5cf376b552f45147670364afae78634bfe88c6df40551083d22`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e20f966342aaf6bccf5c4b7115069d1ad15f4be0218767ac0e45ca33bb52732e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2013ab8d62f3ccb8c2e89ebf0ecad2fb1fbafbec9d62e51618cf903e644c9d5f`

```dockerfile
```

-	Layers:
	-	`sha256:5305069e7119a6723692b17c3111e996259ed3ed57ec4745802166ffd8b970cc`  
		Last Modified: Fri, 19 Jun 2026 01:11:21 GMT  
		Size: 5.1 MB (5099293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6403953fae2c3931a05028f4c7bffb56ffaf6133a959fe2adecf63055f5938fc`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 24.9 KB (24878 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-resolute` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:aeb4f582b2488360a463ef4a340023dace8fdfb7edb10a1ce89865d867d005d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107689419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074b361e637234feee3d28bc42e716fe41397d9ddaa7649e6362183e38ce2927`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9196.tar --tag 26.04
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9196.tar
# Fri, 19 Jun 2026 01:11:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:11:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:11:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:11:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:31 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 19 Jun 2026 01:11:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c572f291b2a0cc05a1d523f3dda4d3f1992c3e480debf2e1bc9278aeab115625`  
		Last Modified: Wed, 10 Jun 2026 08:00:25 GMT  
		Size: 40.7 MB (40709186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dda33820b52cf93fd5ff3808c770af252cf0565784b42e52e3dd74e2ebf5b2`  
		Last Modified: Wed, 10 Jun 2026 08:00:29 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d966563b059c99513caeaa34ad0b9e0965e49e6f018e93359755804bc1dc64`  
		Last Modified: Fri, 19 Jun 2026 01:11:50 GMT  
		Size: 19.9 MB (19927374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c254ab3c23a00c5ad7ea97bf468e436210ac59ee54621fa6cf0fa1a18213f83d`  
		Last Modified: Fri, 19 Jun 2026 01:11:51 GMT  
		Size: 47.1 MB (47050033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3eabe26550dd242b48bfaae309dd4103f806c77bb9b6e8f72c9882da661234`  
		Last Modified: Fri, 19 Jun 2026 01:11:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d26e5a5335f2df57b81788e001e068f68f784a618b84f25915a4bb32f3dfd`  
		Last Modified: Fri, 19 Jun 2026 01:11:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5fc62882b27d07350e7879fc93c41c4a7a328270e4bbeab00d363b5d16bc7609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4f9f519525e8f786106530d95b1dfa22b788f6ab3b432a1402d34a84083239`

```dockerfile
```

-	Layers:
	-	`sha256:2163d906e8c9a9c022fe1b5ba9ebc3b9cc23167fa26726e42b32c34736dba5ac`  
		Last Modified: Fri, 19 Jun 2026 01:11:50 GMT  
		Size: 5.1 MB (5097433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376a204f51bbee8260ed4417883f8521aa0a16eca948b854215add3fd86a57f3`  
		Last Modified: Fri, 19 Jun 2026 01:11:49 GMT  
		Size: 24.9 KB (24905 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-resolute` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e2edddb9e640b40a590b3bc2338e8d02e890351798bae849c92ce470d15f5942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116517526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31cf739affcf47381d4be99f7ed1f8008cadde8738083c58c17f1a88b2b47f3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 10 Jun 2026 03:34:08 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9159.tar --tag 26.04
# Wed, 10 Jun 2026 03:34:09 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:34:09 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:34:09 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:34:09 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:34:09.982131+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:34:10 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:34:09.982131+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:34:10 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9159.tar
# Fri, 19 Jun 2026 01:10:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:10:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:10:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:10:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:10:33 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 19 Jun 2026 01:12:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:12:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:12:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:12:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d0ad782fe3317d182d855cc9406d3d23462337de4ab974a6d00a845910465af8`  
		Last Modified: Wed, 10 Jun 2026 08:00:40 GMT  
		Size: 46.6 MB (46593798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8e59391e45c204081dd6a3d3c4682dd0978a8db5fd9745f69792cd691e0624`  
		Last Modified: Wed, 10 Jun 2026 08:00:44 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab861743f7b3380829889eee9c5e2dd1d9ea9c0bc715c1f9173babad0ba3a68c`  
		Last Modified: Fri, 19 Jun 2026 01:11:19 GMT  
		Size: 22.4 MB (22433429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c191b928e356797b974127d62941f7429f7a47fa2790e1fb8ec3dd5bd567b6c7`  
		Last Modified: Fri, 19 Jun 2026 01:13:33 GMT  
		Size: 47.5 MB (47487466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b71a5c98ba9cf3bfde2517639e8bc3af43a5068f99a3c16ecf5e9ef03ee05`  
		Last Modified: Fri, 19 Jun 2026 01:13:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d320c13b771ded654e33527ad25f710bad1d934966e234bc3bd0280f9216c34`  
		Last Modified: Fri, 19 Jun 2026 01:13:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:506bf24ab583d0d3c1fb79879c6270cf91f1ab9f6c1b2526a2339119e27bba90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffecbd58dd2138e93d06d65a9c2f32f9f61c547f91a993bb6f8bf46115c34bab`

```dockerfile
```

-	Layers:
	-	`sha256:5585e84bdcb97b5e5533c6ef55b08de137281201d14d690b640eb52fcb165b2f`  
		Last Modified: Fri, 19 Jun 2026 01:13:31 GMT  
		Size: 5.1 MB (5101024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:668c67e6013944a30539971bcee54b4c8c348c32bd38c6d1756f321b128e29f6`  
		Last Modified: Fri, 19 Jun 2026 01:13:31 GMT  
		Size: 24.8 KB (24820 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-resolute` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:8b8c215ff28aa881875e23799d41c8e42d05200203bb45012ab4f55715865819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106178786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a959d02f25678b18d2ee141e262dd4406284725b233bd00b0b060affa77fe7f6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 10 Jun 2026 07:47:21 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9183.tar --tag 26.04
# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T07:47:22.176605+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T07:47:22.176605+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 07:47:22 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9183.tar
# Fri, 19 Jun 2026 01:09:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:09:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:09:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:09:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:09:29 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 19 Jun 2026 01:10:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='08c8c193fc2e8e6eb4450d3ddcefa78889eef338b2bbc0b30e5a6d586fc6d646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:10:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:10:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:10:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:fff40c9207bf9ed5e68aadd6d83ec56f6b350421754c4d815f674a213be1edd8`  
		Last Modified: Wed, 10 Jun 2026 08:01:20 GMT  
		Size: 41.0 MB (40957425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bc0b48de22f57cae536e3f925926b013a50a63629708ed6e139cac57b87e60`  
		Last Modified: Wed, 10 Jun 2026 08:01:23 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658c1bf93e39c7b8f646b9fbc9f1d158c03f80e2bafb89e70a61c5b4703ed5a9`  
		Last Modified: Fri, 19 Jun 2026 01:09:53 GMT  
		Size: 20.7 MB (20676542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f4694504e7f4b6a61ef9af85cf464d5985f4bfdbc08ce5bc7abf44015b9d7b`  
		Last Modified: Fri, 19 Jun 2026 01:10:22 GMT  
		Size: 44.5 MB (44541991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ba1f5990781c4c1b286b0aab898dccb84804dc6bb0e60baf00b877f9b8137d`  
		Last Modified: Fri, 19 Jun 2026 01:10:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a857008d4a1ebbacde79db9a21aba4a1254225584d5934ff57b3d8e5a8875a7`  
		Last Modified: Fri, 19 Jun 2026 01:10:22 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e1b5deafc708f0580546b6c882fca686b36a7a2afd804db2f486314cb68308fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea395a05fbe39334227376ce3e249d8ace1bcdd1856afff5d8ba5cfc1141fd8c`

```dockerfile
```

-	Layers:
	-	`sha256:45953c70e578a7fc2b2a855482e20b354a24bea394500ee71c25be94717d74b9`  
		Last Modified: Fri, 19 Jun 2026 01:10:22 GMT  
		Size: 5.1 MB (5099174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7bd0298f52ddcd97a7cec3c0e3dfb265c0e53ab78d9de11eb3b84596e29e213`  
		Last Modified: Fri, 19 Jun 2026 01:10:22 GMT  
		Size: 24.8 KB (24772 bytes)  
		MIME: application/vnd.in-toto+json
