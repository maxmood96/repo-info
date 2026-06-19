## `eclipse-temurin:21-jre`

```console
$ docker pull eclipse-temurin@sha256:8ec353b20d3aab0758572236b81b967c7077c40c4d0819ce97f9a1329d684603
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:21-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:92c037c0c822f05cce41807682052136d9f1d8ef3c0cc6a514833b4f21528453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114811134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab54c87a45866c6c7cb76fac6099bee98feb0cb7c0d76841a02ad31967c20bb`
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
# Fri, 19 Jun 2026 01:11:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:11:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:11:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:11:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:31 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 19 Jun 2026 01:11:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:35 GMT
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
	-	`sha256:615a4ff2c6307fd0c5e826eee696ae3f0033453e344616ea7fb5f682b3ccfb9d`  
		Last Modified: Fri, 19 Jun 2026 01:11:51 GMT  
		Size: 20.1 MB (20122737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7852e663f18cd4bf5da0f535caacba2bd355d89d8b4df3868e0b59dba43d2cf5`  
		Last Modified: Fri, 19 Jun 2026 01:11:52 GMT  
		Size: 53.1 MB (53123328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860799bd61a18c5249afc515d19d73e68f1a67387c6d87f7bc06d1a09ec03694`  
		Last Modified: Fri, 19 Jun 2026 01:11:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde47f424aaad69abbdd8df6625b8780c63c1ae7ab0cda40553c8afb70ab0a0a`  
		Last Modified: Fri, 19 Jun 2026 01:11:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:57d70b89f08ea14a1244d4f70b63056469272543b10fd8de537de453fb180070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc79c7e9570279480e18a0e78474d084dccf414a065489726fc02d93ef52da7`

```dockerfile
```

-	Layers:
	-	`sha256:2619fded60d729ba0668799239fa14da4b648054f2097301af2619d724ba19c0`  
		Last Modified: Fri, 19 Jun 2026 01:11:50 GMT  
		Size: 5.1 MB (5099012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba5723fbc80c6daec7f6fbf1b886833aa3f39eb9eece08eae9fb5fc04a3045fc`  
		Last Modified: Fri, 19 Jun 2026 01:11:50 GMT  
		Size: 24.0 KB (23976 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4b1af96961053f7a9fa67192d1444f43795a79d3a620ecb8a60b6f0beb440cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112954451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ba3215d1dc7010e70098f8c1b492f95a91a24a9ef18a9fbbb4ec015120a5cb`
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
# Fri, 19 Jun 2026 01:11:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 01:11:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 01:11:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Jun 2026 01:11:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:09 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 19 Jun 2026 01:11:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:11:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:11:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:11:12 GMT
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
	-	`sha256:f3735eb622b92a2a3e5f4a14518d575a1f2b57e11bcf5e52eb8cdc4727abf237`  
		Last Modified: Fri, 19 Jun 2026 01:11:28 GMT  
		Size: 19.9 MB (19927450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482e060d7e8732c1146f276c7d23e4d555c4759a149a36b4bf9f022358664e63`  
		Last Modified: Fri, 19 Jun 2026 01:11:29 GMT  
		Size: 52.3 MB (52314987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7bba5b6382e1a99560af2de1f98e9b68185c6b1e6bda08afd8a5d339891717`  
		Last Modified: Fri, 19 Jun 2026 01:11:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637d677290413699f4e81981f7df6139544656db1e3c03d2062f65fb39f67ee1`  
		Last Modified: Fri, 19 Jun 2026 01:11:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f045f3a7ffafdbc42cd5ab29204595752021d1fe4a2677646d4107d17ed7e28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6425ad05b40be26f148b382ef6d4f273f04164a2966457ae3cb79eb7444089`

```dockerfile
```

-	Layers:
	-	`sha256:6e9375e00ade3929dfa580e5dd264acb541fd59bf14f998012bae1c9ce22f52d`  
		Last Modified: Fri, 19 Jun 2026 01:11:27 GMT  
		Size: 5.1 MB (5098681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86651d3c83539d2f38a725816497cfb482828107675c215481fbceb5bf7410a2`  
		Last Modified: Fri, 19 Jun 2026 01:11:27 GMT  
		Size: 24.1 KB (24110 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b14c3c4c8454e21f6ac3cb76a1529792bc1e2fbb73aa46bf9d90fea621f3d88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122178905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a56fc8e9aa1a07b9cf58fb974c3ed2e6d8a6eb3483038ac50ab6722bd8e634`
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
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 19 Jun 2026 01:14:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:14:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:14:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:14:40 GMT
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
	-	`sha256:065381a8eebab402564aa1aee79ddc415c62a42e3406b483bcdf9cd56173235e`  
		Last Modified: Fri, 19 Jun 2026 01:15:24 GMT  
		Size: 53.1 MB (53148847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b92512817afb4f08e4aeaab95bf3e42a87db2bab902f4ae35064c5f08c7af63`  
		Last Modified: Fri, 19 Jun 2026 01:15:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93258e640b93be697ae69c41e0bb0f70a750f648266fb07aad23eaa18289aff5`  
		Last Modified: Fri, 19 Jun 2026 01:15:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d0675c269c1c3d21486be5296ffcec05c641370b2d991e7a171f2d7c31712b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28d9851e9cf3743eec2855481228c595f804f9ec50b76175403e5b2b318c984`

```dockerfile
```

-	Layers:
	-	`sha256:3e7393cb06ad887186f6dedbe246b2c2ae4bb756c9b81884e8d53343bfe5cd40`  
		Last Modified: Fri, 19 Jun 2026 01:15:22 GMT  
		Size: 5.1 MB (5102272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f990927d476b8751fd7930103c40b42243a0ad642a8e734fde321e89f8d3070`  
		Last Modified: Fri, 19 Jun 2026 01:15:21 GMT  
		Size: 24.0 KB (24024 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:7dce9a716b06aa1e210bd7837e3c86d898f37cb5a13a18d1798a468ae438ce81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111305503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9cb903c8f0551af83b226aef067ba6f005b0d2d7497ff075a39a6b34cfa1e5`
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
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 19 Jun 2026 01:10:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 19 Jun 2026 01:10:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Jun 2026 01:10:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Jun 2026 01:10:27 GMT
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
	-	`sha256:213d805607f563d77a095e000480297883dd5201cecb711560506fea726dad89`  
		Last Modified: Fri, 19 Jun 2026 01:10:02 GMT  
		Size: 20.7 MB (20676607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3a16cae62974755397edc2bd6bd2d4b8e5509e8d401b4f366633be95f07526`  
		Last Modified: Fri, 19 Jun 2026 01:10:50 GMT  
		Size: 49.7 MB (49668642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61b5298c40af660c0685ddcd7cc983b5c48fbdde3d6adb4380153505a2a6f00`  
		Last Modified: Fri, 19 Jun 2026 01:10:49 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b390e741ddd7a7a409a0324c064be96ad2bc08ead14df483de44746123801f47`  
		Last Modified: Fri, 19 Jun 2026 01:10:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3b6bb97372d6912e30871b4d370c968358fbd0e64d79bb4f07bb461494f9e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0bc4f0b64a0faf4b02eb18b7786890aa7f61e1208a75d6d244823d57d28ac8`

```dockerfile
```

-	Layers:
	-	`sha256:d20b3976fc560c59238bb781806c67722610c280d01a9ea18016f25bfff2946e`  
		Last Modified: Fri, 19 Jun 2026 01:10:49 GMT  
		Size: 5.1 MB (5100422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a09635ce56d14cb4952a995566f57cb2de7fb325212b9224e179fdd5be35522`  
		Last Modified: Fri, 19 Jun 2026 01:10:48 GMT  
		Size: 24.0 KB (23976 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:26af77718eb91b05ec454c5a3c70aa4eba7a0bf0c2c1f15d3ca736602b95475c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363352717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b68828ee995128c3227ad440c1a311359278f24c79fd8b91fc6577ea6b1f5cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:12:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:21:56 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 09 Jun 2026 22:22:22 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ;     Write-Host ('Verifying sha256 (570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Jun 2026 22:22:29 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd9775be4031937efdc97f503b8e8073012c6d3367d79761e42678fea5e5a9f`  
		Last Modified: Tue, 09 Jun 2026 22:14:23 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6c838fd720d1cafce6510be825d1971befe5577fb28134718bb9b7a6071663`  
		Last Modified: Tue, 09 Jun 2026 22:22:33 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349c7a4214a6b536dfed37643772e3950e24ab3e942bbfbd86b9a484b126e53d`  
		Last Modified: Tue, 09 Jun 2026 22:22:41 GMT  
		Size: 83.8 MB (83839284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1e821ef8cc2d58b93910d1f1311bf11b681268ae71052ba45233860f7a4214`  
		Last Modified: Tue, 09 Jun 2026 22:22:33 GMT  
		Size: 367.8 KB (367770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:5c99cff49bb76d71b52f669101ce89c3d2f1e19ee7fb24fc00ef06f8f1095f9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216434500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3447ea1d76bb6c16797d15b625e3b409fcd00537d6fe5628062351e39bceca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:20:28 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 09 Jun 2026 22:20:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_windows_hotspot_21.0.11_10.msi ;     Write-Host ('Verifying sha256 (570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '570b2b7f4d39638afe416e14285e08f27fd14995e0716dcbc07f936a5b91868a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 09 Jun 2026 22:20:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c9b713a469c080f684d10fd327070faf916b6d9b86f859442eebbd39bdd7b`  
		Last Modified: Tue, 09 Jun 2026 22:13:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e553cbe149ffb213e52edbd74e1bc0da47edc1482a0cc875219ca6cfd80dd`  
		Last Modified: Tue, 09 Jun 2026 22:20:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fb51c22493a9cea4163796ba78db23a34d8fe49cf49b2d5a0c8bf2b184af63`  
		Last Modified: Tue, 09 Jun 2026 22:21:03 GMT  
		Size: 84.0 MB (83954355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41614aee85eaa8ce9f7e78fe24662af1f78b72341e1a268f11375cb8a29cf18`  
		Last Modified: Tue, 09 Jun 2026 22:20:56 GMT  
		Size: 352.0 KB (352002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
