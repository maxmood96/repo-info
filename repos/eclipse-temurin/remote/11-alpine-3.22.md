## `eclipse-temurin:11-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:33101416691462934b9e77e59e562853c98273ebc4cd65871d0ddaed0b47ce83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b03689d305e6130142fc1641322b745266de216be78b5247d12962bbbf485a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161044155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8bdc2f675e229731b5901797cb7c9e94a4d4e5ced458093033c44f0798ab09`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:14:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:14:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:14:40 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:14:40 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Fri, 17 Apr 2026 00:14:49 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 17 Apr 2026 00:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699be1eab523c95bbfeef69e39eb2261148eb5a377b2d1279fd9937a8eca14d0`  
		Last Modified: Fri, 17 Apr 2026 00:15:05 GMT  
		Size: 16.3 MB (16316969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e330757c7de032ee575b4748237c44ec839b59f3d827f54bde166228f6591a76`  
		Last Modified: Fri, 17 Apr 2026 00:15:08 GMT  
		Size: 140.9 MB (140916587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e4b802a7fd80fe855483cab4b674d3c0885cd560aa4cb6eb37600d4e31b4ad`  
		Last Modified: Fri, 17 Apr 2026 00:15:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2633582c0a2a58cc0542f530a1e8849e3dea3ceeafbda08accbfd9a27c5079`  
		Last Modified: Fri, 17 Apr 2026 00:15:04 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7d4a5c4235a86024e5af21822a0ac4d70f08ae6dfe9ff17c303f5316e3e231fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1020780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c198023e90be8356c6b08b6990930af7af4eb5f7a52003d0a8d811f14efc27c7`

```dockerfile
```

-	Layers:
	-	`sha256:d757a023a37e8a3fa2cdbf015c0f825327b9fa320a963a304629722938acfbc1`  
		Last Modified: Fri, 17 Apr 2026 00:15:04 GMT  
		Size: 1.0 MB (1001611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ecb4c7e6f77f1f2e33214f9204e857e682b7dd83b7132e0c075e75b87cc159f`  
		Last Modified: Fri, 17 Apr 2026 00:15:04 GMT  
		Size: 19.2 KB (19169 bytes)  
		MIME: application/vnd.in-toto+json
