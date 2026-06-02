## `eclipse-temurin:21-jdk-noble`

```console
$ docker pull eclipse-temurin@sha256:81cecb98bcca2d5d5c3d496e71779073865db0d0bd776ecf434e017f20dac638
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:21-jdk-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:fbb9a7078ae8b5cdb71640e2d543bede2b92b8f20097b824e2434d515f402af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210873953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86a832840eeb5a39a54e4b0ec8164d84a37e6e7190b86d4f261df7cda626f16`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:55 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:15:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:15:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c01f3db1a2719e1e808c136c592a0317da2de26436d88427de04087774eba8`  
		Last Modified: Tue, 02 Jun 2026 08:15:21 GMT  
		Size: 23.0 MB (22967088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb223f00d1684b6ee21fe982b5801387d1b3ec9f7d64c33554284c601b317f6f`  
		Last Modified: Tue, 02 Jun 2026 08:15:25 GMT  
		Size: 158.2 MB (158171619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4cb00b79d971cc3d3329a372aeae086cab6860dba5ba781ef348d277b9f1a`  
		Last Modified: Tue, 02 Jun 2026 08:15:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11ec3c5f9ee6853717e932b3c91430d0d29bbd47ea5eed1c864199628ef2297`  
		Last Modified: Tue, 02 Jun 2026 08:15:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8d877208ddc63407c0f947640632f094d3400832ca64b7144aeb97bf2eb874e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e63453faa73719123a86f57dd0ff76dd6210b1cb194e52443d054d0e693683`

```dockerfile
```

-	Layers:
	-	`sha256:0b008afe03e602b1b5e97647b5e42866891c5ecd21bbad8891b5de560655b61b`  
		Last Modified: Tue, 02 Jun 2026 08:15:21 GMT  
		Size: 3.5 MB (3525332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87b07ae89ee4600f624e0028ed4625d44daecd16e2af22bd027a7b9d48d25696`  
		Last Modified: Tue, 02 Jun 2026 08:15:20 GMT  
		Size: 23.9 KB (23931 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7b174b01843ba8e9e59df9c55c04c2e2c8c511fbafba5522755f9eae879f5395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209525028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436db4f454add02b001ed6241f64cbf0e7b938eaf1dd9ae1a9126c4d0a37eb3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:16:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:16:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:16:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:16:03 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:16:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:16:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7ab84c2d67441fd3bba3abc37b68773f34e23d567cafb4fc02200349dd96c9`  
		Last Modified: Tue, 02 Jun 2026 08:16:29 GMT  
		Size: 24.2 MB (24172747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564f721386e7e6dd884c7e86149b2eccf2a7567f39b392cac9b7daaec0d44dbd`  
		Last Modified: Tue, 02 Jun 2026 08:16:32 GMT  
		Size: 156.5 MB (156473432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11127b4e771266a8d44b39627af51fefdb6fa421c879eb7d140a973db20c5ea4`  
		Last Modified: Tue, 02 Jun 2026 08:16:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3581c265283ead4745033bea80232c9672330e64126c9d520cf092afdd33e24f`  
		Last Modified: Tue, 02 Jun 2026 08:16:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b26dd9533eed088848c4e2dc1e7301e09aed65f29e6a67182d89bb2711902fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d44b2800e410402c6af2314f05847a72b28b44b470d522dd47c23604b39db1`

```dockerfile
```

-	Layers:
	-	`sha256:5463343c4f2e2032b30ed02807bb57c0363522308d3181aadb3a1c8e9f64cc0b`  
		Last Modified: Tue, 02 Jun 2026 08:16:28 GMT  
		Size: 3.7 MB (3656841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e233efd7026a305a80b2ec0aa5fb62198b811a97424c17959bdd0f3b681c0922`  
		Last Modified: Tue, 02 Jun 2026 08:16:28 GMT  
		Size: 24.1 KB (24054 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:015ed182152d0e5ea48494d63c131d65aec58966dfa190b0d05923047be76b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 MB (216758489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16196b4deccc87a8dd411abb91b759e29d21ca58b58696d2b4a86aebd712b0d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:12:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:12:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:12:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:12:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:12:24 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:12:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:12:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:12:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:12:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:12:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c1670fe2f067637ded122a0663c456ca6091e763c878866bd1996f0f3852f7`  
		Last Modified: Tue, 02 Jun 2026 08:13:11 GMT  
		Size: 24.1 MB (24096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f99ed93216c409ce80de40299956c411fe8d5580c1e4effe74d64e94d62449`  
		Last Modified: Tue, 02 Jun 2026 08:13:29 GMT  
		Size: 158.3 MB (158345909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038eb3036bf5ea5a468b49c2e5dd73daa411d2c8d6810020e7332228fd980030`  
		Last Modified: Tue, 02 Jun 2026 08:13:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64bbf3baca588841b50b9d867afee68ac3fa864c9ec5ee9c6ad293dacbfd78d`  
		Last Modified: Tue, 02 Jun 2026 08:13:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e58cec84b987c636df51aaa1b805561efb3e5f9193267b4ade30cf0aaf09c791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a027251d5cadc0fe366f5da209d723e08f3ad26471710ac083cdd2727378fd1`

```dockerfile
```

-	Layers:
	-	`sha256:837e28719f0d1725dc23dae3aa33616dfd7f348dde551d4c87cc8ce9a9665d33`  
		Last Modified: Tue, 02 Jun 2026 08:13:25 GMT  
		Size: 3.6 MB (3573098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46072e06f65dadd48d7629164e8d63e49b36dba29b574bcd4e24278f9cbe2a78`  
		Last Modified: Tue, 02 Jun 2026 08:13:24 GMT  
		Size: 24.0 KB (23974 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:f44e09d6b42843cb1a40904e52422e8d6c3910a3db71d656d43fa284e86608a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208593927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0165fc0b152891af82a1c83ca4e688ed9b5689cf94e423375703c9fec4f35a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 02:06:08 GMT
ARG RELEASE
# Wed, 20 May 2026 02:06:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 02:06:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 02:06:59 GMT
ADD file:f1fd7ee282731834f2f36b17e9b538e569ade4ce8b89924b635551ff3a45c706 in / 
# Wed, 20 May 2026 02:07:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 18:07:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 18:07:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 18:07:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 18:07:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 18:07:31 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 18:19:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 18:19:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 18:19:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 18:19:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 18:19:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:924f9a731915e06f77b3487378ddf9426f8422fa1d96461bef1d0e0a35c36743`  
		Last Modified: Wed, 20 May 2026 02:15:52 GMT  
		Size: 31.0 MB (30965919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8a013d222cf59769d7670abdeed7b6b225951393f3dc9a97036396ec0727f8`  
		Last Modified: Tue, 02 Jun 2026 18:12:32 GMT  
		Size: 20.2 MB (20155014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e348f2cf4a5220f3241d7c8bbec98de871cb98b259c80e90d5f1ce1e844291d5`  
		Last Modified: Tue, 02 Jun 2026 18:23:53 GMT  
		Size: 157.5 MB (157470551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9bcdb7880dae07773175355a32fab1450f93dbb99cf667b040d1344301d0f8`  
		Last Modified: Tue, 02 Jun 2026 18:23:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b3583d0bba2f4eeb410a3d7c6594ee8aae81196a50b806fb22cad9b947304`  
		Last Modified: Tue, 02 Jun 2026 18:23:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f4a0fd2ef3bde6cc4e234519e8587d8a51182076cd521349057bc67d559688f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3656547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee426c6773271ac68da0744ab5eb019f7c1d03032b2d17b9204681ca434ce2a`

```dockerfile
```

-	Layers:
	-	`sha256:bae0eca838a71bbb32bbd21457de4b879bb6427b9ee4de827577b415672b68f0`  
		Last Modified: Tue, 02 Jun 2026 18:23:31 GMT  
		Size: 3.6 MB (3632573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d18b9c152b156cf6e18b32efa875f96bd5a78bdfcc418b9e90fd4d5cf9474e`  
		Last Modified: Tue, 02 Jun 2026 18:23:30 GMT  
		Size: 24.0 KB (23974 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b8249abda46206c2a29366ec0e1411b93c6217715a77ffac19019c326aad63e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199444666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a4c8be4b1a7e95fccff0691078f4742bba72203d6205f0d8141cf9df182a17`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:11:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:11:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:11:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:11:03 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:11:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:11:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161ab83b783a70ac7e335f06f868087878d7a3e67ada1ea2ed592d86b5ed002d`  
		Last Modified: Tue, 02 Jun 2026 08:11:34 GMT  
		Size: 22.1 MB (22130533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5ba65f654f079fa940ba38ee6ace3fac70039f845c9b29befdb2d4219f8e9a`  
		Last Modified: Tue, 02 Jun 2026 08:11:37 GMT  
		Size: 147.4 MB (147398857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76a6cebb1e74b0c202e5830c582ceb4a363c946651341977e28df6e3c678e23`  
		Last Modified: Tue, 02 Jun 2026 08:11:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43a9502fe3bc0ed260d6f31186168220db755450056002c0f96394792b89dc0`  
		Last Modified: Tue, 02 Jun 2026 08:11:33 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2e4e36037905b9dcc1c5f41dcef5907eb1383e36822e013435ba2cf1e637bc70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3495075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75819d1c481f9d9d20d4361ed24b822d8ace9294a039c6681c03afbf89972558`

```dockerfile
```

-	Layers:
	-	`sha256:c8ba4d360ec500b91255ddecc6a282cdab180923688774dce063ef256d2615a3`  
		Last Modified: Tue, 02 Jun 2026 08:11:33 GMT  
		Size: 3.5 MB (3471143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:976080ec395c05d9f4990e525aee9b44d81eeab68b9a255ea014be1b1fc6aa0e`  
		Last Modified: Tue, 02 Jun 2026 08:11:33 GMT  
		Size: 23.9 KB (23932 bytes)  
		MIME: application/vnd.in-toto+json
