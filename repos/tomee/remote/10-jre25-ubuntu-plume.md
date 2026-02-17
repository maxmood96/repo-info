## `tomee:10-jre25-ubuntu-plume`

```console
$ docker pull tomee@sha256:f282c0b70d231d5f9d016bbb593ea5adf7a0de460b3326da9b5f296082110146
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre25-ubuntu-plume` - linux; amd64

```console
$ docker pull tomee@sha256:ac4dc509d7e001f83f24868bd03a0c9665c4470d6b6bd26a2c558cc40bb6b666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191641623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969c8a19fb8cdb2033fdae99864bf259b05c7aa7825f43899a8607857fced24d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:20:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:20:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:20:27 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Feb 2026 20:20:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:20:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:36:59 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:36:59 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Tue, 17 Feb 2026 21:36:59 GMT
WORKDIR /usr/local/tomee
# Tue, 17 Feb 2026 21:37:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent curl   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:37:17 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 17 Feb 2026 21:37:17 GMT
ENV TOMEE_VER=10.1.4
# Tue, 17 Feb 2026 21:37:17 GMT
ENV TOMEE_BUILD=plume
# Tue, 17 Feb 2026 21:37:24 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 17 Feb 2026 21:37:24 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:37:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c455c0f698f7e1cd2c305f426f9306ffd199fdf279d571220d153da681406c51`  
		Last Modified: Tue, 17 Feb 2026 20:20:59 GMT  
		Size: 11.5 MB (11478448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778806e8a80c3539a1b703b2b5d01890828c8c7de74eb541afb571192642807`  
		Last Modified: Tue, 17 Feb 2026 20:21:01 GMT  
		Size: 62.7 MB (62739588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbc60fb7edbd02ff22bc83c9018ed57979fa894f84276db97e2f09ddfb1ab8a`  
		Last Modified: Tue, 17 Feb 2026 20:20:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e56b9cfb49c83795974306277a5e94d98f7706bbb977020bdd0c132d5e3d85`  
		Last Modified: Tue, 17 Feb 2026 21:37:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bade55bcbc284bc761128e57960042744ee1145579da3f7a22d7f57181b4dd`  
		Last Modified: Tue, 17 Feb 2026 21:37:35 GMT  
		Size: 4.5 MB (4479258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78829dcf0abadd190cc6517803a9544a3463d7e083c6ac8016134d37f33d2f09`  
		Last Modified: Tue, 17 Feb 2026 21:37:35 GMT  
		Size: 75.7 KB (75651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329513599d6b867257604a117d1b22fcb7f70954d08d3fa0575e66a30a2b2a6c`  
		Last Modified: Tue, 17 Feb 2026 21:37:37 GMT  
		Size: 83.1 MB (83138547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-ubuntu-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:a764d7c8e741e4ccf131540d1525a529d0e4e4727149b9f86b2c8f13d4b65c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3701970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3330cd56519830081e4275d443a3bffaceb99b5a32c86467ece8427df82500e6`

```dockerfile
```

-	Layers:
	-	`sha256:83c0a74ca8ed6feb64836e757d8cf209057b10e4bd8a03de439a5bcfc677c6a2`  
		Last Modified: Tue, 17 Feb 2026 21:37:35 GMT  
		Size: 3.7 MB (3666448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc2da07dbd3e5254cf5922540e054f6a9050fb6edada3885294829fb3c4bafa`  
		Last Modified: Tue, 17 Feb 2026 21:37:34 GMT  
		Size: 35.5 KB (35522 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre25-ubuntu-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:0be9aa43333cecf890fa2bc91eaf51aebe3b7d579935b0843919f478b8b9c955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 MB (189760977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f982df16f6ca31a0924b27b84b88fc087961df0e13e7b6cfbe13ab60fdc9539`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:19:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:19:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:19:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:19:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:19:59 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Feb 2026 20:20:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:20:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:37:05 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:37:05 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Tue, 17 Feb 2026 21:37:05 GMT
WORKDIR /usr/local/tomee
# Tue, 17 Feb 2026 21:37:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent curl   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:37:26 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 17 Feb 2026 21:37:26 GMT
ENV TOMEE_VER=10.1.4
# Tue, 17 Feb 2026 21:37:26 GMT
ENV TOMEE_BUILD=plume
# Tue, 17 Feb 2026 21:37:28 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 17 Feb 2026 21:37:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:37:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc53e94bca397afe1821661a3a7edf58b275b328d8ee7c799be1e5b6ffc6cf9`  
		Last Modified: Tue, 17 Feb 2026 20:20:33 GMT  
		Size: 11.5 MB (11473622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3b7a932d578bfc8ff2eb1d14e72aa88210fde1d7d304880764fd89f2629d4a`  
		Last Modified: Tue, 17 Feb 2026 20:20:34 GMT  
		Size: 61.7 MB (61703128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4050c6fc60221d10adf27580cac692e88372fd84042a37ab06a9a51ffdf6729`  
		Last Modified: Tue, 17 Feb 2026 20:20:32 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7da76dac30ea0fbf4e377f078195eb6f4fd09f68d3d82bd47da153e148fa8`  
		Last Modified: Tue, 17 Feb 2026 21:37:40 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9592b7712bb18cac8b8fea8a6a9e9364c780cb7f6792bc8e0ab7f37f3af4e`  
		Last Modified: Tue, 17 Feb 2026 21:37:40 GMT  
		Size: 4.5 MB (4502345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9b59b1d38d10a21be1ec904b7e670b3c61a330d85b98709d383c8bf7f3b90d`  
		Last Modified: Tue, 17 Feb 2026 21:37:40 GMT  
		Size: 75.7 KB (75655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b72d6eaba804c57514cb76e424a21b94386849823ec932c5b64a768a8f23ff5`  
		Last Modified: Tue, 17 Feb 2026 21:37:42 GMT  
		Size: 83.1 MB (83138588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-ubuntu-plume` - unknown; unknown

```console
$ docker pull tomee@sha256:406ac40948172674c43faa97492a95659c30a0c7fbc9f5d00b7d9817abb3890d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3703259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8a1b172025d415e1ff3e9f39010b84c49c06f04a0ca14479b9a4fb673a49da`

```dockerfile
```

-	Layers:
	-	`sha256:c54ea344fc9fc93a55222bfcf92c6d6938575a924a071400322494142d5322bc`  
		Last Modified: Tue, 17 Feb 2026 21:37:40 GMT  
		Size: 3.7 MB (3667252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e2133097d5d60df66ba08c11636032b19e381586930af4ff878996a2b4d6cd`  
		Last Modified: Tue, 17 Feb 2026 21:37:39 GMT  
		Size: 36.0 KB (36007 bytes)  
		MIME: application/vnd.in-toto+json
