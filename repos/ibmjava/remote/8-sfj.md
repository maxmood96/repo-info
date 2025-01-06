## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:34b6b74d56beb4a7533e98aee059e7513900975182eacffcdffc5ca0dd5f1e21
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
$ docker pull ibmjava@sha256:95716bfcfd15daa2492aab533b3e79109c80e3f72a5931b48eabca76eda2b1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101241679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709d73d2e5868a2b60c6a6252042431a5d74e6d9f9d7c4272d3987d04399fa34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3d8f2fbf7a0cdda8ee510bf8fa82df4bbcf08ad707091332b8577ac5cea251bf';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ede7b25ab451be1f224d95e2ea54e86feb2aaf03c92c8f0eac0773ccd53689d5';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='cceb03a0b74d4c6ddb672f675f7bd44ed6883882204cc6ff3222d607f5718191';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='0600b3689b85b636718e1b5fa59b0d7351c592ddc790968abea3a66b84793e1c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6e2315ffd23b1512fff41b0cb6d2c462a779ae0502da54a20bfc2114d61149`  
		Last Modified: Mon, 09 Dec 2024 19:28:29 GMT  
		Size: 1.4 MB (1449649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84202509c66318b6ab00fb73a6bc4bd97699967424a243e169a0cfef46051ce9`  
		Last Modified: Mon, 09 Dec 2024 19:28:30 GMT  
		Size: 70.3 MB (70256342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:968eb6180683d9c6126d33d6dc4146e227c66d39312bed02092deccbe2819d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2049088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65decd5c88bf25d1f5bca1ead8d5e166477d4b7af8f193400d6055f5c4ed0919`

```dockerfile
```

-	Layers:
	-	`sha256:566acec1f67464f745fe4d4108280fc0307e08a196be5a03c3656f5b820b9034`  
		Last Modified: Mon, 09 Dec 2024 19:28:29 GMT  
		Size: 2.0 MB (2035907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03ae2393a0114c11b34ded5a29fb73cd0bd121840ccf8dd8c2056565dd2ac6ab`  
		Last Modified: Mon, 09 Dec 2024 19:28:29 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:46feef6515a568d78cbde9f2fc3d6f74542721a9ebdb7200d83f30f0831a0d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107051479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b9a4b7a4917ee1c2ce9d2050aaf0e439741aa083628554d15a8120f2a7c0db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3d8f2fbf7a0cdda8ee510bf8fa82df4bbcf08ad707091332b8577ac5cea251bf';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ede7b25ab451be1f224d95e2ea54e86feb2aaf03c92c8f0eac0773ccd53689d5';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='cceb03a0b74d4c6ddb672f675f7bd44ed6883882204cc6ff3222d607f5718191';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='0600b3689b85b636718e1b5fa59b0d7351c592ddc790968abea3a66b84793e1c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
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
	-	`sha256:9944b5e6bb040c1a52551709f4e3ad17d9d27f07912a6a82806d6c687b107caf`  
		Last Modified: Mon, 09 Dec 2024 19:30:18 GMT  
		Size: 71.1 MB (71079992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:903f6be9afc840afacbf732198ab927e52349c25e4a256c0bfd559bd3867ffab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2047618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013978d71e11d94c1a9ea0885cac2448701cc83e7bd26f0d7941008227e92867`

```dockerfile
```

-	Layers:
	-	`sha256:9551b5065ff85002eaef84337f3eeb3d6ce6ac71e9fcac7c3f974de2b58f3d6b`  
		Last Modified: Mon, 09 Dec 2024 19:30:16 GMT  
		Size: 2.0 MB (2034403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab42f74e36b23dabd974cb247396ce5fc0b76b81878f8261115ea998fe3efa7`  
		Last Modified: Mon, 09 Dec 2024 19:30:15 GMT  
		Size: 13.2 KB (13215 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:be55ae72ae87bcc33e0bc896aae69b8292a298dd76f96ee0b4ea6d861fdc5f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100300115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b350bc2e286346e6761d39507913ecf7a71e5332692cbc0e89d492a81999a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3d8f2fbf7a0cdda8ee510bf8fa82df4bbcf08ad707091332b8577ac5cea251bf';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ede7b25ab451be1f224d95e2ea54e86feb2aaf03c92c8f0eac0773ccd53689d5';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='cceb03a0b74d4c6ddb672f675f7bd44ed6883882204cc6ff3222d607f5718191';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='0600b3689b85b636718e1b5fa59b0d7351c592ddc790968abea3a66b84793e1c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d359ab9a351f822600f500ec39ec9444924f1e4860d94e5784963eb296a444b1`  
		Last Modified: Tue, 10 Dec 2024 02:24:39 GMT  
		Size: 70.9 MB (70856726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:baea19795aecebbe7d2cb3615ff8663a07bc23e095d4395f815fe98333d578b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2046805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972d3250cf95e8b1ecdc4578cdd1dfb25bc24883ba85a38ceee892103ad120f0`

```dockerfile
```

-	Layers:
	-	`sha256:b255736eb6f856c4678abc49117e5be813d776e08d6c47dcf7332df9ee3a95f4`  
		Last Modified: Tue, 10 Dec 2024 02:24:38 GMT  
		Size: 2.0 MB (2033624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:356e6b5c8ada2f0ffe6d80f85ef100d33fb02c0703550c52ee09e406686f53f7`  
		Last Modified: Tue, 10 Dec 2024 02:24:38 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json
