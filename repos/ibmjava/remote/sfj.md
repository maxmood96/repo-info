## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:40e63a260f2157e4d470318e71373622eb3408b68b6ef0d9894ad1963ff22c86
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
$ docker pull ibmjava@sha256:7628d881ba0674509b2eefe88e4a6982f0aab75f1ef14e2c4717214096da9ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100799732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7296d5cbed60431bcc76d8e60c13892f788941c503ae38d611855de4905cbd2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85062255c784806257f398c294ffa1fc1ece8f3807b331c552f8a5d9eb573ce1`  
		Last Modified: Sat, 17 Aug 2024 02:05:00 GMT  
		Size: 1.4 MB (1438268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c6cd891e8619e69f9425f6a8dc3799f3e975f310d05624cbc3204333a3029a`  
		Last Modified: Sat, 17 Aug 2024 02:05:02 GMT  
		Size: 69.8 MB (69825439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:600d3b9900a3fa6ef979cec3ef9cf488c05892b47b5ef62642347da940716620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2025563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9814f00a2ae2e2e3aa3dcff207179f085b83c07e896209d7234e9cbc62aec232`

```dockerfile
```

-	Layers:
	-	`sha256:350233f3fd6d823d77744d27a5a0dbc0d9f07cf29771e1143ae70b0954ee0cff`  
		Last Modified: Sat, 17 Aug 2024 02:05:00 GMT  
		Size: 2.0 MB (2012636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40349aee86e56f81bd22e7ceea2fbf8c6d34d77b149e5143d9520b589d57ee36`  
		Last Modified: Sat, 17 Aug 2024 02:04:59 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:9f0b346c2bd8fb88be695298bd93a50e71107abd1d4672202c4306ecab6f9c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106319877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed63267ba14206906992a562145e87c0cc20a70c6f7a1aab14072ae737a3837`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
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
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4e478d2a3be6bab56c5ea9225d40cb542bd132a06ee142cb3308146fe7674f`  
		Last Modified: Sat, 17 Aug 2024 01:39:03 GMT  
		Size: 1.5 MB (1523330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad99729ce9ba115729165bf923b99ac59bb28ccb2a63c2807ff3e8a8754b102b`  
		Last Modified: Sat, 17 Aug 2024 01:40:06 GMT  
		Size: 70.3 MB (70332369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:fd729be4b1d30d8a661dba213cd1318076e99cd2aca61ee4ce752335eabf2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2028832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8f221b3e65bc28f1ec04ce76c8b4148c668ea65ff817d5ce2aaeefb4270b51`

```dockerfile
```

-	Layers:
	-	`sha256:7db8905fb3700a2e7dd2ad34660a860506160b33639f16ba44fc85b9220f4517`  
		Last Modified: Sat, 17 Aug 2024 01:40:04 GMT  
		Size: 2.0 MB (2015877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b35e6e66b7448c2ca1434c4e9708322fa559b47276ef9e93bba53f1faf1f4ed6`  
		Last Modified: Sat, 17 Aug 2024 01:40:04 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:39c393af71fb43550c773850e2a0e0ac7f9b266d04e989672f37b177d5b8f8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99911343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0cfffebe571da9b863a4fa0b2930e6bb031fb4eb6c538b53120942e730228c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
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
	-	`sha256:e280dadf5b2aeff3eee5ef7e055d95037f9fdf834a26d90fa2a2127a91d7cf49`  
		Last Modified: Tue, 13 Aug 2024 10:45:20 GMT  
		Size: 28.0 MB (28001322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bd23a2bae158f6db334cabf77fa6c837c47102c7aa7f55dc0c5bba3d8a9928`  
		Last Modified: Sat, 17 Aug 2024 02:32:13 GMT  
		Size: 1.4 MB (1441904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90038246df36bd218e46d1149c88035ef637889453664962ce33e4199b218ba`  
		Last Modified: Sat, 17 Aug 2024 02:33:11 GMT  
		Size: 70.5 MB (70468117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:7a47ad8d939075033d07a906c1e572f78bc8476200f1bb5cfb66a9fa1f1877e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f9bf819acc79352cc76a384e7a248c6a4ba52908bc36ce60fba46ea28182f2`

```dockerfile
```

-	Layers:
	-	`sha256:a1ae001b7c345c00be657fcf1f1cd7f1b54cb72be8bbe08a50d9f5b921cb3e84`  
		Last Modified: Sat, 17 Aug 2024 02:33:10 GMT  
		Size: 2.0 MB (2014992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebfabefeb3a4ddac35712837e898a4f1a0477fa2c5d2cc910e578f26209cf96`  
		Last Modified: Sat, 17 Aug 2024 02:33:10 GMT  
		Size: 12.9 KB (12926 bytes)  
		MIME: application/vnd.in-toto+json
