## `eclipse-temurin:21-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:7efc6ff7398e11cecfc16395541afdcf335ec5b26c84e718d7f1de8322976819
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d1deca18295d70ee2ab4096adc9412225e75cae557affb18acedb5a0b64563f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182312714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fee3658e2562214fd156d010f41f59b4ba508a68deb2734b444a26e6efaffa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
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
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235ea4a0a9071588bfac816cf893a98f514dd4fe270860fa2e2c7df4bc2f589b`  
		Last Modified: Mon, 04 Aug 2025 22:26:27 GMT  
		Size: 20.7 MB (20660778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c13f069fd8a643be7f1e0a72043cc7a1fb2949b5424ef96a4f9b8b6b704dd5d`  
		Last Modified: Mon, 04 Aug 2025 22:26:32 GMT  
		Size: 158.0 MB (158029050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ed3111d6419a5367889b36ef818e830c05dbd3a71e734108e9c204d5ebc1ba`  
		Last Modified: Mon, 04 Aug 2025 22:26:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d23bb5eb8f811c49dae8f456527014d33599bb070f12294d58ce498048c7a1`  
		Last Modified: Mon, 04 Aug 2025 19:11:53 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e3afd428746afc6aa7280ca104002b3e624addd498745e7c4e1c3574ed7a82e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1090479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eae6a6af51e10b61a1e255b884155f379fdb294025ace5a73e6091f7983131d`

```dockerfile
```

-	Layers:
	-	`sha256:f75b2b7dc747d14f310568eb53dda782b66cdae9af47e19d58bbb5f2eb6d7185`  
		Last Modified: Mon, 04 Aug 2025 21:20:26 GMT  
		Size: 1.1 MB (1070030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f9ba4b910acaf34c25458bbb9802a93533da213984f29671de108fa896d57b`  
		Last Modified: Mon, 04 Aug 2025 21:20:27 GMT  
		Size: 20.4 KB (20449 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c1da194f922d35bc46b814cb8a32952881cfb88c1bef1e92ee8eb4b33d16ae7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181155474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722d16c701ad2dc19897b56eddd79305c7df3c4d657cd513cdf4451327ac0a3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
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
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae8cda0c55c50548d42c876509a4c3dd19d9693be2b24556d3df167328dbc14`  
		Last Modified: Mon, 04 Aug 2025 19:30:30 GMT  
		Size: 21.0 MB (21042009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c424e38d147468fbe1e5806c38661d3bff93a15e777aec859da45bca4499f589`  
		Last Modified: Mon, 04 Aug 2025 23:31:42 GMT  
		Size: 156.0 MB (156022686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb113d140186a063684b9ef992d08df4d24eae1c3fb4c664b7949eddd204bf`  
		Last Modified: Mon, 04 Aug 2025 19:30:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c673a0bfd1ff70abaa15482156f2acbe4c96cd6cb37d4e26dfce66ae5d94114`  
		Last Modified: Mon, 04 Aug 2025 19:30:28 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:71a4a3bd313a19bdcb549e18eabedb0e705bf527a12452db39304ded701fc3a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881a2f7c346146f281abfe2306b04458f46b691e29ac4beee8ee0af99c9da8bf`

```dockerfile
```

-	Layers:
	-	`sha256:abdf0d81a3f9f4da4936583cbb0ad821ddd7c78f1dd6517fa799d40a36b91463`  
		Last Modified: Mon, 04 Aug 2025 21:20:30 GMT  
		Size: 1.2 MB (1174550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e2f34ac92f9de5b3cb068a1b5402a23c9d36c68195ee1d5d6675acdf30ded29`  
		Last Modified: Mon, 04 Aug 2025 21:20:31 GMT  
		Size: 20.6 KB (20571 bytes)  
		MIME: application/vnd.in-toto+json
