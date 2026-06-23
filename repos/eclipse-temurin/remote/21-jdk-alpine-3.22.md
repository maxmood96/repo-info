## `eclipse-temurin:21-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:ea9c4e878622d44f0db1d70e14b4ef648e414e88f961e2b9661097bc81389f62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:fd15d0ac4850d5b906c0954e7351b18754e395e2fbb7759c14013c9d02f25775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183302519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff66e965d12dd44534b156faf4095e1a221b5e3329b55c3fe9814c893157f91`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:10 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Mon, 22 Jun 2026 19:57:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:57:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c70729f3fa427816836a00daeb41bf2e16865b0d0fd49f9cc093d3c48441b7`  
		Last Modified: Mon, 22 Jun 2026 19:57:34 GMT  
		Size: 21.1 MB (21115760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b91cbb580745e2eb22f2b3ad42a915dd760c6d883555bbebf8c66edccbefee`  
		Last Modified: Mon, 22 Jun 2026 19:57:37 GMT  
		Size: 158.4 MB (158396754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7ee5d98789e02e3500e8e207c5963d76ea5e48dbe5f519229aeb3847e2bc62`  
		Last Modified: Mon, 22 Jun 2026 19:57:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f43f60d99bf7569dcd63b53d436da0c3872c83c8a39c6216fb4e3b89ea204a`  
		Last Modified: Mon, 22 Jun 2026 19:57:33 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:222d929750dba56793191c45d4840b9e3c29c4fd182b9374f5b055c402919571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1109372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4387920af41fa3b97d7bfe73c8c1ba69e8a0909227f3239ba4994c37ce5a9fa3`

```dockerfile
```

-	Layers:
	-	`sha256:f3cfee0de27b9717e92ee03ca1b7fb500b54fa32072f0589d3b0edd178e8056b`  
		Last Modified: Mon, 22 Jun 2026 19:57:33 GMT  
		Size: 1.1 MB (1088934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40cfae9da60195e0c69abab8af93a372e7b43ff8e91fbf08d3a7b0f0ade34510`  
		Last Modified: Mon, 22 Jun 2026 19:57:33 GMT  
		Size: 20.4 KB (20438 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a9f5acde3ba316c3818dda4a83133073658d172039f2c92b9fabcbb4e025f056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181690264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c9746f81b837f7aaa564127c51f942805b75bac2452533db3ec89d627b70f93`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:56 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:56 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Mon, 22 Jun 2026 19:58:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:58:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:58:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcace108d7f78b08674a6e234d2c1b8ceca06b91af098322eef7ebc23d400eeb`  
		Last Modified: Mon, 22 Jun 2026 19:58:25 GMT  
		Size: 21.2 MB (21165163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824c9905bd9699d89c2956e932500be9af96e4829de7d82e16137fbd99d0b68e`  
		Last Modified: Mon, 22 Jun 2026 19:58:29 GMT  
		Size: 156.4 MB (156402204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d07f7518fbbb05f6c65a2c0b79b89a2e5fde15459a3d4e2f4f4ceaf1a7f70`  
		Last Modified: Mon, 22 Jun 2026 19:58:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab2a9682f8c999c8b4b42cc35b437b44dfbdf44d7726ea13daab581dd97384b`  
		Last Modified: Mon, 22 Jun 2026 19:58:23 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c05f1e0ddab5e9d15c7f85676133eb06a6ff77fdd1b7eea27bc39197791a7738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63df314d60cf1fa5e1e064365885ed23bdd5f8f738cece417f2a8e8e584e7950`

```dockerfile
```

-	Layers:
	-	`sha256:9b2ffbd77959273055207f39c777363b9977920bd8fa694fe4584d0ffbe31324`  
		Last Modified: Mon, 22 Jun 2026 19:58:24 GMT  
		Size: 1.2 MB (1238936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ccce79f48871a57a370cbe449ea60beeed1c61318a92315bdb8268505201058`  
		Last Modified: Mon, 22 Jun 2026 19:58:24 GMT  
		Size: 20.6 KB (20560 bytes)  
		MIME: application/vnd.in-toto+json
