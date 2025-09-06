## `tomcat:9-jre8-temurin-noble`

```console
$ docker pull tomcat@sha256:c5b818f797d864eddb10ece09c84f23b476acaa6c15413f72acdc0fa04a8a84e
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

### `tomcat:9-jre8-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:b0e4d92238205756fa41e6ffe2dc96b9f4b8acd4139437f0afff921297f05855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102519539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604fbc554bde61d3f900f197511cf38d07898db23304018409a0c8dcda9980df`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Sep 2025 16:01:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Sep 2025 16:01:09 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_VERSION=9.0.109
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Fri, 05 Sep 2025 16:01:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 05 Sep 2025 16:01:09 GMT
ENTRYPOINT []
# Fri, 05 Sep 2025 16:01:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39852e4e158856e20b95b481095740d55e35a25b1eda11bc170b798af90ceb9a`  
		Last Modified: Mon, 01 Sep 2025 23:08:38 GMT  
		Size: 17.0 MB (16971672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240bf104c8d2676f146a339f77ee9cd998bde7269c8ee05c56fe907b209f0124`  
		Last Modified: Mon, 01 Sep 2025 23:08:47 GMT  
		Size: 41.9 MB (41878404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773e261ace12e76c82e0e9ca69ccb0ce85036062977600c7ba671fdb765fa6d1`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a40297b555501af51dc2d9c08fb8be558543d2ecb1dbc39db42566cddb089d`  
		Last Modified: Mon, 01 Sep 2025 23:08:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ec7b8341d34b9909a9b811c4557d97e18b9ec0e72a98790a5d1ac664615af`  
		Last Modified: Fri, 05 Sep 2025 22:08:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69fb471ab13c004ae201ea547935c353687b1da6d5fe4d958bb18173395834c`  
		Last Modified: Fri, 05 Sep 2025 22:08:18 GMT  
		Size: 13.7 MB (13719129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a5b4392dc0488cf8b09d0e31bbc62de6b73f4d48cfd6750cb5bfe4ea1a9e37`  
		Last Modified: Fri, 05 Sep 2025 22:08:16 GMT  
		Size: 224.7 KB (224656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:8f3afa155a64e019f1f17805d6458320a260d6d7b9819cfa3701e5e0623e01fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3397681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879437f572367a7b4428d881412fac4084c258507ac36aaca45e32f293f7a588`

```dockerfile
```

-	Layers:
	-	`sha256:000407e3c27370deea8ac74d3f6143eba2382958f3b947484ee138963383d088`  
		Last Modified: Fri, 05 Sep 2025 23:37:59 GMT  
		Size: 3.4 MB (3374575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:498682674e6743995d3d3dadc9bbf5ce3879de6c1edf3cd99ba7f3c1202002f3`  
		Last Modified: Fri, 05 Sep 2025 23:38:00 GMT  
		Size: 23.1 KB (23106 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:bf3e5744dfa231296795bcb7ad6ac004f1512da7056808d2dcee0d04b6b82a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96367376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33184c8a5d22f7886ee8d462a5dea500d84424f29ba720ed16053eb39e81acd`
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
ADD file:cd43b2c2117454679b981355ba71c009d527d1ebe0a6c3fc69420af222fd6ee7 in / 
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Sep 2025 16:01:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Sep 2025 16:01:09 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_VERSION=9.0.109
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Fri, 05 Sep 2025 16:01:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 05 Sep 2025 16:01:09 GMT
ENTRYPOINT []
# Fri, 05 Sep 2025 16:01:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e823e9332188e662391782d0d87ba101759880efca7a17d9a5a20e8906cc8d7`  
		Last Modified: Tue, 19 Aug 2025 17:59:44 GMT  
		Size: 26.9 MB (26851104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ec5a1c77b69aa8bd266738d17902d05a6735dd53a924bdc4748fdec9679522`  
		Last Modified: Tue, 02 Sep 2025 00:15:06 GMT  
		Size: 16.3 MB (16305648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca560a23d9cac1b8b35610c6e3ded08b288368d42c317bb6cb509e37e083d91`  
		Last Modified: Tue, 02 Sep 2025 00:16:14 GMT  
		Size: 39.4 MB (39356300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fb300ae54416b8853bd33921c86b99bf6b6fbd1f7adf00b8bc08f98869616`  
		Last Modified: Tue, 02 Sep 2025 00:16:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaf8b0ef7f86fbbb72ae32b7679d49cb03b2fd245a6e56450cb3742fcdc39c1`  
		Last Modified: Tue, 02 Sep 2025 00:16:12 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99a53426d7c5f7f9c83e487c91ca9c01a52eefc84ff0a58462113169a43b35d`  
		Last Modified: Fri, 05 Sep 2025 22:33:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b802e67654db764c8f257bcc69b0de62e7247d79eb95e4344dac384d99b73e`  
		Last Modified: Fri, 05 Sep 2025 22:33:15 GMT  
		Size: 13.7 MB (13655286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bf51abc522ec2a902365c8397d1c5d10bf78301cac5fde656ec521674883b8`  
		Last Modified: Fri, 05 Sep 2025 22:33:15 GMT  
		Size: 196.4 KB (196424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:4506fda9f9a2a243099e5e1175455c04200bef72e49009566af29df75d611b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3403890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64d542c66051fce3a940251ab638ee37a81b23962d8133d913dc90fd50266d5`

```dockerfile
```

-	Layers:
	-	`sha256:f9ac67ce61e5a0f9c87f37ec01a48953a63d48660e19e5653b87d0d806617ce0`  
		Last Modified: Fri, 05 Sep 2025 23:38:04 GMT  
		Size: 3.4 MB (3380616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e81184506f2227713b67b232640642a8f9d66791639bd0ecb6a802ea2e1099`  
		Last Modified: Fri, 05 Sep 2025 23:38:05 GMT  
		Size: 23.3 KB (23274 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:bbf0b6536bf4e94b1255bc42324f896d146ddde5309737496e712c52149b3de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100686811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f8e2202accad2b8baf661e66533a755eeb7113cbfea2c64af5a40ecb199d7d`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Sep 2025 16:01:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Sep 2025 16:01:09 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_VERSION=9.0.109
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Fri, 05 Sep 2025 16:01:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 05 Sep 2025 16:01:09 GMT
ENTRYPOINT []
# Fri, 05 Sep 2025 16:01:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82cb5b65623a0098d812fc3093e05fc877923cbe33814d2fdf26bfedfdc87fd`  
		Last Modified: Tue, 02 Sep 2025 01:00:01 GMT  
		Size: 17.0 MB (16988801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642b4be3764a47f66dcc38f282833a526565753a7dd5a0182f12dfd7c08f7b39`  
		Last Modified: Tue, 02 Sep 2025 01:00:54 GMT  
		Size: 40.9 MB (40880026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75469cb5f5a17e4cdf253c58eb80777d97d0e6cabd753b261d331d0b53e9f07`  
		Last Modified: Tue, 02 Sep 2025 01:00:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf49c3099bd7ebdd84880ef2c6f9f39927470ce13ee5a4ce6093ff3f8980537`  
		Last Modified: Tue, 02 Sep 2025 01:00:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13953ba1c5fdb2f381d66c4956f5c77215a98e760ac3fa1cd44f0b5416ab3541`  
		Last Modified: Fri, 05 Sep 2025 22:33:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4e02194913c81472a468093e7a44a5f9a49377444ab1e234b05e3b170d7d42`  
		Last Modified: Fri, 05 Sep 2025 22:33:48 GMT  
		Size: 13.7 MB (13729956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09389d00b8330475d94208bd7d9e3a285f7b63b2f56e3cf038a4173390395c`  
		Last Modified: Fri, 05 Sep 2025 22:33:47 GMT  
		Size: 225.2 KB (225175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:03b76a4ba3d910001cec819490eac771a93ff38ac76b6260daf66ebe059168a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3399123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d8b0dca66e44aca13b480652f4443a9f5dc4fe959afeebb7c40671810b7d9d`

```dockerfile
```

-	Layers:
	-	`sha256:0e20767a02ad65e75f944918926a2472a04c66e5e0e1e94608572e6a7899c9e3`  
		Last Modified: Fri, 05 Sep 2025 23:38:09 GMT  
		Size: 3.4 MB (3375797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed127d3b9eff6afa92b95a032f45faf471cfe28bdd48f9765fe112770ca09a8`  
		Last Modified: Fri, 05 Sep 2025 23:38:10 GMT  
		Size: 23.3 KB (23326 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:07e97a4be622902228b446b556aed31c281d98ad484f8c8f1610d2353f1d7de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108417270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d1a1837531213f7f4f30c06df8d80059df6d62fb96cea923ceb771ca8d8570`
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
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Sep 2025 16:01:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Sep 2025 16:01:09 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_VERSION=9.0.109
# Fri, 05 Sep 2025 16:01:09 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Fri, 05 Sep 2025 16:01:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 05 Sep 2025 16:01:09 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 05 Sep 2025 16:01:09 GMT
ENTRYPOINT []
# Fri, 05 Sep 2025 16:01:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85ac53e3ada2c73fae4a44e2b5328577d67806f9e18dabe8b55b2a62e771c8c`  
		Last Modified: Tue, 02 Sep 2025 00:16:49 GMT  
		Size: 18.8 MB (18814806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277df6211e8fddd13e178a064fef52fe83a1bb95c7b69ef9190a481412c3bcc6`  
		Last Modified: Tue, 02 Sep 2025 00:18:14 GMT  
		Size: 41.3 MB (41259419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923887795aa748dcd90d69124af8e69b079faedb488b055cef923bf0686ce4af`  
		Last Modified: Tue, 02 Sep 2025 00:18:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b685737728f37939db08504edc324fa43d01855fd3e7fda9d7faed4573c18b`  
		Last Modified: Tue, 02 Sep 2025 00:18:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74c516bf30e31135253fccae2624292402795d2b0df068c1ba0fed28fcdf12d`  
		Last Modified: Tue, 02 Sep 2025 10:08:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b4a8a4f15d07b0b4c83d2aec0dde21f3b1e7f18db737cf362d8c4f2af43152`  
		Last Modified: Fri, 05 Sep 2025 22:57:49 GMT  
		Size: 13.8 MB (13754281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1025bb71fe378f936c14ee5c0ad53b99e772a5494c9e609c81509fbe827aed1`  
		Last Modified: Fri, 05 Sep 2025 22:57:47 GMT  
		Size: 256.6 KB (256620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:01b228721184ecd1933348a78cc5a9478e52640ad10dd3e2851e95b2d084a2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3402566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6a54453f2d3ceb2c0570de4ec7f9e2642c728b6fbef2090bfb9d5236e1e5b8`

```dockerfile
```

-	Layers:
	-	`sha256:a78f88ece63d81317bf21452dc56edb974d8578f04b0eab2787ed4bf23301841`  
		Last Modified: Fri, 05 Sep 2025 23:38:14 GMT  
		Size: 3.4 MB (3379372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d861d3f7b64691178dfe0eca98f8ec7f5a7ca2401a4562c4a0fffe57311f5d3`  
		Last Modified: Fri, 05 Sep 2025 23:38:15 GMT  
		Size: 23.2 KB (23194 bytes)  
		MIME: application/vnd.in-toto+json
