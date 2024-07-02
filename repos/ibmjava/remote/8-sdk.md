## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:7a13ab3f8db08b892c76692f13d8b011b6585c31d239e6bd6a3185cf2d6c8e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:1fc8862e3d4c97ee79c55a9167391f7068db625f5e0f5c9511b87109cc7b0a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203206456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aa338381ca3b03907d7e0b9a13279faf34eb44c423eb6f1cec60754f89a612`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf754c15c64c10d89ff3d27c6ca5c2ca94ee741ca11a32de9abfb4d9612dbe9`  
		Last Modified: Mon, 01 Jul 2024 23:55:15 GMT  
		Size: 1.4 MB (1438218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd29f8694f9d0ab6629e8cd424eb313fa842ae6f75e989706cb6081ca472480`  
		Last Modified: Mon, 01 Jul 2024 23:55:19 GMT  
		Size: 172.2 MB (172234484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f692323a8b9700a43c9d33cb96d5d105486b8c9249b7ab4496bf171271bb48d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171bf71e460aba61558ab6447bcdebc8583a7606c676357184c4bbeadf626f70`

```dockerfile
```

-	Layers:
	-	`sha256:8c24611d2a8c119ee2e52ddf3fba185eb482f0a1c3e6a069058d087979590eef`  
		Last Modified: Mon, 01 Jul 2024 23:55:15 GMT  
		Size: 2.1 MB (2055787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632d36dfd1f6f47ecbc6f0cf7dab88a397f2bb9fdf7f072f78bb605676af917b`  
		Last Modified: Mon, 01 Jul 2024 23:55:15 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:ef44775393a86e60241d0fe51f663b01a9ccba194b425c50c0d9236134499150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208821538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79e50767a16d00a2a20214ae192ffb7d5784273994083518e35e24168835f95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569aebd0b75fda90f363ccbe2bae86e91da81747055c3eddcecfc6d56ed07267`  
		Last Modified: Tue, 02 Jul 2024 00:00:16 GMT  
		Size: 172.8 MB (172837569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e159f46dd5b13c27ada43a1c8408f0ad48ed34093ceb7e30e3d072aea562bb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851ce891911c095abdbea831c4e7bb6dd91a74fa1cdb0aee4f7ab4bb67eb504c`

```dockerfile
```

-	Layers:
	-	`sha256:c5c4bb4eacc165c0679a1a5e92f69821b323a793208e1db8c76b23053ed471e9`  
		Last Modified: Tue, 02 Jul 2024 00:00:09 GMT  
		Size: 2.1 MB (2058210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af18f017d064cae41714c2b4a9055d7238153677ce7b908149a8efcf7b55b8c9`  
		Last Modified: Tue, 02 Jul 2024 00:00:09 GMT  
		Size: 13.0 KB (12951 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:92ef9f55133612405254b25b8584103c5141b56514c0ecdc28b591bbb8fe3c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191505988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5286b4c3b5e4bf80d06b549c248cab97b9d640f18e3d4dd97f07018da9b04476`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220558a1d6fe452132948c80609a4e29f8f47367b0b46efaf89e63c37bc3da92`  
		Last Modified: Mon, 01 Jul 2024 23:58:32 GMT  
		Size: 162.1 MB (162063510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f947818ad5e0a5e06aa4b1b3c9a09ab623cd9d6123a298232821650afb7b5c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2042436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067b9ddeaaf23dd5efcdd7a276a11da3fe39f12ec9b2f9be1c77833de818098`

```dockerfile
```

-	Layers:
	-	`sha256:61453b70012b462f722109f4405dfb69f712fabcc0c1f6e7b99ac12a2b989f15`  
		Last Modified: Mon, 01 Jul 2024 23:58:30 GMT  
		Size: 2.0 MB (2029513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023ec0453cec5dbd5e180cd4786de3477fdfedc7276cc1247d4a8c4082019e69`  
		Last Modified: Mon, 01 Jul 2024 23:58:30 GMT  
		Size: 12.9 KB (12923 bytes)  
		MIME: application/vnd.in-toto+json
