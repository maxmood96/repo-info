## `tomee:jre21-ubuntu-microprofile`

```console
$ docker pull tomee@sha256:422eab1208ba6bdccf85829ca0c59b309585053f2d05ee18305b90f2feb69c5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre21-ubuntu-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:66a5186b0d1d4a5b7b0df935699e180a12729ec562b67fdec2441dd76e1527e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170187785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27d24c637b539a229b736e45adef2ede13802d5519c8d7732294495bf88c1dc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 05 Oct 2025 18:19:29 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 05 Oct 2025 18:19:29 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
WORKDIR /usr/local/tomee
# Sun, 05 Oct 2025 18:19:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_VER=10.1.2
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_BUILD=microprofile
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 05 Oct 2025 18:19:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f38e2e092670ef283f8cef3be87ca664b534a953c460e93cfc9ffeebbc8224`  
		Last Modified: Thu, 09 Oct 2025 21:13:36 GMT  
		Size: 17.0 MB (16971757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c474f64746d27f2879d262f6299fbbf510deb0689105ba567ba62c6760583d3`  
		Last Modified: Thu, 09 Oct 2025 21:14:09 GMT  
		Size: 53.0 MB (52968909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e9704d175f236f24573f3263c46c98ce312c06751ec7feb8aa18adda6c39e`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2326993b9fe603f4efecedec459c92a6f5cbddca94dc55593db837055ac2e4e8`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe75e68ee2923a6642a9ee7e67eb74177c07814e19f219ad0aa1b9861cfa79d`  
		Last Modified: Thu, 09 Oct 2025 22:25:03 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca89ba5358f395fd80801110ce97d7a79eceb04324936533bba38fda14ea283d`  
		Last Modified: Thu, 09 Oct 2025 22:25:03 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156940b88e66e6ef6f373f33ce0ca246dd0e188b7168af2a6a94162529d9866e`  
		Last Modified: Thu, 09 Oct 2025 22:25:01 GMT  
		Size: 75.6 KB (75629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca5ff15824d33063ed697ffd3f0cd9e6e87b360af03249e4388dd9a7741699`  
		Last Modified: Thu, 09 Oct 2025 22:25:09 GMT  
		Size: 70.4 MB (70445202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-ubuntu-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:062042e3e71f97d771b0c15cbdff27818c4cfc3528b2ed0d33596cabc52ea2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3090cca82b1d7b7581f0ae3948aa7dcb23d53db9b6bcab8bc0e22c79b6364ce9`

```dockerfile
```

-	Layers:
	-	`sha256:7e0a169eb07576767054a7448da0e621de4723f69f8a29591c32ba363cb3691a`  
		Last Modified: Fri, 10 Oct 2025 04:13:35 GMT  
		Size: 3.7 MB (3678833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751153c975990089ca1140bb0908166744035acee36450cb5d7c955202ef046a`  
		Last Modified: Fri, 10 Oct 2025 04:13:36 GMT  
		Size: 35.8 KB (35798 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre21-ubuntu-microprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:360d34473c146adef0108d64c857b72330561b6a3dbecce2858f98c6c93246f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168523377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fbf835275c17e6c6dd9923c9002233d87422317d4c6938d7433043282f897c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Fri, 01 Aug 2025 11:04:34 GMT
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 05 Oct 2025 18:19:29 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 05 Oct 2025 18:19:29 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
WORKDIR /usr/local/tomee
# Sun, 05 Oct 2025 18:19:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_VER=10.1.2
# Sun, 05 Oct 2025 18:19:29 GMT
ENV TOMEE_BUILD=microprofile
# Sun, 05 Oct 2025 18:19:29 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Sun, 05 Oct 2025 18:19:29 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 05 Oct 2025 18:19:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf670432170ff54aa7d7fec54b27ad51dc4b767bc00a3178b28176173ef130c`  
		Last Modified: Thu, 09 Oct 2025 21:14:24 GMT  
		Size: 17.0 MB (16989173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d3072b7ee41b26a0c52ffc0714ce586e836d00c7f9936e7f5c4219d8993682`  
		Last Modified: Thu, 09 Oct 2025 21:15:03 GMT  
		Size: 52.1 MB (52148484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd18b9ed8f5e6430b2e5b01ce34688a7c375b5a5ab76ed710e24a610e354cc1e`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452d8b8a38c043118d3c800c54e6273302aa0642a20b0df0f628b8d0e8866ce`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75a81caa57dc204b7fa7f92818e3d422efc70e08362d4c62cfff68af3fcea34`  
		Last Modified: Thu, 09 Oct 2025 22:25:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0687cff3cffd96602623f64725ff3bd95305945b2dc442bbb7db358d3f8d78e0`  
		Last Modified: Thu, 09 Oct 2025 22:25:11 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683d31b44317b90e0dafb9aa4e964f333c73a56beef6add47934b91e35c2b51a`  
		Last Modified: Thu, 09 Oct 2025 22:25:11 GMT  
		Size: 75.6 KB (75641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab0da3b56c429a4bbe706a3d34a629c12bd1c102bcd5da869beebc8577962cb`  
		Last Modified: Thu, 09 Oct 2025 22:25:16 GMT  
		Size: 70.4 MB (70445228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre21-ubuntu-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:e65dbe418c5f56ac2da84a441e28e902333ede1415e1452014dfe467fdc38abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a77983f04e3da341156f85a926c24c7bdb25207939d405d6167524f96fe4ff`

```dockerfile
```

-	Layers:
	-	`sha256:5c944bdf67414756a465ef0ffdde2001b7ed2d4944088f55bcd5fdd012be7952`  
		Last Modified: Fri, 10 Oct 2025 04:13:42 GMT  
		Size: 3.7 MB (3679640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab17769852f485e2f8c4ffcdf943da81e070feebc744ecc1cc8b75eee789aca8`  
		Last Modified: Fri, 10 Oct 2025 04:13:43 GMT  
		Size: 36.3 KB (36284 bytes)  
		MIME: application/vnd.in-toto+json
