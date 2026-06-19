## `eclipse-temurin:17-resolute`

```console
$ docker pull eclipse-temurin@sha256:41c1c1d2fb1f84d77436116a9c97299c9055def6c685f0826511bfb30e00ecd1
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

### `eclipse-temurin:17-resolute` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:afd132c8643ee1f64f5ce9252ac914ec6ac5bf04be83dc1d6fc313244c6869b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211516108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cca960bab5725dbc1b9a486f303a51026afd81b8926446a0d256a476d8033d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Fri, 19 Jun 2026 01:10:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:10:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:10:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:10:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:10:55 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 19 Jun 2026 01:11:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Jun 2026 01:11:02 GMT
CMD ["jshell"]
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
	-	`sha256:83759bf057249226499f0acdd8b1c78ff24427d05c3110d93876ed1103004dfe`  
		Last Modified: Fri, 19 Jun 2026 01:11:21 GMT  
		Size: 24.0 MB (24038532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caaed84de85b23a93e1a09dcd67163c88a3f56bb56584ee1882cd855b65c14c`  
		Last Modified: Fri, 19 Jun 2026 01:11:24 GMT  
		Size: 145.9 MB (145912509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe16ec1ccf716ef4daa5cbbc11cf7e56b21761f932235a5580f818bd9a6c874`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66812886718425a70cc833106c2e62986c69cda7aaf5e097e9ccb29e35fcdd78`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4fee97f5c0f0f5b0d95055214a7666aaf78c7484c1d4e5a3142560f0f6eeb7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c29aacadc077f6558c510ded6fe78354674cffbf9c2f0b13864703de064f382`

```dockerfile
```

-	Layers:
	-	`sha256:8664a455bc79083242358f80461d783219e5e77918e35cd7c6cdfc11191f9ba4`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 5.4 MB (5364166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98fcdf4fa6b831c92d9b61802be7297df1d905958712db36458e155ec724ba05`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 26.5 KB (26477 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-resolute` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:6779f8ea10d2fc3699b134b64c92b775acda9dfc62d937daa79f5b12f4e34840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203220106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544ba3227718f81f357c7e25a3e5db72631529538cef3e8eb1305a0c0b9fb507`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Fri, 19 Jun 2026 01:11:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:11:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:11:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:11:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:23 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 19 Jun 2026 01:11:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Jun 2026 01:11:37 GMT
CMD ["jshell"]
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
	-	`sha256:d56398a86f6e992d6619e2522b5d924917ac7316467fe10a038f7640b979f100`  
		Last Modified: Fri, 19 Jun 2026 01:11:57 GMT  
		Size: 21.3 MB (21326960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b62ed715501fc22195f17c823f52d7bf23230a6f3f6053b9b6e47fc89156260`  
		Last Modified: Fri, 19 Jun 2026 01:11:59 GMT  
		Size: 143.2 MB (143187174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdca48577c442ef6f341d7d6f5bc28c2888240833453d623fc102118df2c06a`  
		Last Modified: Fri, 19 Jun 2026 01:11:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a323dd282753b4436614567ab67da13dda06eb0c4a24ab8a7b535ef367ba95d7`  
		Last Modified: Fri, 19 Jun 2026 01:11:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:48d7cf30e5bc87ddfdb4b23d60a73e8f51c584cf1e055bb7a8e8f9da1089a285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5315072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed28e54485cf209c71e40e96b75deb134ad43d692ac91836093708d8c339bd21`

```dockerfile
```

-	Layers:
	-	`sha256:82948d15096aa085f881448fe802d0c66f803660478fba15f7471db1e60230fe`  
		Last Modified: Fri, 19 Jun 2026 01:11:56 GMT  
		Size: 5.3 MB (5288473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b64ddf5826dad3f42cfa694f8b18444217f579547a80007144540b975514ce`  
		Last Modified: Fri, 19 Jun 2026 01:11:56 GMT  
		Size: 26.6 KB (26599 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-resolute` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:11f439083d3f96d441d17bfbd0986d736a0587609f6e503e71c690d14aa3240a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209378554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2f709bd7997adbc3348e139166fde30d13290bddc182c765f9ae0579c706c3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Fri, 19 Jun 2026 01:10:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:10:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:10:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:10:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:10:28 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 19 Jun 2026 01:10:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:10:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:10:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:10:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:36 GMT
CMD ["jshell"]
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
	-	`sha256:d2b8ae2cf50069894141d58eb97bea0656f07b7b71cb8be615bf0666c2df05c3`  
		Last Modified: Fri, 19 Jun 2026 01:10:57 GMT  
		Size: 23.9 MB (23924253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2f6aa59d06bbf8666fb8d44c1033842962caded8ac1fb8e4cfc98f14b80b0b`  
		Last Modified: Fri, 19 Jun 2026 01:11:00 GMT  
		Size: 144.7 MB (144742286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6130b1df23e1d1d77b359a719b02463aa344153ff95e581c5264600cae9721ba`  
		Last Modified: Fri, 19 Jun 2026 01:10:55 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa19da4759759c13d56647935a39b65f50993298e996e8b41929403cf70a9d97`  
		Last Modified: Fri, 19 Jun 2026 01:10:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:489cf6e512bdc78e14351a039311d8f8e9802f6258dac2c254e47cc41c1600d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5578217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cd7ef6b2149be22854cb7bf15d79e4def91ec6ee177061543268aef9039ac4`

```dockerfile
```

-	Layers:
	-	`sha256:3228486a8bca13a303c879c6ba87e32aec0f363725b42d17943e0b963f19f583`  
		Last Modified: Fri, 19 Jun 2026 01:10:56 GMT  
		Size: 5.6 MB (5551582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:784ec1a41a452935d321b27ce62ed84ef5395a88b46bbe320237684b775e0750`  
		Last Modified: Fri, 19 Jun 2026 01:10:55 GMT  
		Size: 26.6 KB (26635 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-resolute` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:db4b930b47b6195fff305126ff4c2b26e9d3f896eb47bf0c610154361881d5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217489064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d6790b5d39a51274a2d1851723cafcd7669304abd26fb4c3c09d6a62206a80`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Fri, 19 Jun 2026 01:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:13:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:13:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:13:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:13:05 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 19 Jun 2026 01:13:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:13:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:13:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:13:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Jun 2026 01:13:26 GMT
CMD ["jshell"]
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
	-	`sha256:a71d3554056a55a3c23a79e785d715834819f5cb9dc538c06bbf5d5b62758481`  
		Last Modified: Fri, 19 Jun 2026 01:14:12 GMT  
		Size: 25.1 MB (25118409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a481552f67f62f834abae715596440572695ac655d81404756df3959140279`  
		Last Modified: Fri, 19 Jun 2026 01:14:15 GMT  
		Size: 145.8 MB (145774023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f7ffd094b242c5eb96059251c87b1b27c32bc7de73cdb44aa0e7246b4b8c59`  
		Last Modified: Fri, 19 Jun 2026 01:14:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2845e971dba0179a171be80e0357525d43afb6c2b1bc4a0a15e99936bf7b8d`  
		Last Modified: Fri, 19 Jun 2026 01:14:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8c996c81491a230d047a9e757d51de3f03813392aa87084a1a39e53c2c905a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5466932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1931d14e8664ae8512ffbe584e2c63320d38c37f92da332896cd6f9c8d80100c`

```dockerfile
```

-	Layers:
	-	`sha256:7e5fe74810b163c7d677147aadfebe99753c96b8186230171ff55c775675c206`  
		Last Modified: Fri, 19 Jun 2026 01:14:11 GMT  
		Size: 5.4 MB (5440395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448164f1ace1880c7c0d0bd93496cd4565227fbe31c3bd560687942059470867`  
		Last Modified: Fri, 19 Jun 2026 01:14:11 GMT  
		Size: 26.5 KB (26537 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-resolute` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:10e3ca68502fd20ac6310baf3d9567ddc70d5e60066dde52fdbc992e60702a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199737788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78929bc5a64f9dbc941cbdbed1a09636a794044a89e34a2ab076ccf5cfb81045`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Fri, 19 Jun 2026 01:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:10:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:10:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:10:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:10:11 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 19 Jun 2026 01:10:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='2de430307390123858ea70b3ba399155b88bb05d65e5d3633b3a4d7b19acddb1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        riscv64)          ESUM='191cdd904aef8b8a7a91c98d649c7e3dc75b7341f112061231c2094c418fd630';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:10:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:10:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:18 GMT
CMD ["jshell"]
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
	-	`sha256:9b046e8338ef28fa8532dc4bc3d5f47d88e31f2e058f6d78a1f1448ae4bee29e`  
		Last Modified: Fri, 19 Jun 2026 01:10:46 GMT  
		Size: 22.9 MB (22858135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9dc718075ead844ae8977057068e922410cb51dd83c487db1b502c6af8f40`  
		Last Modified: Fri, 19 Jun 2026 01:10:48 GMT  
		Size: 135.9 MB (135919400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e893c3f147017222fe1119e1516d53cd4b1306a99f5a474a143e57fc7a8c3cdc`  
		Last Modified: Fri, 19 Jun 2026 01:10:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f5d9adda78a4b22fc03c365ca3c0fe4cd99d86443f98b74d59ab7bd75e0b1e`  
		Last Modified: Fri, 19 Jun 2026 01:10:46 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fed84851cb0ec284c21ad6bf16dce2f3017acca05a9719772a9e0486184f10e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5325887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d78e3ccd61e8ca66150c38412e0484b03ef09fdc5bf066544f23f3ba374371`

```dockerfile
```

-	Layers:
	-	`sha256:1834b3c6e73c3917c68c2b5879c0761eb9d72fae875ae6a39e937c8e2728cf33`  
		Last Modified: Fri, 19 Jun 2026 01:10:46 GMT  
		Size: 5.3 MB (5299411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53631e9b5df9b35fca9ac74e1dec399c787b8793c68d5631938e020bd32f437b`  
		Last Modified: Fri, 19 Jun 2026 01:10:45 GMT  
		Size: 26.5 KB (26476 bytes)  
		MIME: application/vnd.in-toto+json
