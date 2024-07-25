## `gradle:jdk11`

```console
$ docker pull gradle@sha256:80054af0b1a69faac8077b02d55d149b315e2e7f8b024416082352520601db31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:jdk11` - linux; amd64

```console
$ docker pull gradle@sha256:e1e5ad10c53d06f40cd131002e87e8d737d2ea8ae09e1656b47e43877013a570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.6 MB (376621725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9818517b039e76bcdbc524b01f36bab896ab2928aad788e93057a8073aa581`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
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
	-	`sha256:409efbe2f4f1cd1f9e9865948519036e61a5d2aaeb595ad74c4011f50cf9cde2`  
		Last Modified: Wed, 24 Jul 2024 01:27:06 GMT  
		Size: 145.6 MB (145559473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42681d4a5e80411c738d72f419734e7e117f29254b1faf48fc6c32ecc8628e5d`  
		Last Modified: Wed, 24 Jul 2024 01:26:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7050869129d5af80920c08b35fbdad7dfb8e56658e0c21c88eca3504e4128042`  
		Last Modified: Wed, 24 Jul 2024 01:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35e53ebbd3947ddc5db274b5dd615cdaa7d55caa7f9eb18dfeb6bda01265c8e`  
		Last Modified: Wed, 24 Jul 2024 03:04:41 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d349193572381841eba88c6d4411e964dc6bbc5a48af2cdd77657ad976de90`  
		Last Modified: Wed, 24 Jul 2024 03:04:41 GMT  
		Size: 51.6 MB (51558412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8f89318b839f53e0fcb683a3905566c3d1d391da2a194e7bd64dded5f1dbc1`  
		Last Modified: Wed, 24 Jul 2024 03:04:42 GMT  
		Size: 136.1 MB (136132041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd8ccc10d27301802c9972dbccfe07ce9d47832926f70cee322f1d7ea379444`  
		Last Modified: Wed, 24 Jul 2024 03:04:41 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11` - unknown; unknown

```console
$ docker pull gradle@sha256:f93e907babeefa170728e6eb291ae7f35539f4a636358ba153b45c82556833ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7107815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a56a34d8e1096fede23cac6fc4cc7d54bcbd1fbb637ee779ba2131a78d1d3f7`

```dockerfile
```

-	Layers:
	-	`sha256:fd760484f53e13e24469d5313f28a4fd20ede864316b147db1dc1be0fb45ad2b`  
		Last Modified: Wed, 24 Jul 2024 03:04:41 GMT  
		Size: 7.1 MB (7084932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21dfdd9df57b8075c28a917871f606fc0bb0d310ff44e3ef8fda0f07d12feece`  
		Last Modified: Wed, 24 Jul 2024 03:04:40 GMT  
		Size: 22.9 KB (22883 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11` - linux; arm variant v7

```console
$ docker pull gradle@sha256:809998bb02f0be29684d58b6b4b2dcf5367db2ca8b9971f8b060345331ef7576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368059918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d58f2ca2e748182d48268c76bfcce5c760fcc52d815c18bd2f20a629a57795`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
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
	-	`sha256:e772aaa7a5bf6b10c1ce08775c1441189837855665c33882873cd87b19babf37`  
		Last Modified: Wed, 24 Jul 2024 01:09:36 GMT  
		Size: 138.0 MB (138036827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a8c19533f8e40ed17820c72f01e249d168bda69fe01144d400a232fd2baa2b`  
		Last Modified: Wed, 24 Jul 2024 01:09:22 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53100acb17bc14b8fba7d8cdb4cbad13f82433d1f6d84ae889b47119424a165`  
		Last Modified: Thu, 25 Jul 2024 18:02:18 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce5d419f96cbebecd71b8ac0005f65c403621f4412ec6eef1c02e3c976f802d`  
		Last Modified: Thu, 25 Jul 2024 19:10:59 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04293b796e1c6fbdcdf7a718ad700761d609f6590cd1998524737926c4e1d24`  
		Last Modified: Thu, 25 Jul 2024 19:11:02 GMT  
		Size: 53.9 MB (53887402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf2beac8be6300b9059ba86cabd33ff0a96308c48dfde73f87bff78cdc76285`  
		Last Modified: Thu, 25 Jul 2024 19:11:03 GMT  
		Size: 136.1 MB (136132042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9763f33e5f78e169fce43ef3772a0509d3fe3972da9b324a2d414748aaf0fe`  
		Last Modified: Thu, 25 Jul 2024 19:11:00 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11` - unknown; unknown

```console
$ docker pull gradle@sha256:7aa13ee0cb200aa676a22ab63615bec85dad3ab9d7013cae4124f142c7588827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7108241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197b9bb35feb0823971b940cba118156b25aeea35e1a9a3b3e5097c1479692cc`

```dockerfile
```

-	Layers:
	-	`sha256:ab6f1519d1c6528c1b1c83e2dcf761c330a71d3c46a2a831db639baf24cf4df6`  
		Last Modified: Thu, 25 Jul 2024 19:11:00 GMT  
		Size: 7.1 MB (7085219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cebdd0951e455c94f0f7d8b682d2e13bc43c5cd4deee7f4d2085ccd4db43c92`  
		Last Modified: Thu, 25 Jul 2024 19:10:59 GMT  
		Size: 23.0 KB (23022 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:59bd2d664146b2d5d8c5ca9ed9a53955e39559d8d745ae9e8e181c53e9eb4349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370915509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6af78167e2178ec24c59514728af7a5892d79e75d5aaa4db53e3deadc376ad`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
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
	-	`sha256:5889725b112cb022cc1c067a539901ef2db01d6e4e977032e319cbd8765ea6ec`  
		Last Modified: Wed, 24 Jul 2024 00:50:48 GMT  
		Size: 142.4 MB (142360728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2a4126b865a87effd21763ced0d525a2caf7235ed4aea5ddfc84ea94d99759`  
		Last Modified: Wed, 24 Jul 2024 00:50:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410b06895c0976b9e66f7e2063c9712690cb326b9b302b5e5b9014a0e4fb9580`  
		Last Modified: Wed, 24 Jul 2024 00:50:39 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057d893207c5cebc30d370ed71ac65957a3388f418916eda71aef5717c2de787`  
		Last Modified: Wed, 24 Jul 2024 12:37:17 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe331d9d93e0d3b1ae7937fd5d9ce4a10bf19c1f0d201ff8c88173d61bfbe35`  
		Last Modified: Wed, 24 Jul 2024 12:37:19 GMT  
		Size: 51.1 MB (51143171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492ed1fffdbce96711f2d7064450e0ca0f94b12a59bf35a446b9debe3480eb02`  
		Last Modified: Wed, 24 Jul 2024 12:37:21 GMT  
		Size: 136.1 MB (136132043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236967660b90331aca619fd4a4276cda40357d1010158a256233d5cf04a7a3a9`  
		Last Modified: Wed, 24 Jul 2024 12:37:18 GMT  
		Size: 59.5 KB (59514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11` - unknown; unknown

```console
$ docker pull gradle@sha256:3f1656d51c82cc53a4a7f905ad24011fca0994592340f6e911394bc2b8059506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbcf908a93cf1cacc24c8024212591b9fa09e58a51cdf630505526bcc826350`

```dockerfile
```

-	Layers:
	-	`sha256:67c4d93690879738383ee97f4eac4707091cc768b89853957f08bebbda4da910`  
		Last Modified: Wed, 24 Jul 2024 12:37:18 GMT  
		Size: 7.1 MB (7091420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d2eff79b653cd9987f42732f57ad311a9c3b7f8030894ead2b09dd7374b6cbf`  
		Last Modified: Wed, 24 Jul 2024 12:37:17 GMT  
		Size: 23.2 KB (23248 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11` - linux; ppc64le

```console
$ docker pull gradle@sha256:c8e955c54c137f7605d02f2335b6fd0c6bb73c3328c55e735f0ceccd4342ce25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.9 MB (373865727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7412155cb8a7ba8fdaaae82aa655bcd65111b8374639c0d2ec162d2c56dc427`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
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
	-	`sha256:a41f6b9cef01e1a7787593c1af9fccda0f8f8371ace3f66ce71fd38e386fee83`  
		Last Modified: Wed, 24 Jul 2024 04:12:08 GMT  
		Size: 132.8 MB (132755205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65a40ff5ab2f8bef478ca3aa3bceea39760dc204383e53ff2308c8e94b5740`  
		Last Modified: Wed, 24 Jul 2024 04:11:56 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eee0151408f19d3a650eeffcc0d2c37f48d43afb71b72f5f1c38097599502cb`  
		Last Modified: Thu, 25 Jul 2024 17:23:55 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0eaf78864f966b6fbb4852748019193ee32b87c60fc83882faa96c58eb64f83`  
		Last Modified: Thu, 25 Jul 2024 19:16:46 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873b1b7013ae151c094f8aaa790f455ddfc3dcb82620bf76e340042da56bb844`  
		Last Modified: Thu, 25 Jul 2024 19:16:48 GMT  
		Size: 55.7 MB (55668604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd33819b672e594ffebb9d7abffc55a8d71f1b117c2c23aa61555c8d2c89ddad`  
		Last Modified: Thu, 25 Jul 2024 19:16:52 GMT  
		Size: 136.1 MB (136132043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df40a8b0fed36081e6de43d295c7fba562fc872f5d9e8779e23d7549122a69`  
		Last Modified: Thu, 25 Jul 2024 19:16:47 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11` - unknown; unknown

```console
$ docker pull gradle@sha256:e795b69b3ac445835afc48dcadf92953f188962ebc2bd504c09483b0bd41e0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7115691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538c58667c4549998b0f89803dd227b0f819e6de5c1b514330af10fa2201610`

```dockerfile
```

-	Layers:
	-	`sha256:a2d9bae07728cd4c65c99f711e98cc9ab3a987cddadcc0294aeefcac9e6d36cf`  
		Last Modified: Thu, 25 Jul 2024 19:16:47 GMT  
		Size: 7.1 MB (7092742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d200acdc60a3bb59f3345722279532eb85cb0e684370e7f14f34a24ca602408`  
		Last Modified: Thu, 25 Jul 2024 19:16:46 GMT  
		Size: 22.9 KB (22949 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11` - linux; s390x

```console
$ docker pull gradle@sha256:a1a6c2ac03869c29ce5e311c1875c3a21820eb06902350173d4dafcfd0702f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354530825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6563ab1e55f9a167c83dcb5782a2fec8ca38f2ba2e1307cbcc2c88da217644`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eaa70dc31cdad42121b062dd92b14960ba0a992a5bedede9795f6d11bf4a38`  
		Last Modified: Tue, 02 Jul 2024 03:54:48 GMT  
		Size: 13.0 MB (12954922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d50ed1e996b9755c879bb0706dd1ad80d705e1e969362827b072c502f5270c`  
		Last Modified: Wed, 24 Jul 2024 00:56:35 GMT  
		Size: 125.5 MB (125524923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad8be2a00f9a53b96ab98a8f095aa1e28adc0806b0b3482445d564106f15ef1`  
		Last Modified: Wed, 24 Jul 2024 00:56:25 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6c4c8712f27ceb1250d68caf114da12c18398473fbaf74d4b0aa2df913f66e`  
		Last Modified: Thu, 25 Jul 2024 17:47:42 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4144b26c6fb45233d133f2f415395105e6da1752faff3af4de199c7f4e04e8`  
		Last Modified: Thu, 25 Jul 2024 19:05:11 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f27ade5dd24327df2837fa359958254272bbba8b2a10075acc464f81e760e13`  
		Last Modified: Thu, 25 Jul 2024 19:05:12 GMT  
		Size: 51.3 MB (51274825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d15176893b2c563c846d719e99662b9ee3ff0b07331d8b3a15530f86196f16f`  
		Last Modified: Thu, 25 Jul 2024 19:05:15 GMT  
		Size: 136.1 MB (136132012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebee6d298810089e6c99efbaa353cc1f11fc70bfe4ac89916c61fc63b78b556`  
		Last Modified: Thu, 25 Jul 2024 19:05:12 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11` - unknown; unknown

```console
$ docker pull gradle@sha256:9a035c94e79761bbbd2fba186df8f7ec1bf05c9216f005f7b1b4607263699876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7107612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daf190643f944907f0c3fb36dbadc21500ed301a445462fe589cb2bf5d86d37`

```dockerfile
```

-	Layers:
	-	`sha256:2689595890744224a6251714723b773d3a4c0a7a5419982caeb317d3171b4eff`  
		Last Modified: Thu, 25 Jul 2024 19:05:11 GMT  
		Size: 7.1 MB (7084731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ac4308d0e3be538ee420067857a7a9c290b5b5c862fb55685a505c813833dab`  
		Last Modified: Thu, 25 Jul 2024 19:05:11 GMT  
		Size: 22.9 KB (22881 bytes)  
		MIME: application/vnd.in-toto+json
