## `lightstreamer:7-jdk8`

```console
$ docker pull lightstreamer@sha256:6d88887c629562e5b6b5d5e094bead6a905211e4c411d1258f350601407ba85f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `lightstreamer:7-jdk8` - linux; amd64

```console
$ docker pull lightstreamer@sha256:3574d6d6167c97586f83ba3d033a5d319c345621a0d8cee1de11978a7258e1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160354604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f51072a29c33b03835936218debc88d1ff249db77b8d4538e753f6a45a9eddf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Wed, 11 Jun 2025 10:41:02 GMT
ARG RELEASE
# Wed, 11 Jun 2025 10:41:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Jun 2025 10:41:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Jun 2025 10:41:02 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 11 Jun 2025 10:41:02 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 11 Jun 2025 10:41:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Jun 2025 10:41:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jun 2025 10:41:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jun 2025 10:41:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Jun 2025 10:41:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 11 Jun 2025 10:41:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Jun 2025 10:41:02 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Wed, 11 Jun 2025 10:41:02 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2 # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
ENV LIGHTSTREAMER_VERSION=7.4.7
# Wed, 11 Jun 2025 10:41:02 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distros/ls-server/7.4.7/Lightstreamer-7.4.7.tar.gz
# Wed, 11 Jun 2025 10:41:02 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
USER lightstreamer
# Wed, 11 Jun 2025 10:41:02 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Jun 2025 10:41:02 GMT
WORKDIR /lightstreamer/bin/unix-like
# Wed, 11 Jun 2025 10:41:02 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb43857d5308a40718704288d12cb0f13a2c0c288decd5254238b35963ff9d7`  
		Last Modified: Mon, 15 Sep 2025 22:12:45 GMT  
		Size: 17.0 MB (16971774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75cee9f1f2e7610dad4413b9e913bd37b54330c43a35bd3c85ad28bad82617e`  
		Last Modified: Mon, 15 Sep 2025 22:12:50 GMT  
		Size: 54.7 MB (54739675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3133ac8c49679b26388b308a6a3d27b36b06ec1443730b47518fd4134e813`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ab2fa29f411732853d26d15ae764cec2feb5409374d10d1f97a71cbdca0a`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ef7150bba5685f883e9ed5736bd7ca75569639157d8183310a214aa45937f8`  
		Last Modified: Tue, 16 Sep 2025 00:13:53 GMT  
		Size: 2.6 KB (2645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec312c931634e26f49dd0dc648de579564d5247d703354508efb51c06f8ca1aa`  
		Last Modified: Tue, 16 Sep 2025 00:15:48 GMT  
		Size: 58.9 MB (58914562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk8` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:21ef387b791bf69f72d8048badf3f4644eeb461a0a4c47a5779e6eec107fa03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f8eff89ae3ae53de49294e9d8ff191086e00e7738452f13dfe74583c708e3f`

```dockerfile
```

-	Layers:
	-	`sha256:dacfa20057a2b6a5c0ac7d2ce5dd00d886d7a29451b37a80a9214544d058f0ef`  
		Last Modified: Tue, 16 Sep 2025 03:09:17 GMT  
		Size: 19.5 KB (19539 bytes)  
		MIME: application/vnd.in-toto+json

### `lightstreamer:7-jdk8` - linux; arm64 variant v8

```console
$ docker pull lightstreamer@sha256:59117b153235198186fac62d96407ee1cbbb1981ef577ae3e6d1bff8e0814f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160826979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3937e210c3f78211218ad465f75240c8102a57d5228223a26186be01c067706f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Wed, 11 Jun 2025 10:41:02 GMT
ARG RELEASE
# Wed, 11 Jun 2025 10:41:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Jun 2025 10:41:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Jun 2025 10:41:02 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 11 Jun 2025 10:41:02 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Wed, 11 Jun 2025 10:41:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Jun 2025 10:41:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jun 2025 10:41:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jun 2025 10:41:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Jun 2025 10:41:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 11 Jun 2025 10:41:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Jun 2025 10:41:02 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Wed, 11 Jun 2025 10:41:02 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2 # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
ENV LIGHTSTREAMER_VERSION=7.4.7
# Wed, 11 Jun 2025 10:41:02 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distros/ls-server/7.4.7/Lightstreamer-7.4.7.tar.gz
# Wed, 11 Jun 2025 10:41:02 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc # buildkit
# Wed, 11 Jun 2025 10:41:02 GMT
USER lightstreamer
# Wed, 11 Jun 2025 10:41:02 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Jun 2025 10:41:02 GMT
WORKDIR /lightstreamer/bin/unix-like
# Wed, 11 Jun 2025 10:41:02 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ec6c766cb339fe7639e7b17d5743545c0002c3dbb08b75eae759be43211807`  
		Last Modified: Thu, 02 Oct 2025 01:17:05 GMT  
		Size: 53.8 MB (53839370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa9f945462c02f1fde3906d24c8d0bed5c81c07e533c43e49ea449b2244882`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a22966219fd178174a348aca3c91573a3628dd260afb986e17e85a311bd26b`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ad93dadac694f22d67bdb66afce80acdc967ee8de07f30494e13d381772edb`  
		Last Modified: Thu, 02 Oct 2025 03:15:38 GMT  
		Size: 2.6 KB (2645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c9fa027ee12d709704432f4a6f9aa6c41ab71ddd9468fde49759ae0e9015f6`  
		Last Modified: Thu, 02 Oct 2025 03:47:00 GMT  
		Size: 58.9 MB (58914526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk8` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:dd46e9423a3af719f948676da6e5bd14cbf732f7a18b18b9b7d34d898bf66e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f991128f1b7eb5890e5bdaa7a7fce270d23a6b2000f0dd90286833cc7b74c310`

```dockerfile
```

-	Layers:
	-	`sha256:7fadeae84c5955a53c26ff28511767d8e9b2e27fa791b2392e96e9e9086417b5`  
		Last Modified: Thu, 02 Oct 2025 06:09:06 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json
