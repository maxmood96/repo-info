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
$ docker pull ibmjava@sha256:995a1043d08a987f2f02451800a8c506bc32e2cf5139056bcb03792a8128a856
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
$ docker pull ibmjava@sha256:49e6745bedb570c5dd42b1294f817f6d71f5967714adc240b2131158bda7c9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166528038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc3115f25e0b4c156f63ff6e7a3abe51fdd166022ef90d5306335e9b141bd1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:27:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:27:50 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:27:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a5a071dc71ec50d9e6bf289bce551e32f53569352f578e0fc2333f145b9d3d`  
		Last Modified: Thu, 13 Nov 2025 23:28:20 GMT  
		Size: 1.5 MB (1450101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a24fa2c8172ddda044d8b4efc0b0e749b7b1f9ef2ea15c077e9c4556dd0ef1`  
		Last Modified: Fri, 14 Nov 2025 00:46:50 GMT  
		Size: 135.5 MB (135541139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:70e13bb318c79f9535d21735da88a4d8bb4e96f0e7b6a3e573fcb0d049e2395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268264b952d71efa2c8bd79546df72975ec2dee8c8b46d2d18c4a2990101523c`

```dockerfile
```

-	Layers:
	-	`sha256:a57fbd1003871d9068f059efab5661ae522a5b441fe89900025a8a2423f22a54`  
		Last Modified: Fri, 14 Nov 2025 03:01:34 GMT  
		Size: 2.2 MB (2174120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cdb55eaf82834ca5f4b5a2c492bcb84d82b36ca51cd510ca53f6b0073fcd2dc`  
		Last Modified: Fri, 14 Nov 2025 03:01:35 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1ad9fb3522729e22305db99e3ff3947f678ca0c15c1f07bc28e4175997ba3869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172470026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd051ab6e2ce7c352ef170aaeebaec0a4b4c0f5e85f14e2b262e1bcd53f4cf4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:09:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:09:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:18 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e7e1d3389415400ac0426941c10b503c7973749305c39086324736e8f0f96f`  
		Last Modified: Fri, 14 Nov 2025 04:35:09 GMT  
		Size: 136.5 MB (136486934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:12fb2ba647ce812c3909cd17cedba997849eb4a2bfb8ac61c3cab3315576be2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6dedc427b00390d24626f01f3d3419b6d97bfbeb2168ea8bcdb400dac1762c`

```dockerfile
```

-	Layers:
	-	`sha256:aa8989a750b6ef2583092c949b853d3856cb06aefe68cba63a6db054ee7ae66a`  
		Last Modified: Fri, 14 Nov 2025 03:01:39 GMT  
		Size: 2.2 MB (2177410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d20cbc736aba0ce8bcc36d9d547b89bb321aee7d92c8dc6f3df04db046b00f2e`  
		Last Modified: Fri, 14 Nov 2025 03:01:40 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:80019858b3b79381eaabb9a23bcfb61c53801667fa26c8e129b68581e075d823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162409511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350b9b82860b39cc7191f3f9ae43638112071ae45e4205320304822ca722c65f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:33 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a9678ab189281593619203e2450fdcbd36a8625ad07efac390df083e4d257`  
		Last Modified: Thu, 13 Nov 2025 23:22:14 GMT  
		Size: 1.5 MB (1455765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24054275a262fe9d62e2d7392bd56dbbe9b0fb90ae5d7d3ad2c3d805bf38e31`  
		Last Modified: Fri, 14 Nov 2025 00:45:19 GMT  
		Size: 133.0 MB (132950461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e67ddbf5c85d7a05c00f9676acc24365a96bba3b830c3a5515ef77f508d70b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae37345e0fbee76db8ef6aa6272952b245127c71725c57c41209be21f23e68d1`

```dockerfile
```

-	Layers:
	-	`sha256:f822cbcce0a87d53242ed7dccfb67a1baa00ca1c7e3eb79a2d976e55711f12ad`  
		Last Modified: Fri, 14 Nov 2025 01:21:30 GMT  
		Size: 2.2 MB (2174081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9676d5aca0e23ac7ee8e90f3db00f93314c81a26d849bc483453c2af36cfc10`  
		Last Modified: Fri, 14 Nov 2025 01:21:31 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:995a1043d08a987f2f02451800a8c506bc32e2cf5139056bcb03792a8128a856
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
$ docker pull ibmjava@sha256:49e6745bedb570c5dd42b1294f817f6d71f5967714adc240b2131158bda7c9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166528038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc3115f25e0b4c156f63ff6e7a3abe51fdd166022ef90d5306335e9b141bd1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:27:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:27:50 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:27:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a5a071dc71ec50d9e6bf289bce551e32f53569352f578e0fc2333f145b9d3d`  
		Last Modified: Thu, 13 Nov 2025 23:28:20 GMT  
		Size: 1.5 MB (1450101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a24fa2c8172ddda044d8b4efc0b0e749b7b1f9ef2ea15c077e9c4556dd0ef1`  
		Last Modified: Fri, 14 Nov 2025 00:46:50 GMT  
		Size: 135.5 MB (135541139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:70e13bb318c79f9535d21735da88a4d8bb4e96f0e7b6a3e573fcb0d049e2395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268264b952d71efa2c8bd79546df72975ec2dee8c8b46d2d18c4a2990101523c`

```dockerfile
```

-	Layers:
	-	`sha256:a57fbd1003871d9068f059efab5661ae522a5b441fe89900025a8a2423f22a54`  
		Last Modified: Fri, 14 Nov 2025 03:01:34 GMT  
		Size: 2.2 MB (2174120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cdb55eaf82834ca5f4b5a2c492bcb84d82b36ca51cd510ca53f6b0073fcd2dc`  
		Last Modified: Fri, 14 Nov 2025 03:01:35 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1ad9fb3522729e22305db99e3ff3947f678ca0c15c1f07bc28e4175997ba3869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172470026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd051ab6e2ce7c352ef170aaeebaec0a4b4c0f5e85f14e2b262e1bcd53f4cf4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:09:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:09:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:18 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e7e1d3389415400ac0426941c10b503c7973749305c39086324736e8f0f96f`  
		Last Modified: Fri, 14 Nov 2025 04:35:09 GMT  
		Size: 136.5 MB (136486934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:12fb2ba647ce812c3909cd17cedba997849eb4a2bfb8ac61c3cab3315576be2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6dedc427b00390d24626f01f3d3419b6d97bfbeb2168ea8bcdb400dac1762c`

```dockerfile
```

-	Layers:
	-	`sha256:aa8989a750b6ef2583092c949b853d3856cb06aefe68cba63a6db054ee7ae66a`  
		Last Modified: Fri, 14 Nov 2025 03:01:39 GMT  
		Size: 2.2 MB (2177410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d20cbc736aba0ce8bcc36d9d547b89bb321aee7d92c8dc6f3df04db046b00f2e`  
		Last Modified: Fri, 14 Nov 2025 03:01:40 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:80019858b3b79381eaabb9a23bcfb61c53801667fa26c8e129b68581e075d823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162409511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350b9b82860b39cc7191f3f9ae43638112071ae45e4205320304822ca722c65f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:33 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a9678ab189281593619203e2450fdcbd36a8625ad07efac390df083e4d257`  
		Last Modified: Thu, 13 Nov 2025 23:22:14 GMT  
		Size: 1.5 MB (1455765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24054275a262fe9d62e2d7392bd56dbbe9b0fb90ae5d7d3ad2c3d805bf38e31`  
		Last Modified: Fri, 14 Nov 2025 00:45:19 GMT  
		Size: 133.0 MB (132950461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e67ddbf5c85d7a05c00f9676acc24365a96bba3b830c3a5515ef77f508d70b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae37345e0fbee76db8ef6aa6272952b245127c71725c57c41209be21f23e68d1`

```dockerfile
```

-	Layers:
	-	`sha256:f822cbcce0a87d53242ed7dccfb67a1baa00ca1c7e3eb79a2d976e55711f12ad`  
		Last Modified: Fri, 14 Nov 2025 01:21:30 GMT  
		Size: 2.2 MB (2174081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9676d5aca0e23ac7ee8e90f3db00f93314c81a26d849bc483453c2af36cfc10`  
		Last Modified: Fri, 14 Nov 2025 01:21:31 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:ec1454045d40defd3f805a884b90b9913464068dec60e6c959369dd77c028fc2
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
$ docker pull ibmjava@sha256:86c128f42776cb3e149ecec62aedfe8cd6303679519fca7a921539472cce8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203772416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba79bf0593bc38b0aac7311f50cbce54c2f5ab85e906b16f137e0e8661a25437`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:28:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:28:03 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:28:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fda1bb6a32e3206e092d04e6f2b4989287f7414006a3c19fdd79101c7c0320`  
		Last Modified: Thu, 13 Nov 2025 23:28:34 GMT  
		Size: 1.5 MB (1450088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d628e848bfe7ecb94b3fa8754c2036aaf9a7ea4c754f9a7cb38d43ed8a694e2`  
		Last Modified: Fri, 14 Nov 2025 01:40:52 GMT  
		Size: 172.8 MB (172785530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2692227cc89bfbd3f1f4296a5dd5a889122a308f3cb256cc63690f10524d453a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b73fef13052681cbb657dd78389847526710c572f64ccd60f0055a00786dc3`

```dockerfile
```

-	Layers:
	-	`sha256:b5d0eb17b017c673c013cc61cefea119c429b20b0d800e73eec4580fb6dab555`  
		Last Modified: Fri, 14 Nov 2025 03:01:46 GMT  
		Size: 3.1 MB (3084440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12aabb4a687d159154e210f0f786385ba070fd9bf6c6e77b27cbc674951f4afe`  
		Last Modified: Fri, 14 Nov 2025 03:01:47 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:25421d1a5da4a6eee6c765a61f6167da38ffce5ebc751fd28e2ea79c9664c102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209925860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d134fd130e9cf1dd158280b179bdcdbb59042ffcac898601627b536e5c6e91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:11:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:11:29 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:18 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c6623dd21855ae1933ed5c3eda4d5180cd11ab6de8632ffb7cfe68b8b9498`  
		Last Modified: Fri, 14 Nov 2025 04:37:44 GMT  
		Size: 173.9 MB (173942768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:68858208ea0f71112ded405124dca4cb43810cd9a75a17cc019383ac17e7ce68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e88c965570dc6bb50b1f027eae93fa3f0c38a49c8ae240e09cc37638eaf803b`

```dockerfile
```

-	Layers:
	-	`sha256:f7b8f61bf68fa68df756d287275670732f44c8c43365d50bbf8eefb3dc4383d6`  
		Last Modified: Fri, 14 Nov 2025 03:01:52 GMT  
		Size: 3.1 MB (3070389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234c04810a6f657bdef2747e4a0fdeb13e1e0097afa70161549ce9c764ee3ae9`  
		Last Modified: Fri, 14 Nov 2025 03:01:52 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:32526e276ef0662591ca96f83d36f3a5004d8faa0d265c4d04bb8cfda32596da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192762033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851e61fe3ba0db6ca49863c2d260aa2a3ae43d9d5b74d2a6a387a784581131f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:33 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a9678ab189281593619203e2450fdcbd36a8625ad07efac390df083e4d257`  
		Last Modified: Thu, 13 Nov 2025 23:22:14 GMT  
		Size: 1.5 MB (1455765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f435bb0c415b0011e7ce572f4aace1b1bf6baf2e55cffcd5f380b640cd57b19a`  
		Last Modified: Fri, 14 Nov 2025 04:38:17 GMT  
		Size: 163.3 MB (163302983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:cfeb3a351cfa81517ab41fc2afed862f1e899dfdddcf52f7f7d4535b677b23dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6daf1ca7c8b465059fd77c2a6d876aedb2abc365fee497a1414d88431e697`

```dockerfile
```

-	Layers:
	-	`sha256:ad87e48541a92dbb688786b8857b43f74b8d8249eeb45809783e4a5a0faa48fb`  
		Last Modified: Fri, 14 Nov 2025 03:01:57 GMT  
		Size: 2.8 MB (2757756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b92ba9410a9707b9c930f48d91d87829386d27a89bf474a3bd9f89af01534f0d`  
		Last Modified: Fri, 14 Nov 2025 03:01:57 GMT  
		Size: 12.6 KB (12597 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:79b6e7b5f4f45eb532e4dc42477dc8ac7926208c2336ecd461941d39c29b01f3
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
$ docker pull ibmjava@sha256:94c86ca640ae5046c95125186258feb487169dc14a5db3739149ecc45a30e66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101795904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b299bebb433c40b89c3876eecd6aa8965dfdf6019f033c58f229af13cab68dc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:27:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:27:49 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:27:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f22293aa3dd1339100ae535f17165394ff107c8e3d96405d05f60dbd18f33f`  
		Last Modified: Thu, 13 Nov 2025 23:28:15 GMT  
		Size: 1.5 MB (1450120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d0c814951bc26aff8bff2d03b3ec64752fbafbeaf30e4528abafc99f9fc4f`  
		Last Modified: Thu, 13 Nov 2025 23:28:20 GMT  
		Size: 70.8 MB (70808986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e9344b379d323244df6ad5d78a9f1e6655495a33c20d00de0f8b2223d748a1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae97aa9fb04459eba1b3315f5647068b02997c2f37f5e9e5d99d1bb3490246fc`

```dockerfile
```

-	Layers:
	-	`sha256:d6beec6b486e9d9052486b54ddc3494cf60d82e956cd174864a2eed4cc32639e`  
		Last Modified: Fri, 14 Nov 2025 03:01:57 GMT  
		Size: 2.2 MB (2156553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d0c3e94320d49bb99b87a3b2a6412ba1164c208415e2977b987c85e2742207`  
		Last Modified: Fri, 14 Nov 2025 03:01:58 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:518898ecd353b1044020a3ac61e07f26981f33b798bbf9711c40e45d12ffaa2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107727942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c19e111323729ada63eb5bb62d1a94e18e1f008cb6d02beb26b9505c4908fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:10:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:10:32 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:18 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654c90ad57f1edace0e0837db894bc0f380d9c70a6642765f5625f5c2bd33fbb`  
		Last Modified: Fri, 14 Nov 2025 00:11:27 GMT  
		Size: 71.7 MB (71744850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:15a924c340dee20d80c5050ba5a9b2e3f12a5a1f2b70a7f2dee8c255ca85396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9472854f14764c847815b00a80b4630d2a02746fda6fe8d9bff753849d293f6a`

```dockerfile
```

-	Layers:
	-	`sha256:1f34efeedc9393f0bb43fb3d576570fa7073193d90e34d2aec31a7f0b8ee9daf`  
		Last Modified: Fri, 14 Nov 2025 03:02:02 GMT  
		Size: 2.2 MB (2161054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c5abf748813773a40dd4e7e8ebdd3fedbac5808e4446978ace29f3db51f229`  
		Last Modified: Fri, 14 Nov 2025 03:02:03 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:c754e5d3e4a6ca0dc1d32fbbf5150459e7aa23dabfca2e9babb52e88b32539a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101310498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2d682c11770b03a8d42c13260ad11557d9da23c232225f6ccd303c99c9db94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f53e2b06c4170f07ebf435fd72ef9ac6ac15a3124bc334c9b384fb2289ba66`  
		Last Modified: Thu, 13 Nov 2025 23:22:20 GMT  
		Size: 1.5 MB (1455744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfc6a31a90c9551e444527c9e1bb0727b7f3199306d593fec65d07940d0a8c5`  
		Last Modified: Thu, 13 Nov 2025 23:22:27 GMT  
		Size: 71.9 MB (71851469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5da19de5508346b8f1487fea4acb01e86f75db8078fad59a63c9372748181d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00225b72fe8bfd0bb9dfa99f09128dc1c66397f42de7a6a034fd4a8e1671a59`

```dockerfile
```

-	Layers:
	-	`sha256:5f989522c73a9337d0f297c998ef0be16b7597c489b888eab913735242270344`  
		Last Modified: Fri, 14 Nov 2025 03:02:08 GMT  
		Size: 2.2 MB (2160175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:937e6097f5a082656133be1b409dfec0d50a9082cb45b3421aabe98123715c36`  
		Last Modified: Fri, 14 Nov 2025 03:02:09 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:995a1043d08a987f2f02451800a8c506bc32e2cf5139056bcb03792a8128a856
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
$ docker pull ibmjava@sha256:49e6745bedb570c5dd42b1294f817f6d71f5967714adc240b2131158bda7c9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166528038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc3115f25e0b4c156f63ff6e7a3abe51fdd166022ef90d5306335e9b141bd1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:27:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:27:50 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:27:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a5a071dc71ec50d9e6bf289bce551e32f53569352f578e0fc2333f145b9d3d`  
		Last Modified: Thu, 13 Nov 2025 23:28:20 GMT  
		Size: 1.5 MB (1450101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a24fa2c8172ddda044d8b4efc0b0e749b7b1f9ef2ea15c077e9c4556dd0ef1`  
		Last Modified: Fri, 14 Nov 2025 00:46:50 GMT  
		Size: 135.5 MB (135541139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:70e13bb318c79f9535d21735da88a4d8bb4e96f0e7b6a3e573fcb0d049e2395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268264b952d71efa2c8bd79546df72975ec2dee8c8b46d2d18c4a2990101523c`

```dockerfile
```

-	Layers:
	-	`sha256:a57fbd1003871d9068f059efab5661ae522a5b441fe89900025a8a2423f22a54`  
		Last Modified: Fri, 14 Nov 2025 03:01:34 GMT  
		Size: 2.2 MB (2174120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cdb55eaf82834ca5f4b5a2c492bcb84d82b36ca51cd510ca53f6b0073fcd2dc`  
		Last Modified: Fri, 14 Nov 2025 03:01:35 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1ad9fb3522729e22305db99e3ff3947f678ca0c15c1f07bc28e4175997ba3869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172470026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd051ab6e2ce7c352ef170aaeebaec0a4b4c0f5e85f14e2b262e1bcd53f4cf4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:09:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:09:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:18 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e7e1d3389415400ac0426941c10b503c7973749305c39086324736e8f0f96f`  
		Last Modified: Fri, 14 Nov 2025 04:35:09 GMT  
		Size: 136.5 MB (136486934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:12fb2ba647ce812c3909cd17cedba997849eb4a2bfb8ac61c3cab3315576be2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6dedc427b00390d24626f01f3d3419b6d97bfbeb2168ea8bcdb400dac1762c`

```dockerfile
```

-	Layers:
	-	`sha256:aa8989a750b6ef2583092c949b853d3856cb06aefe68cba63a6db054ee7ae66a`  
		Last Modified: Fri, 14 Nov 2025 03:01:39 GMT  
		Size: 2.2 MB (2177410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d20cbc736aba0ce8bcc36d9d547b89bb321aee7d92c8dc6f3df04db046b00f2e`  
		Last Modified: Fri, 14 Nov 2025 03:01:40 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:80019858b3b79381eaabb9a23bcfb61c53801667fa26c8e129b68581e075d823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162409511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350b9b82860b39cc7191f3f9ae43638112071ae45e4205320304822ca722c65f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:33 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a9678ab189281593619203e2450fdcbd36a8625ad07efac390df083e4d257`  
		Last Modified: Thu, 13 Nov 2025 23:22:14 GMT  
		Size: 1.5 MB (1455765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24054275a262fe9d62e2d7392bd56dbbe9b0fb90ae5d7d3ad2c3d805bf38e31`  
		Last Modified: Fri, 14 Nov 2025 00:45:19 GMT  
		Size: 133.0 MB (132950461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e67ddbf5c85d7a05c00f9676acc24365a96bba3b830c3a5515ef77f508d70b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae37345e0fbee76db8ef6aa6272952b245127c71725c57c41209be21f23e68d1`

```dockerfile
```

-	Layers:
	-	`sha256:f822cbcce0a87d53242ed7dccfb67a1baa00ca1c7e3eb79a2d976e55711f12ad`  
		Last Modified: Fri, 14 Nov 2025 01:21:30 GMT  
		Size: 2.2 MB (2174081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9676d5aca0e23ac7ee8e90f3db00f93314c81a26d849bc483453c2af36cfc10`  
		Last Modified: Fri, 14 Nov 2025 01:21:31 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:995a1043d08a987f2f02451800a8c506bc32e2cf5139056bcb03792a8128a856
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
$ docker pull ibmjava@sha256:49e6745bedb570c5dd42b1294f817f6d71f5967714adc240b2131158bda7c9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166528038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc3115f25e0b4c156f63ff6e7a3abe51fdd166022ef90d5306335e9b141bd1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:27:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:27:50 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:27:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a5a071dc71ec50d9e6bf289bce551e32f53569352f578e0fc2333f145b9d3d`  
		Last Modified: Thu, 13 Nov 2025 23:28:20 GMT  
		Size: 1.5 MB (1450101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a24fa2c8172ddda044d8b4efc0b0e749b7b1f9ef2ea15c077e9c4556dd0ef1`  
		Last Modified: Fri, 14 Nov 2025 00:46:50 GMT  
		Size: 135.5 MB (135541139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:70e13bb318c79f9535d21735da88a4d8bb4e96f0e7b6a3e573fcb0d049e2395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268264b952d71efa2c8bd79546df72975ec2dee8c8b46d2d18c4a2990101523c`

```dockerfile
```

-	Layers:
	-	`sha256:a57fbd1003871d9068f059efab5661ae522a5b441fe89900025a8a2423f22a54`  
		Last Modified: Fri, 14 Nov 2025 03:01:34 GMT  
		Size: 2.2 MB (2174120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cdb55eaf82834ca5f4b5a2c492bcb84d82b36ca51cd510ca53f6b0073fcd2dc`  
		Last Modified: Fri, 14 Nov 2025 03:01:35 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1ad9fb3522729e22305db99e3ff3947f678ca0c15c1f07bc28e4175997ba3869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172470026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd051ab6e2ce7c352ef170aaeebaec0a4b4c0f5e85f14e2b262e1bcd53f4cf4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:09:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:09:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:18 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e7e1d3389415400ac0426941c10b503c7973749305c39086324736e8f0f96f`  
		Last Modified: Fri, 14 Nov 2025 04:35:09 GMT  
		Size: 136.5 MB (136486934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:12fb2ba647ce812c3909cd17cedba997849eb4a2bfb8ac61c3cab3315576be2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6dedc427b00390d24626f01f3d3419b6d97bfbeb2168ea8bcdb400dac1762c`

```dockerfile
```

-	Layers:
	-	`sha256:aa8989a750b6ef2583092c949b853d3856cb06aefe68cba63a6db054ee7ae66a`  
		Last Modified: Fri, 14 Nov 2025 03:01:39 GMT  
		Size: 2.2 MB (2177410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d20cbc736aba0ce8bcc36d9d547b89bb321aee7d92c8dc6f3df04db046b00f2e`  
		Last Modified: Fri, 14 Nov 2025 03:01:40 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:80019858b3b79381eaabb9a23bcfb61c53801667fa26c8e129b68581e075d823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162409511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350b9b82860b39cc7191f3f9ae43638112071ae45e4205320304822ca722c65f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:33 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a9678ab189281593619203e2450fdcbd36a8625ad07efac390df083e4d257`  
		Last Modified: Thu, 13 Nov 2025 23:22:14 GMT  
		Size: 1.5 MB (1455765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24054275a262fe9d62e2d7392bd56dbbe9b0fb90ae5d7d3ad2c3d805bf38e31`  
		Last Modified: Fri, 14 Nov 2025 00:45:19 GMT  
		Size: 133.0 MB (132950461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e67ddbf5c85d7a05c00f9676acc24365a96bba3b830c3a5515ef77f508d70b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae37345e0fbee76db8ef6aa6272952b245127c71725c57c41209be21f23e68d1`

```dockerfile
```

-	Layers:
	-	`sha256:f822cbcce0a87d53242ed7dccfb67a1baa00ca1c7e3eb79a2d976e55711f12ad`  
		Last Modified: Fri, 14 Nov 2025 01:21:30 GMT  
		Size: 2.2 MB (2174081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9676d5aca0e23ac7ee8e90f3db00f93314c81a26d849bc483453c2af36cfc10`  
		Last Modified: Fri, 14 Nov 2025 01:21:31 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:ec1454045d40defd3f805a884b90b9913464068dec60e6c959369dd77c028fc2
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
$ docker pull ibmjava@sha256:86c128f42776cb3e149ecec62aedfe8cd6303679519fca7a921539472cce8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203772416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba79bf0593bc38b0aac7311f50cbce54c2f5ab85e906b16f137e0e8661a25437`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:28:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:28:03 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:28:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fda1bb6a32e3206e092d04e6f2b4989287f7414006a3c19fdd79101c7c0320`  
		Last Modified: Thu, 13 Nov 2025 23:28:34 GMT  
		Size: 1.5 MB (1450088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d628e848bfe7ecb94b3fa8754c2036aaf9a7ea4c754f9a7cb38d43ed8a694e2`  
		Last Modified: Fri, 14 Nov 2025 01:40:52 GMT  
		Size: 172.8 MB (172785530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2692227cc89bfbd3f1f4296a5dd5a889122a308f3cb256cc63690f10524d453a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b73fef13052681cbb657dd78389847526710c572f64ccd60f0055a00786dc3`

```dockerfile
```

-	Layers:
	-	`sha256:b5d0eb17b017c673c013cc61cefea119c429b20b0d800e73eec4580fb6dab555`  
		Last Modified: Fri, 14 Nov 2025 03:01:46 GMT  
		Size: 3.1 MB (3084440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12aabb4a687d159154e210f0f786385ba070fd9bf6c6e77b27cbc674951f4afe`  
		Last Modified: Fri, 14 Nov 2025 03:01:47 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:25421d1a5da4a6eee6c765a61f6167da38ffce5ebc751fd28e2ea79c9664c102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209925860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d134fd130e9cf1dd158280b179bdcdbb59042ffcac898601627b536e5c6e91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:11:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:11:29 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:18 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c6623dd21855ae1933ed5c3eda4d5180cd11ab6de8632ffb7cfe68b8b9498`  
		Last Modified: Fri, 14 Nov 2025 04:37:44 GMT  
		Size: 173.9 MB (173942768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:68858208ea0f71112ded405124dca4cb43810cd9a75a17cc019383ac17e7ce68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e88c965570dc6bb50b1f027eae93fa3f0c38a49c8ae240e09cc37638eaf803b`

```dockerfile
```

-	Layers:
	-	`sha256:f7b8f61bf68fa68df756d287275670732f44c8c43365d50bbf8eefb3dc4383d6`  
		Last Modified: Fri, 14 Nov 2025 03:01:52 GMT  
		Size: 3.1 MB (3070389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234c04810a6f657bdef2747e4a0fdeb13e1e0097afa70161549ce9c764ee3ae9`  
		Last Modified: Fri, 14 Nov 2025 03:01:52 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:32526e276ef0662591ca96f83d36f3a5004d8faa0d265c4d04bb8cfda32596da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192762033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851e61fe3ba0db6ca49863c2d260aa2a3ae43d9d5b74d2a6a387a784581131f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:33 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a9678ab189281593619203e2450fdcbd36a8625ad07efac390df083e4d257`  
		Last Modified: Thu, 13 Nov 2025 23:22:14 GMT  
		Size: 1.5 MB (1455765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f435bb0c415b0011e7ce572f4aace1b1bf6baf2e55cffcd5f380b640cd57b19a`  
		Last Modified: Fri, 14 Nov 2025 04:38:17 GMT  
		Size: 163.3 MB (163302983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:cfeb3a351cfa81517ab41fc2afed862f1e899dfdddcf52f7f7d4535b677b23dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6daf1ca7c8b465059fd77c2a6d876aedb2abc365fee497a1414d88431e697`

```dockerfile
```

-	Layers:
	-	`sha256:ad87e48541a92dbb688786b8857b43f74b8d8249eeb45809783e4a5a0faa48fb`  
		Last Modified: Fri, 14 Nov 2025 03:01:57 GMT  
		Size: 2.8 MB (2757756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b92ba9410a9707b9c930f48d91d87829386d27a89bf474a3bd9f89af01534f0d`  
		Last Modified: Fri, 14 Nov 2025 03:01:57 GMT  
		Size: 12.6 KB (12597 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:79b6e7b5f4f45eb532e4dc42477dc8ac7926208c2336ecd461941d39c29b01f3
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
$ docker pull ibmjava@sha256:94c86ca640ae5046c95125186258feb487169dc14a5db3739149ecc45a30e66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101795904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b299bebb433c40b89c3876eecd6aa8965dfdf6019f033c58f229af13cab68dc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:27:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:27:49 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:27:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f22293aa3dd1339100ae535f17165394ff107c8e3d96405d05f60dbd18f33f`  
		Last Modified: Thu, 13 Nov 2025 23:28:15 GMT  
		Size: 1.5 MB (1450120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d0c814951bc26aff8bff2d03b3ec64752fbafbeaf30e4528abafc99f9fc4f`  
		Last Modified: Thu, 13 Nov 2025 23:28:20 GMT  
		Size: 70.8 MB (70808986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e9344b379d323244df6ad5d78a9f1e6655495a33c20d00de0f8b2223d748a1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae97aa9fb04459eba1b3315f5647068b02997c2f37f5e9e5d99d1bb3490246fc`

```dockerfile
```

-	Layers:
	-	`sha256:d6beec6b486e9d9052486b54ddc3494cf60d82e956cd174864a2eed4cc32639e`  
		Last Modified: Fri, 14 Nov 2025 03:01:57 GMT  
		Size: 2.2 MB (2156553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d0c3e94320d49bb99b87a3b2a6412ba1164c208415e2977b987c85e2742207`  
		Last Modified: Fri, 14 Nov 2025 03:01:58 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:518898ecd353b1044020a3ac61e07f26981f33b798bbf9711c40e45d12ffaa2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107727942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c19e111323729ada63eb5bb62d1a94e18e1f008cb6d02beb26b9505c4908fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:10:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:10:32 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:18 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654c90ad57f1edace0e0837db894bc0f380d9c70a6642765f5625f5c2bd33fbb`  
		Last Modified: Fri, 14 Nov 2025 00:11:27 GMT  
		Size: 71.7 MB (71744850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:15a924c340dee20d80c5050ba5a9b2e3f12a5a1f2b70a7f2dee8c255ca85396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9472854f14764c847815b00a80b4630d2a02746fda6fe8d9bff753849d293f6a`

```dockerfile
```

-	Layers:
	-	`sha256:1f34efeedc9393f0bb43fb3d576570fa7073193d90e34d2aec31a7f0b8ee9daf`  
		Last Modified: Fri, 14 Nov 2025 03:02:02 GMT  
		Size: 2.2 MB (2161054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c5abf748813773a40dd4e7e8ebdd3fedbac5808e4446978ace29f3db51f229`  
		Last Modified: Fri, 14 Nov 2025 03:02:03 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:c754e5d3e4a6ca0dc1d32fbbf5150459e7aa23dabfca2e9babb52e88b32539a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101310498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2d682c11770b03a8d42c13260ad11557d9da23c232225f6ccd303c99c9db94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f53e2b06c4170f07ebf435fd72ef9ac6ac15a3124bc334c9b384fb2289ba66`  
		Last Modified: Thu, 13 Nov 2025 23:22:20 GMT  
		Size: 1.5 MB (1455744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfc6a31a90c9551e444527c9e1bb0727b7f3199306d593fec65d07940d0a8c5`  
		Last Modified: Thu, 13 Nov 2025 23:22:27 GMT  
		Size: 71.9 MB (71851469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5da19de5508346b8f1487fea4acb01e86f75db8078fad59a63c9372748181d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00225b72fe8bfd0bb9dfa99f09128dc1c66397f42de7a6a034fd4a8e1671a59`

```dockerfile
```

-	Layers:
	-	`sha256:5f989522c73a9337d0f297c998ef0be16b7597c489b888eab913735242270344`  
		Last Modified: Fri, 14 Nov 2025 03:02:08 GMT  
		Size: 2.2 MB (2160175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:937e6097f5a082656133be1b409dfec0d50a9082cb45b3421aabe98123715c36`  
		Last Modified: Fri, 14 Nov 2025 03:02:09 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json
