## `lightstreamer:7-jdk8`

```console
$ docker pull lightstreamer@sha256:d5046574af4870f01bb3007ec5869d2454e40834cf226b8273207b27d6875851
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `lightstreamer:7-jdk8` - linux; amd64

```console
$ docker pull lightstreamer@sha256:7dc972998f94d8741c4961e33d10f3c13f41e17900bcbd9efe901d72ea126a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160328843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bff589643d09f2537e5029adb723e1561ee81c9839172105610a9f7fc00f2bd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

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
	-	`sha256:0902033b99e157d452a79112774eebf2a83e21f01776cb11967149ca49cfce5b`  
		Last Modified: Wed, 02 Jul 2025 06:09:46 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74e64f9cecd615c83d6e3eeb465ac54b1c2330f9d94bbf8216afd9f9c54a6c5`  
		Last Modified: Wed, 02 Jul 2025 06:09:50 GMT  
		Size: 58.9 MB (58914570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk8` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:94e58edb93459a579627576d4f8d40e3dde9f27ba29e3862abee6b017bcd77e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad5305c16087e6b3b843579d7037790b1de079f5d7e98e9927bcad50c2094b9`

```dockerfile
```

-	Layers:
	-	`sha256:bbf96d048dcd96829db94d6992b30f34a2bcf9d8b795f62baeeecfc1b6f7905a`  
		Last Modified: Wed, 02 Jul 2025 06:08:44 GMT  
		Size: 19.5 KB (19538 bytes)  
		MIME: application/vnd.in-toto+json

### `lightstreamer:7-jdk8` - linux; arm64 variant v8

```console
$ docker pull lightstreamer@sha256:1a787f172dc56db242720dfd16f5d9a3415966d5c458d1f6dfde567d8a3543d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158597625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bc64b92b2f7e85729979364bda7e19c3b7fbdb4d43e6d59562c76551e7d3a8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

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
	-	`sha256:3b03df75f09cb8693e46d5445b3932a975bd1c53769715baa20c221c5ad3c179`  
		Last Modified: Wed, 02 Jul 2025 08:41:09 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df47063e6f153cb2d3294618f83b42a37fe34e65bfc72697655b6bf28e8c24cf`  
		Last Modified: Wed, 02 Jul 2025 12:09:03 GMT  
		Size: 58.9 MB (58914653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk8` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:357eab96709a35394eac69bf21965247a148ae769ce08c41ae08caf01e3a64ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c953c82fee256b0e6fe14a9f1f328b57ab7e2e30b8b64ef73a2ebcb6752cd32`

```dockerfile
```

-	Layers:
	-	`sha256:ec5e5ab60a4589805c18bb11e2ef862e47062d1956d8ce220608b527116c3bb3`  
		Last Modified: Wed, 02 Jul 2025 12:08:52 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json
