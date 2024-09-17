<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ibmjava`

-	[`ibmjava:8`](#ibmjava8)
-	[`ibmjava:8-jre`](#ibmjava8-jre)
-	[`ibmjava:8-sdk`](#ibmjava8-sdk)
-	[`ibmjava:8-sfj`](#ibmjava8-sfj)
-	[`ibmjava:jre`](#ibmjavajre)
-	[`ibmjava:latest`](#ibmjavalatest)
-	[`ibmjava:sdk`](#ibmjavasdk)
-	[`ibmjava:sfj`](#ibmjavasfj)

## `ibmjava:8`

```console
$ docker pull ibmjava@sha256:206f07f685ae2208e0e563a9d096ed8bd7e853d34b15eb8da861558e655f4ee9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:23cee4709893af45adfcbbb150cb6a87646fd1c49e90a42867a9d82343794160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165988129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6522d8ad16894acb73648378885d117acd32f59152cb8c0eb507c868b9f5a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457c1d1531a658e8df67b03b1aedd5932972c09ea092da971395b95255ad78fe`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 1.4 MB (1438182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49083123286fc182df0b1fca6d374c8a140d8b2df476782db907a7ac50099b2e`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 135.0 MB (135014259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:087d2841161b5b195dcb548924bb79450757d2ee354e1eb82776ea0388aad4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2042106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0928b9c6bf2b40479c4c50a33f692bbb5a0a7bc8e8d8189992b64b9d5ce69058`

```dockerfile
```

-	Layers:
	-	`sha256:d14f9e80b96d2f64b8b560c1ae1336a7b3fd59ff72152a4029af613f773f3c8c`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 2.0 MB (2028589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5344ed958558dfbb67879197201e05e6409d64627574e89659fe83e23be413e2`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1934b82a74832797ba47b7e5520ad4ebcca75774a45c5a025674966818e4ebb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171442118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd389f76a6b2726f451b6ccc3f681976e58563af95224a9de61f4623bb0a6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bbf197217bba4985ce7c81155a527635555bffe359b533bea1b556d79b3516`  
		Last Modified: Tue, 17 Sep 2024 01:31:57 GMT  
		Size: 135.5 MB (135470631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ec80602f52cff612df0e31be2a09ce066e1a16c516aadafa423218c63473bf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2044296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476b2182c1302e2140f1e086b78e544c3a0396053294d9d3e19d1a53bae0d731`

```dockerfile
```

-	Layers:
	-	`sha256:b28a115f9f211fa10a710b887d77ae4f2db048a76ce71ecdc53ebefef99c86bf`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 2.0 MB (2030738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff55dc4a11bccf08981244017ffd598b6ccec17d3b6cc5814accf7c8edaab95`  
		Last Modified: Tue, 17 Sep 2024 01:31:53 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:641f4fb5d15cd9bb08941164f6cc589e3550ebc9653b2d29208849ce9d4e1c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161380238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9ce2fb9b4b046e9864ffa08aba748b67099b04129b6cb68166cd4a2d5871c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc820c088a0e7092d35c10e7db527e40828db015630f299fb22a1addd4bd545e`  
		Last Modified: Tue, 17 Sep 2024 02:12:23 GMT  
		Size: 131.9 MB (131936849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2cd65f3dff458bcc38b89f01cbdf2951afcded72fe836b731f492a6d9a1ba674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2041145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d44e92464ce876e837c8d0cbc88d4fea50d661b3a13aff91e1ad9bd639bede6`

```dockerfile
```

-	Layers:
	-	`sha256:7e24080804cbed8f5b350f969c1b47c01711cf0b2969ae436a70dd020a7ee325`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 2.0 MB (2027627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14e9b37f4711b17d387260647da6006560bbc49e7cdeaa88a3ff602245b6552`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:206f07f685ae2208e0e563a9d096ed8bd7e853d34b15eb8da861558e655f4ee9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:23cee4709893af45adfcbbb150cb6a87646fd1c49e90a42867a9d82343794160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165988129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6522d8ad16894acb73648378885d117acd32f59152cb8c0eb507c868b9f5a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457c1d1531a658e8df67b03b1aedd5932972c09ea092da971395b95255ad78fe`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 1.4 MB (1438182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49083123286fc182df0b1fca6d374c8a140d8b2df476782db907a7ac50099b2e`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 135.0 MB (135014259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:087d2841161b5b195dcb548924bb79450757d2ee354e1eb82776ea0388aad4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2042106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0928b9c6bf2b40479c4c50a33f692bbb5a0a7bc8e8d8189992b64b9d5ce69058`

```dockerfile
```

-	Layers:
	-	`sha256:d14f9e80b96d2f64b8b560c1ae1336a7b3fd59ff72152a4029af613f773f3c8c`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 2.0 MB (2028589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5344ed958558dfbb67879197201e05e6409d64627574e89659fe83e23be413e2`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1934b82a74832797ba47b7e5520ad4ebcca75774a45c5a025674966818e4ebb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171442118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd389f76a6b2726f451b6ccc3f681976e58563af95224a9de61f4623bb0a6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bbf197217bba4985ce7c81155a527635555bffe359b533bea1b556d79b3516`  
		Last Modified: Tue, 17 Sep 2024 01:31:57 GMT  
		Size: 135.5 MB (135470631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ec80602f52cff612df0e31be2a09ce066e1a16c516aadafa423218c63473bf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2044296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476b2182c1302e2140f1e086b78e544c3a0396053294d9d3e19d1a53bae0d731`

```dockerfile
```

-	Layers:
	-	`sha256:b28a115f9f211fa10a710b887d77ae4f2db048a76ce71ecdc53ebefef99c86bf`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 2.0 MB (2030738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff55dc4a11bccf08981244017ffd598b6ccec17d3b6cc5814accf7c8edaab95`  
		Last Modified: Tue, 17 Sep 2024 01:31:53 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:641f4fb5d15cd9bb08941164f6cc589e3550ebc9653b2d29208849ce9d4e1c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161380238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9ce2fb9b4b046e9864ffa08aba748b67099b04129b6cb68166cd4a2d5871c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc820c088a0e7092d35c10e7db527e40828db015630f299fb22a1addd4bd545e`  
		Last Modified: Tue, 17 Sep 2024 02:12:23 GMT  
		Size: 131.9 MB (131936849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2cd65f3dff458bcc38b89f01cbdf2951afcded72fe836b731f492a6d9a1ba674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2041145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d44e92464ce876e837c8d0cbc88d4fea50d661b3a13aff91e1ad9bd639bede6`

```dockerfile
```

-	Layers:
	-	`sha256:7e24080804cbed8f5b350f969c1b47c01711cf0b2969ae436a70dd020a7ee325`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 2.0 MB (2027627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14e9b37f4711b17d387260647da6006560bbc49e7cdeaa88a3ff602245b6552`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:025fbd71060d205512a5a5bffb53a5a1eb8ff19a757bcf6a0bc3533a3cc8748e
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
$ docker pull ibmjava@sha256:54f79b627664ae0e80eb7ae04384f2fa1357ebcbb6a56eb68da16a94f9c5e18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203106503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125cc8fd6e3a281bafbca09aea97c34ef2299f6ad9251b5f2fbc7cb9fa1d94d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c22e75fb9dfc02c2b846fdb7ea830b729536ea6e69c37adbe23e490a2a5b387`  
		Last Modified: Tue, 17 Sep 2024 00:59:30 GMT  
		Size: 1.4 MB (1438138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae95ac88ac0804bc3b7ca3e44688c77636d9eed729564f2ccecbc336cb0f2c0`  
		Last Modified: Tue, 17 Sep 2024 00:59:33 GMT  
		Size: 172.1 MB (172132677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8377ba027f8013d1dac2f8002a7d1903c2dc77ef2b4611771e206135d24557f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2097570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7600ced5ca2c2a9ea9522a334cb6894f7e6e57c711eb67d5dd00d64867bb518`

```dockerfile
```

-	Layers:
	-	`sha256:a3b584aa0fa4d6b4f33b5bde45b947ea752def99596508f4920bfb0d40836600`  
		Last Modified: Tue, 17 Sep 2024 00:59:31 GMT  
		Size: 2.1 MB (2084647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2916dd73c4c459966010fc72bcb4cee16d8f5fd2a344ba52c4f8ad1c9156c6`  
		Last Modified: Tue, 17 Sep 2024 00:59:30 GMT  
		Size: 12.9 KB (12923 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:155be61a85304135f4a5fb0f202646d634cbdee31c08a4ef9c8a7e27ece00edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208720340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13772ce0a1db0497acf4672fee866ae4754d57a6d3377863218e59f2ae1d5ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62636db2ac4815fe48801a3b62ed8d568ad28ca0e2330b3a84e227a61b023a72`  
		Last Modified: Tue, 17 Sep 2024 01:34:57 GMT  
		Size: 172.7 MB (172748853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c2b38ddd2c7793409ae9a705e5ea064ac88a7dacbd2544e261597dec16045faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2099736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd743695dda4a33158a39e94c2b9c3d12ac078513a87cdb0e57538c91c2c49`

```dockerfile
```

-	Layers:
	-	`sha256:bab4ee37005b1b2035b044667cc6e94910a2180f324feb400fcf22d6b9c68aae`  
		Last Modified: Tue, 17 Sep 2024 01:34:52 GMT  
		Size: 2.1 MB (2086784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d518a06071241da6083182ba063a703ceb6093cb1710e14ac3d3668c8af31af`  
		Last Modified: Tue, 17 Sep 2024 01:34:52 GMT  
		Size: 13.0 KB (12952 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:bd645f51b108228ea5eaddd74e4c4083ae4ccf297907e2e5670def952e7f3e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191654678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367306913f020efe1b31489ba569fd2288a37d305e7f96bcde6099ad9e4b6ec2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f675c68607c669df079bb79b19cf6109bef13663f5009617064a4ba0e4f20d89`  
		Last Modified: Tue, 17 Sep 2024 02:15:19 GMT  
		Size: 162.2 MB (162211289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0db96ed97fe7aedc9794860187b6abdbebe84cc0f564e5fb692a3bdbf85781ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5055449e053b6aba44ca9879c4f1e4b02692690aa3e362a466e771e2a341cbd`

```dockerfile
```

-	Layers:
	-	`sha256:6488eeca981afe31c0bf835c2826096870f806d4044bbfccd063e914c89219ed`  
		Last Modified: Tue, 17 Sep 2024 02:15:17 GMT  
		Size: 2.1 MB (2059444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa95e8866e05bbc9232fc741a41b7cd64d8cf47ede29bfadf2b5b1d03a552f12`  
		Last Modified: Tue, 17 Sep 2024 02:15:17 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:93aea8e18a402d139c044e0b42adfb3d1d4a4f14e1f1947998e2a73d4ce6e6ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:d02e87021e7d1c4bf9d28c39c5d349d9f28a598dd4a322da90bd0dc2986af4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100799326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2d02d7bfb3deb382b4767f226de05ecb9218c96248a5b3104b7dd6f22661c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='07df7f73c1ab08ca8adcfede1d35789fb36368d42226c32b998c36b84ace8aff';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='35bd6696ddb4a2ab54afc517efdd37ce3471cba589ebbcaad04019caec773510';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='32040e63bbf94b7a6e97ebcf28e4ba4c336c82b2e1c1131658e5762c82c204d7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='11ee2b25766e7c4685f2f2a89f3bf54265a97c8ae52bcddd3a46a21e872ea436';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188f260248587e97ad7aba1c8b62ac0f7ae04a410a8445ef1f6825d263eec7fb`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 1.4 MB (1438210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69ef95f6b840589f2c4d48b50149f7b29fa7959e44f4114c9a24ac1dbba7062`  
		Last Modified: Tue, 17 Sep 2024 00:58:59 GMT  
		Size: 69.8 MB (69825428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0e18653b122f3dfde18b1907c8709dc2a7845932aa550b46b8dca2d66d378696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2025563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee0ebbc80057314270961c40ed730ad1e97f693e1cad9e4ac62912ae358cfbc`

```dockerfile
```

-	Layers:
	-	`sha256:2bdfbdaa8ea50bd44efac9b4892ae3974a8150888a12a15a36337d6d1c52e8b9`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 2.0 MB (2012636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e24ba7cae41a6b29eb53210569edac163b3e8b37bc923b25b103fdb898c30c06`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:fd378abc239a7eaf0a54f396a41840acc925be6bc49d65a72aad7a0673b89de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106303863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f25d214329cea1f12082a1599097205ad25c6f714c287a44f4cb2e74f3f8fde`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='07df7f73c1ab08ca8adcfede1d35789fb36368d42226c32b998c36b84ace8aff';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='35bd6696ddb4a2ab54afc517efdd37ce3471cba589ebbcaad04019caec773510';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='32040e63bbf94b7a6e97ebcf28e4ba4c336c82b2e1c1131658e5762c82c204d7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='11ee2b25766e7c4685f2f2a89f3bf54265a97c8ae52bcddd3a46a21e872ea436';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e3ace98c6423017a0b0be23c57aadb0c7ef36d09ce2272001e0c362d95a894`  
		Last Modified: Tue, 17 Sep 2024 01:33:07 GMT  
		Size: 70.3 MB (70332376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:7f577506064dcb2cd5d6f2ece9467f69eb6a07766f1b3691b920ccb54a083a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2028832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861d6a7fcb8a51593e7b98e41183e4fd917ddaeb2eef90dcf2ff7bf3dc94b202`

```dockerfile
```

-	Layers:
	-	`sha256:cf2a9232f83bb48634b171b50ea33e1405ba3970bf1a56fdff60677a539eef9e`  
		Last Modified: Tue, 17 Sep 2024 01:33:04 GMT  
		Size: 2.0 MB (2015877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21c4e38bcf47aa98045e5bffa6a6e21d67ba56687494a5d0a86426266cf0e40`  
		Last Modified: Tue, 17 Sep 2024 01:33:04 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:404678effb10a31323c00ce5f62b6e9cf2c7325153cb1972a92e9540401aa690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99911524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1a95fc46964b519611a0ed1e4e645ba8e2bc60ce522a984d70dc7bc468c36d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='07df7f73c1ab08ca8adcfede1d35789fb36368d42226c32b998c36b84ace8aff';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='35bd6696ddb4a2ab54afc517efdd37ce3471cba589ebbcaad04019caec773510';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='32040e63bbf94b7a6e97ebcf28e4ba4c336c82b2e1c1131658e5762c82c204d7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='11ee2b25766e7c4685f2f2a89f3bf54265a97c8ae52bcddd3a46a21e872ea436';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2a9d317c2d10b091ecafc0fd6f83a60144f02ea3ade3815ab7ba8a30f34526`  
		Last Modified: Tue, 17 Sep 2024 02:13:32 GMT  
		Size: 70.5 MB (70468135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:131ac1fbbe9debc83a29dd99728fc5c42d22bbd49bf4116ae958a7c4cb5a69c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42168d4f95a050a5be69aa295e0e5bacc807fc5499c6f40a985a77e9d50dff6`

```dockerfile
```

-	Layers:
	-	`sha256:faec85a4e42837ba74045e58c6ed7996208531b5d607a687ce178d3f2fdda0ce`  
		Last Modified: Tue, 17 Sep 2024 02:13:31 GMT  
		Size: 2.0 MB (2014992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b90685c42d1f643654d5bd5c7f283270b064a383c8e62a28366cfdd86d8a0387`  
		Last Modified: Tue, 17 Sep 2024 02:13:31 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:206f07f685ae2208e0e563a9d096ed8bd7e853d34b15eb8da861558e655f4ee9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:23cee4709893af45adfcbbb150cb6a87646fd1c49e90a42867a9d82343794160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165988129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6522d8ad16894acb73648378885d117acd32f59152cb8c0eb507c868b9f5a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457c1d1531a658e8df67b03b1aedd5932972c09ea092da971395b95255ad78fe`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 1.4 MB (1438182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49083123286fc182df0b1fca6d374c8a140d8b2df476782db907a7ac50099b2e`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 135.0 MB (135014259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:087d2841161b5b195dcb548924bb79450757d2ee354e1eb82776ea0388aad4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2042106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0928b9c6bf2b40479c4c50a33f692bbb5a0a7bc8e8d8189992b64b9d5ce69058`

```dockerfile
```

-	Layers:
	-	`sha256:d14f9e80b96d2f64b8b560c1ae1336a7b3fd59ff72152a4029af613f773f3c8c`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 2.0 MB (2028589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5344ed958558dfbb67879197201e05e6409d64627574e89659fe83e23be413e2`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1934b82a74832797ba47b7e5520ad4ebcca75774a45c5a025674966818e4ebb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171442118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd389f76a6b2726f451b6ccc3f681976e58563af95224a9de61f4623bb0a6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bbf197217bba4985ce7c81155a527635555bffe359b533bea1b556d79b3516`  
		Last Modified: Tue, 17 Sep 2024 01:31:57 GMT  
		Size: 135.5 MB (135470631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ec80602f52cff612df0e31be2a09ce066e1a16c516aadafa423218c63473bf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2044296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476b2182c1302e2140f1e086b78e544c3a0396053294d9d3e19d1a53bae0d731`

```dockerfile
```

-	Layers:
	-	`sha256:b28a115f9f211fa10a710b887d77ae4f2db048a76ce71ecdc53ebefef99c86bf`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 2.0 MB (2030738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff55dc4a11bccf08981244017ffd598b6ccec17d3b6cc5814accf7c8edaab95`  
		Last Modified: Tue, 17 Sep 2024 01:31:53 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:641f4fb5d15cd9bb08941164f6cc589e3550ebc9653b2d29208849ce9d4e1c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161380238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9ce2fb9b4b046e9864ffa08aba748b67099b04129b6cb68166cd4a2d5871c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc820c088a0e7092d35c10e7db527e40828db015630f299fb22a1addd4bd545e`  
		Last Modified: Tue, 17 Sep 2024 02:12:23 GMT  
		Size: 131.9 MB (131936849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2cd65f3dff458bcc38b89f01cbdf2951afcded72fe836b731f492a6d9a1ba674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2041145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d44e92464ce876e837c8d0cbc88d4fea50d661b3a13aff91e1ad9bd639bede6`

```dockerfile
```

-	Layers:
	-	`sha256:7e24080804cbed8f5b350f969c1b47c01711cf0b2969ae436a70dd020a7ee325`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 2.0 MB (2027627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14e9b37f4711b17d387260647da6006560bbc49e7cdeaa88a3ff602245b6552`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:206f07f685ae2208e0e563a9d096ed8bd7e853d34b15eb8da861558e655f4ee9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:23cee4709893af45adfcbbb150cb6a87646fd1c49e90a42867a9d82343794160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165988129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6522d8ad16894acb73648378885d117acd32f59152cb8c0eb507c868b9f5a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457c1d1531a658e8df67b03b1aedd5932972c09ea092da971395b95255ad78fe`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 1.4 MB (1438182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49083123286fc182df0b1fca6d374c8a140d8b2df476782db907a7ac50099b2e`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 135.0 MB (135014259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:087d2841161b5b195dcb548924bb79450757d2ee354e1eb82776ea0388aad4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2042106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0928b9c6bf2b40479c4c50a33f692bbb5a0a7bc8e8d8189992b64b9d5ce69058`

```dockerfile
```

-	Layers:
	-	`sha256:d14f9e80b96d2f64b8b560c1ae1336a7b3fd59ff72152a4029af613f773f3c8c`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 2.0 MB (2028589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5344ed958558dfbb67879197201e05e6409d64627574e89659fe83e23be413e2`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1934b82a74832797ba47b7e5520ad4ebcca75774a45c5a025674966818e4ebb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171442118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd389f76a6b2726f451b6ccc3f681976e58563af95224a9de61f4623bb0a6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bbf197217bba4985ce7c81155a527635555bffe359b533bea1b556d79b3516`  
		Last Modified: Tue, 17 Sep 2024 01:31:57 GMT  
		Size: 135.5 MB (135470631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ec80602f52cff612df0e31be2a09ce066e1a16c516aadafa423218c63473bf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2044296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476b2182c1302e2140f1e086b78e544c3a0396053294d9d3e19d1a53bae0d731`

```dockerfile
```

-	Layers:
	-	`sha256:b28a115f9f211fa10a710b887d77ae4f2db048a76ce71ecdc53ebefef99c86bf`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 2.0 MB (2030738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff55dc4a11bccf08981244017ffd598b6ccec17d3b6cc5814accf7c8edaab95`  
		Last Modified: Tue, 17 Sep 2024 01:31:53 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:641f4fb5d15cd9bb08941164f6cc589e3550ebc9653b2d29208849ce9d4e1c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161380238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9ce2fb9b4b046e9864ffa08aba748b67099b04129b6cb68166cd4a2d5871c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc820c088a0e7092d35c10e7db527e40828db015630f299fb22a1addd4bd545e`  
		Last Modified: Tue, 17 Sep 2024 02:12:23 GMT  
		Size: 131.9 MB (131936849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2cd65f3dff458bcc38b89f01cbdf2951afcded72fe836b731f492a6d9a1ba674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2041145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d44e92464ce876e837c8d0cbc88d4fea50d661b3a13aff91e1ad9bd639bede6`

```dockerfile
```

-	Layers:
	-	`sha256:7e24080804cbed8f5b350f969c1b47c01711cf0b2969ae436a70dd020a7ee325`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 2.0 MB (2027627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14e9b37f4711b17d387260647da6006560bbc49e7cdeaa88a3ff602245b6552`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:025fbd71060d205512a5a5bffb53a5a1eb8ff19a757bcf6a0bc3533a3cc8748e
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
$ docker pull ibmjava@sha256:54f79b627664ae0e80eb7ae04384f2fa1357ebcbb6a56eb68da16a94f9c5e18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203106503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125cc8fd6e3a281bafbca09aea97c34ef2299f6ad9251b5f2fbc7cb9fa1d94d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c22e75fb9dfc02c2b846fdb7ea830b729536ea6e69c37adbe23e490a2a5b387`  
		Last Modified: Tue, 17 Sep 2024 00:59:30 GMT  
		Size: 1.4 MB (1438138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae95ac88ac0804bc3b7ca3e44688c77636d9eed729564f2ccecbc336cb0f2c0`  
		Last Modified: Tue, 17 Sep 2024 00:59:33 GMT  
		Size: 172.1 MB (172132677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8377ba027f8013d1dac2f8002a7d1903c2dc77ef2b4611771e206135d24557f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2097570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7600ced5ca2c2a9ea9522a334cb6894f7e6e57c711eb67d5dd00d64867bb518`

```dockerfile
```

-	Layers:
	-	`sha256:a3b584aa0fa4d6b4f33b5bde45b947ea752def99596508f4920bfb0d40836600`  
		Last Modified: Tue, 17 Sep 2024 00:59:31 GMT  
		Size: 2.1 MB (2084647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2916dd73c4c459966010fc72bcb4cee16d8f5fd2a344ba52c4f8ad1c9156c6`  
		Last Modified: Tue, 17 Sep 2024 00:59:30 GMT  
		Size: 12.9 KB (12923 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:155be61a85304135f4a5fb0f202646d634cbdee31c08a4ef9c8a7e27ece00edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208720340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13772ce0a1db0497acf4672fee866ae4754d57a6d3377863218e59f2ae1d5ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62636db2ac4815fe48801a3b62ed8d568ad28ca0e2330b3a84e227a61b023a72`  
		Last Modified: Tue, 17 Sep 2024 01:34:57 GMT  
		Size: 172.7 MB (172748853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c2b38ddd2c7793409ae9a705e5ea064ac88a7dacbd2544e261597dec16045faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2099736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd743695dda4a33158a39e94c2b9c3d12ac078513a87cdb0e57538c91c2c49`

```dockerfile
```

-	Layers:
	-	`sha256:bab4ee37005b1b2035b044667cc6e94910a2180f324feb400fcf22d6b9c68aae`  
		Last Modified: Tue, 17 Sep 2024 01:34:52 GMT  
		Size: 2.1 MB (2086784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d518a06071241da6083182ba063a703ceb6093cb1710e14ac3d3668c8af31af`  
		Last Modified: Tue, 17 Sep 2024 01:34:52 GMT  
		Size: 13.0 KB (12952 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:bd645f51b108228ea5eaddd74e4c4083ae4ccf297907e2e5670def952e7f3e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191654678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367306913f020efe1b31489ba569fd2288a37d305e7f96bcde6099ad9e4b6ec2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f675c68607c669df079bb79b19cf6109bef13663f5009617064a4ba0e4f20d89`  
		Last Modified: Tue, 17 Sep 2024 02:15:19 GMT  
		Size: 162.2 MB (162211289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0db96ed97fe7aedc9794860187b6abdbebe84cc0f564e5fb692a3bdbf85781ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5055449e053b6aba44ca9879c4f1e4b02692690aa3e362a466e771e2a341cbd`

```dockerfile
```

-	Layers:
	-	`sha256:6488eeca981afe31c0bf835c2826096870f806d4044bbfccd063e914c89219ed`  
		Last Modified: Tue, 17 Sep 2024 02:15:17 GMT  
		Size: 2.1 MB (2059444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa95e8866e05bbc9232fc741a41b7cd64d8cf47ede29bfadf2b5b1d03a552f12`  
		Last Modified: Tue, 17 Sep 2024 02:15:17 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:93aea8e18a402d139c044e0b42adfb3d1d4a4f14e1f1947998e2a73d4ce6e6ef
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
$ docker pull ibmjava@sha256:d02e87021e7d1c4bf9d28c39c5d349d9f28a598dd4a322da90bd0dc2986af4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100799326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2d02d7bfb3deb382b4767f226de05ecb9218c96248a5b3104b7dd6f22661c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='07df7f73c1ab08ca8adcfede1d35789fb36368d42226c32b998c36b84ace8aff';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='35bd6696ddb4a2ab54afc517efdd37ce3471cba589ebbcaad04019caec773510';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='32040e63bbf94b7a6e97ebcf28e4ba4c336c82b2e1c1131658e5762c82c204d7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='11ee2b25766e7c4685f2f2a89f3bf54265a97c8ae52bcddd3a46a21e872ea436';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188f260248587e97ad7aba1c8b62ac0f7ae04a410a8445ef1f6825d263eec7fb`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 1.4 MB (1438210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69ef95f6b840589f2c4d48b50149f7b29fa7959e44f4114c9a24ac1dbba7062`  
		Last Modified: Tue, 17 Sep 2024 00:58:59 GMT  
		Size: 69.8 MB (69825428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0e18653b122f3dfde18b1907c8709dc2a7845932aa550b46b8dca2d66d378696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2025563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee0ebbc80057314270961c40ed730ad1e97f693e1cad9e4ac62912ae358cfbc`

```dockerfile
```

-	Layers:
	-	`sha256:2bdfbdaa8ea50bd44efac9b4892ae3974a8150888a12a15a36337d6d1c52e8b9`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 2.0 MB (2012636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e24ba7cae41a6b29eb53210569edac163b3e8b37bc923b25b103fdb898c30c06`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:fd378abc239a7eaf0a54f396a41840acc925be6bc49d65a72aad7a0673b89de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106303863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f25d214329cea1f12082a1599097205ad25c6f714c287a44f4cb2e74f3f8fde`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='07df7f73c1ab08ca8adcfede1d35789fb36368d42226c32b998c36b84ace8aff';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='35bd6696ddb4a2ab54afc517efdd37ce3471cba589ebbcaad04019caec773510';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='32040e63bbf94b7a6e97ebcf28e4ba4c336c82b2e1c1131658e5762c82c204d7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='11ee2b25766e7c4685f2f2a89f3bf54265a97c8ae52bcddd3a46a21e872ea436';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e3ace98c6423017a0b0be23c57aadb0c7ef36d09ce2272001e0c362d95a894`  
		Last Modified: Tue, 17 Sep 2024 01:33:07 GMT  
		Size: 70.3 MB (70332376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:7f577506064dcb2cd5d6f2ece9467f69eb6a07766f1b3691b920ccb54a083a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2028832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861d6a7fcb8a51593e7b98e41183e4fd917ddaeb2eef90dcf2ff7bf3dc94b202`

```dockerfile
```

-	Layers:
	-	`sha256:cf2a9232f83bb48634b171b50ea33e1405ba3970bf1a56fdff60677a539eef9e`  
		Last Modified: Tue, 17 Sep 2024 01:33:04 GMT  
		Size: 2.0 MB (2015877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21c4e38bcf47aa98045e5bffa6a6e21d67ba56687494a5d0a86426266cf0e40`  
		Last Modified: Tue, 17 Sep 2024 01:33:04 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:404678effb10a31323c00ce5f62b6e9cf2c7325153cb1972a92e9540401aa690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99911524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1a95fc46964b519611a0ed1e4e645ba8e2bc60ce522a984d70dc7bc468c36d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='07df7f73c1ab08ca8adcfede1d35789fb36368d42226c32b998c36b84ace8aff';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='35bd6696ddb4a2ab54afc517efdd37ce3471cba589ebbcaad04019caec773510';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='32040e63bbf94b7a6e97ebcf28e4ba4c336c82b2e1c1131658e5762c82c204d7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='11ee2b25766e7c4685f2f2a89f3bf54265a97c8ae52bcddd3a46a21e872ea436';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2a9d317c2d10b091ecafc0fd6f83a60144f02ea3ade3815ab7ba8a30f34526`  
		Last Modified: Tue, 17 Sep 2024 02:13:32 GMT  
		Size: 70.5 MB (70468135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:131ac1fbbe9debc83a29dd99728fc5c42d22bbd49bf4116ae958a7c4cb5a69c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42168d4f95a050a5be69aa295e0e5bacc807fc5499c6f40a985a77e9d50dff6`

```dockerfile
```

-	Layers:
	-	`sha256:faec85a4e42837ba74045e58c6ed7996208531b5d607a687ce178d3f2fdda0ce`  
		Last Modified: Tue, 17 Sep 2024 02:13:31 GMT  
		Size: 2.0 MB (2014992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b90685c42d1f643654d5bd5c7f283270b064a383c8e62a28366cfdd86d8a0387`  
		Last Modified: Tue, 17 Sep 2024 02:13:31 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json
