## `eclipse-temurin:11-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:046d9a602d147b86787a9523e03b1447020191fc164ac87bf4cfe17fec41539a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7bf319e1a9a5efb2ef95b85fbe9f805c909d9aa3ef1475a857e96234b35dea69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160589886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc5f405e1c05efffb8675bc6f3d1030d41582fe1bb838ac546859ddb11a7576`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bd9bbffc5734efb01844a29a113ded889f4da3cda8e182581f06df7d1b2166`  
		Last Modified: Fri, 14 Feb 2025 20:34:24 GMT  
		Size: 16.2 MB (16175556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8886f759d872db74834cddc7f5de5e1d9dac42f43af6818800b460c7c7f23fdf`  
		Last Modified: Fri, 14 Feb 2025 20:34:35 GMT  
		Size: 140.8 MB (140769675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87b59c7b26a9d55a851b5445f42627ca08826874def4fe66efc11b30e2a73bc`  
		Last Modified: Fri, 14 Feb 2025 20:34:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0963aeeacb77ac39d9fdb8e3dbd9693ba930911be387409258faf61e0dc202fb`  
		Last Modified: Fri, 14 Feb 2025 20:34:09 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d71b22354221d93309dc26b11c814384355a3ca07dfa7e11e5e8382e67780b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1015448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d165abe71904dd955e6acf0b24497196cf820df108947c7c1b879e8fa7fb69`

```dockerfile
```

-	Layers:
	-	`sha256:efd7c10ee56f23809b0cccb541329130a30ed517068090b49afe97ca9b8ee713`  
		Last Modified: Fri, 14 Feb 2025 22:12:17 GMT  
		Size: 995.2 KB (995239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7c5cbb57144e5c58a421b80affefa7e38f5dd3b2429547a2cac3e9669fb1ba`  
		Last Modified: Fri, 14 Feb 2025 22:12:17 GMT  
		Size: 20.2 KB (20209 bytes)  
		MIME: application/vnd.in-toto+json
