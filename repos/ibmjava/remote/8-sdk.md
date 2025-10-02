## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:d9b9a4fb8434862dd7fc6cc7a1ac0e29c524ae1c84c5e93dd0b339094a6b04ff
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
$ docker pull ibmjava@sha256:2fa3d7d7fb4c447ccdc5964fe0d32f2c822070d941a8346f0708a287e22f99e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203651463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2bd699c0473df35ee574f35919062cd2ab45459d6e243cdafd57de3134d7e9`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7d68a3d4cc38061e19dd8052519563a02252fbe1d3dbaed60dda2ea6db29ce`  
		Last Modified: Thu, 02 Oct 2025 05:08:59 GMT  
		Size: 1.5 MB (1450032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0744a7a604dbb58fe5e4078242fbaf39f95dc5d2d2e603371c3ec80edda913`  
		Last Modified: Thu, 02 Oct 2025 08:02:15 GMT  
		Size: 172.7 MB (172664613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:733856284fa2c4dfa76ef41b8e5953b3043ef5d484e413c27c50ebb2324f524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3164a3bff509be6c3ac8bd26e713917e903ca392aef8cd737cf57e7110940d`

```dockerfile
```

-	Layers:
	-	`sha256:710ff4ca96997d9fd110affe5f5631cc0e161a8d9bd82a56e648cb876f5885c7`  
		Last Modified: Thu, 02 Oct 2025 08:01:24 GMT  
		Size: 3.1 MB (3083862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b213502c236f67bbd9a05f35264eb2d864025d612dc996ad09324eab6452e6e`  
		Last Modified: Thu, 02 Oct 2025 08:01:25 GMT  
		Size: 12.6 KB (12641 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:30c11ff6c3cdb705bb5faa222efe68d7aa0e66eb9fb7d6ce1fd677742b99f527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209796389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b84871b9f2c296cccdb0928fd788bb463502a1618e8e67ef5ee2a147f76c96`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:a0e12d70bbd76145a664c2ad09da3b7047ca7b4bdf8ee68884253b44216e44e8`  
		Last Modified: Thu, 02 Oct 2025 05:05:44 GMT  
		Size: 173.8 MB (173813397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:88e55f8ea28e7a5fff34532f648984715e1304379f9908cd3ffe35419180264b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81709ea92060ac158053aa1840312fb06bcb49c1ed758d07d9e349f812d6a713`

```dockerfile
```

-	Layers:
	-	`sha256:0206e5b7d743413db2ab729ce45c067f4cf99e7cb331cebe9fecdd7239d756d9`  
		Last Modified: Thu, 02 Oct 2025 05:01:32 GMT  
		Size: 3.1 MB (3069811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:920e4fec4255d5bcb4c95b8d4537eaad89c14f58d86b33b38feac37eb04d80ae`  
		Last Modified: Thu, 02 Oct 2025 05:01:33 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:fecb10a861104f1d154d1c99d5da60632504edd9d67df9392141078623bd6230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192092116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4573702aac5860387ef8adf945172a72557fae224d64a9071a05be143fdf3a4a`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:6118c3e9d908250603547950dd912481d3165025106362693552c9147b413eab`  
		Last Modified: Thu, 02 Oct 2025 05:06:12 GMT  
		Size: 162.6 MB (162632954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3074367e75d87c9cda7133792568d7193f1e35fb4a684e630f404d0e4c451a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2769819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46edf0f541e9db837f605bdffb80326ff0f300a83ca912356afbaa01ab454c66`

```dockerfile
```

-	Layers:
	-	`sha256:139159e0325f070989a7ff6b336f12c74d18e0fc343f2b8b4a3b34a6f1a18076`  
		Last Modified: Thu, 02 Oct 2025 05:01:38 GMT  
		Size: 2.8 MB (2757178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18b1061876e93ffc02eaa94a6c4ce0e36c0736ad63ea27a2e064041d2d1f605`  
		Last Modified: Thu, 02 Oct 2025 05:01:38 GMT  
		Size: 12.6 KB (12641 bytes)  
		MIME: application/vnd.in-toto+json
