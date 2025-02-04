## `lightstreamer:7-jdk21-temurin`

```console
$ docker pull lightstreamer@sha256:ba2be8c5a4d720c04f3c612a907acbb08f67782e1fb2aa98821ef3bf9b718e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `lightstreamer:7-jdk21-temurin` - linux; amd64

```console
$ docker pull lightstreamer@sha256:9ef704f9919d8e86977532a609c94b5b048de3add83658b3341dda7221606af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269253425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a98f805248945d64d962c29e05521e8093f2a9cbcd7fb84c0f1770859e7bea`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Fri, 04 Oct 2024 12:48:42 GMT
ARG RELEASE
# Fri, 04 Oct 2024 12:48:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 04 Oct 2024 12:48:42 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["/bin/bash"]
# Fri, 04 Oct 2024 12:48:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Oct 2024 12:48:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='203796e4ba2689aa921b5e0cdc9e02984d88622f80fcb9acb05a118b05007be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["jshell"]
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Fri, 04 Oct 2024 12:48:42 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2 # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LIGHTSTREAMER_VERSION=7.4.5
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distros/ls-server/7.4.5/Lightstreamer-7.4.5.tar.gz
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
USER lightstreamer
# Fri, 04 Oct 2024 12:48:42 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Oct 2024 12:48:42 GMT
WORKDIR /lightstreamer/bin/unix-like
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbbbc6af9dc7b3eec20b35797f66551a17f035a85f020fc99a0457dd268aae8`  
		Last Modified: Tue, 04 Feb 2025 04:40:27 GMT  
		Size: 22.9 MB (22942749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10b6847b9f1913a9d34980e0354787e49b068cdbdd78c70bab054c6cfbd1660`  
		Last Modified: Tue, 04 Feb 2025 04:40:30 GMT  
		Size: 157.6 MB (157591406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc1c5ea3c7d921e35f64dce04af1c8a2cd97954281eb6af66f6067f6c2c319b`  
		Last Modified: Tue, 04 Feb 2025 04:40:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e6cc55403ad09f9aeca15ab95bf547ad0b78be2b665c486beef7161150987d`  
		Last Modified: Tue, 04 Feb 2025 04:40:25 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1c511c77bb4af545a862a519c676a09a4359e8864809937a95a6ad38637631`  
		Last Modified: Tue, 04 Feb 2025 05:17:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b2e61bd76d550e88004eab965925b4bc734427cedca3984fac61981453349d`  
		Last Modified: Tue, 04 Feb 2025 05:17:45 GMT  
		Size: 59.0 MB (58959839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk21-temurin` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:33a872e35eb58caebb1670b70c331612db675ba107f024691f8e13f1ef246679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fab06b84d09f842c4a6c0e44b0403c6383d8066d219d50ad7ae4a239eff8727`

```dockerfile
```

-	Layers:
	-	`sha256:192d45e9c40e170e86c285b6df05c42689ad6f9416e7408109d5ae762d63c9c6`  
		Last Modified: Tue, 04 Feb 2025 05:17:44 GMT  
		Size: 20.8 KB (20789 bytes)  
		MIME: application/vnd.in-toto+json

### `lightstreamer:7-jdk21-temurin` - linux; arm64 variant v8

```console
$ docker pull lightstreamer@sha256:b0f949772c1a4cb22d13ce9bc58db0ee4ae54ca69fcfeb781e6d4af09945b2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267885685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3660e351e534ec899dbd16290b8f7a368557bc8a86325acb5bd1888c53d85ba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `[".\/LS.sh","run"]`

```dockerfile
# Fri, 04 Oct 2024 12:48:42 GMT
ARG RELEASE
# Fri, 04 Oct 2024 12:48:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 04 Oct 2024 12:48:42 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["/bin/bash"]
# Fri, 04 Oct 2024 12:48:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Oct 2024 12:48:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='203796e4ba2689aa921b5e0cdc9e02984d88622f80fcb9acb05a118b05007be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["jshell"]
# Fri, 04 Oct 2024 12:48:42 GMT
LABEL maintainer=Lightstreamer Server Development Team <support@lightstreamer.com>
# Fri, 04 Oct 2024 12:48:42 GMT
RUN apt-get -y update         && apt-get -y install gnupg         && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9B90BFD14309C7DA5EF58D7D4A8C08966F29B4D2 # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LIGHTSTREAMER_VERSION=7.4.5
# Fri, 04 Oct 2024 12:48:42 GMT
ENV LIGHTSTREAMER_URL_DOWNLOAD=https://lightstreamer.com/distros/ls-server/7.4.5/Lightstreamer-7.4.5.tar.gz
# Fri, 04 Oct 2024 12:48:42 GMT
RUN set -ex;         mkdir /lightstreamer && cd /lightstreamer         && curl -fSL -o Lightstreamer.tar.gz ${LIGHTSTREAMER_URL_DOWNLOAD}         && curl -fSL -o Lightstreamer.tar.gz.asc ${LIGHTSTREAMER_URL_DOWNLOAD}.asc         && gpg --batch --verify Lightstreamer.tar.gz.asc Lightstreamer.tar.gz         && tar -xvf Lightstreamer.tar.gz --strip-components=1         && sed -i -e 's/<appender-ref ref="LSDailyRolling" \/>/<appender-ref ref="LSConsole" \/>/'                   -e '/<logger name="LightstreamerLogger.init/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerLogger.license/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   -e '/<logger name="LightstreamerProxyAdapters/,+2s/<appender-ref ref="LSConsole" \/>/<!-- <appender-ref ref="LSConsole" \/> -->/'                   conf/lightstreamer_log_conf.xml         && groupadd -r -g 10000 lightstreamer         && useradd --no-log-init -r -g lightstreamer -u 10000 lightstreamer         && chown -R lightstreamer:lightstreamer ../lightstreamer         && rm Lightstreamer.tar.gz Lightstreamer.tar.gz.asc # buildkit
# Fri, 04 Oct 2024 12:48:42 GMT
USER lightstreamer
# Fri, 04 Oct 2024 12:48:42 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Oct 2024 12:48:42 GMT
WORKDIR /lightstreamer/bin/unix-like
# Fri, 04 Oct 2024 12:48:42 GMT
CMD ["./LS.sh" "run"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112b468d97fc1b8e58f23cc45c7b4449288dfc6348767e8522c42643be9f62f`  
		Last Modified: Wed, 22 Jan 2025 21:03:59 GMT  
		Size: 24.2 MB (24159896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4c340be4bc8c988e87db3430d1aac7cdb8d542b551f6c08a47c6f3a4657b3a`  
		Last Modified: Fri, 31 Jan 2025 01:46:33 GMT  
		Size: 155.9 MB (155868108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45163bf92b97e067f5621a74418afc1e99f2056a356fe6b9489a4e72d49ab7cf`  
		Last Modified: Fri, 31 Jan 2025 01:46:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cb46593f627267f8b734209a6f18b08573a6f4dbd89288b528091bd5d8bb36`  
		Last Modified: Fri, 31 Jan 2025 01:46:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500624272101fc67a13caab6d96cbf5b30dba3e57d5bcb0ae62c4c9692512910`  
		Last Modified: Fri, 31 Jan 2025 03:30:56 GMT  
		Size: 2.6 KB (2646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23a23d2c056e4a68a6ca6f42ea573ebcda949a8d3d180e7de8e6b537d2926b9`  
		Last Modified: Fri, 31 Jan 2025 03:30:58 GMT  
		Size: 59.0 MB (58959858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `lightstreamer:7-jdk21-temurin` - unknown; unknown

```console
$ docker pull lightstreamer@sha256:407e3fc997fa9dab3fe3ef54d790c7c35411790b0b9b7c28c7a43853bbbcb4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d6395c4c8f961969252f76f32b6ddd1c184eb3cca55c9047aee32e01619764`

```dockerfile
```

-	Layers:
	-	`sha256:3e24fb0653623f28606e658464eec4f88a9d87fcd7d2ced2b97a493f1bccd82e`  
		Last Modified: Fri, 31 Jan 2025 03:30:56 GMT  
		Size: 21.0 KB (20995 bytes)  
		MIME: application/vnd.in-toto+json
