## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:45299bb878db11e7984d1540adc1163665e2b1494ee3e01ec84dc33cb8ef2418
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
$ docker pull ibmjava@sha256:00ebac53fa0630f91c51c1fdaaa66af7fde1713ca8343c89c323dd529f771297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166508469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb2c1fd2e37ab0a06ac3ec8cfcd7e8cbe5f3253399ecfab77210fafd2b7e8ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216d2e3db6dcd0a26f34986ce22173eb5b9d914a38b00cd3a3a15fc67ce7501b`  
		Last Modified: Tue, 18 Feb 2025 21:29:40 GMT  
		Size: 1.5 MB (1450067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693eda7ffc53cac3deec3030ccd5dc4d3f7d5b12def99b48a6a1cbb7ab072bcf`  
		Last Modified: Tue, 18 Feb 2025 21:29:42 GMT  
		Size: 135.5 MB (135522461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5c234edad4e4ee5891790019720c65633b90a6468745432d3652d500cc5a4c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e7fd3d29421858e593aa6a02409496ad64b6f1e7b13dc61dba14148bc6e979`

```dockerfile
```

-	Layers:
	-	`sha256:4b7f415e45c571cb0c6e3baf8ada9a27f88d2edb9300a0c9fc95337a8f37219f`  
		Last Modified: Tue, 18 Feb 2025 21:29:40 GMT  
		Size: 2.1 MB (2051890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc17aacba1a1d951e9b337e9927123232b06642f20e163fb8b090b76aec610f`  
		Last Modified: Tue, 18 Feb 2025 21:29:40 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:9407f72f22f19826e88cfc58dfe23d75dc812e42f381b6c1b8601134841e5910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172338194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d92e859db11b73d03bc75d83524241d504bd489096e8333b5576ff7a2e5c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
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
	-	`sha256:5355d1509fcce51f292ca434a3a68692e5ec8e50218c8dc3ed6712bb03d06c09`  
		Last Modified: Tue, 18 Feb 2025 21:29:57 GMT  
		Size: 136.4 MB (136354222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:29a8a9ebe454c02331eff76fc35ddb5549fa4d923dac50a44623d8f2688600f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2b7041ff3aea2930d0b063b27bab41551d260513dd01567bb77fdcb838f457`

```dockerfile
```

-	Layers:
	-	`sha256:9bfb70d519b71d122403eaac856c72463ceb8a3871c62438dd6e5351594a3d76`  
		Last Modified: Tue, 18 Feb 2025 21:29:53 GMT  
		Size: 2.1 MB (2055066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07fd3de294a9f49cf8bb769ac6504766a2b1c9e1967b2e17757f4a2f6dd40d7`  
		Last Modified: Tue, 18 Feb 2025 21:29:53 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:b5b643b221366ae28110bdea622bea99f8a3bd84f9312d16182ae515d253c94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161996070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9f76b5162d40192c41b3f442bc7a1ff10e0f19d03afe79c36ba5ce904c8686`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:03 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:05 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Sun, 26 Jan 2025 05:32:05 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f4ed4c83fd203a93b2e2d3afc549f52d4e75a4e9c4ecade96808e6a2fe3ebb`  
		Last Modified: Tue, 18 Feb 2025 21:29:44 GMT  
		Size: 1.5 MB (1455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb4869d82527216d9f7895bf7380fd529d09d816d9127b4d85ad359511f1e41`  
		Last Modified: Tue, 18 Feb 2025 21:29:46 GMT  
		Size: 132.5 MB (132539572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:23481f94065ef3b06d6eb18ea1162c8cd5b3062b83796290a3345bd0517763d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cbe058aae3f61cb8b580d62f121586d2a410729a3aaa76062b6f1546cfc664`

```dockerfile
```

-	Layers:
	-	`sha256:020272c42bdde57c03259d0d076d11642b15a75b11c2a1d028c50a8dff97fcc2`  
		Last Modified: Tue, 18 Feb 2025 21:29:44 GMT  
		Size: 2.1 MB (2051841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc50c62899904bf8c378317c9eb02d11653d46f724ef2850ad9cc79435ae32ec`  
		Last Modified: Tue, 18 Feb 2025 21:29:44 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json
