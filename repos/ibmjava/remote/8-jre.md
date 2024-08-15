## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:ec842e2d4a462a6b04c532707922fd0e92eda177e9e7c6c403548a827cd3d76e
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
$ docker pull ibmjava@sha256:47aef27ded00e51d920214d8c97b01a721bae38afe7d54c953e31ce86ba48d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165986505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f8971b184e37dc2f8c727ae181548d62d5c8169c5faace1522b2b9a1eae75e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd6fa24a44fc4a4fd638c41d9bb59a4196e3ed8bca615056b650ab81c476287`  
		Last Modified: Thu, 15 Aug 2024 17:59:08 GMT  
		Size: 1.4 MB (1438222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e067ca01d4cf5cc41126648c6d14bb007961802de3ec8c184c195d7c837b04a1`  
		Last Modified: Thu, 15 Aug 2024 17:59:10 GMT  
		Size: 135.0 MB (135014228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e24fc1ca87dff0d2e6e65de13cc1e4cb885295d2b9818c10ff0b0175bf5b1da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2043995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd6d2770468d6fc93bd744f692effab3065371c7b3558ed6ea68ec0d13fa645`

```dockerfile
```

-	Layers:
	-	`sha256:1b4022328dc0bac6dd4a4b268ee09ea2861ae2d9d03e312d43adf7eeee6d1e47`  
		Last Modified: Thu, 15 Aug 2024 17:59:08 GMT  
		Size: 2.0 MB (2030477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f7f0a7a7b00c3a4510598facbee903b431a65eeec18e1a75fd444c40b464189`  
		Last Modified: Thu, 15 Aug 2024 17:59:08 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:3d4aa03ed7038b28034da5353b0a3b3c777dcef0aabc8422311559599292dec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171454909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee68ab128cd6c18afaab61200629ad5a60a55d1a9ad9cfff59103a24e000358`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
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
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b823c911ee157eda0ab24a76ac49580a066062d8c3dbbe00bf159415ecbf49b6`  
		Last Modified: Thu, 15 Aug 2024 18:18:41 GMT  
		Size: 1.5 MB (1523275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb773c68b75c4a8719fbee948996532dc99714792b4c99f1fe5794da98e12a5`  
		Last Modified: Thu, 15 Aug 2024 18:18:45 GMT  
		Size: 135.5 MB (135470553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0072ad01cae9d113e6717429568ada7a30e997e1a6abb9e8f043bd0c649abfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2046184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fa2279094a00503c97ac49ccc7310073fd6bae406077b46307ceaf16470bba`

```dockerfile
```

-	Layers:
	-	`sha256:dd0bc2677bd041c7ef5a1e53bfe27d34511dfd95042753fdf7229d1b29213f65`  
		Last Modified: Thu, 15 Aug 2024 18:18:42 GMT  
		Size: 2.0 MB (2032626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4577fcfb91be1b9b0f9b164439b0c10df0afd6099550fdc0c461947f59e344f`  
		Last Modified: Thu, 15 Aug 2024 18:18:41 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:6c83ccf89e0d2d34a190e72f73107ab5adc7a2d6fc0669fac19dc0af79e5de21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161379426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20be709cfb263f96b5b4a1ef31eaa79a73004bca4cb9dc48e7ac7eb1c49d9744`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
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
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410f7d43033771545436ae5d16392e1bd692fce0abf07f6d40a2b30d83168ea5`  
		Last Modified: Thu, 15 Aug 2024 18:11:47 GMT  
		Size: 1.4 MB (1441950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9e0849b56a489a55b422efe4481b2d709d621547f54982cf84102af1470e38`  
		Last Modified: Thu, 15 Aug 2024 18:11:50 GMT  
		Size: 131.9 MB (131936936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8862b59eed277f973ba708f34a0e888a3437e49f66d1fd6eecc9cd24b31ea981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2043033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a2dc7b3d3661703e86130a4ce0a1e1fb8dbf993ef3e815a7258cc88621d07b`

```dockerfile
```

-	Layers:
	-	`sha256:2424f88e3fc6c5c9046534af7f07bf9c7dd96fe18ebb56e0672e6ad02c4fa8ac`  
		Last Modified: Thu, 15 Aug 2024 18:11:47 GMT  
		Size: 2.0 MB (2029515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b157ea658638a7928f36957ea00a7e343be52549274762f6c081e653d72cbba`  
		Last Modified: Thu, 15 Aug 2024 18:11:47 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json
