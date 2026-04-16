## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:cb6d7a596278de121699789801ab8eb0b7def6642a69951cf16ca34b23fb9df1
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
$ docker pull ibmjava@sha256:3a14b5984556e8fc0993827621b8c8b64e419028e41bcadca0ce3f435618b19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102230649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df32196461ef0ec34e6a8cc349dd3816390c9497994e1d72f93c981c8b5d9c0b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:43:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:43:00 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 20:43:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 20:43:23 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f7e6e23a459d508a1abf241b2061398a1aec74217c34c26e4045b3c5cc3ec0`  
		Last Modified: Wed, 15 Apr 2026 20:43:32 GMT  
		Size: 1.5 MB (1450156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58e8b751043787aa29355c95bee810f0392f4b6c024cbe7b101d311447c97c`  
		Last Modified: Wed, 15 Apr 2026 20:43:34 GMT  
		Size: 71.0 MB (71043995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0365b137c2c668acff2947f10cd08f1b746965473c7bfa5dd8cabeb126478d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295f4702c2492e56652fd74ef3155c3fda57ecadb47755168a3cd35f2f68474a`

```dockerfile
```

-	Layers:
	-	`sha256:1e2ca45aeb3b6074c931ad4a0ec0ce534e42ea7575c66b789a66281c27b3937f`  
		Last Modified: Wed, 15 Apr 2026 20:43:33 GMT  
		Size: 2.2 MB (2156549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8fd142bb184816755c48c529b4de22b4d14396281337eb0ec91092b9d814a92`  
		Last Modified: Wed, 15 Apr 2026 20:43:32 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:a5da2612afe2fd369a388208deb7e10c1c8b9faeb9f5ead043600761a8b1db03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108169505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbdff74e65251f931c593a9f4a115e49ccacd5ff9988cc4a143f741b8fcd005`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:35:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:35:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:35:59 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:37:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:37:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f08eac5722791db689e31db7f3285ed36585185e1d6504498fb2c08160e1`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 1.5 MB (1536273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd694889bf001caff37f11b8e72dafa84e801353564d721038f5fa09d87031`  
		Last Modified: Wed, 01 Apr 2026 20:37:30 GMT  
		Size: 72.0 MB (71983572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:67066ecdb648f23de1d408590d9c1124eebb66507badf17ece8f13e3a00397df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22a4c76c05bfe2ba2876fe07ea9da6cb3114b6ad73bc133604a3903cd587e31`

```dockerfile
```

-	Layers:
	-	`sha256:b9f85b52a6a2940a2fe7f53ea6d23d3db1f183ac1f7d2496188259d6bdb82592`  
		Last Modified: Wed, 01 Apr 2026 20:37:28 GMT  
		Size: 2.2 MB (2161050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8faabe4539b61fbef265dac4f544a92bba01828ffb3d9fd4ea2f2ec623c9423f`  
		Last Modified: Wed, 01 Apr 2026 20:37:27 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:4d072d9413ac4463a815d1ce6897ccf301ebdb2d7d80339d6d3302a27270a544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101743950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1609f3f652195ca934b1cc87286e2bfea4d0ddaca5d132f790f3647bd8e9c038`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:21:56 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:21:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:21:56 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:24:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:24:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad3ba51fec85d95bc5946df2275446083583154b2c7efc5456844e0bc64a45`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 1.5 MB (1455857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f729be7b49cfec4cd2b235d013ed3581054fa5e8b71feeda1493168cc8c60c`  
		Last Modified: Wed, 01 Apr 2026 20:24:47 GMT  
		Size: 72.1 MB (72085366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9ec577c012d35739d93d78593c621a00c41e638525eefe1ffd40b9d2f3b0aa16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe8db5465e6432d7d69d8dd097d31896481d60f5d01425c196e69c6f3896e73`

```dockerfile
```

-	Layers:
	-	`sha256:ac066dc2bd56d506a69bf1379dc64937b8e7367c67bb31b8eb526fd5a11c9f5a`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 2.2 MB (2160171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3f860477b481f504c6edadc01f659414897fd4b86b3692d5ff115333d5f3f6`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 12.6 KB (12600 bytes)  
		MIME: application/vnd.in-toto+json
