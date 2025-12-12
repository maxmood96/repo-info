## `eclipse-temurin:8u472-b08-jre-jammy`

```console
$ docker pull eclipse-temurin@sha256:5646b5fe4d2872667d8ee27201cdde9a6497bf45030405932da929945387a2ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jre-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c0957ee03a47dd2552b36181a4d11f441f1047336d8715f9d3e60ce50c9707d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87580665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e5590f0fa0a2a8d08a35f4c2beabb6aadc459a677df436356281fd2f42ef1a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 13 Nov 2025 23:20:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Thu, 13 Nov 2025 23:21:02 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d42da29b2619c195f2d196f0bc64cf7347c4ac72d8618648296410ba20c837a`  
		Last Modified: Thu, 13 Nov 2025 23:21:06 GMT  
		Size: 41.9 MB (41891089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa94125d190e370b5bc6035d26b8d573a9f94fb5489af0d5b4e898ac6a7523eb`  
		Last Modified: Thu, 13 Nov 2025 23:21:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53675a133c6bc8e493090499c6df5a23837a682556eaf29bce46837a8957367`  
		Last Modified: Thu, 13 Nov 2025 23:21:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0a9736e14778cff18d442cd8d3e55b634ab12f7c366951ec67922d5a1c9414e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf26971beed517893fbad34acfcde64f34bb6ee4e95e9a460d341ecd3f54a02`

```dockerfile
```

-	Layers:
	-	`sha256:2abf406ea7956a6c0984bef641d15c5718ffa91580643aee1bd981f16ab59fa3`  
		Last Modified: Fri, 14 Nov 2025 01:21:14 GMT  
		Size: 3.9 MB (3909469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c9f9db2ff6cb8a2b670321058e2b45a6c0b82c51148d224ec033c8d0c151fe`  
		Last Modified: Fri, 14 Nov 2025 01:21:15 GMT  
		Size: 21.9 KB (21917 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-jammy` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:a9ce5a2fdf2b85d31d0de36e632e8d0a49e4e2c214bfe75ecf7af1f4d5d79b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81915598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67011fd59e695adefa5f5ee0418b694d93a1d7e47882e4557ee99fff8846a2c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:24:03 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:24:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:24:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:24:03 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:24:06 GMT
ADD file:94045c8d87683c20b28046857f569ac4ad9ec1c53b4f70e51c2badd873183cea in / 
# Mon, 13 Oct 2025 17:24:06 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:09:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:09:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:09:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:09:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 13 Nov 2025 23:10:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 13 Nov 2025 23:10:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:10:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4179ba9965faf453aec60ab64b5f5722816899d199d00def462ceb5d7057ad8b`  
		Last Modified: Wed, 15 Oct 2025 15:02:27 GMT  
		Size: 26.6 MB (26643386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac4efe53d4d6d761b5cae150a2002f56e80bdfd4ebf832bc7a30d28e95a0250`  
		Last Modified: Thu, 13 Nov 2025 23:09:55 GMT  
		Size: 15.9 MB (15889551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d879a3596f9e0127eac8c5165da8aac6618e8a73c27b0e0b2bdfebbcef392f67`  
		Last Modified: Thu, 13 Nov 2025 23:10:30 GMT  
		Size: 39.4 MB (39380252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edde7553af8849f60d9a3f046c1cd9400e2256fb6a2b59e818bfffe1a0b2763`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a29b2afb030da1e13885b86aefafe4d83649959b619752411ba821baf504ef`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:36088dbc4928fbb3d9cf91b415824a20c1d677d10d4ac7a1aea16d0e72424af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f0c44c903f7998e3e8bc2c63b953ca6262bd69930a76b8dc1a9abc14631e86`

```dockerfile
```

-	Layers:
	-	`sha256:8ae5d514d6633a051637ab1953128ee8137828baab02b9007dd332679a8d219d`  
		Last Modified: Fri, 14 Nov 2025 01:21:20 GMT  
		Size: 3.9 MB (3915474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23be84e8ffa745b4227efe00fa630147f8ee6d9188daaf62f47c8f80495bacff`  
		Last Modified: Fri, 14 Nov 2025 01:21:21 GMT  
		Size: 22.0 KB (22007 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:189e5aaa4f9acf4c8f512a80278156449fc7c75c6cbd060d8b2e8aec8108c98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84336814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bbf23575cdb754d200e8a31d6024bbded44c1e4d604488ee8ba12b251084a8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:19:49 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 13 Nov 2025 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 13 Nov 2025 23:19:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:19:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:19:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5369e2c5987fe89fa050043100e241a2725176ee99bac61e572a01fdea160aab`  
		Last Modified: Thu, 13 Nov 2025 23:20:11 GMT  
		Size: 16.1 MB (16066267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f016777af162773ef4add02a6a6cd56692f8a61641bf57a3c7ef03d083c70e`  
		Last Modified: Thu, 13 Nov 2025 23:20:13 GMT  
		Size: 40.9 MB (40884259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d719ef22f239f993ef39c8513bd44ecc003def43e2279a9426d1ff2a18a882c5`  
		Last Modified: Thu, 13 Nov 2025 23:20:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c3383a9ac03ab2522596c3e79dd86cdb7038845158cdcf47b92095b3523c7a`  
		Last Modified: Thu, 13 Nov 2025 23:20:08 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6a3091dbaf973080b8b21deebf0f42f6255620f70191c232b924b41d053fc79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12274c610256244680d538aba0ade1f7ada5a021cfd5db27e83efe6ed733ae09`

```dockerfile
```

-	Layers:
	-	`sha256:5bb27bf6f695ac02458633ba365374c0fe95c961fb560a5dbe2d63a89baec59c`  
		Last Modified: Fri, 14 Nov 2025 01:21:25 GMT  
		Size: 3.9 MB (3909815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b6e6d02fe1f078b8e54ae9f8ec9422e13019c2b177514561412b01d4df3ce5a`  
		Last Modified: Fri, 14 Nov 2025 01:21:26 GMT  
		Size: 22.0 KB (22027 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:a618deb43c622e43e1f6fdc13f43a64abddb1158528b1cec5d1b4213be0e4293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93345670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb16364e241bc8f06d0a062ab8795034bcbc48193d21d40a8619bb0ea368fcc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 13 Nov 2025 23:14:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 13 Nov 2025 23:14:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:14:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:14:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Thu, 13 Nov 2025 23:11:46 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fe621fe04c7d7f5882a7eb6c4a40136fe5fb3f332af8eda36928b5704f36b5`  
		Last Modified: Thu, 13 Nov 2025 23:14:53 GMT  
		Size: 41.3 MB (41272684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da58c71c87846a0a0553468c35c2b9c1657073e762783c88101e7da47cee15ae`  
		Last Modified: Thu, 13 Nov 2025 23:14:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43de536bccc3ee8506cf8fe184cd019150f32a1d38351877a1951fc5b16da7bd`  
		Last Modified: Thu, 13 Nov 2025 23:14:47 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3dfe9c342b3b3563e04cf914b902863753f4a7c08f7e5548a749554d734af53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3936185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33462be54446b129d4e6b193e263e9d0431c30f683288ac088005f1c5d6312c9`

```dockerfile
```

-	Layers:
	-	`sha256:9ff1986296f6001b0f5416761dceee17eef080a1ebd1fc1afb93eadfb54cdead`  
		Last Modified: Fri, 14 Nov 2025 01:21:31 GMT  
		Size: 3.9 MB (3914232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a73a7dd545425b0d32642d0751c75e977f39a0e7c58c926954398b913b750a9`  
		Last Modified: Fri, 14 Nov 2025 01:21:32 GMT  
		Size: 22.0 KB (21953 bytes)  
		MIME: application/vnd.in-toto+json
