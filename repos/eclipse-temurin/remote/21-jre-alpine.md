## `eclipse-temurin:21-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:2d07bba7442286e91cb8b0583c364b645ecbf2ab4b0c8e0eabeab7832bade793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:21-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3dc44495ab3b9409393e7b9de1ea70486d77468d053d9c79d95cd3a458599ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65686961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521ec2dbd4e32371cdc3619bfe91308da2e87eb57d8b57dd3167b562153dd7ff`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 14:52:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jul 2024 14:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jul 2024 14:52:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jul 2024 14:52:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jul 2024 14:52:20 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Mon, 22 Jul 2024 14:52:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f9410264235861deaf30f97bec80870cf3bc38b1d8e57d897d8bb1f706ae6705';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='0dfd0ebab44d777f65bceaff7f79e8e0b9deb74a5eb166922483f1864bcf2052';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jul 2024 14:52:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jul 2024 14:52:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jul 2024 14:52:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b502c76566e71337b4737a25ae762dd54193bc78dba7f7474ea005c07de9efc`  
		Last Modified: Tue, 23 Jul 2024 01:08:16 GMT  
		Size: 8.4 MB (8371901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c98316ca78e8531c662ff55318b692ee7c7b3c0e890207d4b049bfaf1d620e`  
		Last Modified: Tue, 23 Jul 2024 01:11:01 GMT  
		Size: 53.7 MB (53690593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42500819bdcab9903ebb5bad490e671e17b400db43247a31203fa11c1a37fff`  
		Last Modified: Tue, 23 Jul 2024 01:10:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1673c1a2cfa7b5313925f7e710603974824e7b9f1d2295477d77356337f935e0`  
		Last Modified: Tue, 23 Jul 2024 01:10:57 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:fbbccd0b5da2992109e371652af9d52491316857d007c24b9b6ac8dd56b2f181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65248801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17cfa2c2baebe81632f6c458aa09e8a9a478e166675cc5b197b163f224139ea`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 14:52:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jul 2024 14:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jul 2024 14:52:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jul 2024 14:52:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jul 2024 14:52:20 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Mon, 22 Jul 2024 14:52:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f9410264235861deaf30f97bec80870cf3bc38b1d8e57d897d8bb1f706ae6705';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='0dfd0ebab44d777f65bceaff7f79e8e0b9deb74a5eb166922483f1864bcf2052';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jul 2024 14:52:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jul 2024 14:52:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jul 2024 14:52:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dddb19fae622dcaadea15083e993889ddb0b2c9d39619781b5963b11aa3f65e`  
		Last Modified: Tue, 23 Jul 2024 04:15:57 GMT  
		Size: 8.4 MB (8442946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86caa4220d9f591b80a778c2abfef1a98dd168bb7db0c92cbd3b8c30046f91fa`  
		Last Modified: Tue, 23 Jul 2024 04:16:02 GMT  
		Size: 52.7 MB (52717344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7802c028acb42a74e61bb4b7e909aac37096154167086c79c8acb3801baf0ae3`  
		Last Modified: Tue, 23 Jul 2024 04:15:56 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a3d1421c025c33ecdd5292ff30b9bba61ac17657ca7449a64ba90650ac0133`  
		Last Modified: Tue, 23 Jul 2024 04:15:56 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
