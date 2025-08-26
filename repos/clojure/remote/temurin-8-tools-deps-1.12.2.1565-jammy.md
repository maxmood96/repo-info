## `clojure:temurin-8-tools-deps-1.12.2.1565-jammy`

```console
$ docker pull clojure@sha256:3bd4df610afdcd7f8367e8a5086c3817d8887bc49b1982fbbd320be25f2193c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1565-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:986f3a41c0a05eec87b00506940b551ab220e28a20ccbc96f1a5af4e4e758703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151329703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3052db6c44013d09746292f9b142ea3fef875c6d2883c87e38ea6eaf20255c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08483b5f2cfe43842a06f46c6081326e0c2dc3b3243317fd12e60f348d678964`  
		Last Modified: Tue, 12 Aug 2025 17:24:18 GMT  
		Size: 16.2 MB (16150643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3dcc561c9cd39b92ec4fc57a6058ff42002ecf195e80d8ad5748e80389c1ec`  
		Last Modified: Tue, 12 Aug 2025 17:24:18 GMT  
		Size: 54.7 MB (54739766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582c1bed63e3dd80b9aabcadc64e63ef4bcde37bb178fa1bc799c832e74f204a`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6337a833f3117c3db42fc6b211b32a6b6874d435444ee9455d2e28d83e3326d1`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04ce544b19cc2d73785984a157519946ed1c57d8cc84c61450752a01e6375b9`  
		Last Modified: Tue, 26 Aug 2025 17:27:57 GMT  
		Size: 50.9 MB (50899219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0a5854b79d2615fa370d0f4cc4558bcda22744f11d3bb320ba10a85cb2277a`  
		Last Modified: Tue, 26 Aug 2025 17:27:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:5ea83254d6a176331138237f114bd06443a765301b128b0da6a9b148e68d7f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6435824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf5d1787a3a97b55adc75e440e4237f032a88dc25bc3779820b358eff792ce2`

```dockerfile
```

-	Layers:
	-	`sha256:eedb82cb50cb2fd5f2b3d5673c10ed3ad4764d2ebb526ea6c10f7b32e21b38c6`  
		Last Modified: Tue, 26 Aug 2025 18:44:41 GMT  
		Size: 6.4 MB (6422289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94023c66322d50cc06e64759ccfd738384e9d5df4731757c40348e2da412de44`  
		Last Modified: Tue, 26 Aug 2025 18:44:42 GMT  
		Size: 13.5 KB (13535 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:622acbba783a2921fe7904a3e14a32e31b6cd7d1fcdb975ba0b1b1ca213ad8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148114990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9159086a114d9a00e34aa8b51d3af58665cdbd1578418fb976f5eb4720fae6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e940b12283a67ff1c771864e58b58f224257969d16e19a179b3f8289c4d4dfcb`  
		Last Modified: Tue, 12 Aug 2025 18:31:10 GMT  
		Size: 53.8 MB (53839507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30fdff5a53ba3d2e43df30b5277041df566c24f5be4476b4e386dad68d69e`  
		Last Modified: Tue, 12 Aug 2025 18:31:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0ff686944578d38ac0413872ba73e79256657b51fdd048ef40b36aa1225695`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e213dea4c24cf68c66f675397069792883b4e270bae634b07458f2d4d69873`  
		Last Modified: Tue, 26 Aug 2025 17:31:21 GMT  
		Size: 50.8 MB (50849413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665168b85f944e28808bb53ea8af889e02f0eaffff9987fa4aca894dfe4ec854`  
		Last Modified: Tue, 26 Aug 2025 17:31:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:ebace742c99f259be5b4196d240b7f136459d1aa778155b7d9c6be1cf36b029a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6442380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e660de578aee4325037be6740a801947dfaf042e46908fa950fba51a7dce0e4`

```dockerfile
```

-	Layers:
	-	`sha256:e435f114f4f5e6d609639ededcf3ee8f95e4902e8732fc054f104596cd3f2812`  
		Last Modified: Tue, 26 Aug 2025 18:44:49 GMT  
		Size: 6.4 MB (6428753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182c0af84aa0f2867a1ea784d195b9ba1f4152702d537ce7a66acbf23e5acc20`  
		Last Modified: Tue, 26 Aug 2025 18:44:50 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:475818927aadb78d02501f8aa8bc3e42885937ddd9637b2517396f5edb955d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159074218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956e5d7318610b4273c3a79a6260c1062a9a9566c9c544c6738c9bf9d3f3726`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c50520b2833414582dcec4e87265a64dd9e5acd7b3ec03378e25ec51523b3`  
		Last Modified: Tue, 12 Aug 2025 17:29:14 GMT  
		Size: 17.6 MB (17624214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3563e462f65953d910e2846e6de3725502677044b4826058e62802811ea8a0ad`  
		Last Modified: Tue, 12 Aug 2025 17:29:23 GMT  
		Size: 52.2 MB (52167149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b266375691d61b72291e1f0d9e5169842674c1de091aecfdb3193e356c28d2ad`  
		Last Modified: Tue, 12 Aug 2025 17:29:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00321eef6c5bf0386430936d8260d05c426c784f7873c0c85189e55e3fa08055`  
		Last Modified: Tue, 12 Aug 2025 17:29:13 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dba1041387bca49a74b3d67c2126a9cd1e96e3dcd61c316f47e2c5e618fba34`  
		Last Modified: Tue, 26 Aug 2025 17:33:58 GMT  
		Size: 54.8 MB (54836629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc4909a516fbb912c10afebdc324980db7c2dd548bd1dcf3d9e7cbfef8580bf`  
		Last Modified: Tue, 26 Aug 2025 17:33:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:b8f8ab55988e47b340a46eab4c25ad3855697fe5a6970b9c9c4679a1032af498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6441675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c7414d9a622a0092721c9db76d2bc20e030b55ef4a1d6b6868832afe25948f`

```dockerfile
```

-	Layers:
	-	`sha256:67e7637b31cc67d9b16f635555ce27ed8605e48266c3533e4e31ee1a3eb0ac56`  
		Last Modified: Tue, 26 Aug 2025 18:44:56 GMT  
		Size: 6.4 MB (6428105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2820ad5d68d12b0c08af89b210547807261cbb3b65c5cffd6e06c1a36183914a`  
		Last Modified: Tue, 26 Aug 2025 18:44:57 GMT  
		Size: 13.6 KB (13570 bytes)  
		MIME: application/vnd.in-toto+json
