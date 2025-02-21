## `eclipse-temurin:11-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:02e570d34c7eb6d43eb3fab8d53d3277b2b927e5acab8566392a9d884df9d04e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f8f635caec27964beff8fbf1016f1eff15630f2985b56b765cce887175720f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160422314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f510f10b0ea9a9b2ef85eacea614a941b8a90d95d5a6e9a7b5577bc03520ebd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2e1f667395cdb1e872bd7320e3eda96c0f0978e29e574e75f9cdf61160e8974a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf3f2e42769e3299bc683c57ce4fefd34dc88d2c4a3597808ac7d21f76e9968`  
		Last Modified: Fri, 14 Feb 2025 19:25:19 GMT  
		Size: 16.0 MB (16023347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dece8a3c0cf17032f41e96e92c176e934e4370faf8e69c1cdc59562f88ee5c2`  
		Last Modified: Fri, 14 Feb 2025 19:25:20 GMT  
		Size: 140.8 MB (140769659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7abaa76ae3d91dfc7e60c3a65837995ec30a9f23a94ea0a4eb10d80cc49a05e`  
		Last Modified: Fri, 14 Feb 2025 19:25:19 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7be8a1ed75802683285c6f70c11d6fb09da8e37b45263a566e7b6feb641471`  
		Last Modified: Fri, 14 Feb 2025 19:25:19 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4d6d5f155869c5b8a54cf17cbc0ef2173739131ebe08377d81ed23e843de49f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8865390e54fe14ee360ef63c807d31bb686f775a641a14691ce1f1436b8d2f7a`

```dockerfile
```

-	Layers:
	-	`sha256:cf474ccde6b3e2fc600c2095256002bec8e41e32387009b1e5ad99ee04220c2f`  
		Last Modified: Fri, 14 Feb 2025 19:25:19 GMT  
		Size: 987.3 KB (987346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647dfda0bd40e0b05c06e3452c272dfbe9c1a2a69a49fb1277b6b1ce81f31b54`  
		Last Modified: Fri, 14 Feb 2025 19:25:19 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json
