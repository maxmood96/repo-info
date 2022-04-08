<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ibmjava`

-	[`ibmjava:8`](#ibmjava8)
-	[`ibmjava:8-jre`](#ibmjava8-jre)
-	[`ibmjava:8-jre-alpine`](#ibmjava8-jre-alpine)
-	[`ibmjava:8-sdk`](#ibmjava8-sdk)
-	[`ibmjava:8-sdk-alpine`](#ibmjava8-sdk-alpine)
-	[`ibmjava:8-sfj`](#ibmjava8-sfj)
-	[`ibmjava:8-sfj-alpine`](#ibmjava8-sfj-alpine)
-	[`ibmjava:jre`](#ibmjavajre)
-	[`ibmjava:jre-alpine`](#ibmjavajre-alpine)
-	[`ibmjava:latest`](#ibmjavalatest)
-	[`ibmjava:sdk`](#ibmjavasdk)
-	[`ibmjava:sdk-alpine`](#ibmjavasdk-alpine)
-	[`ibmjava:sfj`](#ibmjavasfj)
-	[`ibmjava:sfj-alpine`](#ibmjavasfj-alpine)

## `ibmjava:8`

```console
$ docker pull ibmjava@sha256:1a3dac899e45c2197778de3f3618ee823a4c153f65a4e33d75681bdc875fcba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:35e4eb1ce734bcb48b39238c2afa857269468d3733e4e608c2473e433c9de00b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158678953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec4b2d51d4029ef1771cf2ef1e54b866dd29f4cb0492fa3aab44007da58d34e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:11:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 04:11:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:20:47 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:21:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:21:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfba7ea970cb1c55200b82df4d841cb3aeceb410b11a8979aa633a92e7d236b`  
		Last Modified: Wed, 06 Apr 2022 04:13:29 GMT  
		Size: 3.0 MB (2959903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf43ddabf8b190bcc496a15e916d6bf2ab1b9ef76eb6bca6f56b9159a32cd88a`  
		Last Modified: Fri, 08 Apr 2022 20:25:22 GMT  
		Size: 129.0 MB (129010112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; 386

```console
$ docker pull ibmjava@sha256:117f8905426f27f345f8206c995f2695269913b502b76f585fca6633b79b8e07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147407280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e8c9fb2351f6859b19abb144931d7ec6f3797c40963c4e3cb872ac59b1f77c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:01 GMT
ADD file:d9edbb973ba7a0ee377e64ec7b7135478b3259223d5fbb83185ae0653ec0773f in / 
# Tue, 05 Apr 2022 22:39:02 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:56:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 22:56:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:40:03 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:40:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:40:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:12d1023794ad0425246985d1a3b4e8ad7a1368a1a6bd0f7a2827dd443349538b`  
		Last Modified: Tue, 05 Apr 2022 13:12:34 GMT  
		Size: 27.2 MB (27162492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7cb5790f060933c43ae1b003f69b6cf1bb7e024de0a59705e22882def104b8`  
		Last Modified: Tue, 05 Apr 2022 22:58:55 GMT  
		Size: 3.0 MB (2988442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b01dffadba21b5b21d23d24c9ca7b6bd40b9941d5b8d7d5570594816cb023f0`  
		Last Modified: Fri, 08 Apr 2022 20:42:52 GMT  
		Size: 117.3 MB (117256346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:85d27d7bdd55ef5872e06b697a5e1d282a230a7030393cc81f85477398c6f632
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162036775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af32f69dfb7fb5248170b61ce624d8281e5e5f4eac8522ca80e608545dca3c3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:13:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 05:14:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:19:06 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:20:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdbaeb83a31ef16299d247a8ff263c6635af307374780bb9be69adac828283a`  
		Last Modified: Wed, 06 Apr 2022 05:19:24 GMT  
		Size: 3.1 MB (3082224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed467ddf76c9c8fba4c5495d0734eb315c997ee70e897346eb187202d898497`  
		Last Modified: Fri, 08 Apr 2022 20:23:18 GMT  
		Size: 128.5 MB (128516122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:9d5bcf32772f0aa690eb35ec4867d6d9ebfafd65a1841256f1c47a65ff14a13e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154066324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8401007b521e5c51d15889e958b9591f22764cca593bfc4dd2dd160a5f34f1bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:41:55 GMT
ADD file:7da6edcff7f600bf3a5d740cd585065c6b3748ff587c0627def91686d1bfe54d in / 
# Tue, 05 Apr 2022 22:41:57 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:04:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 23:04:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:44:01 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:44:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:44:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4b0f8a5e4614be4866f08e8772b57664127164f512df03d05a52607176caa02f`  
		Last Modified: Tue, 05 Apr 2022 13:13:37 GMT  
		Size: 25.4 MB (25365860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df112729db94ceb85cc2f4f1a8a29c4c17240f3414e928932240687367857b`  
		Last Modified: Tue, 05 Apr 2022 23:07:59 GMT  
		Size: 2.7 MB (2676913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc257c141a0ac54a34910c8ba6f9df5ee7a246c36f82896f2c775897f381b8ff`  
		Last Modified: Fri, 08 Apr 2022 20:47:07 GMT  
		Size: 126.0 MB (126023551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:1a3dac899e45c2197778de3f3618ee823a4c153f65a4e33d75681bdc875fcba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:35e4eb1ce734bcb48b39238c2afa857269468d3733e4e608c2473e433c9de00b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158678953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec4b2d51d4029ef1771cf2ef1e54b866dd29f4cb0492fa3aab44007da58d34e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:11:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 04:11:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:20:47 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:21:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:21:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfba7ea970cb1c55200b82df4d841cb3aeceb410b11a8979aa633a92e7d236b`  
		Last Modified: Wed, 06 Apr 2022 04:13:29 GMT  
		Size: 3.0 MB (2959903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf43ddabf8b190bcc496a15e916d6bf2ab1b9ef76eb6bca6f56b9159a32cd88a`  
		Last Modified: Fri, 08 Apr 2022 20:25:22 GMT  
		Size: 129.0 MB (129010112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:117f8905426f27f345f8206c995f2695269913b502b76f585fca6633b79b8e07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147407280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e8c9fb2351f6859b19abb144931d7ec6f3797c40963c4e3cb872ac59b1f77c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:01 GMT
ADD file:d9edbb973ba7a0ee377e64ec7b7135478b3259223d5fbb83185ae0653ec0773f in / 
# Tue, 05 Apr 2022 22:39:02 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:56:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 22:56:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:40:03 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:40:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:40:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:12d1023794ad0425246985d1a3b4e8ad7a1368a1a6bd0f7a2827dd443349538b`  
		Last Modified: Tue, 05 Apr 2022 13:12:34 GMT  
		Size: 27.2 MB (27162492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7cb5790f060933c43ae1b003f69b6cf1bb7e024de0a59705e22882def104b8`  
		Last Modified: Tue, 05 Apr 2022 22:58:55 GMT  
		Size: 3.0 MB (2988442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b01dffadba21b5b21d23d24c9ca7b6bd40b9941d5b8d7d5570594816cb023f0`  
		Last Modified: Fri, 08 Apr 2022 20:42:52 GMT  
		Size: 117.3 MB (117256346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:85d27d7bdd55ef5872e06b697a5e1d282a230a7030393cc81f85477398c6f632
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162036775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af32f69dfb7fb5248170b61ce624d8281e5e5f4eac8522ca80e608545dca3c3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:13:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 05:14:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:19:06 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:20:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdbaeb83a31ef16299d247a8ff263c6635af307374780bb9be69adac828283a`  
		Last Modified: Wed, 06 Apr 2022 05:19:24 GMT  
		Size: 3.1 MB (3082224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed467ddf76c9c8fba4c5495d0734eb315c997ee70e897346eb187202d898497`  
		Last Modified: Fri, 08 Apr 2022 20:23:18 GMT  
		Size: 128.5 MB (128516122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:9d5bcf32772f0aa690eb35ec4867d6d9ebfafd65a1841256f1c47a65ff14a13e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154066324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8401007b521e5c51d15889e958b9591f22764cca593bfc4dd2dd160a5f34f1bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:41:55 GMT
ADD file:7da6edcff7f600bf3a5d740cd585065c6b3748ff587c0627def91686d1bfe54d in / 
# Tue, 05 Apr 2022 22:41:57 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:04:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 23:04:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:44:01 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:44:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:44:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4b0f8a5e4614be4866f08e8772b57664127164f512df03d05a52607176caa02f`  
		Last Modified: Tue, 05 Apr 2022 13:13:37 GMT  
		Size: 25.4 MB (25365860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df112729db94ceb85cc2f4f1a8a29c4c17240f3414e928932240687367857b`  
		Last Modified: Tue, 05 Apr 2022 23:07:59 GMT  
		Size: 2.7 MB (2676913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc257c141a0ac54a34910c8ba6f9df5ee7a246c36f82896f2c775897f381b8ff`  
		Last Modified: Fri, 08 Apr 2022 20:47:07 GMT  
		Size: 126.0 MB (126023551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre-alpine`

```console
$ docker pull ibmjava@sha256:766a478342a7e3aef267182bc13267bbd713f7fa55c57bbeb719d8baa33a52c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ibmjava:8-jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:c39912ec610610174c3851f75fac03d5bb4e2d08befd9f538f9542fd3de4dae3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137355503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672fd20f6ae171514824f494d0906e83197a85e5a2bde158740fa3e2b1cca165`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:19 GMT
ADD file:c1aa87a3b464fca64d769444b5201bc0426a1f517c91c4a7916270e10f8b300b in / 
# Tue, 05 Apr 2022 00:20:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:06:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 07:06:39 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Tue, 05 Apr 2022 07:06:56 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Fri, 08 Apr 2022 20:21:27 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:22:12 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Fri, 08 Apr 2022 20:22:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b7ca6aea1ddfe716f3694edb811ab35114db9e93f3ce38d7dab6b4d9270cb0c`  
		Last Modified: Tue, 05 Apr 2022 00:21:10 GMT  
		Size: 2.8 MB (2808060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c7df5cbcf1855fd251c9bae9f74f809e3a8c187df1c16f96385d2a5c19ca4f`  
		Last Modified: Tue, 05 Apr 2022 07:09:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103607a10c2c26537590f455b8a876ef03bd7c8ba5c02f6f662261752b4aeee4`  
		Last Modified: Tue, 05 Apr 2022 07:09:08 GMT  
		Size: 5.5 MB (5534716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18094580014c9181cf58773a402855905156611f28ca92c3a97d4da102d491`  
		Last Modified: Fri, 08 Apr 2022 20:25:46 GMT  
		Size: 129.0 MB (129012186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:b135f77cea1434fb0dbf4fb76c456788a6dbe2fc32539766ac351aff29bda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:c91b486a46aa1cf52c5527d515d58cdc3e9948750594116f112f0c41d9e9fff8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195811907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a9ab5d68a91adf3b33aac037b8760a8b19d7bfdd7c1934d57c83d836242853`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:11:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 04:11:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:20:47 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9261e658294baf2367802c07b6b6b8208a453556ca4189839661a54bab40f730';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fde521653a0c85e2a7b579f5ea7453a060e38a6e4f6b19134aed0f246d754146';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d8ed3c8a3756f4d4962bbd3219dfee51a43445ce61d5eeb383ac782884c21c7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='911de16288399945444e9a33dbb80f363d512c3864cdbeb9124e8d6d8b33769c';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='fcaad2566d4ad801eb6334572940d70d13e540f66a39601fd89d2b8c686519d4';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:24:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfba7ea970cb1c55200b82df4d841cb3aeceb410b11a8979aa633a92e7d236b`  
		Last Modified: Wed, 06 Apr 2022 04:13:29 GMT  
		Size: 3.0 MB (2959903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83c7ea7a9a6a38136f72bd8ed2d0dad47da5c67215c7291797408f2f94b6247`  
		Last Modified: Fri, 08 Apr 2022 20:26:38 GMT  
		Size: 166.1 MB (166143066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:7f66ad2736078ed2110a9fbaaea4dd116895683bf58bfff006cc5d61562de7d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184438412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5972ee1222870e96da7a6e0e7a57667d6a01c0d65ac163637141b739e81bbefc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:01 GMT
ADD file:d9edbb973ba7a0ee377e64ec7b7135478b3259223d5fbb83185ae0653ec0773f in / 
# Tue, 05 Apr 2022 22:39:02 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:56:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 22:56:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:40:03 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:42:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9261e658294baf2367802c07b6b6b8208a453556ca4189839661a54bab40f730';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fde521653a0c85e2a7b579f5ea7453a060e38a6e4f6b19134aed0f246d754146';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d8ed3c8a3756f4d4962bbd3219dfee51a43445ce61d5eeb383ac782884c21c7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='911de16288399945444e9a33dbb80f363d512c3864cdbeb9124e8d6d8b33769c';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='fcaad2566d4ad801eb6334572940d70d13e540f66a39601fd89d2b8c686519d4';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:42:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:12d1023794ad0425246985d1a3b4e8ad7a1368a1a6bd0f7a2827dd443349538b`  
		Last Modified: Tue, 05 Apr 2022 13:12:34 GMT  
		Size: 27.2 MB (27162492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7cb5790f060933c43ae1b003f69b6cf1bb7e024de0a59705e22882def104b8`  
		Last Modified: Tue, 05 Apr 2022 22:58:55 GMT  
		Size: 3.0 MB (2988442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae891502cf5920885a81a5ae56ec0a6013c2cb86096589089d464b537303f4f`  
		Last Modified: Fri, 08 Apr 2022 20:44:01 GMT  
		Size: 154.3 MB (154287478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:999f41e89d83c0ab97b70f3fe923a305d1209dcfd20edb5c9c7dc3cd085c2c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199313995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7474a52c70f9dbdf6ac3a53823ca58140ec4686eea1e634da456e8d1563d98ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:13:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 05:14:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:19:06 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:22:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9261e658294baf2367802c07b6b6b8208a453556ca4189839661a54bab40f730';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fde521653a0c85e2a7b579f5ea7453a060e38a6e4f6b19134aed0f246d754146';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d8ed3c8a3756f4d4962bbd3219dfee51a43445ce61d5eeb383ac782884c21c7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='911de16288399945444e9a33dbb80f363d512c3864cdbeb9124e8d6d8b33769c';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='fcaad2566d4ad801eb6334572940d70d13e540f66a39601fd89d2b8c686519d4';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:22:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdbaeb83a31ef16299d247a8ff263c6635af307374780bb9be69adac828283a`  
		Last Modified: Wed, 06 Apr 2022 05:19:24 GMT  
		Size: 3.1 MB (3082224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf92cc6bd0a8e7e8b5f7175ff60b7ad1a0c210df358dc50ebd64f308cd1587ea`  
		Last Modified: Fri, 08 Apr 2022 20:24:14 GMT  
		Size: 165.8 MB (165793342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:733d6c70cb30634132cc76ca79a5ca2dd92c8f043c51cb223a970dbe8ee7afe6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184355187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febcc0fe9c8ab62cf1f4eec1391e15e2719089c311f714f81b366da06d14a524`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:41:55 GMT
ADD file:7da6edcff7f600bf3a5d740cd585065c6b3748ff587c0627def91686d1bfe54d in / 
# Tue, 05 Apr 2022 22:41:57 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:04:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 23:04:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:44:01 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:46:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9261e658294baf2367802c07b6b6b8208a453556ca4189839661a54bab40f730';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fde521653a0c85e2a7b579f5ea7453a060e38a6e4f6b19134aed0f246d754146';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d8ed3c8a3756f4d4962bbd3219dfee51a43445ce61d5eeb383ac782884c21c7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='911de16288399945444e9a33dbb80f363d512c3864cdbeb9124e8d6d8b33769c';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='fcaad2566d4ad801eb6334572940d70d13e540f66a39601fd89d2b8c686519d4';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:46:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4b0f8a5e4614be4866f08e8772b57664127164f512df03d05a52607176caa02f`  
		Last Modified: Tue, 05 Apr 2022 13:13:37 GMT  
		Size: 25.4 MB (25365860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df112729db94ceb85cc2f4f1a8a29c4c17240f3414e928932240687367857b`  
		Last Modified: Tue, 05 Apr 2022 23:07:59 GMT  
		Size: 2.7 MB (2676913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8d7593cb7e22faa5bf43964561c430ae35b53c13f0a324f171eb4bdaf799f3`  
		Last Modified: Fri, 08 Apr 2022 20:47:44 GMT  
		Size: 156.3 MB (156312414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk-alpine`

```console
$ docker pull ibmjava@sha256:731e5a33de3a8d5ecf076c078731118153ee954ae22073f0f5893f863603f419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ibmjava:8-sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:4f8ad2029e78f7b91721745a77fc6011a7c0e09b9edeffb6b20b6ec34a6e63cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d97059433fcd8428a7c29c69dcd9dbe776e9afa01c3616a03fb9aa71488fa0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:19 GMT
ADD file:c1aa87a3b464fca64d769444b5201bc0426a1f517c91c4a7916270e10f8b300b in / 
# Tue, 05 Apr 2022 00:20:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:06:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 07:06:39 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Tue, 05 Apr 2022 07:06:56 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Fri, 08 Apr 2022 20:21:27 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:24:44 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9261e658294baf2367802c07b6b6b8208a453556ca4189839661a54bab40f730';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fde521653a0c85e2a7b579f5ea7453a060e38a6e4f6b19134aed0f246d754146';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d8ed3c8a3756f4d4962bbd3219dfee51a43445ce61d5eeb383ac782884c21c7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='911de16288399945444e9a33dbb80f363d512c3864cdbeb9124e8d6d8b33769c';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='fcaad2566d4ad801eb6334572940d70d13e540f66a39601fd89d2b8c686519d4';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Fri, 08 Apr 2022 20:24:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b7ca6aea1ddfe716f3694edb811ab35114db9e93f3ce38d7dab6b4d9270cb0c`  
		Last Modified: Tue, 05 Apr 2022 00:21:10 GMT  
		Size: 2.8 MB (2808060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c7df5cbcf1855fd251c9bae9f74f809e3a8c187df1c16f96385d2a5c19ca4f`  
		Last Modified: Tue, 05 Apr 2022 07:09:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103607a10c2c26537590f455b8a876ef03bd7c8ba5c02f6f662261752b4aeee4`  
		Last Modified: Tue, 05 Apr 2022 07:09:08 GMT  
		Size: 5.5 MB (5534716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716265507af4fd2abbe2c32cdd57f2cbcbb40f024321e9de5cd25ce71f0209cd`  
		Last Modified: Fri, 08 Apr 2022 20:26:59 GMT  
		Size: 166.2 MB (166158893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:7044a806d5d42c605a5bcde3d75440fc0579ffdc4387259a0be4e55a07d6d7a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:5bb1f53885cc3c5924c62ef1837c67d2362cde7bc4c357daa489de6f0770709f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94462174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3d70dff40c328ddafd22c98d6617ba492a01635b95e9f577dfc625b4c501c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:11:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 04:11:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:20:47 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:22:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='74ff23fc37cebf1652c60aacea2c8b18a19b15c727f80b1f246c6cbf8a577fbd';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='64c8fa951fde04474c8ad6f3307689289342774a7c3e6fbeb53f10aa87ea2397';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='94a602ec66153cc33b7fa4270b392b057514c2f248732c4c6ce5663e7b8e0e53';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c0aa51bdae9aa9dbdd9c1e3d78fccb435321ef3fdfb5ef37fd9463386c6026dd';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='4ab65ac072deb0da26fcc10ac85c47035af4d9692da9b972dccd72e036120650';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:22:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfba7ea970cb1c55200b82df4d841cb3aeceb410b11a8979aa633a92e7d236b`  
		Last Modified: Wed, 06 Apr 2022 04:13:29 GMT  
		Size: 3.0 MB (2959903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc4b6bf05772120974617bd757e94851b41ed3f2aaf85f632e4b51547f509c0`  
		Last Modified: Fri, 08 Apr 2022 20:26:01 GMT  
		Size: 64.8 MB (64793333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:bd5efee12f1d0a865a155f5ce6555517b018ad11f4c7ac11699d1af14e920e2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94342768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b0a23942ac11dc0372b1f9332306a992ac86c15206cce3b68c01b7348dba78`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:01 GMT
ADD file:d9edbb973ba7a0ee377e64ec7b7135478b3259223d5fbb83185ae0653ec0773f in / 
# Tue, 05 Apr 2022 22:39:02 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:56:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 22:56:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:40:03 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:41:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='74ff23fc37cebf1652c60aacea2c8b18a19b15c727f80b1f246c6cbf8a577fbd';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='64c8fa951fde04474c8ad6f3307689289342774a7c3e6fbeb53f10aa87ea2397';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='94a602ec66153cc33b7fa4270b392b057514c2f248732c4c6ce5663e7b8e0e53';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c0aa51bdae9aa9dbdd9c1e3d78fccb435321ef3fdfb5ef37fd9463386c6026dd';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='4ab65ac072deb0da26fcc10ac85c47035af4d9692da9b972dccd72e036120650';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:41:16 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:12d1023794ad0425246985d1a3b4e8ad7a1368a1a6bd0f7a2827dd443349538b`  
		Last Modified: Tue, 05 Apr 2022 13:12:34 GMT  
		Size: 27.2 MB (27162492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7cb5790f060933c43ae1b003f69b6cf1bb7e024de0a59705e22882def104b8`  
		Last Modified: Tue, 05 Apr 2022 22:58:55 GMT  
		Size: 3.0 MB (2988442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc4508ae09035ea44ad607fa66470d358b1922a213250eb1b720ab850583f`  
		Last Modified: Fri, 08 Apr 2022 20:43:21 GMT  
		Size: 64.2 MB (64191834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:df67c938bc4e640ab8a334f9060ed1ec2d827c6b22f4740ccb382b250e20f1f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98525841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6257133fe9d82d641a56d9188fe8b0174edb9b12cc64055e827ea5c05a612e0a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:13:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 05:14:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:19:06 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:21:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='74ff23fc37cebf1652c60aacea2c8b18a19b15c727f80b1f246c6cbf8a577fbd';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='64c8fa951fde04474c8ad6f3307689289342774a7c3e6fbeb53f10aa87ea2397';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='94a602ec66153cc33b7fa4270b392b057514c2f248732c4c6ce5663e7b8e0e53';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c0aa51bdae9aa9dbdd9c1e3d78fccb435321ef3fdfb5ef37fd9463386c6026dd';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='4ab65ac072deb0da26fcc10ac85c47035af4d9692da9b972dccd72e036120650';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:21:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdbaeb83a31ef16299d247a8ff263c6635af307374780bb9be69adac828283a`  
		Last Modified: Wed, 06 Apr 2022 05:19:24 GMT  
		Size: 3.1 MB (3082224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f6a7b934f78406132c5bae524e0e68dc04373740a56555bc90fb885ded46f3`  
		Last Modified: Fri, 08 Apr 2022 20:23:44 GMT  
		Size: 65.0 MB (65005188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:b34eef37ac33a8bc5eec961f58107a38ad11a66251ae15a82ee8bdaff4418e33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93891890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d44c33cac659a32827ff100dcf54b0ae6de038572deca9260b6f086f456f2b3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:41:55 GMT
ADD file:7da6edcff7f600bf3a5d740cd585065c6b3748ff587c0627def91686d1bfe54d in / 
# Tue, 05 Apr 2022 22:41:57 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:04:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 23:04:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:44:01 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='74ff23fc37cebf1652c60aacea2c8b18a19b15c727f80b1f246c6cbf8a577fbd';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='64c8fa951fde04474c8ad6f3307689289342774a7c3e6fbeb53f10aa87ea2397';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='94a602ec66153cc33b7fa4270b392b057514c2f248732c4c6ce5663e7b8e0e53';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c0aa51bdae9aa9dbdd9c1e3d78fccb435321ef3fdfb5ef37fd9463386c6026dd';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='4ab65ac072deb0da26fcc10ac85c47035af4d9692da9b972dccd72e036120650';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:45:29 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4b0f8a5e4614be4866f08e8772b57664127164f512df03d05a52607176caa02f`  
		Last Modified: Tue, 05 Apr 2022 13:13:37 GMT  
		Size: 25.4 MB (25365860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df112729db94ceb85cc2f4f1a8a29c4c17240f3414e928932240687367857b`  
		Last Modified: Tue, 05 Apr 2022 23:07:59 GMT  
		Size: 2.7 MB (2676913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3779825003b6d414336c25bd15d0e55293f61486586c4a856ea52dc0dde4f023`  
		Last Modified: Fri, 08 Apr 2022 20:47:25 GMT  
		Size: 65.8 MB (65849117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj-alpine`

```console
$ docker pull ibmjava@sha256:214155e791e2f9457414e1af3690c7fd2374b7a6d108555f6206745d3a209eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ibmjava:8-sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:62a81e03233d23303c667347c1213313609937f66af2ef18ada54d62de31b519
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73149658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156ff382c7ee7896f58f2d20425d769822cfdf9604eacc5257813ac7402c041c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:19 GMT
ADD file:c1aa87a3b464fca64d769444b5201bc0426a1f517c91c4a7916270e10f8b300b in / 
# Tue, 05 Apr 2022 00:20:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:06:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 07:06:39 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Tue, 05 Apr 2022 07:06:56 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Fri, 08 Apr 2022 20:21:27 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:23:14 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='74ff23fc37cebf1652c60aacea2c8b18a19b15c727f80b1f246c6cbf8a577fbd';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='64c8fa951fde04474c8ad6f3307689289342774a7c3e6fbeb53f10aa87ea2397';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='94a602ec66153cc33b7fa4270b392b057514c2f248732c4c6ce5663e7b8e0e53';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c0aa51bdae9aa9dbdd9c1e3d78fccb435321ef3fdfb5ef37fd9463386c6026dd';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='4ab65ac072deb0da26fcc10ac85c47035af4d9692da9b972dccd72e036120650';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Fri, 08 Apr 2022 20:23:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b7ca6aea1ddfe716f3694edb811ab35114db9e93f3ce38d7dab6b4d9270cb0c`  
		Last Modified: Tue, 05 Apr 2022 00:21:10 GMT  
		Size: 2.8 MB (2808060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c7df5cbcf1855fd251c9bae9f74f809e3a8c187df1c16f96385d2a5c19ca4f`  
		Last Modified: Tue, 05 Apr 2022 07:09:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103607a10c2c26537590f455b8a876ef03bd7c8ba5c02f6f662261752b4aeee4`  
		Last Modified: Tue, 05 Apr 2022 07:09:08 GMT  
		Size: 5.5 MB (5534716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3116f387e1b4a8aa8e53668214bf04ca2fd8da373f1b6690f3cf738fe52a9a20`  
		Last Modified: Fri, 08 Apr 2022 20:26:16 GMT  
		Size: 64.8 MB (64806341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:1a3dac899e45c2197778de3f3618ee823a4c153f65a4e33d75681bdc875fcba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:35e4eb1ce734bcb48b39238c2afa857269468d3733e4e608c2473e433c9de00b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158678953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec4b2d51d4029ef1771cf2ef1e54b866dd29f4cb0492fa3aab44007da58d34e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:11:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 04:11:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:20:47 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:21:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:21:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfba7ea970cb1c55200b82df4d841cb3aeceb410b11a8979aa633a92e7d236b`  
		Last Modified: Wed, 06 Apr 2022 04:13:29 GMT  
		Size: 3.0 MB (2959903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf43ddabf8b190bcc496a15e916d6bf2ab1b9ef76eb6bca6f56b9159a32cd88a`  
		Last Modified: Fri, 08 Apr 2022 20:25:22 GMT  
		Size: 129.0 MB (129010112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; 386

```console
$ docker pull ibmjava@sha256:117f8905426f27f345f8206c995f2695269913b502b76f585fca6633b79b8e07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147407280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e8c9fb2351f6859b19abb144931d7ec6f3797c40963c4e3cb872ac59b1f77c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:01 GMT
ADD file:d9edbb973ba7a0ee377e64ec7b7135478b3259223d5fbb83185ae0653ec0773f in / 
# Tue, 05 Apr 2022 22:39:02 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:56:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 22:56:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:40:03 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:40:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:40:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:12d1023794ad0425246985d1a3b4e8ad7a1368a1a6bd0f7a2827dd443349538b`  
		Last Modified: Tue, 05 Apr 2022 13:12:34 GMT  
		Size: 27.2 MB (27162492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7cb5790f060933c43ae1b003f69b6cf1bb7e024de0a59705e22882def104b8`  
		Last Modified: Tue, 05 Apr 2022 22:58:55 GMT  
		Size: 3.0 MB (2988442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b01dffadba21b5b21d23d24c9ca7b6bd40b9941d5b8d7d5570594816cb023f0`  
		Last Modified: Fri, 08 Apr 2022 20:42:52 GMT  
		Size: 117.3 MB (117256346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:85d27d7bdd55ef5872e06b697a5e1d282a230a7030393cc81f85477398c6f632
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162036775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af32f69dfb7fb5248170b61ce624d8281e5e5f4eac8522ca80e608545dca3c3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:13:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 05:14:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:19:06 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:20:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdbaeb83a31ef16299d247a8ff263c6635af307374780bb9be69adac828283a`  
		Last Modified: Wed, 06 Apr 2022 05:19:24 GMT  
		Size: 3.1 MB (3082224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed467ddf76c9c8fba4c5495d0734eb315c997ee70e897346eb187202d898497`  
		Last Modified: Fri, 08 Apr 2022 20:23:18 GMT  
		Size: 128.5 MB (128516122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:9d5bcf32772f0aa690eb35ec4867d6d9ebfafd65a1841256f1c47a65ff14a13e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154066324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8401007b521e5c51d15889e958b9591f22764cca593bfc4dd2dd160a5f34f1bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:41:55 GMT
ADD file:7da6edcff7f600bf3a5d740cd585065c6b3748ff587c0627def91686d1bfe54d in / 
# Tue, 05 Apr 2022 22:41:57 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:04:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 23:04:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:44:01 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:44:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:44:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4b0f8a5e4614be4866f08e8772b57664127164f512df03d05a52607176caa02f`  
		Last Modified: Tue, 05 Apr 2022 13:13:37 GMT  
		Size: 25.4 MB (25365860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df112729db94ceb85cc2f4f1a8a29c4c17240f3414e928932240687367857b`  
		Last Modified: Tue, 05 Apr 2022 23:07:59 GMT  
		Size: 2.7 MB (2676913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc257c141a0ac54a34910c8ba6f9df5ee7a246c36f82896f2c775897f381b8ff`  
		Last Modified: Fri, 08 Apr 2022 20:47:07 GMT  
		Size: 126.0 MB (126023551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre-alpine`

```console
$ docker pull ibmjava@sha256:766a478342a7e3aef267182bc13267bbd713f7fa55c57bbeb719d8baa33a52c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ibmjava:jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:c39912ec610610174c3851f75fac03d5bb4e2d08befd9f538f9542fd3de4dae3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137355503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672fd20f6ae171514824f494d0906e83197a85e5a2bde158740fa3e2b1cca165`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:19 GMT
ADD file:c1aa87a3b464fca64d769444b5201bc0426a1f517c91c4a7916270e10f8b300b in / 
# Tue, 05 Apr 2022 00:20:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:06:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 07:06:39 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Tue, 05 Apr 2022 07:06:56 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Fri, 08 Apr 2022 20:21:27 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:22:12 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Fri, 08 Apr 2022 20:22:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b7ca6aea1ddfe716f3694edb811ab35114db9e93f3ce38d7dab6b4d9270cb0c`  
		Last Modified: Tue, 05 Apr 2022 00:21:10 GMT  
		Size: 2.8 MB (2808060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c7df5cbcf1855fd251c9bae9f74f809e3a8c187df1c16f96385d2a5c19ca4f`  
		Last Modified: Tue, 05 Apr 2022 07:09:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103607a10c2c26537590f455b8a876ef03bd7c8ba5c02f6f662261752b4aeee4`  
		Last Modified: Tue, 05 Apr 2022 07:09:08 GMT  
		Size: 5.5 MB (5534716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef18094580014c9181cf58773a402855905156611f28ca92c3a97d4da102d491`  
		Last Modified: Fri, 08 Apr 2022 20:25:46 GMT  
		Size: 129.0 MB (129012186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:1a3dac899e45c2197778de3f3618ee823a4c153f65a4e33d75681bdc875fcba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:35e4eb1ce734bcb48b39238c2afa857269468d3733e4e608c2473e433c9de00b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158678953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec4b2d51d4029ef1771cf2ef1e54b866dd29f4cb0492fa3aab44007da58d34e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:11:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 04:11:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:20:47 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:21:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:21:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfba7ea970cb1c55200b82df4d841cb3aeceb410b11a8979aa633a92e7d236b`  
		Last Modified: Wed, 06 Apr 2022 04:13:29 GMT  
		Size: 3.0 MB (2959903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf43ddabf8b190bcc496a15e916d6bf2ab1b9ef76eb6bca6f56b9159a32cd88a`  
		Last Modified: Fri, 08 Apr 2022 20:25:22 GMT  
		Size: 129.0 MB (129010112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; 386

```console
$ docker pull ibmjava@sha256:117f8905426f27f345f8206c995f2695269913b502b76f585fca6633b79b8e07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147407280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e8c9fb2351f6859b19abb144931d7ec6f3797c40963c4e3cb872ac59b1f77c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:01 GMT
ADD file:d9edbb973ba7a0ee377e64ec7b7135478b3259223d5fbb83185ae0653ec0773f in / 
# Tue, 05 Apr 2022 22:39:02 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:56:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 22:56:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:40:03 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:40:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:40:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:12d1023794ad0425246985d1a3b4e8ad7a1368a1a6bd0f7a2827dd443349538b`  
		Last Modified: Tue, 05 Apr 2022 13:12:34 GMT  
		Size: 27.2 MB (27162492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7cb5790f060933c43ae1b003f69b6cf1bb7e024de0a59705e22882def104b8`  
		Last Modified: Tue, 05 Apr 2022 22:58:55 GMT  
		Size: 3.0 MB (2988442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b01dffadba21b5b21d23d24c9ca7b6bd40b9941d5b8d7d5570594816cb023f0`  
		Last Modified: Fri, 08 Apr 2022 20:42:52 GMT  
		Size: 117.3 MB (117256346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:85d27d7bdd55ef5872e06b697a5e1d282a230a7030393cc81f85477398c6f632
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162036775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af32f69dfb7fb5248170b61ce624d8281e5e5f4eac8522ca80e608545dca3c3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:13:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 05:14:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:19:06 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:20:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdbaeb83a31ef16299d247a8ff263c6635af307374780bb9be69adac828283a`  
		Last Modified: Wed, 06 Apr 2022 05:19:24 GMT  
		Size: 3.1 MB (3082224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed467ddf76c9c8fba4c5495d0734eb315c997ee70e897346eb187202d898497`  
		Last Modified: Fri, 08 Apr 2022 20:23:18 GMT  
		Size: 128.5 MB (128516122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:9d5bcf32772f0aa690eb35ec4867d6d9ebfafd65a1841256f1c47a65ff14a13e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154066324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8401007b521e5c51d15889e958b9591f22764cca593bfc4dd2dd160a5f34f1bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:41:55 GMT
ADD file:7da6edcff7f600bf3a5d740cd585065c6b3748ff587c0627def91686d1bfe54d in / 
# Tue, 05 Apr 2022 22:41:57 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:04:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 23:04:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:44:01 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:44:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:44:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4b0f8a5e4614be4866f08e8772b57664127164f512df03d05a52607176caa02f`  
		Last Modified: Tue, 05 Apr 2022 13:13:37 GMT  
		Size: 25.4 MB (25365860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df112729db94ceb85cc2f4f1a8a29c4c17240f3414e928932240687367857b`  
		Last Modified: Tue, 05 Apr 2022 23:07:59 GMT  
		Size: 2.7 MB (2676913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc257c141a0ac54a34910c8ba6f9df5ee7a246c36f82896f2c775897f381b8ff`  
		Last Modified: Fri, 08 Apr 2022 20:47:07 GMT  
		Size: 126.0 MB (126023551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:b135f77cea1434fb0dbf4fb76c456788a6dbe2fc32539766ac351aff29bda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:c91b486a46aa1cf52c5527d515d58cdc3e9948750594116f112f0c41d9e9fff8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195811907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a9ab5d68a91adf3b33aac037b8760a8b19d7bfdd7c1934d57c83d836242853`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:11:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 04:11:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:20:47 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9261e658294baf2367802c07b6b6b8208a453556ca4189839661a54bab40f730';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fde521653a0c85e2a7b579f5ea7453a060e38a6e4f6b19134aed0f246d754146';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d8ed3c8a3756f4d4962bbd3219dfee51a43445ce61d5eeb383ac782884c21c7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='911de16288399945444e9a33dbb80f363d512c3864cdbeb9124e8d6d8b33769c';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='fcaad2566d4ad801eb6334572940d70d13e540f66a39601fd89d2b8c686519d4';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:24:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfba7ea970cb1c55200b82df4d841cb3aeceb410b11a8979aa633a92e7d236b`  
		Last Modified: Wed, 06 Apr 2022 04:13:29 GMT  
		Size: 3.0 MB (2959903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83c7ea7a9a6a38136f72bd8ed2d0dad47da5c67215c7291797408f2f94b6247`  
		Last Modified: Fri, 08 Apr 2022 20:26:38 GMT  
		Size: 166.1 MB (166143066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:7f66ad2736078ed2110a9fbaaea4dd116895683bf58bfff006cc5d61562de7d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184438412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5972ee1222870e96da7a6e0e7a57667d6a01c0d65ac163637141b739e81bbefc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:01 GMT
ADD file:d9edbb973ba7a0ee377e64ec7b7135478b3259223d5fbb83185ae0653ec0773f in / 
# Tue, 05 Apr 2022 22:39:02 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:56:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 22:56:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:40:03 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:42:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9261e658294baf2367802c07b6b6b8208a453556ca4189839661a54bab40f730';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fde521653a0c85e2a7b579f5ea7453a060e38a6e4f6b19134aed0f246d754146';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d8ed3c8a3756f4d4962bbd3219dfee51a43445ce61d5eeb383ac782884c21c7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='911de16288399945444e9a33dbb80f363d512c3864cdbeb9124e8d6d8b33769c';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='fcaad2566d4ad801eb6334572940d70d13e540f66a39601fd89d2b8c686519d4';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:42:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:12d1023794ad0425246985d1a3b4e8ad7a1368a1a6bd0f7a2827dd443349538b`  
		Last Modified: Tue, 05 Apr 2022 13:12:34 GMT  
		Size: 27.2 MB (27162492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7cb5790f060933c43ae1b003f69b6cf1bb7e024de0a59705e22882def104b8`  
		Last Modified: Tue, 05 Apr 2022 22:58:55 GMT  
		Size: 3.0 MB (2988442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae891502cf5920885a81a5ae56ec0a6013c2cb86096589089d464b537303f4f`  
		Last Modified: Fri, 08 Apr 2022 20:44:01 GMT  
		Size: 154.3 MB (154287478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:999f41e89d83c0ab97b70f3fe923a305d1209dcfd20edb5c9c7dc3cd085c2c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199313995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7474a52c70f9dbdf6ac3a53823ca58140ec4686eea1e634da456e8d1563d98ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:13:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 05:14:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:19:06 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:22:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9261e658294baf2367802c07b6b6b8208a453556ca4189839661a54bab40f730';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fde521653a0c85e2a7b579f5ea7453a060e38a6e4f6b19134aed0f246d754146';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d8ed3c8a3756f4d4962bbd3219dfee51a43445ce61d5eeb383ac782884c21c7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='911de16288399945444e9a33dbb80f363d512c3864cdbeb9124e8d6d8b33769c';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='fcaad2566d4ad801eb6334572940d70d13e540f66a39601fd89d2b8c686519d4';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:22:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdbaeb83a31ef16299d247a8ff263c6635af307374780bb9be69adac828283a`  
		Last Modified: Wed, 06 Apr 2022 05:19:24 GMT  
		Size: 3.1 MB (3082224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf92cc6bd0a8e7e8b5f7175ff60b7ad1a0c210df358dc50ebd64f308cd1587ea`  
		Last Modified: Fri, 08 Apr 2022 20:24:14 GMT  
		Size: 165.8 MB (165793342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:733d6c70cb30634132cc76ca79a5ca2dd92c8f043c51cb223a970dbe8ee7afe6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184355187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febcc0fe9c8ab62cf1f4eec1391e15e2719089c311f714f81b366da06d14a524`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:41:55 GMT
ADD file:7da6edcff7f600bf3a5d740cd585065c6b3748ff587c0627def91686d1bfe54d in / 
# Tue, 05 Apr 2022 22:41:57 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:04:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 23:04:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:44:01 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:46:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9261e658294baf2367802c07b6b6b8208a453556ca4189839661a54bab40f730';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fde521653a0c85e2a7b579f5ea7453a060e38a6e4f6b19134aed0f246d754146';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d8ed3c8a3756f4d4962bbd3219dfee51a43445ce61d5eeb383ac782884c21c7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='911de16288399945444e9a33dbb80f363d512c3864cdbeb9124e8d6d8b33769c';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='fcaad2566d4ad801eb6334572940d70d13e540f66a39601fd89d2b8c686519d4';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:46:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4b0f8a5e4614be4866f08e8772b57664127164f512df03d05a52607176caa02f`  
		Last Modified: Tue, 05 Apr 2022 13:13:37 GMT  
		Size: 25.4 MB (25365860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df112729db94ceb85cc2f4f1a8a29c4c17240f3414e928932240687367857b`  
		Last Modified: Tue, 05 Apr 2022 23:07:59 GMT  
		Size: 2.7 MB (2676913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8d7593cb7e22faa5bf43964561c430ae35b53c13f0a324f171eb4bdaf799f3`  
		Last Modified: Fri, 08 Apr 2022 20:47:44 GMT  
		Size: 156.3 MB (156312414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk-alpine`

```console
$ docker pull ibmjava@sha256:731e5a33de3a8d5ecf076c078731118153ee954ae22073f0f5893f863603f419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ibmjava:sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:4f8ad2029e78f7b91721745a77fc6011a7c0e09b9edeffb6b20b6ec34a6e63cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d97059433fcd8428a7c29c69dcd9dbe776e9afa01c3616a03fb9aa71488fa0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:19 GMT
ADD file:c1aa87a3b464fca64d769444b5201bc0426a1f517c91c4a7916270e10f8b300b in / 
# Tue, 05 Apr 2022 00:20:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:06:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 07:06:39 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Tue, 05 Apr 2022 07:06:56 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Fri, 08 Apr 2022 20:21:27 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:24:44 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9261e658294baf2367802c07b6b6b8208a453556ca4189839661a54bab40f730';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fde521653a0c85e2a7b579f5ea7453a060e38a6e4f6b19134aed0f246d754146';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d8ed3c8a3756f4d4962bbd3219dfee51a43445ce61d5eeb383ac782884c21c7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='911de16288399945444e9a33dbb80f363d512c3864cdbeb9124e8d6d8b33769c';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='fcaad2566d4ad801eb6334572940d70d13e540f66a39601fd89d2b8c686519d4';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Fri, 08 Apr 2022 20:24:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b7ca6aea1ddfe716f3694edb811ab35114db9e93f3ce38d7dab6b4d9270cb0c`  
		Last Modified: Tue, 05 Apr 2022 00:21:10 GMT  
		Size: 2.8 MB (2808060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c7df5cbcf1855fd251c9bae9f74f809e3a8c187df1c16f96385d2a5c19ca4f`  
		Last Modified: Tue, 05 Apr 2022 07:09:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103607a10c2c26537590f455b8a876ef03bd7c8ba5c02f6f662261752b4aeee4`  
		Last Modified: Tue, 05 Apr 2022 07:09:08 GMT  
		Size: 5.5 MB (5534716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716265507af4fd2abbe2c32cdd57f2cbcbb40f024321e9de5cd25ce71f0209cd`  
		Last Modified: Fri, 08 Apr 2022 20:26:59 GMT  
		Size: 166.2 MB (166158893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:7044a806d5d42c605a5bcde3d75440fc0579ffdc4387259a0be4e55a07d6d7a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:5bb1f53885cc3c5924c62ef1837c67d2362cde7bc4c357daa489de6f0770709f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94462174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3d70dff40c328ddafd22c98d6617ba492a01635b95e9f577dfc625b4c501c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:11:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 04:11:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:20:47 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:22:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='74ff23fc37cebf1652c60aacea2c8b18a19b15c727f80b1f246c6cbf8a577fbd';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='64c8fa951fde04474c8ad6f3307689289342774a7c3e6fbeb53f10aa87ea2397';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='94a602ec66153cc33b7fa4270b392b057514c2f248732c4c6ce5663e7b8e0e53';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c0aa51bdae9aa9dbdd9c1e3d78fccb435321ef3fdfb5ef37fd9463386c6026dd';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='4ab65ac072deb0da26fcc10ac85c47035af4d9692da9b972dccd72e036120650';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:22:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfba7ea970cb1c55200b82df4d841cb3aeceb410b11a8979aa633a92e7d236b`  
		Last Modified: Wed, 06 Apr 2022 04:13:29 GMT  
		Size: 3.0 MB (2959903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc4b6bf05772120974617bd757e94851b41ed3f2aaf85f632e4b51547f509c0`  
		Last Modified: Fri, 08 Apr 2022 20:26:01 GMT  
		Size: 64.8 MB (64793333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:bd5efee12f1d0a865a155f5ce6555517b018ad11f4c7ac11699d1af14e920e2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94342768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b0a23942ac11dc0372b1f9332306a992ac86c15206cce3b68c01b7348dba78`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:01 GMT
ADD file:d9edbb973ba7a0ee377e64ec7b7135478b3259223d5fbb83185ae0653ec0773f in / 
# Tue, 05 Apr 2022 22:39:02 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:56:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 22:56:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:40:03 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:41:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='74ff23fc37cebf1652c60aacea2c8b18a19b15c727f80b1f246c6cbf8a577fbd';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='64c8fa951fde04474c8ad6f3307689289342774a7c3e6fbeb53f10aa87ea2397';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='94a602ec66153cc33b7fa4270b392b057514c2f248732c4c6ce5663e7b8e0e53';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c0aa51bdae9aa9dbdd9c1e3d78fccb435321ef3fdfb5ef37fd9463386c6026dd';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='4ab65ac072deb0da26fcc10ac85c47035af4d9692da9b972dccd72e036120650';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:41:16 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:12d1023794ad0425246985d1a3b4e8ad7a1368a1a6bd0f7a2827dd443349538b`  
		Last Modified: Tue, 05 Apr 2022 13:12:34 GMT  
		Size: 27.2 MB (27162492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7cb5790f060933c43ae1b003f69b6cf1bb7e024de0a59705e22882def104b8`  
		Last Modified: Tue, 05 Apr 2022 22:58:55 GMT  
		Size: 3.0 MB (2988442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffc4508ae09035ea44ad607fa66470d358b1922a213250eb1b720ab850583f`  
		Last Modified: Fri, 08 Apr 2022 20:43:21 GMT  
		Size: 64.2 MB (64191834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:df67c938bc4e640ab8a334f9060ed1ec2d827c6b22f4740ccb382b250e20f1f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98525841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6257133fe9d82d641a56d9188fe8b0174edb9b12cc64055e827ea5c05a612e0a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:13:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 05:14:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:19:06 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:21:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='74ff23fc37cebf1652c60aacea2c8b18a19b15c727f80b1f246c6cbf8a577fbd';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='64c8fa951fde04474c8ad6f3307689289342774a7c3e6fbeb53f10aa87ea2397';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='94a602ec66153cc33b7fa4270b392b057514c2f248732c4c6ce5663e7b8e0e53';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c0aa51bdae9aa9dbdd9c1e3d78fccb435321ef3fdfb5ef37fd9463386c6026dd';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='4ab65ac072deb0da26fcc10ac85c47035af4d9692da9b972dccd72e036120650';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:21:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdbaeb83a31ef16299d247a8ff263c6635af307374780bb9be69adac828283a`  
		Last Modified: Wed, 06 Apr 2022 05:19:24 GMT  
		Size: 3.1 MB (3082224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f6a7b934f78406132c5bae524e0e68dc04373740a56555bc90fb885ded46f3`  
		Last Modified: Fri, 08 Apr 2022 20:23:44 GMT  
		Size: 65.0 MB (65005188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:b34eef37ac33a8bc5eec961f58107a38ad11a66251ae15a82ee8bdaff4418e33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93891890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d44c33cac659a32827ff100dcf54b0ae6de038572deca9260b6f086f456f2b3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:41:55 GMT
ADD file:7da6edcff7f600bf3a5d740cd585065c6b3748ff587c0627def91686d1bfe54d in / 
# Tue, 05 Apr 2022 22:41:57 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:04:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 23:04:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 08 Apr 2022 20:44:01 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='74ff23fc37cebf1652c60aacea2c8b18a19b15c727f80b1f246c6cbf8a577fbd';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='64c8fa951fde04474c8ad6f3307689289342774a7c3e6fbeb53f10aa87ea2397';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='94a602ec66153cc33b7fa4270b392b057514c2f248732c4c6ce5663e7b8e0e53';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c0aa51bdae9aa9dbdd9c1e3d78fccb435321ef3fdfb5ef37fd9463386c6026dd';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='4ab65ac072deb0da26fcc10ac85c47035af4d9692da9b972dccd72e036120650';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 08 Apr 2022 20:45:29 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4b0f8a5e4614be4866f08e8772b57664127164f512df03d05a52607176caa02f`  
		Last Modified: Tue, 05 Apr 2022 13:13:37 GMT  
		Size: 25.4 MB (25365860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df112729db94ceb85cc2f4f1a8a29c4c17240f3414e928932240687367857b`  
		Last Modified: Tue, 05 Apr 2022 23:07:59 GMT  
		Size: 2.7 MB (2676913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3779825003b6d414336c25bd15d0e55293f61486586c4a856ea52dc0dde4f023`  
		Last Modified: Fri, 08 Apr 2022 20:47:25 GMT  
		Size: 65.8 MB (65849117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj-alpine`

```console
$ docker pull ibmjava@sha256:214155e791e2f9457414e1af3690c7fd2374b7a6d108555f6206745d3a209eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ibmjava:sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:62a81e03233d23303c667347c1213313609937f66af2ef18ada54d62de31b519
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73149658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156ff382c7ee7896f58f2d20425d769822cfdf9604eacc5257813ac7402c041c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:19 GMT
ADD file:c1aa87a3b464fca64d769444b5201bc0426a1f517c91c4a7916270e10f8b300b in / 
# Tue, 05 Apr 2022 00:20:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:06:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 07:06:39 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Tue, 05 Apr 2022 07:06:56 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Fri, 08 Apr 2022 20:21:27 GMT
ENV JAVA_VERSION=8.0.7.6
# Fri, 08 Apr 2022 20:23:14 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='74ff23fc37cebf1652c60aacea2c8b18a19b15c727f80b1f246c6cbf8a577fbd';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='64c8fa951fde04474c8ad6f3307689289342774a7c3e6fbeb53f10aa87ea2397';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='94a602ec66153cc33b7fa4270b392b057514c2f248732c4c6ce5663e7b8e0e53';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c0aa51bdae9aa9dbdd9c1e3d78fccb435321ef3fdfb5ef37fd9463386c6026dd';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='4ab65ac072deb0da26fcc10ac85c47035af4d9692da9b972dccd72e036120650';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Fri, 08 Apr 2022 20:23:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b7ca6aea1ddfe716f3694edb811ab35114db9e93f3ce38d7dab6b4d9270cb0c`  
		Last Modified: Tue, 05 Apr 2022 00:21:10 GMT  
		Size: 2.8 MB (2808060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c7df5cbcf1855fd251c9bae9f74f809e3a8c187df1c16f96385d2a5c19ca4f`  
		Last Modified: Tue, 05 Apr 2022 07:09:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103607a10c2c26537590f455b8a876ef03bd7c8ba5c02f6f662261752b4aeee4`  
		Last Modified: Tue, 05 Apr 2022 07:09:08 GMT  
		Size: 5.5 MB (5534716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3116f387e1b4a8aa8e53668214bf04ca2fd8da373f1b6690f3cf738fe52a9a20`  
		Last Modified: Fri, 08 Apr 2022 20:26:16 GMT  
		Size: 64.8 MB (64806341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
