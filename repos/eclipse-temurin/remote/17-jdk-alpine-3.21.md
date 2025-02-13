## `eclipse-temurin:17-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:6b35cd5d4ae2866fce49e3a86abe080c8410ceb10e1d51476f79e63b14d1c4d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:84ab9f8337afb11532aa04a75fad4bd8a120665584d361b714ddd183a57dc573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168269217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22cd0aaf73e1edf2dff131783adfe68ced29debdf1555926b446158dc405ded`
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='259c85e16f7bbfdfb3e0a2ec1c5d6e2063300d413422286583265a9d8a882358';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:e964c090714275a4065e7acea241466fc487f2081bfb24e52722b02aa023934d`  
		Last Modified: Mon, 03 Feb 2025 20:16:58 GMT  
		Size: 20.9 MB (20908693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecda534f804788bc889d59c4e16afbcff57b89cab14639f41351998e0f6c354`  
		Last Modified: Mon, 03 Feb 2025 20:42:11 GMT  
		Size: 143.7 MB (143716399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c1b586d223d730dc8abb27b6539523713b21fc6623d20b76cbcb67e56f94ce`  
		Last Modified: Mon, 03 Feb 2025 20:32:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43895d73efd1a8a528e3d0fea9b8b264f32ef501fe42aedf37f113017882492`  
		Last Modified: Mon, 03 Feb 2025 20:14:43 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b658caa69587d3973542240597c55a3f7f5c75d299d9d3b7b72e71b7360c027f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1117085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ebb254be3eab892504ff94a84bd1e01315fac36c7b1a05c8c2f56fb7a7b085`

```dockerfile
```

-	Layers:
	-	`sha256:4557b1a9aa7c2d92e86e7245855d66227bc5881339b700ca51eec712b9a26e0e`  
		Last Modified: Wed, 12 Feb 2025 10:33:11 GMT  
		Size: 1.1 MB (1096435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef1ed3bc37e2378f52f06138c84d6242c5a81fa23f012ccd82591523bb79510`  
		Last Modified: Fri, 07 Feb 2025 18:11:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json
