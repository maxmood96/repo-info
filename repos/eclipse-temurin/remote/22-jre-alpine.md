## `eclipse-temurin:22-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:cff33794a241b7381015bcb2fd3c21de05bb573754b1a95165d476edb148cb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:22-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4c15065e58b4af5723191bfe2a08d7df0a53b3c0f3acd46f9125032fd8f5ef13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65019746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2069b353c6af37194d8613379afd40c30d9e87bf9d72948c5eb071b368d3fa5b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb3885be4b9f555d70d534dc1ac22d07bbd3a9246a6c56ad69897208c2d750cc';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_aarch64_alpine-linux_hotspot_22_36.tar.gz';          ;;        amd64|x86_64)          ESUM='9b94b27229d21b74f9484b5963fd9517561a99a98f46c3f29c4b28c311e091a3';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_alpine-linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21a63612cbe8d148f75173be90696fbe03e2a6e9c901e2c039bcf1bcdeec0b9`  
		Last Modified: Thu, 28 Mar 2024 02:02:51 GMT  
		Size: 8.5 MB (8537401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90354418ca4b0fc99c3b22071351208c058619a6f8fde91e0e5c728ce24c4fba`  
		Last Modified: Thu, 28 Mar 2024 02:14:35 GMT  
		Size: 53.1 MB (53072728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbed6bdd23426289b320e4a99454c17c491947be893adc8b8a252ac01c79516`  
		Last Modified: Thu, 28 Mar 2024 02:14:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822603f48d992501ce4b5141590f17d0cb84ae43e14adcd9b332b584f85eaf3d`  
		Last Modified: Thu, 28 Mar 2024 02:14:28 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:450d7fa496bbbfebc14a77b6ebce3b2dee5ee1e6cac8b61a13c68a35f4aa9573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63971071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6242e6ce4d18848b04cf73b86201517d28dec5a3c4eb78068dcf8f3bf050a9c7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb3885be4b9f555d70d534dc1ac22d07bbd3a9246a6c56ad69897208c2d750cc';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_aarch64_alpine-linux_hotspot_22_36.tar.gz';          ;;        amd64|x86_64)          ESUM='9b94b27229d21b74f9484b5963fd9517561a99a98f46c3f29c4b28c311e091a3';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_alpine-linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336bedc657c1154d28325d2a957fd6433bcec36ef3d4148c5dc05764246f2305`  
		Last Modified: Thu, 28 Mar 2024 00:55:36 GMT  
		Size: 8.6 MB (8610228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6592b865254cb1738226c160f12f4d3a769a73f9a4bb966c7a56c37779709d3`  
		Last Modified: Thu, 28 Mar 2024 00:57:25 GMT  
		Size: 52.0 MB (52012241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4162bad29aeb9556138df152e24e410d5bd920265efd9a8956796cfee34a1fe4`  
		Last Modified: Thu, 28 Mar 2024 00:57:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6471b431a667c61fee0291cfa50e2de28c5e4785f93e91a9fd27e336264b10`  
		Last Modified: Thu, 28 Mar 2024 00:57:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
