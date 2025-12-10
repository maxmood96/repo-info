## `tomee:10-jre17-Temurin-microprofile`

```console
$ docker pull tomee@sha256:92d54c8a952326dafcb2d368dff8bf6999003ff9e7625612e3a5f944153f26ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre17-Temurin-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:c627d55bd8bf339e50f99ba2018eac1f19566eff83a2091a960bc36d0f8184c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164276349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a84e9112cf3c35893e29ccea826946e81f4c6a8d1421fbedecab661c1a4219`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:38 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:45:41 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:45:41 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Fri, 14 Nov 2025 00:45:41 GMT
WORKDIR /usr/local/tomee
# Fri, 14 Nov 2025 00:45:45 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:45:55 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 14 Nov 2025 00:45:55 GMT
ENV TOMEE_VER=10.1.2
# Fri, 14 Nov 2025 00:45:55 GMT
ENV TOMEE_BUILD=microprofile
# Fri, 14 Nov 2025 00:45:56 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 14 Nov 2025 00:45:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 00:45:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12c659f8ac16f8d9fc5114f9b2bbc77d6367df6b5f9070ec314a45711853b3a`  
		Last Modified: Thu, 13 Nov 2025 23:22:00 GMT  
		Size: 17.0 MB (16972143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1e0321681ccbedcbfd0d195ec926ba8b1fb3ac6881aedeb6107b5d2dfa3f28`  
		Last Modified: Thu, 13 Nov 2025 23:22:04 GMT  
		Size: 47.1 MB (47055469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469f7f46f06bf8f05ffa00c679b9cfed78488d3273e4ad9a245a063d965a2083`  
		Last Modified: Thu, 13 Nov 2025 23:21:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Thu, 13 Nov 2025 23:21:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7322b19a1dd5dadfbd4531b1b7d6248f90f38c4471771e8d8a7c3e21a5e362f2`  
		Last Modified: Fri, 14 Nov 2025 00:46:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fea5cd96044a1c3a65088caea7a1b97f42185975d8ae1a1d40fe5c172a8a4ca`  
		Last Modified: Fri, 14 Nov 2025 00:46:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc808e4839217afa1e9baef04a7b07231cf52922de23399ad8d9371d3c4672a1`  
		Last Modified: Fri, 14 Nov 2025 00:46:14 GMT  
		Size: 75.6 KB (75630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e9218aed9ef72849bacdab7e3c531cf44c6bdaabb04aa846f5809f3bafb7b3`  
		Last Modified: Fri, 14 Nov 2025 00:46:19 GMT  
		Size: 70.4 MB (70445276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-Temurin-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:8bb030797c20b5543893c73c9f436905d939bb7ee4785667271dfbb5e3f0e606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3712101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f9a4b6efdd948f34e4a8b88ea76ecda51c2c3b9556a9364ef9899d2375133d`

```dockerfile
```

-	Layers:
	-	`sha256:8ef36e686fe8b868c25e7d9c1a9bcfe22f6866e1d4170593fc9f147fe257ed7e`  
		Last Modified: Fri, 14 Nov 2025 02:13:43 GMT  
		Size: 3.7 MB (3676337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5607154d15e7b7bed639daa692a019b4e05d8ca0b0d279cc00bb5c2da18922d5`  
		Last Modified: Fri, 14 Nov 2025 02:13:44 GMT  
		Size: 35.8 KB (35764 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre17-Temurin-microprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:5a959faa53277c591e968de1b281dbfd81e2e08abce5228f3e758754c090475a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162913442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4b609d778bf78a00709e6c6676c741cf766693949994a60b7c1b9b0bfea53c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:17 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:47:43 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:47:43 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Fri, 14 Nov 2025 00:47:43 GMT
WORKDIR /usr/local/tomee
# Fri, 14 Nov 2025 00:47:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:47:58 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 14 Nov 2025 00:47:58 GMT
ENV TOMEE_VER=10.1.2
# Fri, 14 Nov 2025 00:47:58 GMT
ENV TOMEE_BUILD=microprofile
# Fri, 14 Nov 2025 00:48:00 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 14 Nov 2025 00:48:00 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 00:48:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f217617b8adc8e338c40dc9cbb2fb089ae4ae063ca4eb78bf0dfc9d762cafc`  
		Last Modified: Thu, 13 Nov 2025 23:21:40 GMT  
		Size: 17.0 MB (16989109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae42f591e3344a684d2b9ff93f75c9f6662804c81d6d39e86bc6c9210e560cf6`  
		Last Modified: Thu, 13 Nov 2025 23:21:43 GMT  
		Size: 46.5 MB (46538289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf53f68aed0c96936c4fce1a47200aa8f99f2894c8171c7f1bee9996efa7f442`  
		Last Modified: Thu, 13 Nov 2025 23:21:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95530a3b2040ac287e294550a0badaa71a7759a355f6026f419c3f6880121ea`  
		Last Modified: Thu, 13 Nov 2025 23:21:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3304850b9e6693ef19eb1386bf34164488ff2b57416471f1dea61e0717091d`  
		Last Modified: Fri, 14 Nov 2025 00:48:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be88792c536d80ef7840e2345c26b02fefd4620627ba9ef66481128c7fb883ec`  
		Last Modified: Fri, 14 Nov 2025 00:48:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaff0f178e601a54081f7d55579806d3dad9f3c79c5828ac9379293cd211265`  
		Last Modified: Fri, 14 Nov 2025 00:48:19 GMT  
		Size: 75.7 KB (75663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef78ef166ed76757b4e61f4796148a0120ea8d25cab903dfa4a1902e3a36b0ca`  
		Last Modified: Fri, 14 Nov 2025 00:48:35 GMT  
		Size: 70.4 MB (70445283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre17-Temurin-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:b939ac58a79b98b80eeff3e5812aecb67153c640bfee1ed785a064c4cd864244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d3050be68d860d2007aee8fecaeee80af2281a78bfdaa9b545c904400c86c5`

```dockerfile
```

-	Layers:
	-	`sha256:d6c0b02150731cf36d0d6ebb46c38b417fbd1ab7cde39f6db145798b340fb43a`  
		Last Modified: Fri, 14 Nov 2025 02:13:48 GMT  
		Size: 3.7 MB (3677144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a40e867cb21f96a93f27e3886871b1aeb6df823103cc70948b9b1c33e26e6d`  
		Last Modified: Fri, 14 Nov 2025 02:13:49 GMT  
		Size: 36.2 KB (36249 bytes)  
		MIME: application/vnd.in-toto+json
