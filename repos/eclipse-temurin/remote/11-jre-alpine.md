## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:1cc1ad1955d30f45362175ae99414a2fc632383cefd2d626f823ec6d56523ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f0b030c2fcc7e5a5f790ad7a3ab1c26b5225ad67a9ef169ae2ef7d8d8117a24e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56140197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5348b07c1702d084639b26118fb84f2ee942284a4a5df999d13733bacfc65d1b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:11:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Dec 2023 07:11:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 07:11:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Dec 2023 07:11:20 GMT
RUN set -eux;     apk add --no-cache         bash         fontconfig ttf-dejavu         java-cacerts         libretls zlib         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/*
# Fri, 01 Dec 2023 07:11:56 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Fri, 01 Dec 2023 07:12:23 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6a3d1759bdf91433411d37ca2ad1505a7f214c1401797834e9884165c2457368';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 01 Dec 2023 07:12:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 01 Dec 2023 07:12:24 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Dec 2023 07:12:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ce2a3866efc31d675066df134952e4237faaf14332528051e5efca30a21a4a`  
		Last Modified: Fri, 01 Dec 2023 07:14:41 GMT  
		Size: 9.3 MB (9276515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697f379a044ca90f8bb226a30d63143556894f17f1f712db02dfd722d2197262`  
		Last Modified: Fri, 01 Dec 2023 07:15:47 GMT  
		Size: 43.5 MB (43460367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a7c79bb3e25dfb538643f08ec72134f715116ede71a64ccf9032a6bcb2d22f`  
		Last Modified: Fri, 01 Dec 2023 07:15:42 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfd3b7886029886b45e28ce2bd96fd3f1ae4a927ad5fbd5283b2fa9e57a7c40`  
		Last Modified: Fri, 01 Dec 2023 07:15:41 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
