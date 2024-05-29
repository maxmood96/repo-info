## `clojure:temurin-8-tools-deps-1.11.3.1456-jammy`

```console
$ docker pull clojure@sha256:b3bd05e74775a8d431f0454fc82344f27fd688cc23b062598a0d2de2de06d4ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.3.1456-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:c69b5ca6abdcaccd2e86d8497b5ec8bbc91c2fd1c126dd4694b183e41886b84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.4 MB (198375807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc69be348d4ee639508135c090e88f8fe7c33008bb8ffcc00492d8bd3b7dbb2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce394e5c05f6275f1a3d93ef078caadf4c6e88066e708ffa5cea964ded0c3c2`  
		Last Modified: Thu, 02 May 2024 01:15:30 GMT  
		Size: 12.9 MB (12905606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e985ee26d7966950debab0bf9d7e17e8d0a9cc5b9b36f2d3066975605faa23`  
		Last Modified: Thu, 02 May 2024 01:15:37 GMT  
		Size: 103.6 MB (103602282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63f033143623e93ed39f65fc99423eb715bdb5bdfee213fd8173f9b6e813a43`  
		Last Modified: Thu, 02 May 2024 01:15:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95775e4b4d5153b3651e53c635338b8c37d6cd12fb3dff3f6df1534464e41628`  
		Last Modified: Thu, 02 May 2024 01:15:28 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788de98df00dfc15b8030b8b5f66d6f7e27902b7b5de0a52c64f06f002646cf1`  
		Last Modified: Wed, 29 May 2024 19:56:51 GMT  
		Size: 51.4 MB (51426726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec991aebc071dbfc416d7751a374b2ba65533be45c1566aaad3d5580495c6e`  
		Last Modified: Wed, 29 May 2024 19:56:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:4e6ed0f47c43ad9196621c216ea56bc640417676fcf29525d4b50f1ebe71d8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5750768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b21dccb812bdffb68b7d2b7b6270a6251e36e1d9953f3603d1f5f5ddf98bac3`

```dockerfile
```

-	Layers:
	-	`sha256:178aa38d136872ac185eb228c63c4f86bf037af114b0dd71bbb1163e07a1b0c5`  
		Last Modified: Wed, 29 May 2024 19:56:51 GMT  
		Size: 5.7 MB (5736691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af735a40b4fa4f559704423dd85343e1287298cecb0a7f8350ebfd439979980`  
		Last Modified: Wed, 29 May 2024 19:56:50 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.3.1456-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c4ea92a3b6057e5054c809f492de942acec2af1f497bc7037b4c7e2c71a7b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195367165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc4d7cf6508a45aaeea59d5b3d91a8f16c0fcae26d52d8549fafc76cd6fc870`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2472ac6840da0115175cae8b0be8d1b8c2b6b74acb5fc6bf185b0c9333b8a3`  
		Last Modified: Thu, 02 May 2024 04:17:28 GMT  
		Size: 12.8 MB (12847034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c050069391baee7bb13200b3297c944c954a22f0428769272d51e6cba8118a36`  
		Last Modified: Thu, 02 May 2024 04:17:34 GMT  
		Size: 102.7 MB (102704159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd259c2f39c587be8bdd17660976c6158388173b58e226f2b5095d399cf658f2`  
		Last Modified: Thu, 02 May 2024 04:17:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22bcaede3cb82201c2804d7a050cbf18f994bd6f0b34f3ec133a47cc3c24ca9`  
		Last Modified: Thu, 02 May 2024 04:17:27 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f2f5822040b5c4fe17735ddfba85bddb5c4ad9031fa613fdca91bf29f4eb6e`  
		Last Modified: Wed, 29 May 2024 20:34:53 GMT  
		Size: 51.4 MB (51413249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86c591c6083f36a146da2abcf6cbd7ac37abb391165f996137e33fb11eb791`  
		Last Modified: Wed, 29 May 2024 20:34:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:ab4874dd00ae62d42ca9378725c7d75f9d822d7fc3f0ff5005dc03b01a2bd9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3008b38a7c22ce4267b086d768b7fa9f0bdbc51a7ebfc9b6c3ba6df70c63502a`

```dockerfile
```

-	Layers:
	-	`sha256:1172717270b8c454f44ff5c14aaa2e2d005b725858dc00a1c9b2ab096c60f4c4`  
		Last Modified: Wed, 29 May 2024 20:34:51 GMT  
		Size: 5.7 MB (5743102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b240796152aadccf2b695f5698105a6d797620885daa1a9510269dc6103b645`  
		Last Modified: Wed, 29 May 2024 20:34:51 GMT  
		Size: 14.4 KB (14405 bytes)  
		MIME: application/vnd.in-toto+json
