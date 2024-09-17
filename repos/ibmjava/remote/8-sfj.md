## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:93aea8e18a402d139c044e0b42adfb3d1d4a4f14e1f1947998e2a73d4ce6e6ef
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
$ docker pull ibmjava@sha256:d02e87021e7d1c4bf9d28c39c5d349d9f28a598dd4a322da90bd0dc2986af4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100799326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2d02d7bfb3deb382b4767f226de05ecb9218c96248a5b3104b7dd6f22661c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188f260248587e97ad7aba1c8b62ac0f7ae04a410a8445ef1f6825d263eec7fb`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 1.4 MB (1438210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69ef95f6b840589f2c4d48b50149f7b29fa7959e44f4114c9a24ac1dbba7062`  
		Last Modified: Tue, 17 Sep 2024 00:58:59 GMT  
		Size: 69.8 MB (69825428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0e18653b122f3dfde18b1907c8709dc2a7845932aa550b46b8dca2d66d378696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2025563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee0ebbc80057314270961c40ed730ad1e97f693e1cad9e4ac62912ae358cfbc`

```dockerfile
```

-	Layers:
	-	`sha256:2bdfbdaa8ea50bd44efac9b4892ae3974a8150888a12a15a36337d6d1c52e8b9`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 2.0 MB (2012636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e24ba7cae41a6b29eb53210569edac163b3e8b37bc923b25b103fdb898c30c06`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:fd378abc239a7eaf0a54f396a41840acc925be6bc49d65a72aad7a0673b89de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106303863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f25d214329cea1f12082a1599097205ad25c6f714c287a44f4cb2e74f3f8fde`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e3ace98c6423017a0b0be23c57aadb0c7ef36d09ce2272001e0c362d95a894`  
		Last Modified: Tue, 17 Sep 2024 01:33:07 GMT  
		Size: 70.3 MB (70332376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:7f577506064dcb2cd5d6f2ece9467f69eb6a07766f1b3691b920ccb54a083a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2028832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861d6a7fcb8a51593e7b98e41183e4fd917ddaeb2eef90dcf2ff7bf3dc94b202`

```dockerfile
```

-	Layers:
	-	`sha256:cf2a9232f83bb48634b171b50ea33e1405ba3970bf1a56fdff60677a539eef9e`  
		Last Modified: Tue, 17 Sep 2024 01:33:04 GMT  
		Size: 2.0 MB (2015877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21c4e38bcf47aa98045e5bffa6a6e21d67ba56687494a5d0a86426266cf0e40`  
		Last Modified: Tue, 17 Sep 2024 01:33:04 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:404678effb10a31323c00ce5f62b6e9cf2c7325153cb1972a92e9540401aa690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99911524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1a95fc46964b519611a0ed1e4e645ba8e2bc60ce522a984d70dc7bc468c36d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
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
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2a9d317c2d10b091ecafc0fd6f83a60144f02ea3ade3815ab7ba8a30f34526`  
		Last Modified: Tue, 17 Sep 2024 02:13:32 GMT  
		Size: 70.5 MB (70468135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:131ac1fbbe9debc83a29dd99728fc5c42d22bbd49bf4116ae958a7c4cb5a69c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42168d4f95a050a5be69aa295e0e5bacc807fc5499c6f40a985a77e9d50dff6`

```dockerfile
```

-	Layers:
	-	`sha256:faec85a4e42837ba74045e58c6ed7996208531b5d607a687ce178d3f2fdda0ce`  
		Last Modified: Tue, 17 Sep 2024 02:13:31 GMT  
		Size: 2.0 MB (2014992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b90685c42d1f643654d5bd5c7f283270b064a383c8e62a28366cfdd86d8a0387`  
		Last Modified: Tue, 17 Sep 2024 02:13:31 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json
