## `eclipse-temurin:8-jdk`

```console
$ docker pull eclipse-temurin@sha256:3b1808f3745f1bbbb3611a4f774a0a8940af9de318f1d725e49e2ea8fbc176e6
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
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:8-jdk` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:8b9f3b9e66100c7bc8b2cbd7eddb1cc37190d2648555e2e2eac23a754437bf69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101411571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8018bec3aa51310a87e9f8f017aa2816f3f22bf44f81898486c9e146855e08ab`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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

### `eclipse-temurin:8-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b3b695ea2fc854e9b94341667851fb81e5ece994ed332eab09782b8ac300dabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3515123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465701e4498b5d8fdcc1d275261ba6058497de8c07b7069d2ddbbee20cd09dbd`

```dockerfile
```

-	Layers:
	-	`sha256:a8a4125297eeddb0c08ab83ef95321f121f0e907dd259a8e9ed0b0ee4d60a244`  
		Last Modified: Wed, 02 Jul 2025 06:18:24 GMT  
		Size: 3.5 MB (3491700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab6c4a79686811e4ba259add47420937b206846f8d5b5ff3e0b6ba4fd3ce709`  
		Last Modified: Wed, 02 Jul 2025 06:18:25 GMT  
		Size: 23.4 KB (23423 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:bd48771887232110aae3a8263dcaddf663371752b36f6bcf7d56f24208baddf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93269363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418b64e4dc3da7dd981a74644917aae75073d2c17482ec7dd123ba73695e025f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ADD file:88b7ca184cec1707b10b6b543ddfa7abfcacc2605cdd5919877294ff5290aa3e in / 
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
```

-	Layers:
	-	`sha256:149362fdfa6e6a5d9f009b896da3be3172c395ba2287b57d4969f3f46e573055`  
		Last Modified: Fri, 20 Jun 2025 10:02:42 GMT  
		Size: 26.8 MB (26844462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87008fd131e34e3e3f4ffd352cf8db54b0e89603b6dc942d3c4f194b46bdfc32`  
		Last Modified: Wed, 02 Jul 2025 10:26:30 GMT  
		Size: 16.3 MB (16304975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833b37eaab93bc620e24cc784d7ac0c5b090ac10744655af91bd611c05b82cf`  
		Last Modified: Wed, 02 Jul 2025 10:26:32 GMT  
		Size: 50.1 MB (50117494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326fd937f1c2481342d99efea0e151a2ccbe995fbc6d39328ef913c99c6e9cd`  
		Last Modified: Wed, 02 Jul 2025 10:26:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a71f02ce012d63b69d3036e12d509b160995eb5d062eaec6a43febbbade595`  
		Last Modified: Wed, 02 Jul 2025 10:26:29 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2652b546bb4a86c3fd2d85f1e23c3187d5e91d49dd56653e87e97afda841294a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6572461e31cb1ad36f0af91267070b32ab1d343e86f96d3ccb9357ef106af0b2`

```dockerfile
```

-	Layers:
	-	`sha256:87488dee10bddaaa50323a79abf7a926b6a1e42d3d5f9c486a7028ba74415c00`  
		Last Modified: Wed, 02 Jul 2025 12:15:55 GMT  
		Size: 3.5 MB (3495698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa637db25519293f3068a23f44021d6f3ebbc2d602b80fa5d357dfeb865d4ff5`  
		Last Modified: Wed, 02 Jul 2025 12:15:56 GMT  
		Size: 23.5 KB (23541 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:0236cb5d99b0003401cdeb18a0548845583c844f2901a0d8a9c8248cdcc6aeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99680272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3351a0fc23ba82f7e71e224d40be79b3827935ae27ef337358c73a29e63b9954`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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

### `eclipse-temurin:8-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e8c4d54437c5f62d3dc46e94f56707abae3803983e391ad4e1f85d32144be6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab00922c0b2c117a8f121bda3865898356bba72ca6a7cf989c941ddb8463a76`

```dockerfile
```

-	Layers:
	-	`sha256:91ef3e59908813fcad9807cbf04f2af184683c3721a88a299070784f6fb7223b`  
		Last Modified: Wed, 02 Jul 2025 06:18:35 GMT  
		Size: 3.5 MB (3492893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd8adfa94be3dc786b9cdff62187c1b266112eca890018f3355578b5e817d67c`  
		Last Modified: Wed, 02 Jul 2025 06:18:35 GMT  
		Size: 23.6 KB (23581 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4e432efce4584e17dd278a72598e94cbe1893705c2511954825eecfeb45f2c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105309835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38415d5a9405fb484159ed27951986d1855196bb979885c4d0c03e585866fb72`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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

### `eclipse-temurin:8-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7f7aa26e8618390aae5f2f55a60e709f1f4531d1cd900b86981f75ac1ab64292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3517938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3df4bd7daba85c08692c706d771ea3a96e900be5a7610ea03f58432df85b06`

```dockerfile
```

-	Layers:
	-	`sha256:07b1e880ae020b02dad28be50e965aace4032989cdea418e51d5aa8d401f22a3`  
		Last Modified: Wed, 02 Jul 2025 06:18:39 GMT  
		Size: 3.5 MB (3494454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e2a0e4623f71200e93e9ca61fd99846c60465a204ab46460ad780bfcc416963`  
		Last Modified: Wed, 02 Jul 2025 06:18:40 GMT  
		Size: 23.5 KB (23484 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:3bfbfc83625c3980ed38c5d0cd991daa3b37e53d03b47ace3ee78f3dc829a535
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3682940135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5875ae7408dc82dff90f35f20110830621945162ea35327108e764d8e7747a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:08:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:01 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 09 Jul 2025 18:09:24 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:09:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c2756b49a5dfe757a8d93034ce5673878fdafcbffe218f253bc179456b4a28`  
		Last Modified: Wed, 09 Jul 2025 19:08:42 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e7776178422716e95ed1d69c25cfcd7d4f7785c65e2d7218423d1a543522d3`  
		Last Modified: Wed, 09 Jul 2025 19:08:44 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5fbb79c72928b6ba7c3921fee5187946c5300e056e7eae411b6abaff233e32`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 191.4 MB (191398803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa399bd281e7a0d1ffacd5c7284d696e564a1c8cf0a7f94b492f719b32d8afdd`  
		Last Modified: Wed, 09 Jul 2025 19:09:10 GMT  
		Size: 365.4 KB (365377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:757e06446a852adf0177a8ad7f750ab8958304f1707edcc76f7a80fa62713f4c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472341471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065511f5196e61492f55ba274720bd91dca584562098d62289f7a86d3faa4b5f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:07:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:07:08 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 09 Jul 2025 18:07:27 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '989f085584ca58701eab2d2b2f5576b7594325f0a6f85572b34586774963c46c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:07:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e968c765ce0196c1c28247aa391c86c9455177d10ca62157f128625a99c313b`  
		Last Modified: Wed, 09 Jul 2025 19:08:16 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354f692f64005cf1e7d201ec94a0ce78d1144944b0fd97447e17e0e4f3ca5f08`  
		Last Modified: Wed, 09 Jul 2025 19:08:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18207b4712584b24c1a8882580e73e6fc2b9c9f4564e85bd28a4f419be66a507`  
		Last Modified: Wed, 09 Jul 2025 19:08:26 GMT  
		Size: 191.4 MB (191377532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30060c0ad934c9ab349ba67def6950f53d140de91ae02f7647dcb5401f7a7c13`  
		Last Modified: Wed, 09 Jul 2025 19:08:17 GMT  
		Size: 357.9 KB (357863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
