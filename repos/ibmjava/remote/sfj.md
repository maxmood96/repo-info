## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:e041d15f6abe07a37d6defdcb81c3aa56b5b66bde34591763420ed01a3e29fbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:f65bd073daedb49ed96802b60a76f60119b31e755431165c909ccf2d0dbba269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101481307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2eee2c497b4bcd0e07509983c88e6dee908c0234575ca514ac4392d3a2e696`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d6a70c8cfbaff37e547ebecf7b3ad0758bfb5289727983c56aa59c351a0026`  
		Last Modified: Wed, 02 Jul 2025 03:11:21 GMT  
		Size: 1.5 MB (1450016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0edd65963a4164de0d591d28a7fa637d8a55f8059bf8909fc2eb308395c09be`  
		Last Modified: Wed, 02 Jul 2025 03:11:26 GMT  
		Size: 70.5 MB (70495605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5a88e7f28b4a1d36de3580b70b1332e328c78e543bc84f4d65e581ee74812303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47467b5a1d6ef284a8136d436a11f46fb18d8e688f7ee3fb1021c1b54409594`

```dockerfile
```

-	Layers:
	-	`sha256:02f800dfa9063efbc4c3a838a283f891bb91d9751eb26d90d530e95c57ce42f2`  
		Last Modified: Wed, 02 Jul 2025 08:01:32 GMT  
		Size: 2.2 MB (2155939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1775d7d9d6cba9c0132d826a03a9cd2d7acb92cd1ec6ebe326ba6fcff1ffc800`  
		Last Modified: Wed, 02 Jul 2025 08:01:32 GMT  
		Size: 13.2 KB (13180 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:f79d9191c2cfd63a96e6104b819c0a7e5fcaa6935ef4ae9e712668f0c03f94d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107307499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c70aece4bce65f968965847dc6fa280d3cfd62a5160edbf632c9d9b15729da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b508e78ad839eb5804b4140d689c487ab1a9a5ee9bf667cf9d4f054b0f8aa3c`  
		Last Modified: Wed, 02 Jul 2025 03:55:31 GMT  
		Size: 71.3 MB (71328642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3d952bf4ba0008d0443b61c87f05520f6967a47d4dadf989491a93cec747473c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9310ab59c178144de5d53c77bfe20c325f5f00e0f4293e4b036a8aa4558b4`

```dockerfile
```

-	Layers:
	-	`sha256:5d99fc4ae86321e2a3eb17e319204cf5633501cf2c3fe9242c24a88a74f84451`  
		Last Modified: Wed, 02 Jul 2025 05:01:39 GMT  
		Size: 2.2 MB (2160440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cb3a42bca34bb15e981eeb6605c067349398490bf65c4b242538754665e3fc`  
		Last Modified: Wed, 02 Jul 2025 05:01:39 GMT  
		Size: 13.2 KB (13215 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:b61fcc1e3394922624f0fdb0fc3b2347aba3a05bb3358635e4f62babbc240ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100549501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b655ffbc6779da83e76f5aa0d8f03cd71161a0141acb526da3ca8ad54e88122`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f78588c4bb31985140e15e675b5832054fdf1cef60bb357597ede86a9b3e5`  
		Last Modified: Wed, 02 Jul 2025 04:47:58 GMT  
		Size: 1.5 MB (1455774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bdb28d67633587c8dee48a18d043dd21029b1a1d5da6d4773f8fce9a5fdda9`  
		Last Modified: Wed, 02 Jul 2025 04:49:58 GMT  
		Size: 71.1 MB (71091552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9816e5997f5b5c386169983e8580805733c89dd4b5962060b78879bd2ff259ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fddbb029316ccf02e292a218584f912b16df652872954b7a3a1cef655e123ea5`

```dockerfile
```

-	Layers:
	-	`sha256:d7df4a294962a55647be2bf3df71e1fddbdfbdc8ef889c7875f15ef3df5c6cc4`  
		Last Modified: Wed, 02 Jul 2025 08:01:39 GMT  
		Size: 2.2 MB (2159561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3011ea50a23a02def12b297ef9343fcb0dc50380c23bf76bc8372c6e06a1326`  
		Last Modified: Wed, 02 Jul 2025 08:01:40 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json
