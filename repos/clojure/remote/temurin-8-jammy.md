## `clojure:temurin-8-jammy`

```console
$ docker pull clojure@sha256:af0b493446e2f5f0f2776d500d6822fcb3b2c011f1e690efc0cfd3ff16f9a318
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:4a9edfb3833115e9224f10b5ed4426f681e07736684394bf6f95fbd8ae2c2067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152235950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e6e76b6f268f3265670145b41574ceb9734635a2bf6920d24089486d5d9a8b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:47 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 17 Feb 2026 20:18:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 17 Feb 2026 20:18:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:18:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:18:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 19:45:26 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:26 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:45:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d575991a97516fe461d4e4036a37490052a3d42ec380135d014249e16b1d678`  
		Last Modified: Tue, 17 Feb 2026 20:19:05 GMT  
		Size: 16.1 MB (16147788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0b973da87013b4caa78560f8706f4fcbdd328d7074ecdfa3390ab544161c0`  
		Last Modified: Tue, 17 Feb 2026 20:19:06 GMT  
		Size: 55.2 MB (55172963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d04e9b76c9330773ad34e27f2ffd784cd5c7f803429c3e33b076dabc1eaa92`  
		Last Modified: Tue, 17 Feb 2026 20:19:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb62655189e57181dc9e9917aeadb642b3c3f71685e790a6d97c4b694ded9b`  
		Last Modified: Tue, 17 Feb 2026 20:19:01 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856b62ea0173873a30a69b902dd4ceb37a851491ba179b7190072eaeb37de517`  
		Last Modified: Mon, 02 Mar 2026 19:45:55 GMT  
		Size: 51.4 MB (51374750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2410d3e4928cab5eaeb67e5b0205d73e7f8e881035cb5910fb4c65ba191bdf82`  
		Last Modified: Mon, 02 Mar 2026 19:45:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:cf8e39069733b2d903b7cc42ec1f59be3386380cf7dd105d920198b48b8b3a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6437955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d305aa8fc93e15904b451e099e1f698d6aaea787fe6b7d4495d3c520fa1558`

```dockerfile
```

-	Layers:
	-	`sha256:e60c4867061fbf603d9fb9981346d419a0ee35a7b1e20db432c8e829594ec8d8`  
		Last Modified: Mon, 02 Mar 2026 19:45:54 GMT  
		Size: 6.4 MB (6424463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6fa348a9e98129977ddb7e2c33563f118d9383f4ffade676cd02888ebcf89e`  
		Last Modified: Mon, 02 Mar 2026 19:45:54 GMT  
		Size: 13.5 KB (13492 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:493c94591b9a8b6f4fba2fbd79c7a31a13c31b0094d56a307678d73bb65a4456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149088433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98056cacc447aa7350cc5c102cfa1f9106958fba519bf3bb0173dedc90329b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:05 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 17 Feb 2026 20:18:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 17 Feb 2026 20:18:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:18:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:18:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 19:45:07 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:07 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:45:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7806d17e9ea35546ce7f8897d9eb3e563c896a4d457aa7bd483c75d5752d42d5`  
		Last Modified: Tue, 17 Feb 2026 20:18:22 GMT  
		Size: 16.1 MB (16072810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac19c4a6790d9064fd08710d03b9d92f2329665fd30116701752164d394bf11`  
		Last Modified: Tue, 17 Feb 2026 20:18:23 GMT  
		Size: 54.3 MB (54261211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e07cc29f914c855e86aadf03859379c5a794b411f5bc729de7f7783962f348`  
		Last Modified: Tue, 17 Feb 2026 20:18:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc732f08a4245616d1b8635415f6bd65f861ae777b581ca362a8731f3c9eeca`  
		Last Modified: Tue, 17 Feb 2026 20:18:22 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94a90993be3499d73ffdca5595de67f189746c00bdfc615dfbebbbcfcc54229`  
		Last Modified: Mon, 02 Mar 2026 19:45:40 GMT  
		Size: 51.4 MB (51366384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef7b369ca4b3ce23668d42cc503f2719b35a4be51042aeab8cdcee44841093`  
		Last Modified: Mon, 02 Mar 2026 19:45:39 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:87e826c897899385bae3886512191e3c9b4437e8b7321838adc647b20fff00cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27197e30831ef9c76bd6140553849f1298cf368b9d1b11e47a6d19af12114712`

```dockerfile
```

-	Layers:
	-	`sha256:00e899c688846d2b45a3b2d8fe761d9431a8d039fb49d8d28c6501032a425199`  
		Last Modified: Mon, 02 Mar 2026 19:45:39 GMT  
		Size: 6.4 MB (6430929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e3ab143ec2b1778250e35adc8789ee89ebd81e79ed38f04251f766b08028896`  
		Last Modified: Mon, 02 Mar 2026 19:45:39 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:ed655da26c266e83f6370b2360ac3919211a07e7816d2d4d1ca7795a5c37eb62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160166762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768ec3f947b356809db95fee15b741e7ad07bd853be7687374f148e02bf9a983`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:12:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:12:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 17 Feb 2026 20:12:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 17 Feb 2026 20:12:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:12:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 19:46:47 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:47 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Mon, 02 Mar 2026 19:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09208b6847dfa6f5490506d2bee63693e328ebe8d9f225275578ecadc7fc35c0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 17.6 MB (17619110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710143c7ff3d51a339d8cd69e9b5b3fd38d2ece1427d22b48b97861e5d3f43a1`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 52.7 MB (52652143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb68859ee7db699eb2c5aec8b18157074688404a6bb734cc0ad343f36716850`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad4f2a3068a410a64aec02aa86a654b4b55dabf17d17f79144ae5070446671f`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6a80f8baaccebbee33cf8aed62c3cc5f192ce9fb8f5481eb7b7a9faa2270d3`  
		Last Modified: Mon, 02 Mar 2026 19:48:32 GMT  
		Size: 55.4 MB (55446327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fc6499aeb0163d0cf7f8a35b74fccac5a2361bd21b4c01d599933dca4e1ec8`  
		Last Modified: Mon, 02 Mar 2026 19:48:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:630b34ad7cdaa0400e3d1ad8aaa4ca925430f0ca4ab1ae6990e2b6bcde2df39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6443811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1985ab8c1c92d5acc19cd436427699cb5a811398e5d5b35127bbb778fcabf0`

```dockerfile
```

-	Layers:
	-	`sha256:c6446b88bb92c41d0e18f107183cdd02416fd8821bff1223b7bffdd60f066c7c`  
		Last Modified: Mon, 02 Mar 2026 19:48:30 GMT  
		Size: 6.4 MB (6430281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c8cb8b64fc8da6a8a96e05d681be6e6ab87e56b22b1799e5eb458624aa7b036`  
		Last Modified: Mon, 02 Mar 2026 19:48:29 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json
