## `eclipse-temurin:11-jdk`

```console
$ docker pull eclipse-temurin@sha256:d5750bfec0716086bfd170d1bbe110cbf2a8f8490282a6a2b3174244904ef0d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
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
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:11-jdk` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:53e51d98c1d888069501d4e61f94cf9f8add3bf16a3930efd49261953d61dd89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192326099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea120c1bcb2c6d9148fae7b8e980f64001aa52a5cf4b0edccf36453f59dd5811`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7cf6ce712595785e41a7a15e225133307496d59128ffe840c227987d8d9514`  
		Last Modified: Fri, 31 Jan 2025 01:29:58 GMT  
		Size: 17.0 MB (16962271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4233bc911fbc218505b2e8a27e926a0575cd2694c5eeb322bb86c693419f3f`  
		Last Modified: Fri, 31 Jan 2025 01:30:00 GMT  
		Size: 145.6 MB (145609418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af40d3a48132e5420f4a00420bf67103835fddf971270f7c4b2b55783646614f`  
		Last Modified: Fri, 31 Jan 2025 01:29:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f8eb4b6379460b80dd66d5f873c571d726380eda636994bee7e130a2e31bb0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427ebf3d77ad7f677a882970e256734cb38f7e1bbda1ceeb21a3481c09b9d748`

```dockerfile
```

-	Layers:
	-	`sha256:1fc04d68dfb46b52ad143707adc08bc3f1c05a1f2079576d8bb83608b52f7c78`  
		Last Modified: Fri, 31 Jan 2025 01:29:57 GMT  
		Size: 3.2 MB (3222470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8b3a59ae05787bd92471c81b9f6b0a69b85804344baedf7bed96de08f6b0df`  
		Last Modified: Fri, 31 Jan 2025 01:29:57 GMT  
		Size: 24.4 KB (24438 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:30972aa7e5d9de07923ab9b320078ecb32861237d0bd058a57a3c95a33c759d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181263800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49581056ab62465acb6554309605477ccac7c92d5479f3ec0a0753d05d17e381`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:50 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:53 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Tue, 19 Nov 2024 16:18:53 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb203c12bccdd1ea39918100081ec35064e46ee449912ba202946ac25bc73f1c`  
		Last Modified: Fri, 31 Jan 2025 01:36:55 GMT  
		Size: 138.1 MB (138091813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845a454a570b880a269560d45624129531ac4d202ecb0d34a29ac770b6228772`  
		Last Modified: Fri, 31 Jan 2025 01:36:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568d23c7af99b7447c279de480a0a2d0927cb8961f51371812f523b44ed692e9`  
		Last Modified: Fri, 31 Jan 2025 01:36:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a1679054f1e2267d45d7f211d9aaa49d3725d8c7a01f3ecb76094f1d064bc85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3248706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b86414f88958dd8e1beabdb6c07a12d13e28f510c845fff344c0b7d9e97a64`

```dockerfile
```

-	Layers:
	-	`sha256:30fbc53d998b70e8d39a566bf6e26b90877eda5dd41e02f776f098504401cfdc`  
		Last Modified: Fri, 31 Jan 2025 01:36:51 GMT  
		Size: 3.2 MB (3224150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7bef737a4121ab72d2976cd6cb5bcc4e6da699f853cd8fc791d1d5ddbb4cc2`  
		Last Modified: Fri, 31 Jan 2025 01:36:51 GMT  
		Size: 24.6 KB (24556 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:695c551b921c618a6fc27847cea068241cbdf88d1bb46444c41e9ad7bf32f699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188268592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5637d94c1dccc27dabfe69ae4eaf527c7d9d034033a0c800b8f28ca1407c4b5d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2ddcaa27e0d982156436b240bae97c28739cbd0a338c37c2a4dda20a225894`  
		Last Modified: Fri, 31 Jan 2025 01:36:35 GMT  
		Size: 142.4 MB (142390623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb66e82b52fdfb5e76e26ea1f3962cae9bb2f8f4f5f9ff15dd3a70e3b1d68516`  
		Last Modified: Fri, 31 Jan 2025 01:36:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2820c4a897f876a7827c2b8b199917a662d1d146464d78c6d6ee0d2ca78dc`  
		Last Modified: Fri, 31 Jan 2025 01:36:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1a29cd07cb6255c453cbfbb45e9945431e3cdba7d620d9e6032201c04c9ece04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3248783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5081254793ee45be1494a95d464d20c1b1df5920112cc3154ed18df5cdf81a3`

```dockerfile
```

-	Layers:
	-	`sha256:a02a2c392d58f2be590565e87311c9d9e2c0b82fdb82e4e174a7075091555864`  
		Last Modified: Fri, 31 Jan 2025 01:36:31 GMT  
		Size: 3.2 MB (3224187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ae3fe370089aa91da3a51d41fc2e63ae06e65ede1bf01baf09365897c4715e`  
		Last Modified: Fri, 31 Jan 2025 01:36:31 GMT  
		Size: 24.6 KB (24596 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:88388742822079fc7997afe6f5cfb25dcfaedd8924be2e11a121b90c41827fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186024153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c596813d331f86dc2a9e0966a2fddb295bbb93725ab5024fc40e6702594176b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08691d29d174440113fb3d94aec487ff706b850acfce25b3870b67886fdc90`  
		Last Modified: Tue, 03 Dec 2024 04:44:50 GMT  
		Size: 18.8 MB (18845906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7d80311db8feb346293d14485090decc038766cc881f2172f953848c765e6d`  
		Last Modified: Fri, 31 Jan 2025 01:40:31 GMT  
		Size: 132.8 MB (132786984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9336d8b5561571f4b2ba2a5a000f2a68506832a80a538a9b9f287cb3e386b4d6`  
		Last Modified: Fri, 31 Jan 2025 01:40:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7b252e24eb5bce3b441b2661e0934bb326aae36ff2487f86fbba17cfb8df72`  
		Last Modified: Fri, 31 Jan 2025 01:40:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5a91502672cf0a4ef05e10256b3a5fd58412937ccbb0e4a061430dc26f7e3b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3248976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a874a3935a639369e3ef2163bff085d6a809e89967905126d2b1987f15556b`

```dockerfile
```

-	Layers:
	-	`sha256:93423afb645b8f1467c50c350e870abaa5bb2d0c27bb64807ba95a315191d27c`  
		Last Modified: Fri, 31 Jan 2025 01:40:27 GMT  
		Size: 3.2 MB (3224478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea9e6ec48f15653c55027a3ad3c45ba957ca8552ff768328ca1497c5b8d63997`  
		Last Modified: Fri, 31 Jan 2025 01:40:27 GMT  
		Size: 24.5 KB (24498 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:39ca8e71dea9f75d1fffd1cef209c8c47f01694b946b1ce2c7d9b6270ab76942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173214174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b318802a3bfa0aa26e7e8b972e3b64dc947becc9e7b38ff6e2c18a5e35bf20c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:14 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:16 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Tue, 19 Nov 2024 16:18:16 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13455a8ef0bbd24a83e365c2d75ff490c2b96ae8d038965b9151dd68fc2f3011`  
		Last Modified: Wed, 22 Jan 2025 21:45:34 GMT  
		Size: 17.6 MB (17614209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c646652aacc0e574d848e72315aa82d29f6644333df53fb45cb4be3f33b857`  
		Last Modified: Fri, 31 Jan 2025 01:32:31 GMT  
		Size: 125.6 MB (125576699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c650d692c0358059f01960ed5efeaf90abc7a9e860e4a30f39b657a0586c268`  
		Last Modified: Fri, 31 Jan 2025 01:32:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8e6749bf20bbfdda86035820ccb362bd8f524e30bd2e1153f058fad2d9d8df`  
		Last Modified: Fri, 31 Jan 2025 01:32:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9ea383d6b3d70fb2db9fbd05690fb34fc0c31d7403f88126076c5a03f0a359da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7d94df4aebbdb662a916a8029259d9db4acd15f7816d6c5b1aa6052730828a`

```dockerfile
```

-	Layers:
	-	`sha256:3dee7c14a7b5d747c19e1a6f65e3712ff838833abb7dd355278afca6d27ce5aa`  
		Last Modified: Fri, 31 Jan 2025 01:32:29 GMT  
		Size: 3.2 MB (3220878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4605ed4a3fa1df386d7f02c8206881b226181c6758942fb0b250c8075a71e0c5`  
		Last Modified: Fri, 31 Jan 2025 01:32:29 GMT  
		Size: 24.4 KB (24438 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:cd3b1f83b73022f7f28b3ca867c0f7e8ff226f4e9316ce4c623779b013ad3060
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2870006072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab245a301ed76a8db990da7208a24b6873984f25bf1ec17ff06f0a499c7dd441`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 01:33:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:34:00 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 01:34:26 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:34:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:34:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b5891c17be17045d0755c0ab570b1d03ead2d2b748cd98581cd098b53947d8`  
		Last Modified: Fri, 31 Jan 2025 01:34:39 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea4d6727407f9ca4ac1c9fe1ed405da6896c0f837f519b9fe003e4ba09de4f6`  
		Last Modified: Fri, 31 Jan 2025 01:34:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d33068f766f905f11e36dfdab41d20a7a707836fb188dc0687386d842ac8136`  
		Last Modified: Fri, 31 Jan 2025 01:34:56 GMT  
		Size: 369.3 MB (369330504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1386db4246fbd6efa3bd5eb3b3855c59be7c9f80669edd808788bf0e028142d3`  
		Last Modified: Fri, 31 Jan 2025 01:34:39 GMT  
		Size: 394.0 KB (394010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b4606d079e4fc5053d4dfc60b7cdf4d76fb1457ea0364c9c99abeef97b2276`  
		Last Modified: Fri, 31 Jan 2025 01:34:39 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:762017571016d50a605feb792b4579194a96bc2f3a54679dbbc797dba30996e0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2632051578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684ef2b9ef164dfbab291b9f931e2606a72ae15ab2060aa699e45dcee71f55a4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 02:12:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 02:12:13 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 02:12:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 02:13:01 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 02:13:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5eff04532649c1cc24a7a1a077ef832362bd7bad25840a148def2b710d7aa51`  
		Last Modified: Fri, 31 Jan 2025 02:13:05 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b4b08b2f379d50ad034f14cd7e51e436414cb2a6cd7f8df494e69c3734d89e`  
		Last Modified: Fri, 31 Jan 2025 02:13:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc026f9cc8bd26d6b37bbc404deb6c7fe811828d768ea99927a4d8497ff59a29`  
		Last Modified: Fri, 31 Jan 2025 02:13:19 GMT  
		Size: 369.3 MB (369302403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edebfdfab99905a0941cfc03a1e23891ad78a6ec8a390785bac218ba8045e07`  
		Last Modified: Fri, 31 Jan 2025 02:13:05 GMT  
		Size: 360.1 KB (360080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82ac20a053be9e02c5cacfcaa80d78212b5564875b06680e02ab43850b70568`  
		Last Modified: Fri, 31 Jan 2025 02:13:05 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:ebf8d00b357039c8fc43c75068b03e18a7de1732cf9559cb976606cb1efc7c52
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2491827092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2191ba38c6c4cacec8327fc670416d92f558d88bf7aae776ab2613ef1f335b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:29:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:29:30 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 01:31:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_windows_hotspot_11.0.26_4.msi ;     Write-Host ('Verifying sha256 (25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '25bc11bd05e4dad95ebefde017bd5eb29dfe8624bbd46beeca8eba4b4d77fae1') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:31:31 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:31:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3305b3f827ea5e312c439de2ae9d84cda279b0e91e211e6697db135682d19f42`  
		Last Modified: Fri, 31 Jan 2025 01:31:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121df579b621f652c96072468f80a74e8f6561726330a0609d18c56420540b58`  
		Last Modified: Fri, 31 Jan 2025 01:31:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4128024d0f04d6000b81408b46385283b924cd8e1cdfa881203b66da4a398e0a`  
		Last Modified: Fri, 31 Jan 2025 01:31:48 GMT  
		Size: 369.3 MB (369296952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fef4e1c51b0709b2735694f338efa7fa97d222884acf3f51879ad9d33fa9544`  
		Last Modified: Fri, 31 Jan 2025 01:31:35 GMT  
		Size: 314.1 KB (314084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562f1ad69ed045f232d4b3458f07815d0e52ac4f3c0e186243e5076d9c415ae`  
		Last Modified: Fri, 31 Jan 2025 01:31:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
