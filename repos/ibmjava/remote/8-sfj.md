## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:826d1e282690e4d50c8d1fa61dc5eacce7f8f8046828a0b3ff4b8d78571a8304
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
$ docker pull ibmjava@sha256:4280ae84ea8aaeb7be70d746bc75891ccd5ebad49180fbe0e89c61fb4ea6c188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100892152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aec332a0bfdaed3dc6e549c8a40135253b4e9282be404f283f39160f4509086`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0dc4d4ec556f14815ea704157d8e442cdd0c7bb25f01f6db0a93e83e674309cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e56abc6d514c83549009267683c8f676a609566ca5e2a29826eebce0dd2f4cef';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='58f97d39de714ed9c86481ab6becf1623336f6016511863732d674444db72993';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='29fa3d5ae701b54a25ab2a074ff6654f285338b4b6cbac23654d740782fab736';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b94759cab840f5cd99fb9e48dc8632f42708c02a5bcd1e365f16fcd4fc03e`  
		Last Modified: Tue, 25 Jun 2024 22:57:15 GMT  
		Size: 1.5 MB (1469359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b07401adc35f221288de5c14608ec0f53bdc449419b91186b72594517320a9`  
		Last Modified: Tue, 25 Jun 2024 22:57:16 GMT  
		Size: 69.9 MB (69889039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3b6932ebeb8982f04867b0f4fc5f5702154dcfa6d598deff235eb3edd06f4e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2000284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4569ce1753ef10d93d4a6534482421d7fd2c4a5203a88e2960faf8a593f58d2`

```dockerfile
```

-	Layers:
	-	`sha256:4b22959ccb9ca82ccc2b76d7fcaebf87ae0de3da1495a097e4bf630c4a5371e9`  
		Last Modified: Tue, 25 Jun 2024 22:57:14 GMT  
		Size: 2.0 MB (1987357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb8e6afa484ce6c0c8fd844a73e64f341af1402dd2af13f4b6d83b7c4e88521`  
		Last Modified: Tue, 25 Jun 2024 22:57:14 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:d177352b4ad01fdabf683f56ad180d4359a362b7ec8f261cab06ed793cc5aaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106426100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49e65d10e2a08673142504c1312217a73ec18b238c7075c15db6d45bddc55ce`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0dc4d4ec556f14815ea704157d8e442cdd0c7bb25f01f6db0a93e83e674309cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e56abc6d514c83549009267683c8f676a609566ca5e2a29826eebce0dd2f4cef';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='58f97d39de714ed9c86481ab6becf1623336f6016511863732d674444db72993';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='29fa3d5ae701b54a25ab2a074ff6654f285338b4b6cbac23654d740782fab736';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:fda7976df36ad654d7984b39a8052dca7f11e2acce96ededbd11f839ad0a9d1e`  
		Last Modified: Tue, 25 Jun 2024 23:51:19 GMT  
		Size: 70.4 MB (70390994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3263efb13c774478185c0c7189ca40fccc44eb3c5fcb0a69105ba6a14a535545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3898091071ddff1a8727e06ce880599682b118295fb1ccae5c84864eaad00e49`

```dockerfile
```

-	Layers:
	-	`sha256:0fb174743354af290f3dd3255b765daceb9910aee13165f13b44581122d247f4`  
		Last Modified: Tue, 25 Jun 2024 23:51:17 GMT  
		Size: 2.0 MB (1990741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7c7713e6a1592285a107298930629ebb4e9458de4538335fcd92e57ad0e29d`  
		Last Modified: Tue, 25 Jun 2024 23:51:16 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:7a115df809c8195f6937ff1c8fce3bf66a4bcb75aabd1035a9715ad96f6f8310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99849167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e2dc17e3fadd7ea8295cea75b7e1bb6b31b2bbbbcc935aec7012a1a8f2fb2d`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0dc4d4ec556f14815ea704157d8e442cdd0c7bb25f01f6db0a93e83e674309cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e56abc6d514c83549009267683c8f676a609566ca5e2a29826eebce0dd2f4cef';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='58f97d39de714ed9c86481ab6becf1623336f6016511863732d674444db72993';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='29fa3d5ae701b54a25ab2a074ff6654f285338b4b6cbac23654d740782fab736';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:5360f7e1b49c938735e55303af7f943230a8b0b6ca3721d8380ac979f1da1c44`  
		Last Modified: Tue, 25 Jun 2024 23:30:43 GMT  
		Size: 70.4 MB (70371323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:261945bdd7b40cde7fce47ab154c7510e5f9e7004d1428273d931c075d04a3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dc6155af04ffae38d8c1af7d50112d78619fd55d8e710bd468cc724ec598d5`

```dockerfile
```

-	Layers:
	-	`sha256:1c9d93a0ed6c80e019b9a9073ee72421385dade8e672eaff2f1ac4cc8c693bda`  
		Last Modified: Tue, 25 Jun 2024 23:30:42 GMT  
		Size: 2.0 MB (1988746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7e450689c10c9f8f1a1ffdd43d3d43b499023f29f2e1061864b056fa1150d6`  
		Last Modified: Tue, 25 Jun 2024 23:30:42 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json
