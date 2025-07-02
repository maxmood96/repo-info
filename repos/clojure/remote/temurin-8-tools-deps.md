## `clojure:temurin-8-tools-deps`

```console
$ docker pull clojure@sha256:c1f555e3ca8c86ac3a0be8e158f03272fed85caaff01e136398f7a7bc0c821d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:312ca7196fd8b273b1ca7df2056287276ba2db5e277d08f45431ccdf5f032c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156394151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a03074603eea9b82485cb9c5d7b335c7919eb8d3d475d92e3ac0bed811dc8b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
ARG RELEASE
# Sun, 27 Apr 2025 20:21:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 27 Apr 2025 20:21:59 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0ef7185ad48c9e66bbe8746a80b3821af33f732c0495dcdd7f939446cd0f79`  
		Last Modified: Wed, 02 Jul 2025 03:10:15 GMT  
		Size: 17.0 MB (16969475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c264db84a642aa0bc9f5d769ec9cf673dae329419018871364079538557c8`  
		Last Modified: Wed, 02 Jul 2025 03:10:22 GMT  
		Size: 54.7 MB (54721298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a735d85a95a558802cb348c4655a6c02e2d912f77f11bca4bdf8275bbd853c0`  
		Last Modified: Wed, 02 Jul 2025 03:10:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf2cb0c37e19485ea23c46d6248f2c7bf4e87faf58cec260525877c593f5cee`  
		Last Modified: Wed, 02 Jul 2025 03:10:14 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6503ca94cb1a642f3f3516fe9c95369f39a1b3bf9fc7cc029b50b682153d49`  
		Last Modified: Wed, 02 Jul 2025 13:37:56 GMT  
		Size: 55.0 MB (54981933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da7fe130ae4d793eaed49fcf826293254a09b3184297045c39182d9ee719af9`  
		Last Modified: Wed, 02 Jul 2025 13:38:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:a67df1b8a0e2ba8f0cd745a9e1f6ac7283f3c1ec8662f8b096c91308cdcc4544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4435af0c0a027dba2aec24fca352dd8cb56d9e834cb87d46cb0838e15a056d`

```dockerfile
```

-	Layers:
	-	`sha256:e9769af3e5b67b3758eae4263531c51f96f86693a85978770aca80685d331927`  
		Last Modified: Wed, 02 Jul 2025 06:43:54 GMT  
		Size: 5.9 MB (5874082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d72ecaade4b09afb6ca13cc8e2509ef18b2eb25ebdfcfbd885d48e32ccacc908`  
		Last Modified: Wed, 02 Jul 2025 06:43:55 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6cd8a11958796c3dbe37c1436249c0fabce178b6e2a1cf02c0d1971d53a7df7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154606577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605c239a6cb250180758b375c555c6a0128a1f9d1920dee5efca2385fe6ed1fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
ARG RELEASE
# Sun, 27 Apr 2025 20:21:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 27 Apr 2025 20:21:59 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2fa422bbd08bc40d85a4e1666805f0d0f323a1834f9494578f07cf2106f303`  
		Last Modified: Wed, 02 Jul 2025 05:07:14 GMT  
		Size: 17.0 MB (16988217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cf8f9739e678c55dfee40848da6b5cf8307a23110a25ac56c132a77b569c56`  
		Last Modified: Wed, 02 Jul 2025 05:07:17 GMT  
		Size: 53.8 MB (53833603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74e8838b3a5fba1babe19bc4205d62b0c7d3392e2e277492526f2598b0c3b0f`  
		Last Modified: Wed, 02 Jul 2025 05:07:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99056e46db9433900d26afad2977085896bba43d226175ba18fa12e8c981d48f`  
		Last Modified: Wed, 02 Jul 2025 05:07:11 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aecc9969229dbe88cc263ac7887123b29e6569b19d389e0aa095173dc9ebb56`  
		Last Modified: Wed, 02 Jul 2025 12:14:29 GMT  
		Size: 54.9 MB (54925657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a688f442b9c05f55ca6dd44739ce1dff139c8a3abd9228507e026cecd89e6301`  
		Last Modified: Wed, 02 Jul 2025 12:14:25 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:38d4b1faeb824fb605bfc42bf22b8537b85b69d21eab8ad29813821712073982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531161e2397de255334ae2a56cbf507e5b5d74158ab7d4c05a3ece1e2caed344`

```dockerfile
```

-	Layers:
	-	`sha256:bde9c48bb6a60c4c2ca7e90f6377bce7518e158a75b5e97b2dd237c8e9191bb2`  
		Last Modified: Wed, 02 Jul 2025 15:45:11 GMT  
		Size: 5.9 MB (5881368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac824c016cd64245d6114a3b9d3d45a4b72e96550b2191bf37c89329df0e725`  
		Last Modified: Wed, 02 Jul 2025 15:45:12 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:c94348be5da02eba87be5a6cd20231f25ef86f6d82a9d0a6070560a2d568ea99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164904212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fbb50782e7108c8e049abdb67aeb3ac09d786ee31b37677fda9418c38cf330`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
ARG RELEASE
# Sun, 27 Apr 2025 20:21:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 27 Apr 2025 20:21:59 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0111803c0bfac8b5cf9f7f497b1d1327406384bede031585f6063cf0af7d1a63`  
		Last Modified: Wed, 02 Jul 2025 03:16:25 GMT  
		Size: 18.8 MB (18817031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d50646a76dd92c07f18982f5fad0b486dada1acac114dcd360fe451486b02`  
		Last Modified: Wed, 02 Jul 2025 03:16:27 GMT  
		Size: 52.2 MB (52168866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b29d32b0df2fc06d6b685a2e7342a569dd558ae832aebb92e9f65fe2ef662e5`  
		Last Modified: Wed, 02 Jul 2025 03:16:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfba87881a59d17ac46a8d4d993bf919cf127f4d3c3afbb9125f67bb8641719`  
		Last Modified: Wed, 02 Jul 2025 03:16:24 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219e3563cbee787fa4d9f667191f1856d2ff001a1055adbd5e9c57e91494524a`  
		Last Modified: Wed, 02 Jul 2025 10:04:50 GMT  
		Size: 59.6 MB (59593729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3209ddb96113112db4b13e1d93188cb518475b558abdda824eed0240fac4d6`  
		Last Modified: Wed, 02 Jul 2025 10:04:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:ec412537903633cd9df561f2c20cc61b47926fbee1d6f96f3c31b855094aaa79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5894185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd7340de7083bf837aaa522c90d99e7e7ea89144888003844d96e11199238f5`

```dockerfile
```

-	Layers:
	-	`sha256:93b08fa7cf03663848a0187bad1e7b877f8527c109b62790ca22ed9c4426bc55`  
		Last Modified: Wed, 02 Jul 2025 12:42:35 GMT  
		Size: 5.9 MB (5879920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:395b011f35d0a0cfca1829deb4b0f3c14de91d738bc0045d234921c5dbb8f5ec`  
		Last Modified: Wed, 02 Jul 2025 12:42:35 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json
