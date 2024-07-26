## `gradle:6-jdk8-jammy`

```console
$ docker pull gradle@sha256:d8d72c37004a367695084d1cb9881fab59ecfc64e530dd222f5227e3321c3637
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

### `gradle:6-jdk8-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:2fd9c0e4ca0d5b2c60f36bd237a1188dfa12c7a6d3ae6d06b0b078ad8ca56f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306619899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a669d9dd3571c9cdcc90e250affafff917a07a0cdf85451424fef6482d8dcc`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ARG RELEASE
# Thu, 18 Jan 2024 04:04:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4040a9fc8f154e4bdc7b1fada39d21321aa2fa67f5ec71b3c6ced523d6bca756`  
		Last Modified: Thu, 25 Jul 2024 17:26:10 GMT  
		Size: 103.6 MB (103615844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876aecb20e71daf56b1b8ebbe1e3e11f26f6d9ca83e6933e9fb7b9c5a9db53e`  
		Last Modified: Thu, 25 Jul 2024 17:26:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaf0a30f7dfdef304092a7f19ad21c11e30bcf6bf04e60ff7b75b504d6cf8f4`  
		Last Modified: Thu, 25 Jul 2024 17:26:03 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088074edc5899ff51d4eecd5d0533eca01bba4a309a8ccf1b5969619d7655ef`  
		Last Modified: Thu, 25 Jul 2024 19:02:51 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992b9153db6cd9b05e264929b66df07a1ed8fe39aa0fec62449151a9f17f9fa`  
		Last Modified: Thu, 25 Jul 2024 19:02:52 GMT  
		Size: 51.6 MB (51558849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8fd3ad93a521919dfa457f5ecb3a8e5c137a080c0047c648cb03ca9be79ad0`  
		Last Modified: Thu, 25 Jul 2024 19:02:53 GMT  
		Size: 107.7 MB (107696666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625a45093e9323026d1dfcf51ffc8dbe585c4b8e71062fc27193ec1c30c97be1`  
		Last Modified: Thu, 25 Jul 2024 19:02:51 GMT  
		Size: 431.3 KB (431267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:e6af442b6ef855c4cccaee5f67b1547bed16426311bab257c382b2daab6dfd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7056151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940d5b777f2f99eeb1c66c4bf6f18e4c1cf9b6d206d2d3ecc7b8cc0bacd43161`

```dockerfile
```

-	Layers:
	-	`sha256:c0acf010d52e8dc6ee56625a17d16aaafc09b31865951bb1015a7fc7f20f1eb3`  
		Last Modified: Thu, 25 Jul 2024 19:02:51 GMT  
		Size: 7.0 MB (7033889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1706c659b744d5d8f6332da9034fd8caf414d32a6fe388acce5b710090222b1`  
		Last Modified: Thu, 25 Jul 2024 19:02:51 GMT  
		Size: 22.3 KB (22262 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:0b25c208e69072fd03c68e76a2fa7687f658f1a468fd87002a63ee8376f29fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300867520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dadb15729c950c00f985b3107b0220c842d6021e93a3f30b8c19ddc834d989`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ARG RELEASE
# Thu, 18 Jan 2024 04:04:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3600b7820ccdab844af0b11c36a1aeadc460c5a3bc6a6fd0211a3fa9024fb1`  
		Last Modified: Tue, 02 Jul 2024 04:32:24 GMT  
		Size: 12.5 MB (12462968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2795f90fa7d600dee1f4eb73c08bb2d18123b06d13636002d46176c4b2f023f3`  
		Last Modified: Thu, 25 Jul 2024 18:01:01 GMT  
		Size: 99.2 MB (99249372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c3b2a91fa20610bf53f9d0a722666976bbced1fddeabec3b2f1cafa30130f`  
		Last Modified: Thu, 25 Jul 2024 18:00:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602dfe42d8b2b444328e0fb2b51ef2d074bcde8a413952b8269fe2bb2b489f6`  
		Last Modified: Thu, 25 Jul 2024 18:00:53 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068d95d53efed676b1e435cff0a1e48ef014cb7525253c097ec22c7b45c606a`  
		Last Modified: Thu, 25 Jul 2024 19:07:53 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c1ce057d0503b41ea67548546bceb86d4979bf86afdca11d1107c23067e98e`  
		Last Modified: Thu, 25 Jul 2024 19:07:55 GMT  
		Size: 53.9 MB (53886899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d412218fd8f1912f977c7198ffcad72621233068915d116bf70e4fc605a4e6`  
		Last Modified: Thu, 25 Jul 2024 19:22:07 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc79240795620f602c2b3b5e0ce29e2465af2fc5cc7a706bed4b1522eb71b77`  
		Last Modified: Thu, 25 Jul 2024 19:22:04 GMT  
		Size: 31.3 KB (31275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:7dda0c50697c384ac5df513164b4c63757059dcb27b961ebf9a19d50be1ac93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7058038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fece9779311ef2f89fc46faa602b656f6172d7b2ad6e247ae42d626dd1308d`

```dockerfile
```

-	Layers:
	-	`sha256:8a639910e3f678eb6ff66551993bebc799173fc2b59bda949de863bd0e82df6d`  
		Last Modified: Thu, 25 Jul 2024 19:22:04 GMT  
		Size: 7.0 MB (7035659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c54d956391b9eabda76df754a0c06f011b91d8a0c1ba20a7657a06081462603`  
		Last Modified: Thu, 25 Jul 2024 19:22:03 GMT  
		Size: 22.4 KB (22379 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b074858586e483f691074886699fb10899cd5ef613c920e6f41cd9cb308422a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303214752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0174714998a0f0aa78b73cdc718c0d69d932a27c0a0a0a623ce55e6e44423b45`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ARG RELEASE
# Thu, 18 Jan 2024 04:04:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4067f34463c503bd1fc838a5a6c6cbdf7b3ee1ed2cad8f75d5eca793d63c74f`  
		Last Modified: Thu, 25 Jul 2024 17:43:14 GMT  
		Size: 102.7 MB (102732944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a973d000c12857de1a9afcc1f6575e1dd49435948c0f1830133cfbd3e54e136`  
		Last Modified: Thu, 25 Jul 2024 17:43:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e421cc4972493dfec2b6fad92dee87647b38449557801031eb514d85be4509`  
		Last Modified: Thu, 25 Jul 2024 17:43:07 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b66c1232cb7c68aca789c4dfc0783fbc061707e0c25b33d1957ec827cc00833`  
		Last Modified: Thu, 25 Jul 2024 21:51:12 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc3778db0594ac6b8dc10ea13d968a6e4105aa0919bd7a9203a279ab42c58a6`  
		Last Modified: Thu, 25 Jul 2024 21:51:13 GMT  
		Size: 51.1 MB (51139668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1e862f63804cc12f81573f1f9bee2b4ccd723680467a2eb285500955268e18`  
		Last Modified: Thu, 25 Jul 2024 22:08:28 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24835c942b4526a6b81a3c35214e94020690969aaba2ed9ef342c80abd4cd152`  
		Last Modified: Thu, 25 Jul 2024 22:08:25 GMT  
		Size: 425.0 KB (425034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:5bb568f5794d5872b27a4a97c244525dcc64a43a66d2b962455f41425f848ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef10fd8858a01f44ca5830dad4b54ce539dabaf402d3ca53452bb79257eafef`

```dockerfile
```

-	Layers:
	-	`sha256:d44f3afebb905731ec41557202a77ecaeeec2a117326e5ee03ea04ed9a344437`  
		Last Modified: Thu, 25 Jul 2024 22:08:25 GMT  
		Size: 7.0 MB (7040353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2692b856640dc4b09fd92ab6c17bdf47a45d9826f265346c4d44e03a9165a7ae`  
		Last Modified: Thu, 25 Jul 2024 22:08:25 GMT  
		Size: 22.6 KB (22601 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:c34bc1dd37772ff8823e2d80ac9ea4fca2c5f133c4376b73f6db6df256a2e060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313786876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0917a264319de080ef975cbfb1ccda8684db940187f75f8e1f2fbe270c290778`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ARG RELEASE
# Thu, 18 Jan 2024 04:04:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0c5ba122f1b7831956945687e0f65a5f15a39c1576c982761c6c15b1d3795a`  
		Last Modified: Thu, 25 Jul 2024 17:21:51 GMT  
		Size: 101.1 MB (101079872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be7d46fbb1add9f75159cb8103318aa75ca3272c709f23c0a755f18099043e9`  
		Last Modified: Thu, 25 Jul 2024 17:21:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e412dc67342cc5f7de185ae98cea64af8adc9e12c148807fc400ad86dcfe59da`  
		Last Modified: Thu, 25 Jul 2024 17:21:38 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04928876adf89e4cae719d810de477e533693fb27b5d5f581cc378deaf942100`  
		Last Modified: Thu, 25 Jul 2024 19:12:03 GMT  
		Size: 4.3 KB (4328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff40305605fb81b2c94f4e781156cc7eb4eef9e780b013fe8e577d284868dcb4`  
		Last Modified: Thu, 25 Jul 2024 19:12:06 GMT  
		Size: 55.7 MB (55665808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23bdc59d007311fdbb80ca9db6f9078dd2a5fffa73e9a4c1d344d0841b82c90`  
		Last Modified: Thu, 25 Jul 2024 19:33:50 GMT  
		Size: 107.7 MB (107696667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5afb8fea4f1db92f153b19aa3ba8f68491176c95342a1a84c982736a9f5da12`  
		Last Modified: Thu, 25 Jul 2024 19:33:46 GMT  
		Size: 35.0 KB (34981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:46e886ae200850b23560e4499c09ee12941c099bd196117da16fd3c25e9fd219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260e42e4e47d29451d0f16f6f196b65a71d488ad81ad8a6d350be702ccc32b74`

```dockerfile
```

-	Layers:
	-	`sha256:b688cc10a1c363aef7d0512e8665380e25e3984ebde2d9e01b005ebd83187e80`  
		Last Modified: Thu, 25 Jul 2024 19:33:47 GMT  
		Size: 7.0 MB (7040581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c8dee26662eccb04333c82f4c17db8b23602c6d6fa6764fa98318a8424b427`  
		Last Modified: Thu, 25 Jul 2024 19:33:46 GMT  
		Size: 22.3 KB (22317 bytes)  
		MIME: application/vnd.in-toto+json
