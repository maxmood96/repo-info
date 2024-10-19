## `eclipse-temurin:21-alpine`

```console
$ docker pull eclipse-temurin@sha256:37abc85b7046a2301ce60e76a28ab07a339e864fd9376c4b44b64b07c44a52d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ba5efc1e5c42597c350bcd1c742adcea7ea4713a0a815a7ce65b1bbab4b44efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176474084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4fb9e4ed7605aa5b69b4c2c80de9387a1c664ab65a4bfb04a64b3206f9bdba7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca5acd076b6b247150e53c4b3d290f2482f5db4874a00a1723060c42a082784`  
		Last Modified: Sat, 19 Oct 2024 00:55:14 GMT  
		Size: 14.0 MB (14032615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e03e32cb8679889260ec6080d73bd68a90a2c5bff446ccc2d0943214bdf06e`  
		Last Modified: Sat, 19 Oct 2024 00:55:15 GMT  
		Size: 158.8 MB (158815427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dce63d44a5acb91b5e3af5e7fdec0fa5d37661dd0f44de718bfd5462393c5c`  
		Last Modified: Sat, 19 Oct 2024 00:55:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55ad2cd42fcd56490fa6e1c1707a8a5c584502931a063cdab7f0c28cabd9a47`  
		Last Modified: Sat, 19 Oct 2024 00:55:13 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9bbbcabb4f2b977b1c13675467ba9f0da181b35675ea660a05027ee2048a39fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.7 KB (983713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e290ed02ce13b942060c2ef11029d6986287303edbdacabec04f982404e380a`

```dockerfile
```

-	Layers:
	-	`sha256:0d58efc8b7d1a0b7e94a93d788f5bad763501a4327368d5b8d8edf88b87fef6e`  
		Last Modified: Sat, 19 Oct 2024 00:55:13 GMT  
		Size: 964.8 KB (964820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9145ce1d748dd0ca7e2cbce40f322a4ed0f294e59a932f109ecaed245537ef7d`  
		Last Modified: Sat, 19 Oct 2024 00:55:13 GMT  
		Size: 18.9 KB (18893 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a22ee5cb6481406b26b2d0644971f2ec5546ca28419f355848c4f9aa71b557b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175180483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3151ed266c720374c3e9a966e32978bd0903a75578684ffaf3bf42f537fdd7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ffed20e52cfa038b814b564cae31f18768ff4978e451b3979a4568ce125972`  
		Last Modified: Sat, 19 Oct 2024 01:17:09 GMT  
		Size: 14.4 MB (14362084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2388756f8ec65c140c36713213b6565416269860aea13b5566de8b44a4b0c`  
		Last Modified: Sat, 19 Oct 2024 01:17:13 GMT  
		Size: 156.7 MB (156728518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6f36a89d33f6b9c381a9fc7a6884cfad92a3803e97d8fcad7837b34b1092ae`  
		Last Modified: Sat, 19 Oct 2024 01:17:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e51964a9dcb1d8f1b1ce17616e80685d60888a9d58cb84f6f88d46ac28e5b7`  
		Last Modified: Sat, 19 Oct 2024 01:17:08 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1b6920416925e9b3670ffa6a5d4a759695299783c89aa04a67c1ec8154c7cfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1088510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacef24290194c278b7b1bd6c65e614a5fefc97a28b5a3a01ce7c1a4dd8cc7fb`

```dockerfile
```

-	Layers:
	-	`sha256:964a2ced2ce923997905c40a38700f10448fc77bd7385172a1bff7a3014407fd`  
		Last Modified: Sat, 19 Oct 2024 01:17:08 GMT  
		Size: 1.1 MB (1069501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57daae93897238a7dd80b24cbde2adf5f2f892df0dd2740b2aeb4ed4c531f4ce`  
		Last Modified: Sat, 19 Oct 2024 01:17:08 GMT  
		Size: 19.0 KB (19009 bytes)  
		MIME: application/vnd.in-toto+json
