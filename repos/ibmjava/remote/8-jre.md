## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:caeac2e699120707ecf543710f949185406bc25000ccc84f25592bc056f7decf
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
$ docker pull ibmjava@sha256:16efa3e0cdbbb2a6489beb94c07b1fb6a1ad4b313c710d03b634e31de88ebd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166319247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11383c60ecd1177d27abbb62fda75d33741f8824a9dabfc1a334737e1aaf6c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Dec 2024 08:06:01 GMT
ARG RELEASE
# Mon, 09 Dec 2024 08:06:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Dec 2024 08:06:01 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 09 Dec 2024 08:06:01 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b1674f3fd30e4dcb3d385291132f551ac8d7344403a5ad960a2d20279739bee3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='057a8c0a079e1cf27b60c6bc03d164be99a94aed6d84025b6659178e51da78ca';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ec722e7ca051a1d708246c568656558c2a630bf9d727c90745bee7a3518cd76d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71a55e0ed61840d5a67bd0cb6637df80c114e2aca15b28929763c9296c3eda8d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1f7c6f067e6983975aa811b86a015fce44d929aad19de3813920bf01f890f6`  
		Last Modified: Tue, 04 Feb 2025 04:25:02 GMT  
		Size: 1.5 MB (1450018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaaba61617a28037919e0a43aaf4b03fc262e7635ab77073d2245f1601983b1`  
		Last Modified: Tue, 04 Feb 2025 04:25:06 GMT  
		Size: 135.3 MB (135333288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:225e2bd6548de9f282735bda5b754fe346b23ec9f26b61b98f54eb54291da2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2066225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc7cb56b4fde3baa032b4b3bd3ec373225aa24152f132402c3d39972604712b`

```dockerfile
```

-	Layers:
	-	`sha256:9c33d829db88fe1a443f3850ee8449136bf7f678c556792d4c12ca356d031721`  
		Last Modified: Tue, 04 Feb 2025 04:25:02 GMT  
		Size: 2.1 MB (2052454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be463d39361de7da2f7b297c709a1e536d132a5b24f357f069ddc24efc893ea4`  
		Last Modified: Tue, 04 Feb 2025 04:25:02 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:845d1102fa4ff57b7b5966483cc3e28e5fca5e2f9e69814497b7856900ffbb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172145557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e802fa3e26fb78b46c5b7d8262b605221e547223b6380f5e741177759f3995fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Dec 2024 08:06:01 GMT
ARG RELEASE
# Mon, 09 Dec 2024 08:06:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Dec 2024 08:06:01 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Mon, 09 Dec 2024 08:06:01 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b1674f3fd30e4dcb3d385291132f551ac8d7344403a5ad960a2d20279739bee3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='057a8c0a079e1cf27b60c6bc03d164be99a94aed6d84025b6659178e51da78ca';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ec722e7ca051a1d708246c568656558c2a630bf9d727c90745bee7a3518cd76d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71a55e0ed61840d5a67bd0cb6637df80c114e2aca15b28929763c9296c3eda8d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549562dbb9f45949b79117ad60c4bbdb1ae9a0fd0a32b6119b57bf804e7f1c77`  
		Last Modified: Tue, 04 Feb 2025 08:22:06 GMT  
		Size: 1.5 MB (1536037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8221b0b1602df9f0f596a6283b80e03191825096571de972cc3842eb41c1efef`  
		Last Modified: Tue, 04 Feb 2025 08:22:11 GMT  
		Size: 136.2 MB (136161585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a2b45572a4578271fd51d14fe0f52df9605f94a98b28ec5834edce160d93547f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af44b14e88d6fb402f298f1fecb8905c795e52c505a4e5475f636a623edcdf08`

```dockerfile
```

-	Layers:
	-	`sha256:933ffe3e4092f86cb7ab355ec4f33af3d10d5062bda4f57675238c8827b1121b`  
		Last Modified: Tue, 04 Feb 2025 08:22:06 GMT  
		Size: 2.1 MB (2055630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a2f357e965ab2f2a9c517c2a16f8f115a22d43d975585a7937c798d0de4bbb`  
		Last Modified: Tue, 04 Feb 2025 08:22:06 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:a925c3fe4da8bee3488d7ad48d265663e7502eb5b379583be67cb677c88c2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161798708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37074a0a572a9c6f662f1352c2920c1edd1050d14dd6f6290505df2b1b01d2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Dec 2024 08:06:01 GMT
ARG RELEASE
# Mon, 09 Dec 2024 08:06:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Dec 2024 08:06:01 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Mon, 09 Dec 2024 08:06:01 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b1674f3fd30e4dcb3d385291132f551ac8d7344403a5ad960a2d20279739bee3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='057a8c0a079e1cf27b60c6bc03d164be99a94aed6d84025b6659178e51da78ca';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ec722e7ca051a1d708246c568656558c2a630bf9d727c90745bee7a3518cd76d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71a55e0ed61840d5a67bd0cb6637df80c114e2aca15b28929763c9296c3eda8d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd4605c2f3ea5db01805ac2f6f0f57e95cff85dce667f56133b28c0f20728ce`  
		Last Modified: Tue, 04 Feb 2025 08:30:44 GMT  
		Size: 1.5 MB (1455537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b0aa57767add1200e71da3d869d870693a42d4ec453f4660401c0d9526d184`  
		Last Modified: Tue, 04 Feb 2025 08:30:47 GMT  
		Size: 132.3 MB (132342240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:651a50b2a50cf1f6ef4a879113aa0bffb6e2fb8bbc5b40e1b3eabb36a356ee87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2066177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5535e9b57f3cc3c558cebb8c4256ea3ef38dcda9402b9a721666f6f9fb729160`

```dockerfile
```

-	Layers:
	-	`sha256:2accc09c143619ef94d4542d514fe2b5abd3b16376228b5e8fc574ec810b236b`  
		Last Modified: Tue, 04 Feb 2025 08:30:44 GMT  
		Size: 2.1 MB (2052405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f645e53c634aa7c46c6f3418c59e6f4c34aca35e8b2a64d968dfcedb735dfb`  
		Last Modified: Tue, 04 Feb 2025 08:30:44 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json
