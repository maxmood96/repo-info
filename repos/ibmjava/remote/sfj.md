## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:ccc952cb2d40a20b2524c9e9325a9407cdf89e781d1de7c495f49ee2cc388945
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
$ docker pull ibmjava@sha256:a5d1311e8e66784cdad426022a05f086a3a7864cab18f85918ad9b344492e389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101766881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f069aefb171bb11485f0f4a0e418228abf4644482ebed495270c1108ae01ea77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Sep 2025 07:18:43 GMT
ARG RELEASE
# Thu, 11 Sep 2025 07:18:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Sep 2025 07:18:43 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 11 Sep 2025 07:18:43 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5cc1fe4a2152a92f4eb29e17d29c0b87571724d32c79d01c02ff8e1e39162cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='41ad5b9cf2a6b78925bbf89b087358a409c949a7dd21318213faa84edc0f4f6c';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='7761751660e6eef25e16627dd18850eb978eb71757cfbc443d142a0ff24d3019';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef17c6a3999998bd42c81672df03548ed5f7cc790fe632ebaa501b7b76d24764`  
		Last Modified: Thu, 02 Oct 2025 05:08:57 GMT  
		Size: 1.5 MB (1450050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991cebceeab0cc2f3bf6cb7fe3a64954beb7c5f9a1ef04f20a614ca9ccb2e6eb`  
		Last Modified: Thu, 02 Oct 2025 05:09:06 GMT  
		Size: 70.8 MB (70780013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:63c42dd5c8ec3f7146729d61d5ef36be186436ced8cb720e63d4c06f7e9b589f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bf4600d791f1fb778eafb7bfa4248bffe73873cce0fff86376e030da0090ed`

```dockerfile
```

-	Layers:
	-	`sha256:542e12b3707ca28ac37cf850545404f1b489dc691fc36fd66419a0996149b01c`  
		Last Modified: Thu, 02 Oct 2025 08:01:29 GMT  
		Size: 2.2 MB (2155973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c23bc6b8f28ef5c196c0af5f33b5a521d3711ccad59ef42b695864232ea827c`  
		Last Modified: Thu, 02 Oct 2025 08:01:29 GMT  
		Size: 12.6 KB (12644 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:6d710a11e05851e8561216a359748055092b44ea4e67b4e837d55ddca6f2579d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107701465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141672d28ef48757b2553c91711092b7720915a76b326203c2c0bdbf7e6e5828`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Sep 2025 07:18:43 GMT
ARG RELEASE
# Thu, 11 Sep 2025 07:18:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Sep 2025 07:18:43 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Thu, 11 Sep 2025 07:18:43 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5cc1fe4a2152a92f4eb29e17d29c0b87571724d32c79d01c02ff8e1e39162cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='41ad5b9cf2a6b78925bbf89b087358a409c949a7dd21318213faa84edc0f4f6c';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='7761751660e6eef25e16627dd18850eb978eb71757cfbc443d142a0ff24d3019';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fbbb835d2e356809aec45fea40b6f5278fa45ef4d3e943633fba2d851c7c9`  
		Last Modified: Thu, 02 Oct 2025 03:15:21 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee784be21898e6e11ff5a3f56e80ed04cec1d7be610aa19d808ac245b5340c2`  
		Last Modified: Thu, 02 Oct 2025 02:38:08 GMT  
		Size: 71.7 MB (71718473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:babf4bd74c9079bc9f954d0057cf8cfba082083283349f307aae3529c4d52be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399f8312448865289c612a24d9090bded382083eb45cf3e37e46bf231d30b7b1`

```dockerfile
```

-	Layers:
	-	`sha256:6ada6d81601ba7db81fd505f3eae368aad6fff3856407202f480896ab2f42bb9`  
		Last Modified: Thu, 02 Oct 2025 05:01:40 GMT  
		Size: 2.2 MB (2160474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4248c35b133a6990a90611032761b35298a52555892198f9d4f8cc0079026007`  
		Last Modified: Thu, 02 Oct 2025 05:01:41 GMT  
		Size: 12.7 KB (12678 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:169d0e03dc12115977ec0c09d9a5a660160ff95005f3b1c38f98fde7bf48f348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100737626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02470f5af5e905bc0980d7b85844a55def2bd05f096dd2e46423b8e26b07fda7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Sep 2025 07:18:43 GMT
ARG RELEASE
# Thu, 11 Sep 2025 07:18:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Sep 2025 07:18:43 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Thu, 11 Sep 2025 07:18:43 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5cc1fe4a2152a92f4eb29e17d29c0b87571724d32c79d01c02ff8e1e39162cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='41ad5b9cf2a6b78925bbf89b087358a409c949a7dd21318213faa84edc0f4f6c';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='7761751660e6eef25e16627dd18850eb978eb71757cfbc443d142a0ff24d3019';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543bf796c5e3ca3d689f3ec6349f0c52c782a4da34026d3f7dbd32fbf895bed`  
		Last Modified: Thu, 02 Oct 2025 02:03:56 GMT  
		Size: 1.5 MB (1455749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2079453741ffa70128078da1d3bad2362c3b274cf67e0d031145700465b91e`  
		Last Modified: Thu, 02 Oct 2025 02:04:23 GMT  
		Size: 71.3 MB (71278464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:39505bc7dd79c6261d271b26a7b444a57154eca433651eb98cf19b69fe81cc4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d851b0ad3157ea3b6b9dd2becbc55cf6f2d727cc2933d0ef3aad40ac5134d33`

```dockerfile
```

-	Layers:
	-	`sha256:20e047be9535dc97eff387e0083faeed97670b60a125797b06c45bc2c86fe44f`  
		Last Modified: Thu, 02 Oct 2025 05:01:45 GMT  
		Size: 2.2 MB (2159595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:549755b2d202dce69c88199434125bccba0df693c0e7e95ccd8daefaa215c4f6`  
		Last Modified: Thu, 02 Oct 2025 05:01:46 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.in-toto+json
