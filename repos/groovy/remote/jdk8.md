## `groovy:jdk8`

```console
$ docker pull groovy@sha256:de9288d5f3d60889c092a9b5b89916e5c3825145bb91b0ba6e2896eb7549bd66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `groovy:jdk8` - linux; amd64

```console
$ docker pull groovy@sha256:14fbba628e4889b7488c4467606f41b85c586426e26d282b859daef3c9dc4f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180285529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa829958c43395d4bcd5838104387451ada084678d77964cad7e46e78f94f6f2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 30 Jun 2024 17:46:17 GMT
ARG RELEASE
# Sun, 30 Jun 2024 17:46:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Jun 2024 17:46:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["/bin/bash"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Jun 2024 17:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Jun 2024 17:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["groovysh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 30 Jun 2024 17:46:17 GMT
WORKDIR /home/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_VERSION=4.0.22
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
USER 1000:1000
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7748081ef4ddd702e42523024d72d06310dc54b43c9adb4b055d0635856ed821`  
		Last Modified: Tue, 17 Sep 2024 01:07:27 GMT  
		Size: 103.6 MB (103615884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc99609f4e5977496e24a88e9e762beeeab065f1cd4cde1fdbb7f9f0a785f774`  
		Last Modified: Tue, 17 Sep 2024 01:07:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10d82a4fe81df64994baefc053e0dc3e19d9ca18b8a4974332e91f93131a59e`  
		Last Modified: Tue, 17 Sep 2024 01:07:18 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43669bbff3e6bdd8a57d2567ef41c8fc1a471af728bdbb8e0b2c7621e429ba4`  
		Last Modified: Tue, 17 Sep 2024 01:59:45 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a2a0f266bdac1608bf1779635ec1bb694b97a21bbd84c8a788ea2fea93b70`  
		Last Modified: Tue, 17 Sep 2024 01:59:45 GMT  
		Size: 3.5 MB (3500077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e66f242e52e606b714aea7498a91da6bba37b31a30a951442f43db2797d594c`  
		Last Modified: Tue, 17 Sep 2024 01:59:46 GMT  
		Size: 29.9 MB (29851949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dc30e9588aa17d064af69aec618599132a1153a8c387323a1089062d4a360a`  
		Last Modified: Tue, 17 Sep 2024 01:59:45 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8` - unknown; unknown

```console
$ docker pull groovy@sha256:f2e8071416fb372d93353051b3c16f4632d5bedd0e710fc27ec269380176f398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 KB (27785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d82c20a2a9d79d488fd34b0bebdb4a74c0834188aa9934227e4545b73d0e4b8`

```dockerfile
```

-	Layers:
	-	`sha256:cac99c32caa1ce215b40e5c105380b8ec67a722bd8bb8107fe1fbf4ab8ae749e`  
		Last Modified: Tue, 17 Sep 2024 01:59:45 GMT  
		Size: 2.9 KB (2887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9315517b75386f2fee68633000341805c73bd76eb9ed68e20cb1480e6090f75`  
		Last Modified: Tue, 17 Sep 2024 01:59:45 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk8` - linux; arm variant v7

```console
$ docker pull groovy@sha256:e6153d0dabc1f9b34719f1cf27b19a8493f64176c0f6cb0828bb0a602578b4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172744335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af870034a15fe31db03f846b81fec9121fa1a1c99763a38487bf3c93e885a3fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 30 Jun 2024 17:46:17 GMT
ARG RELEASE
# Sun, 30 Jun 2024 17:46:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Jun 2024 17:46:17 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["/bin/bash"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Jun 2024 17:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Jun 2024 17:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["groovysh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 30 Jun 2024 17:46:17 GMT
WORKDIR /home/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_VERSION=4.0.22
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
USER 1000:1000
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31edfebc2dc37b7fcd5adfb6ee3872ba74788ba24e8c2c3a40107b9fd85153c`  
		Last Modified: Tue, 17 Sep 2024 01:23:55 GMT  
		Size: 12.5 MB (12463235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dceebff5900ca60d8a97a8b3777b7610dca77f4a4e9b0a9d1ab04e501e841f73`  
		Last Modified: Tue, 17 Sep 2024 01:24:02 GMT  
		Size: 99.2 MB (99249283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f2e37aff38b72d45e9c18a61deda9e561d3f12bacf728fce034b713054e733`  
		Last Modified: Tue, 17 Sep 2024 01:23:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4f214b3bba8fc06f489b17c82f25faec9c0572f4bae38934809991422e935`  
		Last Modified: Tue, 17 Sep 2024 01:23:52 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4a1a01493b696ac6a202dfb457b31db5e48aaa6d6bf63c85d2a6546b7a5b17`  
		Last Modified: Tue, 17 Sep 2024 02:12:04 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3b79949590042dfaf434f68c237f114d9a1e4efddbb18a8bf525dadea1a056`  
		Last Modified: Tue, 17 Sep 2024 02:12:05 GMT  
		Size: 3.6 MB (3639094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354e78d8409829b5e5be294b2b97e627531c44ccd58d1c414f417f68b00d0466`  
		Last Modified: Tue, 17 Sep 2024 02:12:06 GMT  
		Size: 29.9 MB (29851952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2796a92738c5b2c9c61451494585e4132374b94dbf73270008a3b05e57ae6ef`  
		Last Modified: Tue, 17 Sep 2024 02:12:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8` - unknown; unknown

```console
$ docker pull groovy@sha256:677b89db6f3ed3d06146bfff0ee947a7ef5a82876438875ce218dd92e92dd63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b289efbeed3108c850a4696b0489e45289c88adcf51cafb100d2e4d83bb0119b`

```dockerfile
```

-	Layers:
	-	`sha256:28c67e18900c6cfc2be96eaf9775ae6ceaafa768890aac8a26d372959f77098a`  
		Last Modified: Tue, 17 Sep 2024 02:12:05 GMT  
		Size: 3.7 MB (3735700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6facc307990249c99dd3e89ebcb0aef5acb50c74c282766e829a7733d990092c`  
		Last Modified: Tue, 17 Sep 2024 02:12:04 GMT  
		Size: 25.0 KB (25016 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk8` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:253c5abb5fc041fbe49ad8a6d7aa1b3448e8f3c8d830298c38e9a7fd12d0390e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.3 MB (177270565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c28036d0939f3b6b9b2ae382ba6d065601e3d95d01e6dd9ac7cb6ac54d7e96`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 30 Jun 2024 17:46:17 GMT
ARG RELEASE
# Sun, 30 Jun 2024 17:46:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Jun 2024 17:46:17 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["/bin/bash"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Jun 2024 17:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Jun 2024 17:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["groovysh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 30 Jun 2024 17:46:17 GMT
WORKDIR /home/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_VERSION=4.0.22
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
USER 1000:1000
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee3c18d11ada1b8c61be4cdde6a7b77092f6a333a08ea4b2a44951edb9c7f76`  
		Last Modified: Tue, 17 Sep 2024 01:37:33 GMT  
		Size: 102.7 MB (102732866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb9ee7d7cf98ca380289182bb1c6ceeea651a94d1c8d67745ff50df481881da`  
		Last Modified: Tue, 17 Sep 2024 01:37:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa527af5ede58b8c5dcb94dd664e9489e2a23b1a2252a3f93c3df9a7a6de9e6c`  
		Last Modified: Tue, 17 Sep 2024 01:37:26 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425229ca64e86fa33ef5cf8b2406c767bdaa722ab187ecd02e856cce13d13329`  
		Last Modified: Tue, 17 Sep 2024 05:32:37 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d525587dbb5aa22e4e608548f1b2485852d070535d7908d518a33652c5960d`  
		Last Modified: Tue, 17 Sep 2024 05:32:38 GMT  
		Size: 3.5 MB (3468667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f94e03229a8cff5a8dae986a14b4a1c164c10e7db99a483fdd234a367029d33`  
		Last Modified: Tue, 17 Sep 2024 05:32:39 GMT  
		Size: 29.9 MB (29851950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c10b805b473b9d4e533e22dcf0a5dba88048c6384d8c8ca549fa3603b32ad58`  
		Last Modified: Tue, 17 Sep 2024 05:32:38 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8` - unknown; unknown

```console
$ docker pull groovy@sha256:05f382df468da82c1caf3a71d2f3d78dfacadaa0bc6b910df6840375f0855c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d962d94a5c6211a44206cea785b34f1f701fcee5b4233dd598d16726f63170ab`

```dockerfile
```

-	Layers:
	-	`sha256:69b00d2a7a13b8014856df200cab0a072c2982dd36c68b5e1c340dc3bf9aa7f5`  
		Last Modified: Tue, 17 Sep 2024 05:32:38 GMT  
		Size: 3.7 MB (3733260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1ddccdd073ac5e51bb3ebcabc2bc903e2871369bc2ba553cdd5a56c0eff8d70`  
		Last Modified: Tue, 17 Sep 2024 05:32:37 GMT  
		Size: 25.2 KB (25238 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk8` - linux; ppc64le

```console
$ docker pull groovy@sha256:15beaeb4add0f3d57c1cf19e618c6f3c6f4949fac52aaf07d03c96a8d15c3215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184438241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5151231771993af81e28061c9516722ed31c5365c6dca6b93e1dd7ee4e14e86`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 30 Jun 2024 17:46:17 GMT
ARG RELEASE
# Sun, 30 Jun 2024 17:46:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Jun 2024 17:46:17 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["/bin/bash"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Jun 2024 17:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Jun 2024 17:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["groovysh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 30 Jun 2024 17:46:17 GMT
WORKDIR /home/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_VERSION=4.0.22
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
USER 1000:1000
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334ceb702fdfcb85bc9cfaab00b3806cae756a959247b670cefbabf87a47b2b6`  
		Last Modified: Tue, 17 Sep 2024 01:05:47 GMT  
		Size: 101.1 MB (101079847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd32a1efeedd13b4fd46b3be8b973aefa290a0b75368f31a31fedaffe3672f8`  
		Last Modified: Tue, 17 Sep 2024 01:05:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746fb58333d3760a3857439edea9f2a6bb4e48a6a73ce68ebf98f1dd16365cd9`  
		Last Modified: Tue, 17 Sep 2024 01:05:37 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e530fb7d22db1cd15b79cf8373a2f9681d780c1a07b90723afbae725febd41a4`  
		Last Modified: Tue, 17 Sep 2024 03:36:21 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd3771edd27c9a5d03d8041c0639894c7ae4fd180d78e558fe738865a3dbf13`  
		Last Modified: Tue, 17 Sep 2024 03:36:22 GMT  
		Size: 4.2 MB (4199262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814e1990fea41c2202bf6d76a59f2ee81614b3811f48ec0c4a5fef48f85eb4db`  
		Last Modified: Tue, 17 Sep 2024 03:36:23 GMT  
		Size: 29.9 MB (29851949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83639fa74aa63e9e9e5642b56572138f896026afaaff37d539c7a6e3cd530651`  
		Last Modified: Tue, 17 Sep 2024 03:36:21 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8` - unknown; unknown

```console
$ docker pull groovy@sha256:748867fdd07ce3cf7ab999516be31d6f5f8efef4a390e2e4eeb959493eacb9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3761349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c41024e88f416af3347153cb5622d6464063602ad5f3a42289906a0761b0737`

```dockerfile
```

-	Layers:
	-	`sha256:0a507ee1aafe6c1861ede64e2e59673da9720dbfeef087cd5f4f98f2d6472a08`  
		Last Modified: Tue, 17 Sep 2024 03:36:22 GMT  
		Size: 3.7 MB (3736397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2444d8d2bae85ee1fa98133b3694157368cca006391c056245aeeadba50c602c`  
		Last Modified: Tue, 17 Sep 2024 03:36:21 GMT  
		Size: 25.0 KB (24952 bytes)  
		MIME: application/vnd.in-toto+json
