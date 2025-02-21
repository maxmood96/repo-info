## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:4eac461dd7375388cbe8bb21f60a2bae48d43b5ce1a6630abb9d9b920f34f4e8
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
$ docker pull ibmjava@sha256:bb37f0796e35f3143fb2e8b815b948f29f89ad111751766f5da61b65bcb60f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101277577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44cf60a32cbe8804445689c791120caa4a02165e3efa4cb88122212ca5497bd`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='eed8efe1f3df198a66d24595f35433608aaed346916463353f64f664609df1a3';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d90bbeb03ba463c18d363088f606fdfe04905f52d6d79b53ff797ef5e3537f35';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f2c9a80832c6b631422fb72e18c269fb32d771e690bb9a821c8fa086ae685301';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='2e21e291682130e60d2d1a45a5f218a91f3d836061b7e3f6128ebd9a1f50a1d2';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8734ac738a48835f6f2603e6f40d356c185a1475225a9b062ebe4f1e133086`  
		Last Modified: Tue, 18 Feb 2025 21:29:25 GMT  
		Size: 1.5 MB (1450065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e06009dd7006856fb31282aec5decd347ee523a5f2993cb9d1169b3ba6c8efc`  
		Last Modified: Tue, 18 Feb 2025 21:29:26 GMT  
		Size: 70.3 MB (70291571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:13f671f20c281d232adabf67cb7bec4f19bad89bb994546d2409bbb6f8cb74b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2047506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77dc28aaff7ac7069f1af0ae80f5a3e0b4ddfef6d29cde57ecd33203a31001f`

```dockerfile
```

-	Layers:
	-	`sha256:e0f019ce2aabe45236cb53a6cde86e1c5586d1faef6b13392d9c1629ce06fb36`  
		Last Modified: Tue, 18 Feb 2025 21:29:25 GMT  
		Size: 2.0 MB (2034325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b13defd55ce7447f391cdc03317084dd88726d9349a5ddbde7248ee68e17a01`  
		Last Modified: Tue, 18 Feb 2025 21:29:25 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:668af527f0bf385dfbf9ee3331205a08c07f893dec93bd6d671a1bdebb5fa90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107105286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da25c692adc39988ed5a88d495ec987c1147e05b6bc3efaed6f17c8c3086b0f7`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='eed8efe1f3df198a66d24595f35433608aaed346916463353f64f664609df1a3';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d90bbeb03ba463c18d363088f606fdfe04905f52d6d79b53ff797ef5e3537f35';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f2c9a80832c6b631422fb72e18c269fb32d771e690bb9a821c8fa086ae685301';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='2e21e291682130e60d2d1a45a5f218a91f3d836061b7e3f6128ebd9a1f50a1d2';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:572ce67234b3a3c83eed112903fac78c06f709c166b5981bd7b4251e388bc382`  
		Last Modified: Tue, 18 Feb 2025 21:31:13 GMT  
		Size: 71.1 MB (71121314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:13af863715cf5caf1e1cb094a4a0e6de93c08f715990b7df50e0bd2f53620492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c69436704dd53f4da75f02ea546e9c146bcffeb042d0f2ccaebd87e8e44576`

```dockerfile
```

-	Layers:
	-	`sha256:3421f2e7059f4825d15e950315abb60a08ce8978b331986b1d0208c6a9e286e6`  
		Last Modified: Tue, 18 Feb 2025 21:31:11 GMT  
		Size: 2.0 MB (2038712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253cb264bf2e917fcff28c0b1380917229c094fdb998bf4bd4e84ffb2534f2a1`  
		Last Modified: Tue, 18 Feb 2025 21:31:11 GMT  
		Size: 13.2 KB (13215 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:b426589c5b50ebf41f26e610f7a68ea50af4285e40764de3610fe8e621a14963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100360338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ba023052edbcdb52b8ded9367478cdbc64234b49bb1c9fabd119acb39e6aff`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='eed8efe1f3df198a66d24595f35433608aaed346916463353f64f664609df1a3';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d90bbeb03ba463c18d363088f606fdfe04905f52d6d79b53ff797ef5e3537f35';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f2c9a80832c6b631422fb72e18c269fb32d771e690bb9a821c8fa086ae685301';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='2e21e291682130e60d2d1a45a5f218a91f3d836061b7e3f6128ebd9a1f50a1d2';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:b0e1d0e91c4571ad113750e5dc3cebdf9445aecd450c8112a81a127b1f9a5af0`  
		Last Modified: Tue, 18 Feb 2025 21:31:02 GMT  
		Size: 70.9 MB (70903840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:fab280796a2cf1ecf673c019e7816492e7ab6344faeb47459fd877177f06c1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92415d42c469a32c3fc4f4fa7f74ed2426a5d2c5fed0cebfc8b7b53c64b4c03e`

```dockerfile
```

-	Layers:
	-	`sha256:f40fa7abcdf3bca0ca43346165057302b5b4d233dd823af0d3c51898b775e7d3`  
		Last Modified: Tue, 18 Feb 2025 21:31:01 GMT  
		Size: 2.0 MB (2037937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb60a6c71716d9a684b26bb3d7125f013941d1d8b2647ba30db29636f6caf8c5`  
		Last Modified: Tue, 18 Feb 2025 21:31:00 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json
