## `eclipse-temurin:21-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:de8fb8a9519be119b275af9f3962ec31564acdc8f08fbc8a17aea9774baf27ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:aba8bc68b781e7ae3eb71a1e0413a52347ba43b479c071b11341fbef51406333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182093926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01229e15d68f8c071b2630bee3e0e13c42abc2a3b986d805789d7bcadb359c0`
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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='2798990401d9c47eaeddb7d5148f577770e4c1013b9223290a43765463204ae4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='6c66470a9143ad562570a34c1583d9fa50bf904f6f9ced642e9d800ce043a0f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516a502606e8cd798051ccb08fc256c430a75341a9acb17bdf1bbc6804294041`  
		Last Modified: Fri, 14 Feb 2025 19:25:39 GMT  
		Size: 20.7 MB (20667769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f43d0a0d45d4fb0142de630a21a0c14d0f3fff707126db671582fb6fa0544`  
		Last Modified: Fri, 14 Feb 2025 19:25:41 GMT  
		Size: 157.8 MB (157796849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0b904214820dff00364b185948ca785a47c7fd16deb47767771d0835f9259`  
		Last Modified: Fri, 14 Feb 2025 19:25:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049f824cd49b3e51c906f07faa37074e34368f19c3679a20f9ff25e70fa0eae3`  
		Last Modified: Fri, 14 Feb 2025 19:25:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4f7ce9a6012eade07f219938ab88027a082029b26958c2f5114368348e83d912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1087673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efded3cd669e0935bc07c93915e12576707c8b7f735613c1af651bf4aa7ed495`

```dockerfile
```

-	Layers:
	-	`sha256:7e82ee23bd2372c627f21d63936976fb0416e50bc823fe068381b25272255874`  
		Last Modified: Fri, 14 Feb 2025 22:14:22 GMT  
		Size: 1.1 MB (1067224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b633873a0d18d326b48d518569ed45c5802c4714cc64a64c8ca6099f4f15fcee`  
		Last Modified: Fri, 14 Feb 2025 22:14:22 GMT  
		Size: 20.4 KB (20449 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:9b9cfd52b0965d45d4a1a0ef57fb8671c0853649129b5cb0887e025389274f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180926735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c172cb1ee4d0db43fe74ba8db84d445474b084426c44d20b4028b087db51838`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
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
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='2798990401d9c47eaeddb7d5148f577770e4c1013b9223290a43765463204ae4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='6c66470a9143ad562570a34c1583d9fa50bf904f6f9ced642e9d800ce043a0f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b57795d9838d4ab7da718bb75c1aa894db71d000660f5159c42d40d07be61b`  
		Last Modified: Fri, 07 Feb 2025 08:23:42 GMT  
		Size: 21.0 MB (21045569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a028d463b58d7c99fd2aa10948ed0523becf1cef19f396f9f2897b16a2bd18ae`  
		Last Modified: Fri, 07 Feb 2025 11:24:55 GMT  
		Size: 155.8 MB (155787986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d421a371ac0b6197944ea3ac5aa768a689a3066a423bbfe7013602d55130fb`  
		Last Modified: Fri, 07 Feb 2025 08:23:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed4c4dfcedf4c3053176234c90a5425f025fb0aea83f2f288136b87b23caa7f`  
		Last Modified: Fri, 07 Feb 2025 11:20:55 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7d823ac6ed768c429dc42994742dacd50875b081e99e6d2d792d42f17d973314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1192315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f9240e18bb551f17ac521eb49fc1d2c9aa1fc060e706fa24ccb25af3978320`

```dockerfile
```

-	Layers:
	-	`sha256:8dcde0357719ab789bddda31e58908f0d09df2f9bae4413490c0e48b2195fcf4`  
		Last Modified: Fri, 14 Feb 2025 22:14:23 GMT  
		Size: 1.2 MB (1171744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7b5fd6006ea486964913dd1f440b8f177e6019f88f92fc7cf0137c49b609fd`  
		Last Modified: Fri, 14 Feb 2025 22:14:23 GMT  
		Size: 20.6 KB (20571 bytes)  
		MIME: application/vnd.in-toto+json
