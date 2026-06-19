## `eclipse-temurin:25-jre-resolute`

```console
$ docker pull eclipse-temurin@sha256:c6ae8885b823b94dd1f95ce2551e7bdc4d043f1ebb4d5568f5482bfc3c1a526d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:25-jre-resolute` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:caee2a37fa7e47f6a87e5d10beec01f887696fdcb3c0320ac81bdf5b56b6eca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116758534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f0d0e539e60fe4a24a583f3adf126478669c04ea1f5e485f404c6d7b3a17b2`
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
# Fri, 19 Jun 2026 01:10:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:10:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:10:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:10:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:10:57 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 19 Jun 2026 01:11:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:12 GMT
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
	-	`sha256:9ad255c515b01e3d7380b097af05a25b01929c9f005348e9372658cf8c0cc01c`  
		Last Modified: Fri, 19 Jun 2026 01:11:29 GMT  
		Size: 12.1 MB (12146974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9892a140ee9c84bdb6754680210ee39a7bac1c9882aa389a966adb5c80c8d8`  
		Last Modified: Fri, 19 Jun 2026 01:11:31 GMT  
		Size: 63.0 MB (63046619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9765109addb123960b51e169270c4fc235e4b541a2cd46dddf3f8f5fb1c4d7c`  
		Last Modified: Fri, 19 Jun 2026 01:11:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:aa33eca06d57e29d233ff243ed2a872d2fed2da7b23d082a148cab006eafeb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4857552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ea20832e8cfbb9486efe986dfd8189395d7c846cb91c67d035a80683885d90`

```dockerfile
```

-	Layers:
	-	`sha256:5cee8bbbc90b1a4e278f45cdec6608b44ac93e7734785c0799e03770bd56a9a2`  
		Last Modified: Fri, 19 Jun 2026 01:11:29 GMT  
		Size: 4.8 MB (4833082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68801bb9d6aed2f33ca2326c5fc343190ac16bb2afd970083de1883d817958c8`  
		Last Modified: Fri, 19 Jun 2026 01:11:29 GMT  
		Size: 24.5 KB (24470 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-resolute` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:94011bcf7f29dcb0653da093344518e1b7a2f62d903e15f73ab752b280b555f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114754300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b2c758fc885c809027fb4359169bcb02cece047418801c892bd025cc240300`
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
# Fri, 19 Jun 2026 01:10:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:10:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:10:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:10:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:10:49 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 19 Jun 2026 01:11:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:04 GMT
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
	-	`sha256:70f71984badbf47e062ecebad5c2e3caaf00e94877fa31ce6d9ede8f94bf08a9`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 12.1 MB (12095815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541eb89265a05c29afa62264481595c553c7fa9859a8e47afde3e935ed6fca1c`  
		Last Modified: Fri, 19 Jun 2026 01:11:23 GMT  
		Size: 61.9 MB (61946600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b9c042a06bb651c03d116dd27abc54a918f5f38410e8608c10c3d645270dd5`  
		Last Modified: Fri, 19 Jun 2026 01:11:19 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cb0bf6a2c7394ecdb3a59d7898cd3d7c5201e32605617a4762a557de10b8f763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4857326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9c361e43294b5c2c7b076f710e54e1cc88032267398da5c808c5a10cfa0100`

```dockerfile
```

-	Layers:
	-	`sha256:bac8502c16549b0ca887d8310483efde77c20c36f5a51e1285408503994d33dc`  
		Last Modified: Fri, 19 Jun 2026 01:11:20 GMT  
		Size: 4.8 MB (4832722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9f39b75a5915b1a58d7bcb6a6f3acb0a37860ee3cf496123560f9d4eaeddbf`  
		Last Modified: Fri, 19 Jun 2026 01:11:19 GMT  
		Size: 24.6 KB (24604 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-resolute` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:59b9fbbdb571289d94209846a28fd285aee0a35098a5719854c0d7931bdb2aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121848307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd407ee6899530ba221bdaeaa1768cdd8c56426f686a5e926218a8cfa0383ac`
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
# Fri, 19 Jun 2026 01:15:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:15:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:15:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:15:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:15:54 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 19 Jun 2026 01:16:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:16:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:16:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:16:33 GMT
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
	-	`sha256:c02856b803f202decb5d7c2a5d82ab9f7fabe088d58382a9e20054bdea1d0349`  
		Last Modified: Fri, 19 Jun 2026 01:17:13 GMT  
		Size: 12.8 MB (12805621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5638e60714fe90534ca2509b84c40ce0cffa43652a0ccfefed1d0a60d81d6a8`  
		Last Modified: Fri, 19 Jun 2026 01:17:15 GMT  
		Size: 62.4 MB (62446183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facd0d7dffde63a1cf8a61b99a332230c99bac3da7647d87c31db100b47d78d3`  
		Last Modified: Fri, 19 Jun 2026 01:17:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8db11b0ac4b3737a05cefbf87240e4b2a511e77864d4ea9e3219f213eab38a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4860017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b087044f9a5b55493324a6cbeb1e3304012e60383b9fc3645b68ff6453aebe`

```dockerfile
```

-	Layers:
	-	`sha256:ae5b26fc7371f928f75f60fceca38621503b7597144ff521bb48d52441dacf14`  
		Last Modified: Fri, 19 Jun 2026 01:17:13 GMT  
		Size: 4.8 MB (4835499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71355caf86c2e3fe82c610782145d92f3c5f2e95343e8e973022593aae8c7122`  
		Last Modified: Fri, 19 Jun 2026 01:17:13 GMT  
		Size: 24.5 KB (24518 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-resolute` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:aae1851389241558e233c3f7f1c00cc9843adb437870a2bcca7b98b49136f568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113954913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e3b0faab45eace2f9936ac8aa3d35a318cf923e1318a7e9617d0aac7156699`
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
# Fri, 19 Jun 2026 01:11:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:11:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:11:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:11:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:20 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 19 Jun 2026 01:11:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:33 GMT
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
	-	`sha256:90efee5fad29dfe3ef95f29f908dba485fb19a2de90286e8a58859a511ee1a5e`  
		Last Modified: Fri, 19 Jun 2026 01:11:57 GMT  
		Size: 12.5 MB (12460012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7aa1c392bbee14c5e641e766fc9dd3a3c85d22adca6b5a96e033e2fa14cb5d`  
		Last Modified: Fri, 19 Jun 2026 01:11:59 GMT  
		Size: 60.5 MB (60534774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde47f424aaad69abbdd8df6625b8780c63c1ae7ab0cda40553c8afb70ab0a0a`  
		Last Modified: Fri, 19 Jun 2026 01:11:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-resolute` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:69971b225fef6095c30fb76fa3cdb974637e583ad809bac079cf274994fe46b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4858367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e904007d9684b894f8a9d271b98c60c5f8c580c132c4d24861c610a2fbf347`

```dockerfile
```

-	Layers:
	-	`sha256:4f7c77a2ae2df4ddd511b246aa45f2f89a43985dda4e3f653cf842f5a46c9b16`  
		Last Modified: Fri, 19 Jun 2026 01:11:57 GMT  
		Size: 4.8 MB (4833897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee1716e6275997b047c0b939caff04db3d9b6c21b785291b0a17a57f07f3180`  
		Last Modified: Fri, 19 Jun 2026 01:11:57 GMT  
		Size: 24.5 KB (24470 bytes)  
		MIME: application/vnd.in-toto+json
