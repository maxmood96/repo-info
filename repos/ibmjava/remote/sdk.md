## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:e0c323fcf360f3998c9831a95b52c1e048048df044f1d71693056a7ee813694a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:a8a959c23ce5b8d77936b2fce1e2f33b5d2cc4fe7daceee8fa48b8d0ff5df119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203215307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d319563b74ff06322e7f51b39fcd2eac8dcee444208e659c4a3843c9b07349fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 May 2024 05:12:02 GMT
ARG RELEASE
# Thu, 09 May 2024 05:12:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 09 May 2024 05:12:02 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 09 May 2024 05:12:02 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 05:12:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 09 May 2024 05:12:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 05:12:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6d7ddb94d08079895f4fabec6cc12c9acbb1f398d547dbfaa306cc2faf837`  
		Last Modified: Tue, 25 Jun 2024 22:57:25 GMT  
		Size: 1.5 MB (1469335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf32957134ad52256fcac2824cb56f06163e9eba54a44c9312ca67458220d8`  
		Last Modified: Tue, 25 Jun 2024 22:57:27 GMT  
		Size: 172.2 MB (172212218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:23efab1834ca487397c307c29b362a4f30d0180eede4008547bf87989c784d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2066960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bbc849255da33b9c004439fac42bac1bb33d21ddad38776d887c1c06d17862`

```dockerfile
```

-	Layers:
	-	`sha256:61cecfadceb961c7e0d0b8113edef133f87bcdaf07ae21ac297b3924be448d03`  
		Last Modified: Tue, 25 Jun 2024 22:57:26 GMT  
		Size: 2.1 MB (2054038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e38435ffa3e703e89e2e849304d40a327d331de9e55d2d183b60468c2a45bc5`  
		Last Modified: Tue, 25 Jun 2024 22:57:26 GMT  
		Size: 12.9 KB (12922 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:8db440d82d2cfa50057e7c69fb1171cf6e7bec41686085d017ff9c95578665e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208841101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19267522d340f26c418f6837ec8d94eaf2d64b11f6a66812098fe793aa09ecba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 May 2024 05:12:02 GMT
ARG RELEASE
# Thu, 09 May 2024 05:12:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 09 May 2024 05:12:02 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Thu, 09 May 2024 05:12:02 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 05:12:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 09 May 2024 05:12:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 05:12:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6361c43922dd1b73a50a72a014784973eb6b06d1b73af66328a1fedcc021e480`  
		Last Modified: Tue, 25 Jun 2024 23:50:31 GMT  
		Size: 1.6 MB (1574413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2f2b2bb92517562cc54a7709a1649468050868172a075982c9539f0882cc5e`  
		Last Modified: Tue, 25 Jun 2024 23:52:29 GMT  
		Size: 172.8 MB (172805995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:88bccdc63f96a800fb81cadad4c205581b69425c9d14911f48f1a281021f4267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21db540e988ddb268ee3eab84cd5b499767dc45b2d54ebda0a0602bc45094bb2`

```dockerfile
```

-	Layers:
	-	`sha256:157e24d73638ac7bd92608084c85eecc4ba1f920c48109ea26415eb9acff3025`  
		Last Modified: Tue, 25 Jun 2024 23:52:24 GMT  
		Size: 2.1 MB (2056461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46f5777f5d04514482930a0f6ff24ed60d5648cef4e961496395b7f726c4f2eb`  
		Last Modified: Tue, 25 Jun 2024 23:52:24 GMT  
		Size: 13.0 KB (12952 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:0645e8b60e71f613d08e293195d77b2bbe76f8c7d898286d2042a21ed9a2e35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191519123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c32a6c27e28c805dddca01ae89778b1ff723eb1bfc6f84e0f64261d6676a5fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 May 2024 05:12:02 GMT
ARG RELEASE
# Thu, 09 May 2024 05:12:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 09 May 2024 05:12:02 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Thu, 09 May 2024 05:12:02 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 05:12:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 09 May 2024 05:12:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 05:12:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51938117bdde1396c0e2d8ef3c52c92b614260596f918f02273bccf82a7f3ff4`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 1.5 MB (1477329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4682166c6f2936c53cc51970d9c062706c3618580e5db67faa6dee70be84f899`  
		Last Modified: Tue, 25 Jun 2024 23:31:34 GMT  
		Size: 162.0 MB (162041279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:fd21008e1b9acd37b396b7569b897c27444f047b969607bb170552073b10b8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2040688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a46215bb2dd86a04bdda1cd109c0e81c68420cccdf35081202584df4cb62e`

```dockerfile
```

-	Layers:
	-	`sha256:30bee264f47343be57ca6b825938db56bf71524dbfd16920e8e6cefa7b87e527`  
		Last Modified: Tue, 25 Jun 2024 23:31:32 GMT  
		Size: 2.0 MB (2027764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:176e686f83fe08e660bb840f75571a8ad02d240b6a60194e367b8465cf90bc3a`  
		Last Modified: Tue, 25 Jun 2024 23:31:32 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json
