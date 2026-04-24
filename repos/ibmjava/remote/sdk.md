## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:1404efae6d95a96688dc58afb47a2afa95242b2baf730de74dd688e5f53cb121
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
$ docker pull ibmjava@sha256:9b1161b5997708d69456ffefe711060b0685003a718a5959d5b85375da5cc061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204707915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79996c84f0736757f63244b16fd497c36881d752b0e18dd2453d9120c9a53e1b`
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
# Fri, 24 Apr 2026 17:26:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:54 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:50 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd87c806116a3327741f8989fb20f94e5b7e156ca698501e1e0b0514c15176cc`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da11bf882625bc0731870fe51d67be8846835897063fdf7fbe2617b1a03e93`  
		Last Modified: Fri, 24 Apr 2026 17:29:10 GMT  
		Size: 173.5 MB (173521349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:45700dc05c34a9716c88c91d29db5679f43e8ff656dc81407744ab39c28171a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1976f38d39862ae8eb753f1f592043f3f45cbd6a3c73acee46f5e07f3831dfa2`

```dockerfile
```

-	Layers:
	-	`sha256:4685c695f7b699126f04c0133c6f05db0c8092762b2599d18d9fbdc415dc41aa`  
		Last Modified: Fri, 24 Apr 2026 17:29:06 GMT  
		Size: 3.1 MB (3085059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1d4c19363db2ec5c457921a18518fdc1b0c704368555bde399a36f22a8226a`  
		Last Modified: Fri, 24 Apr 2026 17:29:06 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:3cd62e59e8ac469bec05bbd31d2586260abfb38968b00020cb63727009b5bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210829577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244f1472f52f0660860e5c83bd857c6d650fdc27d9e85977c41aefb8a84ce5ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:27:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:27:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2132eaca12df4dc2a7b0af262a8068d86a7122d98ccc02571ca194fca2fb9e83`  
		Last Modified: Fri, 24 Apr 2026 17:28:02 GMT  
		Size: 174.6 MB (174644995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:648e9b3bb1e063fc9a77657904e3c3679a9af72a63a02eafad60f4e5b60c4a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513215ed1fe85c669bbbca9beb60df20ac0b233725aa806169610f5562009769`

```dockerfile
```

-	Layers:
	-	`sha256:fe2c542a9494fcebe3022bc6fb0348723ce899268dc778b1bc2eaa7523295b0b`  
		Last Modified: Fri, 24 Apr 2026 17:27:59 GMT  
		Size: 3.1 MB (3071008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31851a69dcf03f352b961db6065aa6700bdb371137b792bfc5e4650826622af6`  
		Last Modified: Fri, 24 Apr 2026 17:27:58 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:6bde71d20c9b03076df1700c452f830b1bc451f8fc04f363d94e177deedd3189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194827646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e38a8d9e206d1097635fb25f299c08692f008d8683b22a26a0a609814d26c9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:59:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:17 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:50 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a94005458eecbf59d36fdcb472759320381954eb3b9e0a8ea9c1e920dc2a0`  
		Last Modified: Wed, 15 Apr 2026 21:00:37 GMT  
		Size: 1.5 MB (1455873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d965b2264e89cbb2ca1fd752191cb709cc08ea307b3d630dd92092bcc30f153b`  
		Last Modified: Fri, 24 Apr 2026 17:30:11 GMT  
		Size: 165.2 MB (165169474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:666ff2484eff1711ff3f4ff50ee0f8d8a28b6a47b9fac3c9279dea5db248d931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6eb9845959b3fa0d5c2070645a6cca71486ee13fe72ea94165d45a60540bac`

```dockerfile
```

-	Layers:
	-	`sha256:5ef4874ad01ae0cb3663f01a0ca21317c72acf77f59b8e0513f712d5a59b4214`  
		Last Modified: Fri, 24 Apr 2026 17:29:56 GMT  
		Size: 2.8 MB (2758361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e21a593ba4aa71089bc08fb484ed9d46aa64d44ad80fb00e6c327dc3be099a`  
		Last Modified: Fri, 24 Apr 2026 17:29:53 GMT  
		Size: 12.6 KB (12597 bytes)  
		MIME: application/vnd.in-toto+json
