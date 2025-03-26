## `eclipse-temurin:24_36-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:7b2b481c0d8d9575d0b5739256c54b54ed6dd86b8ae09820e6aa33ba3a06cc9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:24_36-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2e82dd4b77052695e36a8fd544c0184ec5f68ad96619c94a748c243ae6c311ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114669589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64685866abd304530bc1a74b55f4b2bf98ebf88eb7ed99af525b61cfd87193e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4a673456aa6e726b86108a095a21868b7ebcdde050a92b3073d50105ff92f07f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='a642608f0da78344ee6812fb1490b8bc1d7ad5a18064c70994d6f330568c51cb';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9e4e6bbb3d8fe7ba4feb76b9f85cc591b594ed37c725031140c217b982045`  
		Last Modified: Tue, 25 Mar 2025 21:57:50 GMT  
		Size: 21.0 MB (20950921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09b1f076e8ade81f12374738d4768afffa7e33753b8e5edec2e7165fd328397`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 90.1 MB (90074010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fee87929fdd34f08d09385a3965e44dcfaa3724ce5f1a2515708890b07049e`  
		Last Modified: Tue, 25 Mar 2025 21:57:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d237c308bf2aec9726a2aad84026d710a041c7de9ee1603fe9726cd1491bed2`  
		Last Modified: Tue, 25 Mar 2025 21:57:49 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:804282c0581466bfbe1d36b91327028a3b54f7b464a3edd0f6c2c2c451b87add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1069069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee76bb72cd154c2484d2ee7f14537651b22461b0c5ff234582da921f91fe05a`

```dockerfile
```

-	Layers:
	-	`sha256:e32d55db0aebfee481c4b0cdb30d39b240f5dd134263c44d65e2c1f65f256260`  
		Last Modified: Tue, 25 Mar 2025 21:57:49 GMT  
		Size: 1.0 MB (1047679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d9edba0f567942c7178a23c14ce8f1e1395d18681ff480240e357e9fdbb7da`  
		Last Modified: Tue, 25 Mar 2025 21:57:49 GMT  
		Size: 21.4 KB (21390 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8f3616540a21f35dd288aa11572eb1276293f9d7c8b3a35e5658011de06562f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114068029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f56da2741b1e7e0c50a687558580bef843821253d1d96ccb59c066ae0b225ac`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4a673456aa6e726b86108a095a21868b7ebcdde050a92b3073d50105ff92f07f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='a642608f0da78344ee6812fb1490b8bc1d7ad5a18064c70994d6f330568c51cb';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f842771dcdbb28ddb6a422c590c5f3e15a297ce1682b299a55262a41a82054a5`  
		Last Modified: Tue, 25 Mar 2025 22:02:38 GMT  
		Size: 21.0 MB (21005979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d68017f3baed76b9a8df11f4e768ceef349ed0219dce6150cd06b9eea13bcc3`  
		Last Modified: Tue, 25 Mar 2025 22:02:40 GMT  
		Size: 89.1 MB (89066611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c279fe722887fc47203b0801f2a62e834e7f9dafe6491f4856c6759757b0dbb`  
		Last Modified: Tue, 25 Mar 2025 22:02:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338963c04c16d3cca3bc7f8354470f29dad0b65bd206ab5a02ad73d87373ab1a`  
		Last Modified: Tue, 25 Mar 2025 22:02:38 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:add7f0ef876dea2a4f7157facfec5d7d27e1841b0f2c9c9f80751091e3422ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1219262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f1ced7b3e2141affe44ebb487be58beb80700bd8640ef7c501e201454f8e62`

```dockerfile
```

-	Layers:
	-	`sha256:ff27fa0e8c625fd95d6a918751547f82f6feea5e12bd3bb2d2cead6cf85dc23b`  
		Last Modified: Tue, 25 Mar 2025 22:02:38 GMT  
		Size: 1.2 MB (1197714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0584f90b7173c73d3a470e7a523a0a37f9ade283e1dd58267dd4e50918494b5e`  
		Last Modified: Tue, 25 Mar 2025 22:02:37 GMT  
		Size: 21.5 KB (21548 bytes)  
		MIME: application/vnd.in-toto+json
