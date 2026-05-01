## `tomee:10-jre25-ubuntu-plus`

```console
$ docker pull tomee@sha256:0d8c84f9e7b9226a0b5db4f12e161a8e3b9d587740cba3ec4d2853c6af5f6107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre25-ubuntu-plus` - linux; amd64

```console
$ docker pull tomee@sha256:70deebf086428adf70c15cbe5bd80ac0d46bfde372526b058daaf690c067ed20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183830652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbddb017ff1116a7c9f4e982f29f30b598438c1193bc2c6097dfb9be159846c6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:33 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:52:09 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:09 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 30 Apr 2026 23:52:09 GMT
WORKDIR /usr/local/tomee
# Thu, 30 Apr 2026 23:52:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent curl   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
ENV TOMEE_VER=10.1.4
# Thu, 30 Apr 2026 23:52:26 GMT
ENV TOMEE_BUILD=plus
# Thu, 30 Apr 2026 23:52:27 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 30 Apr 2026 23:52:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:52:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191a1bea837eca9a44b1c34ab4dd5a859fb2c2f0730259b2a733a608ea883bd6`  
		Last Modified: Thu, 30 Apr 2026 23:30:05 GMT  
		Size: 11.5 MB (11479095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe21702fcd1c69c16d0bd83f87aff92266d210ea37d3d040493acf85ac4a62`  
		Last Modified: Thu, 30 Apr 2026 23:30:07 GMT  
		Size: 63.0 MB (63042478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c999e71703cb09c68bab49067fa8d026dc8370282f6135990ac69b0ccb16b37`  
		Last Modified: Thu, 30 Apr 2026 23:30:05 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467175a5526315e383a7c869c5ea31f1aea4e75743e0e3eead71da0325f4852e`  
		Last Modified: Thu, 30 Apr 2026 23:52:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f54c9223cca61f63b65c170b396bcfb0d35bf00ed6b3050a9f31332db2c92f5`  
		Last Modified: Thu, 30 Apr 2026 23:52:39 GMT  
		Size: 4.5 MB (4481051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d706e7f4a47c0a338814ed7cf1367e08199a563c357bcd554e9068eefddd44`  
		Last Modified: Thu, 30 Apr 2026 23:52:38 GMT  
		Size: 75.7 KB (75654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bbb4d100924df7afadb812c2d251341e0f4ad6d499f28c3d163a7d7f788519`  
		Last Modified: Thu, 30 Apr 2026 23:52:40 GMT  
		Size: 75.0 MB (75016875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-ubuntu-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:6e905635cbba0b37ef88cc8158b2f4f59727fb46e1718ea8f9a7bd21e2ac3457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3683671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b924d5e05a554010b88b9f68b8f9ab684bc0ea672d402943e0314684aaebb79d`

```dockerfile
```

-	Layers:
	-	`sha256:1418f531953256adafe76d8775cff0be68e99eacae866bcb69c7563dcd404221`  
		Last Modified: Thu, 30 Apr 2026 23:52:38 GMT  
		Size: 3.6 MB (3648220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd5a4dd23d410e60e8ab6d913cb3dfd3f7ee8603f93c15c042044a7cdbc7e5a`  
		Last Modified: Thu, 30 Apr 2026 23:52:38 GMT  
		Size: 35.5 KB (35451 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre25-ubuntu-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:96d9bd7c93112cfcb1670974f08c4e9690e3270617eb2df93ef4006f4ec9e67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181892398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e688f620d78397a6964e5b0f6dbda7b3af0c85dba6b65dc28ce35cb6f4c2a7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:38 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:30:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:30:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:30:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:30:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:51:49 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:51:49 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 30 Apr 2026 23:51:49 GMT
WORKDIR /usr/local/tomee
# Thu, 30 Apr 2026 23:52:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent curl   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:52:10 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 30 Apr 2026 23:52:10 GMT
ENV TOMEE_VER=10.1.4
# Thu, 30 Apr 2026 23:52:10 GMT
ENV TOMEE_BUILD=plus
# Thu, 30 Apr 2026 23:52:17 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 30 Apr 2026 23:52:17 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Apr 2026 23:52:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b502206b1d693f9f65c15a390ab1af25442fef8155a462be7ff05ca7d3e8c7`  
		Last Modified: Thu, 30 Apr 2026 23:30:19 GMT  
		Size: 11.5 MB (11474371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575f27cf1d92903883bac4bec927051337774783b6eaeb93ccc0fbd2a6449c9a`  
		Last Modified: Thu, 30 Apr 2026 23:30:20 GMT  
		Size: 61.9 MB (61943078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd4dab533194e1c28ff921fa8c55c5e3a28c8fe780c0aad21a1b08ddbb34cf4`  
		Last Modified: Thu, 30 Apr 2026 23:30:18 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a07ee2b4ec95e8a8f6700164b84f6a4c71275c4d27bd37243d3ec167a0780b`  
		Last Modified: Thu, 30 Apr 2026 23:52:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfc9db416c672c80fcfc7de81d54fd45dd6a311899cc199a9afed8cc97d2310`  
		Last Modified: Thu, 30 Apr 2026 23:52:28 GMT  
		Size: 4.5 MB (4504090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade894cf5b3e9bb9afc2db485624676a524ac1b7ebaeb7c0452e6473d7737485`  
		Last Modified: Thu, 30 Apr 2026 23:52:28 GMT  
		Size: 75.7 KB (75666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e106d6ff5e654f90ba631b69b248c6ce25b17b54ec14571c21cb9f2997d7448`  
		Last Modified: Thu, 30 Apr 2026 23:52:30 GMT  
		Size: 75.0 MB (75016890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-ubuntu-plus` - unknown; unknown

```console
$ docker pull tomee@sha256:ecc6d449e2a3f9445cf62139e68ab3317ff2a2f5e440d47da900bdffa3b97a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d80a6c288a33ca5bb15f8d7c5d29d61edafba75c70f84fce89626ea25aeb25`

```dockerfile
```

-	Layers:
	-	`sha256:606bd76c37ed677f2e23bfb6231eb948dba0dd2372e912388f26798ad6da9246`  
		Last Modified: Thu, 30 Apr 2026 23:52:28 GMT  
		Size: 3.6 MB (3649024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9203ecc647423f5c037d899e973b1a1f53fb25133dfda770ca939c7764a79048`  
		Last Modified: Thu, 30 Apr 2026 23:52:28 GMT  
		Size: 35.9 KB (35936 bytes)  
		MIME: application/vnd.in-toto+json
