## `eclipse-temurin:17-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:4cfdd49f5b335b4e9deff08751b178d47fcef9e047a94318131084129fe2198f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ffd95b1fc7142e8d63e3cbf1836942db96542d1e1a53a079ce8c0c855d9662da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66810963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9204f1a4e3900edf953b8bee42dcb21041f03cf928cd4a625bced95feef1fd1d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:14:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:14:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:14:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:14:09 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:14:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:18:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3226a10cf4f7ef8f835148ce8737490f0cf63e38a1e3ba26cf1e05d9e28adf5c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:18:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:18:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:18:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9f9ac5610fc517155e0d020f98577d6ea9a151a84839cf23bfb721c67d756d`  
		Last Modified: Thu, 05 Feb 2026 22:14:22 GMT  
		Size: 16.1 MB (16081507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04810747ee286222060fa36fe1980f36795342a2d640590d305f61f18e0af64`  
		Last Modified: Thu, 05 Feb 2026 22:18:25 GMT  
		Size: 47.1 MB (47099184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bb90ee7740c0a480e3953e1de36631c66c2d35b7eb130283b572409ff932ad`  
		Last Modified: Thu, 05 Feb 2026 22:18:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e0fabaf1eb55a9ba3d06ac5b895bc95b72739dcd0c2adb3751ba9f8766897a`  
		Last Modified: Thu, 05 Feb 2026 22:18:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fd56dce9396ff4a60ca88cfa01ced50ea517d6c9fe2405c4fdc6eb4df536ce04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **908.5 KB (908482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0879db5415051a1ad643085192596c9315a223020cafda2c8ae2ed9d63d0d45`

```dockerfile
```

-	Layers:
	-	`sha256:f9d42016a3eb94cc357b5d083d49dc1ecc34ce5a84ec628ba557e13af772d92e`  
		Last Modified: Thu, 05 Feb 2026 22:18:24 GMT  
		Size: 890.3 KB (890268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ec798df16c128a093b782b252ffa1a43f361bf547ccae86d1a8906c24cf058`  
		Last Modified: Thu, 05 Feb 2026 22:18:24 GMT  
		Size: 18.2 KB (18214 bytes)  
		MIME: application/vnd.in-toto+json
