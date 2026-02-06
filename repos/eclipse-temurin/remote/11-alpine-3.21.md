## `eclipse-temurin:11-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:035c8a910ecf047ad8baef6593d25084910b7eb040051207a45ec2cd0fdfc760
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bd95aac2c93d0e55a4de1b889c5a9e82d14ead814638dd03c0e8662ac500d489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160737527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f24e71aa9e14a06bc0b1e03296bdcdaea76ca0f160bf618a55a2e105e2fadb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:15:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:15:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:15:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa92feb649a4fb8d7d1fb59d25aefc768eaf769fc0146084a45700bdcf747740`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 16.2 MB (16174652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0891e0c6d15535fa3b4c7416765c6ad898083886343cd713c93467164e8a985`  
		Last Modified: Thu, 05 Feb 2026 22:15:30 GMT  
		Size: 140.9 MB (140916723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c49197c1699daebe1d7e8c5f9cb010f0ad90fdcc74bec6fb29e94d5d5e5b296`  
		Last Modified: Thu, 05 Feb 2026 22:15:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94d4c23b54dea844a1f43a1c762f06f455eca428bcbfebca78b796dda310617`  
		Last Modified: Thu, 05 Feb 2026 22:15:27 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1a3fcec81a150d05252806bfc2759571b27d4d11530116fb6799b80e23d46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1019909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f59ea8aa3186c5603bc11dc52efa409af6f9721f661ae18968f29a11be449a5`

```dockerfile
```

-	Layers:
	-	`sha256:e834e7aa02761a4a52398d5af28bf95ca3764cdb8c20c90b6b722e9f08ef4ed5`  
		Last Modified: Thu, 05 Feb 2026 22:15:27 GMT  
		Size: 1000.7 KB (1000739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6b5ed2d9a4192c0d76398970ecf2daea0167749648e879474549ca8e3dd291`  
		Last Modified: Thu, 05 Feb 2026 22:15:27 GMT  
		Size: 19.2 KB (19170 bytes)  
		MIME: application/vnd.in-toto+json
