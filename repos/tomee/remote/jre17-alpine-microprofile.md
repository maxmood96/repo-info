## `tomee:jre17-alpine-microprofile`

```console
$ docker pull tomee@sha256:8b93a927519b6d3182959975dfdd5cbededddaa46677a5ae398ccb325d51c5ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `tomee:jre17-alpine-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:8ea844e89ecac5ddd0f47f25bca77fe3cdb825192f4de4b389ff15a5bbe71cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137962306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70247826f66335e72228b0175150f6598f5532356c2940f7a6e4c76dfccd25e5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='38c90337ca2471085f9292d24bec75413b4e56c7826ef25e150a40cc2f727e36';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Jun 2025 00:04:37 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jun 2025 00:04:37 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
WORKDIR /usr/local/tomee
# Fri, 27 Jun 2025 00:04:37 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/* # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
ENV TOMEE_VER=10.1.0
# Fri, 27 Jun 2025 00:04:37 GMT
ENV TOMEE_BUILD=microprofile
# Fri, 27 Jun 2025 00:04:37 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Fri, 27 Jun 2025 00:04:37 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 27 Jun 2025 00:04:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66c12a520b9eace736b92bf41240c7483e040e711ff64a857f45361e4321637`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 16.2 MB (16176522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa898b139fbf654b3535786328985e65debbedfbf22748da2ed23b70c2ce50ab`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 46.6 MB (46628593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6744199aa66ab985e37e72924f1568a6751afa2c508c42a1b3b945f3a8850a7`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dce0e52e6a8d74608859f62a4527e9b0c1c8fc882eadac6fa9076824efffb5`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e4a9b555f081a76bff58595c5095aedb6e5337b4dc23b0667a05d89e71c92f`  
		Last Modified: Fri, 27 Jun 2025 00:17:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd6c803776f36896fcab39ab3ca836f30cfcc4a0eacf0a53152ad9ae73250b8`  
		Last Modified: Fri, 27 Jun 2025 00:17:22 GMT  
		Size: 1.1 MB (1148490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7f5406db00dc54f2267a3b28fa03cc49280bb03936612975a37a2a6fa805ca`  
		Last Modified: Fri, 27 Jun 2025 00:17:22 GMT  
		Size: 75.6 KB (75612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59831cee5ecd4b44067911f0f3a34e29dac7236b02fb01018e3dbeca86191c32`  
		Last Modified: Fri, 27 Jun 2025 00:17:32 GMT  
		Size: 70.3 MB (70288234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre17-alpine-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:3a4d4717ff6c67c9d748e2a4c62e84c44fa0a40453c630c354efced6f7ff3e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a36ff6a2d22489918181dc59d7d29cb080dc5d42151b2dd4f30951b646b4b2`

```dockerfile
```

-	Layers:
	-	`sha256:199fd6f4e2001ee5c0d03a80a52e3dc052608717b30351ac1464fe0ee997c38a`  
		Last Modified: Fri, 27 Jun 2025 01:13:48 GMT  
		Size: 1.3 MB (1296540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22706964b9ffb2bcd03cdbce8bc728c72c50519ce917397e9de489c26bfc3ae9`  
		Last Modified: Fri, 27 Jun 2025 01:13:48 GMT  
		Size: 30.3 KB (30332 bytes)  
		MIME: application/vnd.in-toto+json
