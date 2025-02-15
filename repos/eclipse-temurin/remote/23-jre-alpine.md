## `eclipse-temurin:23-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:88593498863c64b43be16e8357a3c70ea475fc20a93bf1e07f4609213a357c87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:23-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:55d6ecee9ac7a76bc31d76eb51755f3c98ae8a088dda3590155061266841190a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72952973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52bdbc6758fd8a9e5fc3000fe16f229b613bbbfa0198122956f007153133e30`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='248a2ffb3abcb0cee7841ce648af7af415c96ee88cba4f8bf676c0115d38de5e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='4513750bd10cc6c38f0c19d335dac7dcc112bba64e52010f81ba29e7a71e2a76';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b4ddc782f3e1e82e9337f6eda5a81568faa000d5333ee9c1a73da8e32060ef`  
		Last Modified: Fri, 14 Feb 2025 22:30:13 GMT  
		Size: 16.2 MB (16175601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956bc91adb8d54245b80bec4f02859d8a2a546dca77c48ccdc98a8b3ac4d40fe`  
		Last Modified: Fri, 14 Feb 2025 22:30:17 GMT  
		Size: 53.1 MB (53132715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcb7041227e1e17f23bb4c72ecf53934cb71f6edb103a666e4bc6d6513f07b6`  
		Last Modified: Fri, 14 Feb 2025 22:30:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d8cc948f02df41d9ab39eaba03df0d8a8ffd482e188736c72fc8a9b1e913f6`  
		Last Modified: Fri, 14 Feb 2025 22:30:18 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1b1218f2567670d9d856f77cdb9c1704b776d66f3da5f46b2c31c89546e4df65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.4 KB (914395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9d0080b84e5d37cf7e598b6cd01b0cfe33631dbe21623b6eb6e9eb5152c39d`

```dockerfile
```

-	Layers:
	-	`sha256:20809389c2ee8d9bddb564dd7ffc65c0ef2e1f53ea85e08856fe5e47475ade33`  
		Last Modified: Fri, 14 Feb 2025 22:15:30 GMT  
		Size: 894.7 KB (894668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab5133e8760f03bc8926aa0d23564363637f22a53cf3de7458d41cca28531119`  
		Last Modified: Fri, 14 Feb 2025 22:15:30 GMT  
		Size: 19.7 KB (19727 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6cc988f1cc9241a17033e1a011b4a9feaa9328eefb7feec6b177e97ce35922ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72256908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69436354174adba59a9d04fdfc334a1b8d3aafe0ceba84fc096f37a5c349c5cc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='248a2ffb3abcb0cee7841ce648af7af415c96ee88cba4f8bf676c0115d38de5e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_aarch64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='4513750bd10cc6c38f0c19d335dac7dcc112bba64e52010f81ba29e7a71e2a76';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jre_x64_alpine-linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ef25395adf8ce8e3c308217ae1b2fe858832aa585adde8a15afea0afa6aab9`  
		Last Modified: Sat, 15 Feb 2025 01:22:18 GMT  
		Size: 16.1 MB (16138226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e648272ede2b0e62d8a0c6381cf539bb673284707cb043e4e039b709995259`  
		Last Modified: Sat, 15 Feb 2025 01:50:06 GMT  
		Size: 52.1 MB (52123245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e560400de7dbd8eafb93f37175d85b75eb46bce3add348a47803c00877cc2a`  
		Last Modified: Sat, 15 Feb 2025 01:50:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced48deadd3199a1635123c5501533a86232afddb5e68a40aad9b7860a50b37b`  
		Last Modified: Sat, 15 Feb 2025 01:50:04 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e2c14d6064dab31d753adf2e1fd159d5fbb2f2d18b37b81aa0a343b9d629c227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **913.3 KB (913346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0511073f8dd130cc70c98f025e6d048a6637a4eba18ba61b759965681c9ca6f3`

```dockerfile
```

-	Layers:
	-	`sha256:cd0241d5e7fcc26687a1863c06da187461ca4f4a0f9043f00bb12ea5cb01a52d`  
		Last Modified: Sat, 15 Feb 2025 01:14:54 GMT  
		Size: 893.5 KB (893485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291a876aad45a5f0e351d778987248f647c1608ddcd03097e00651ad9cea3b15`  
		Last Modified: Sat, 15 Feb 2025 01:14:54 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.in-toto+json
