## `eclipse-temurin:23-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:0201d625fb7777efbba99cdfc99805a58f844413f31b39af0b5cd14057d2b666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:23-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:36bcb71ce333fe9d789ea48e47d3ddb95a9e05ce7d86452732920e4f5ee2d094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190095451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d92f5dafbf399b79e53015d527adb336690ee881bca10668cc6fb06b6e070e1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b55c5c881a2fed17ec5a59feaa33d9263703b399d1bfae3a5eaed3f140aa4570';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='2c05c6dfea23a83fdbfaf5b03cc3cfd8d998c8069e930e0e585a39d4a99f3d99';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3606bfc1ff94989733a3efb303d50016e471489b714ed7daf1ae0490f80b52`  
		Last Modified: Mon, 03 Feb 2025 21:17:00 GMT  
		Size: 20.9 MB (20908716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02e9501475e83106c0e84ddee25cd2eac588c2e8f0420fbdcdf0d6f8fc1f694`  
		Last Modified: Mon, 03 Feb 2025 20:23:50 GMT  
		Size: 165.5 MB (165542611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9e4bebda8fa04819d9e8f002171cb240080cb024c4413c6d8313d5da284bba`  
		Last Modified: Mon, 03 Feb 2025 21:35:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b0c9453479824b697beefdd4f4a6e47fc09a3d0e65f2b8b1bc732ffb696fd`  
		Last Modified: Mon, 03 Feb 2025 20:17:50 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2e6c17c77f117760e1c750c27f0e8fd4b4009c48dc7175667ccd7710f5897384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1122879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d04decdee607decce282404ff4c47fadc0ef1beaa3fa55dda673023822ac44`

```dockerfile
```

-	Layers:
	-	`sha256:f90280f8b49e8cb68a7d9c4bb2d1f215cca2f29d636703817f21885599a8ae0b`  
		Last Modified: Fri, 14 Feb 2025 10:32:07 GMT  
		Size: 1.1 MB (1101436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899cb8e19eed870c1c6b6c8bc325a221ab99774d802ef65a95781727e8c8fdc2`  
		Last Modified: Fri, 14 Feb 2025 10:32:09 GMT  
		Size: 21.4 KB (21443 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5855cac300a93c09d3b6ae3b0695e7591458bccc93ccc52fca0a993149f6e487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188339868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6792da71cc7019942eaf0a653dd9f7828b55099dec81ebd4bae783b31de92ed1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='b55c5c881a2fed17ec5a59feaa33d9263703b399d1bfae3a5eaed3f140aa4570';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='2c05c6dfea23a83fdbfaf5b03cc3cfd8d998c8069e930e0e585a39d4a99f3d99';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceae889eece3aa36cf341c7932ef99f4d89a493af360439046e550e71531cbc`  
		Last Modified: Thu, 23 Jan 2025 08:04:11 GMT  
		Size: 21.0 MB (20965085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ac014d0f23ca2bf7377d7b0924fc88363caa8aa3626caf271f03e078df59e`  
		Last Modified: Mon, 03 Feb 2025 20:42:23 GMT  
		Size: 163.4 MB (163380016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7683d41d19879a68bb63398afd385926f8ee1656682373247b65fcd1a1a04b78`  
		Last Modified: Tue, 04 Feb 2025 20:41:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9b0efb10bf6ee2483a1d96b2fd983feb86d4f57ab99b2839d4241bf159e4d`  
		Last Modified: Mon, 03 Feb 2025 20:42:14 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cf5661f02e9c59521acb8f93fea30eef88f5d3cadecc287bb0ecc890fd31fbe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1272454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adf7c05da28fecb3e479ad59d28e7b51a94c6003dd7ddf321b56a97849e6795`

```dockerfile
```

-	Layers:
	-	`sha256:f8cd38650b4545412f8be7d0d85e2e33fc5d0aae5f78629d6ecc67d2b64f41f7`  
		Last Modified: Fri, 14 Feb 2025 12:00:49 GMT  
		Size: 1.3 MB (1250853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00dbd64c79b04a18e1bbaeb29e6a1cfd8eb344c839de4b15620812d05055470f`  
		Last Modified: Fri, 14 Feb 2025 12:00:52 GMT  
		Size: 21.6 KB (21601 bytes)  
		MIME: application/vnd.in-toto+json
