## `eclipse-temurin:21-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:02530d421294840308bd3dd026ec204e0ba62fc6f644e2694b77924bfa29c083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:169ae852d3f57bebda9b247bf7318471ece4297b65837b951fa36384f581e8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182611747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564580d8e7805369e209604621f32fd862e2537f9e1da5611bd15a33dbd84847`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4773cfdc59d66b75f4a68ac843b2b5854791840114cf8bb1b56fb6f7826ae498';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='73c4cbe10f4f385383d9cb54d34f2bee2c68b5265f9e3d954f3326948c40c0be';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2253a4d43fd45e951f421a2ea55e87aa04e396092dc2a418aec3f1c56922fe1`  
		Last Modified: Mon, 04 Aug 2025 19:11:48 GMT  
		Size: 20.9 MB (20942672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5722c9c4fc13f7e2c3ba0bfd2f0307ca369daefbefabd9b6df0404d3e1ffcba3`  
		Last Modified: Mon, 04 Aug 2025 21:21:03 GMT  
		Size: 158.0 MB (158029095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d416d465d741db836b79714e6bcec80502300d722f119ad8743e79febc8b8922`  
		Last Modified: Mon, 04 Aug 2025 19:11:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee1666465fd9f5d1f3950040cdc75c3c349f5462e1187f4847892fe8b6a1b40`  
		Last Modified: Mon, 04 Aug 2025 19:11:44 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0716b173a38e4b62add3845cf0dfbcdcd8e6b7f588353f0c67261d3cc0be711b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1122154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5c43ca9ca0da9a225491fe0139a942320900dec8a6b9adbbeb3995cddb2c79`

```dockerfile
```

-	Layers:
	-	`sha256:33fc9f286d1edd3c6c3d26f0d3c303a4198226214e459adcf6180151a95e753d`  
		Last Modified: Mon, 04 Aug 2025 21:20:33 GMT  
		Size: 1.1 MB (1101705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f25d440ad4400c64c7f1caf67b4491b23c3a58b60a1aeb7caa1cfed748ad9643`  
		Last Modified: Mon, 04 Aug 2025 21:20:33 GMT  
		Size: 20.4 KB (20449 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:dc79fa32411a715dbeb815c333ff1eb5a45cab4ca368bbd82789c6a5f939d255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180998434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45f4e88f0576f203f6dd3b25a1ae48ea373bfbab99bbfcfb714cd16a3e98af9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4773cfdc59d66b75f4a68ac843b2b5854791840114cf8bb1b56fb6f7826ae498';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='73c4cbe10f4f385383d9cb54d34f2bee2c68b5265f9e3d954f3326948c40c0be';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4921d16d47a336ad3c37c50ee608abc168d7bd9b1ace231696f3bab3de28839e`  
		Last Modified: Mon, 04 Aug 2025 19:31:17 GMT  
		Size: 21.0 MB (20986434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd475c8abc8ae8cf26531659778dfd70d8499d5a0adc1948624c297e9a42162`  
		Last Modified: Mon, 04 Aug 2025 22:17:03 GMT  
		Size: 156.0 MB (156022653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b625bb612752361a9dc21ec1fa3358e25fab94715b96283611e77ab0dadf99a`  
		Last Modified: Mon, 04 Aug 2025 19:31:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b0e0927b110f66ac30f422df15634d6abb87481bfee805eb1cf5b7120ed3f2`  
		Last Modified: Mon, 04 Aug 2025 19:31:15 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9306390615d96023ca2b52728e69c93c2e042e3c19e45a88ba9109d65abf8e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1272278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1423f03a93d892015e00f966619f2f81901bb65782a457eadd4cc1497c83b86a`

```dockerfile
```

-	Layers:
	-	`sha256:a22880959e4603b62b5c302245912bfcb08817830579c02da0f5bb74e4b9a2f9`  
		Last Modified: Mon, 04 Aug 2025 21:20:37 GMT  
		Size: 1.3 MB (1251707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c246d5b361db3a805b7ecd15b14d75e8023337938eb3d8cd0fe3483bf930e57`  
		Last Modified: Mon, 04 Aug 2025 21:20:38 GMT  
		Size: 20.6 KB (20571 bytes)  
		MIME: application/vnd.in-toto+json
