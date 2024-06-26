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
$ docker pull ibmjava@sha256:51cfc2773f7d4d33124d61971a27d054e32e0591ad1aca41fd7a7b68d86e5713
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
$ docker pull ibmjava@sha256:72e681dd5aceafde97793f8c94aaf6e8c8f9ebbb8525083ea1c4c997beba663d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166009004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e35c160d442c56de5dab6668e1367ccef1e31269bd760787bba3c3062144b6`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfb9852b79dffd5d428110be3cb4bf7d4ae580d42cd7a2c00ec3163f5832667`  
		Last Modified: Tue, 25 Jun 2024 22:57:22 GMT  
		Size: 1.5 MB (1469310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dc5494e972e03d226df580d37885081680fb879c71d3a270c277c04d388168`  
		Last Modified: Tue, 25 Jun 2024 22:57:24 GMT  
		Size: 135.0 MB (135005940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:b04195bbdf3ec909799efb4f744158f912a37582fa3b7d965b273ff7e5d4038a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2014969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fd4022b1e86a9d46c81834b25cfc9728dfc9506d8673f01dfa2fa50164689f`

```dockerfile
```

-	Layers:
	-	`sha256:73f9c081625ee219788926176edf6a0bb932dd5fc414b41fe3740a2ccf272e90`  
		Last Modified: Tue, 25 Jun 2024 22:57:22 GMT  
		Size: 2.0 MB (2001451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a529962aa38374ed3190412a7f213f92b2c35d3b7dcc9e09ccd7751b995d10f`  
		Last Modified: Tue, 25 Jun 2024 22:57:23 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5cc77deec8a2a0ceef95078adae45548b7c667d1576cde1740b56477fdd0ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171511306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b87681eef4eb45f93bec661f72179920e0d72d24eab384ba7973f1af965d6f`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:bf8e9d1f2ecee34b45176bbe52a7d5ddb1addb4d7aad74aac2e430a39375078c`  
		Last Modified: Tue, 25 Jun 2024 23:50:35 GMT  
		Size: 135.5 MB (135476200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e29284b022d1303f72a6595de0d0529c6655da8676c50381d011d5aa9d9539be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2017444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4119e7219f13b5f9eeb5a6be0675c20ff3c0d66c4560ffda1db448eb6bb02e22`

```dockerfile
```

-	Layers:
	-	`sha256:d9c490db614852b58d942a0abd272d43a2fd0bf5863b51c1fd89a0837c98b311`  
		Last Modified: Tue, 25 Jun 2024 23:50:31 GMT  
		Size: 2.0 MB (2003886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79dc504b2ccfcccd2c78ec31fb01834dc645cc9625dbfc588150ef85eaa9205b`  
		Last Modified: Tue, 25 Jun 2024 23:50:31 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:2b4e008cf6948d1a11f78845291030d069db9595668ed9ce4d929028e6a7de95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161236050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7fda134be65e43c6665e70f7cb06fc15155cc23bed8e8ccf90e79463a825bd`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:e6bdd291cdc1c7ce3a43a7023e6e95c2b9eea5140b0abb7cbdd8e9a372771f58`  
		Last Modified: Tue, 25 Jun 2024 23:30:02 GMT  
		Size: 131.8 MB (131758206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a2c028c02feb964d160ec23383569141507c4a18628e50d025f64eec72d8bedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2013469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43597d2d47638a1339c19234a5902383520d85d1b0839b4d794ddcc19498b584`

```dockerfile
```

-	Layers:
	-	`sha256:1edc175a182eaad1aaf8f3246e899bdf831ad84d7847861a9c577c77ea4bfa0c`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 2.0 MB (1999951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84fa3d3baf9db902d25cd9cc267e2874741219683e814cc4e498de15b453e48c`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:51cfc2773f7d4d33124d61971a27d054e32e0591ad1aca41fd7a7b68d86e5713
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
$ docker pull ibmjava@sha256:72e681dd5aceafde97793f8c94aaf6e8c8f9ebbb8525083ea1c4c997beba663d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166009004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e35c160d442c56de5dab6668e1367ccef1e31269bd760787bba3c3062144b6`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfb9852b79dffd5d428110be3cb4bf7d4ae580d42cd7a2c00ec3163f5832667`  
		Last Modified: Tue, 25 Jun 2024 22:57:22 GMT  
		Size: 1.5 MB (1469310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dc5494e972e03d226df580d37885081680fb879c71d3a270c277c04d388168`  
		Last Modified: Tue, 25 Jun 2024 22:57:24 GMT  
		Size: 135.0 MB (135005940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:b04195bbdf3ec909799efb4f744158f912a37582fa3b7d965b273ff7e5d4038a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2014969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fd4022b1e86a9d46c81834b25cfc9728dfc9506d8673f01dfa2fa50164689f`

```dockerfile
```

-	Layers:
	-	`sha256:73f9c081625ee219788926176edf6a0bb932dd5fc414b41fe3740a2ccf272e90`  
		Last Modified: Tue, 25 Jun 2024 22:57:22 GMT  
		Size: 2.0 MB (2001451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a529962aa38374ed3190412a7f213f92b2c35d3b7dcc9e09ccd7751b995d10f`  
		Last Modified: Tue, 25 Jun 2024 22:57:23 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5cc77deec8a2a0ceef95078adae45548b7c667d1576cde1740b56477fdd0ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171511306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b87681eef4eb45f93bec661f72179920e0d72d24eab384ba7973f1af965d6f`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:bf8e9d1f2ecee34b45176bbe52a7d5ddb1addb4d7aad74aac2e430a39375078c`  
		Last Modified: Tue, 25 Jun 2024 23:50:35 GMT  
		Size: 135.5 MB (135476200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e29284b022d1303f72a6595de0d0529c6655da8676c50381d011d5aa9d9539be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2017444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4119e7219f13b5f9eeb5a6be0675c20ff3c0d66c4560ffda1db448eb6bb02e22`

```dockerfile
```

-	Layers:
	-	`sha256:d9c490db614852b58d942a0abd272d43a2fd0bf5863b51c1fd89a0837c98b311`  
		Last Modified: Tue, 25 Jun 2024 23:50:31 GMT  
		Size: 2.0 MB (2003886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79dc504b2ccfcccd2c78ec31fb01834dc645cc9625dbfc588150ef85eaa9205b`  
		Last Modified: Tue, 25 Jun 2024 23:50:31 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:2b4e008cf6948d1a11f78845291030d069db9595668ed9ce4d929028e6a7de95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161236050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7fda134be65e43c6665e70f7cb06fc15155cc23bed8e8ccf90e79463a825bd`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:e6bdd291cdc1c7ce3a43a7023e6e95c2b9eea5140b0abb7cbdd8e9a372771f58`  
		Last Modified: Tue, 25 Jun 2024 23:30:02 GMT  
		Size: 131.8 MB (131758206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a2c028c02feb964d160ec23383569141507c4a18628e50d025f64eec72d8bedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2013469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43597d2d47638a1339c19234a5902383520d85d1b0839b4d794ddcc19498b584`

```dockerfile
```

-	Layers:
	-	`sha256:1edc175a182eaad1aaf8f3246e899bdf831ad84d7847861a9c577c77ea4bfa0c`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 2.0 MB (1999951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84fa3d3baf9db902d25cd9cc267e2874741219683e814cc4e498de15b453e48c`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:e0c323fcf360f3998c9831a95b52c1e048048df044f1d71693056a7ee813694a
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
$ docker pull ibmjava@sha256:a8a959c23ce5b8d77936b2fce1e2f33b5d2cc4fe7daceee8fa48b8d0ff5df119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203215307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d319563b74ff06322e7f51b39fcd2eac8dcee444208e659c4a3843c9b07349fc`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6d7ddb94d08079895f4fabec6cc12c9acbb1f398d547dbfaa306cc2faf837`  
		Last Modified: Tue, 25 Jun 2024 22:57:25 GMT  
		Size: 1.5 MB (1469335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf32957134ad52256fcac2824cb56f06163e9eba54a44c9312ca67458220d8`  
		Last Modified: Tue, 25 Jun 2024 22:57:27 GMT  
		Size: 172.2 MB (172212218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:23efab1834ca487397c307c29b362a4f30d0180eede4008547bf87989c784d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2066960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bbc849255da33b9c004439fac42bac1bb33d21ddad38776d887c1c06d17862`

```dockerfile
```

-	Layers:
	-	`sha256:61cecfadceb961c7e0d0b8113edef133f87bcdaf07ae21ac297b3924be448d03`  
		Last Modified: Tue, 25 Jun 2024 22:57:26 GMT  
		Size: 2.1 MB (2054038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e38435ffa3e703e89e2e849304d40a327d331de9e55d2d183b60468c2a45bc5`  
		Last Modified: Tue, 25 Jun 2024 22:57:26 GMT  
		Size: 12.9 KB (12922 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:8db440d82d2cfa50057e7c69fb1171cf6e7bec41686085d017ff9c95578665e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208841101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19267522d340f26c418f6837ec8d94eaf2d64b11f6a66812098fe793aa09ecba`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:ad2f2b2bb92517562cc54a7709a1649468050868172a075982c9539f0882cc5e`  
		Last Modified: Tue, 25 Jun 2024 23:52:29 GMT  
		Size: 172.8 MB (172805995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:88bccdc63f96a800fb81cadad4c205581b69425c9d14911f48f1a281021f4267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21db540e988ddb268ee3eab84cd5b499767dc45b2d54ebda0a0602bc45094bb2`

```dockerfile
```

-	Layers:
	-	`sha256:157e24d73638ac7bd92608084c85eecc4ba1f920c48109ea26415eb9acff3025`  
		Last Modified: Tue, 25 Jun 2024 23:52:24 GMT  
		Size: 2.1 MB (2056461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46f5777f5d04514482930a0f6ff24ed60d5648cef4e961496395b7f726c4f2eb`  
		Last Modified: Tue, 25 Jun 2024 23:52:24 GMT  
		Size: 13.0 KB (12952 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:0645e8b60e71f613d08e293195d77b2bbe76f8c7d898286d2042a21ed9a2e35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191519123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c32a6c27e28c805dddca01ae89778b1ff723eb1bfc6f84e0f64261d6676a5fb`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:4682166c6f2936c53cc51970d9c062706c3618580e5db67faa6dee70be84f899`  
		Last Modified: Tue, 25 Jun 2024 23:31:34 GMT  
		Size: 162.0 MB (162041279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:fd21008e1b9acd37b396b7569b897c27444f047b969607bb170552073b10b8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2040688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a46215bb2dd86a04bdda1cd109c0e81c68420cccdf35081202584df4cb62e`

```dockerfile
```

-	Layers:
	-	`sha256:30bee264f47343be57ca6b825938db56bf71524dbfd16920e8e6cefa7b87e527`  
		Last Modified: Tue, 25 Jun 2024 23:31:32 GMT  
		Size: 2.0 MB (2027764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:176e686f83fe08e660bb840f75571a8ad02d240b6a60194e367b8465cf90bc3a`  
		Last Modified: Tue, 25 Jun 2024 23:31:32 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

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

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:51cfc2773f7d4d33124d61971a27d054e32e0591ad1aca41fd7a7b68d86e5713
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
$ docker pull ibmjava@sha256:72e681dd5aceafde97793f8c94aaf6e8c8f9ebbb8525083ea1c4c997beba663d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166009004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e35c160d442c56de5dab6668e1367ccef1e31269bd760787bba3c3062144b6`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfb9852b79dffd5d428110be3cb4bf7d4ae580d42cd7a2c00ec3163f5832667`  
		Last Modified: Tue, 25 Jun 2024 22:57:22 GMT  
		Size: 1.5 MB (1469310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dc5494e972e03d226df580d37885081680fb879c71d3a270c277c04d388168`  
		Last Modified: Tue, 25 Jun 2024 22:57:24 GMT  
		Size: 135.0 MB (135005940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:b04195bbdf3ec909799efb4f744158f912a37582fa3b7d965b273ff7e5d4038a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2014969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fd4022b1e86a9d46c81834b25cfc9728dfc9506d8673f01dfa2fa50164689f`

```dockerfile
```

-	Layers:
	-	`sha256:73f9c081625ee219788926176edf6a0bb932dd5fc414b41fe3740a2ccf272e90`  
		Last Modified: Tue, 25 Jun 2024 22:57:22 GMT  
		Size: 2.0 MB (2001451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a529962aa38374ed3190412a7f213f92b2c35d3b7dcc9e09ccd7751b995d10f`  
		Last Modified: Tue, 25 Jun 2024 22:57:23 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5cc77deec8a2a0ceef95078adae45548b7c667d1576cde1740b56477fdd0ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171511306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b87681eef4eb45f93bec661f72179920e0d72d24eab384ba7973f1af965d6f`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:bf8e9d1f2ecee34b45176bbe52a7d5ddb1addb4d7aad74aac2e430a39375078c`  
		Last Modified: Tue, 25 Jun 2024 23:50:35 GMT  
		Size: 135.5 MB (135476200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e29284b022d1303f72a6595de0d0529c6655da8676c50381d011d5aa9d9539be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2017444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4119e7219f13b5f9eeb5a6be0675c20ff3c0d66c4560ffda1db448eb6bb02e22`

```dockerfile
```

-	Layers:
	-	`sha256:d9c490db614852b58d942a0abd272d43a2fd0bf5863b51c1fd89a0837c98b311`  
		Last Modified: Tue, 25 Jun 2024 23:50:31 GMT  
		Size: 2.0 MB (2003886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79dc504b2ccfcccd2c78ec31fb01834dc645cc9625dbfc588150ef85eaa9205b`  
		Last Modified: Tue, 25 Jun 2024 23:50:31 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:2b4e008cf6948d1a11f78845291030d069db9595668ed9ce4d929028e6a7de95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161236050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7fda134be65e43c6665e70f7cb06fc15155cc23bed8e8ccf90e79463a825bd`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:e6bdd291cdc1c7ce3a43a7023e6e95c2b9eea5140b0abb7cbdd8e9a372771f58`  
		Last Modified: Tue, 25 Jun 2024 23:30:02 GMT  
		Size: 131.8 MB (131758206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a2c028c02feb964d160ec23383569141507c4a18628e50d025f64eec72d8bedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2013469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43597d2d47638a1339c19234a5902383520d85d1b0839b4d794ddcc19498b584`

```dockerfile
```

-	Layers:
	-	`sha256:1edc175a182eaad1aaf8f3246e899bdf831ad84d7847861a9c577c77ea4bfa0c`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 2.0 MB (1999951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84fa3d3baf9db902d25cd9cc267e2874741219683e814cc4e498de15b453e48c`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:51cfc2773f7d4d33124d61971a27d054e32e0591ad1aca41fd7a7b68d86e5713
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
$ docker pull ibmjava@sha256:72e681dd5aceafde97793f8c94aaf6e8c8f9ebbb8525083ea1c4c997beba663d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166009004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e35c160d442c56de5dab6668e1367ccef1e31269bd760787bba3c3062144b6`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfb9852b79dffd5d428110be3cb4bf7d4ae580d42cd7a2c00ec3163f5832667`  
		Last Modified: Tue, 25 Jun 2024 22:57:22 GMT  
		Size: 1.5 MB (1469310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dc5494e972e03d226df580d37885081680fb879c71d3a270c277c04d388168`  
		Last Modified: Tue, 25 Jun 2024 22:57:24 GMT  
		Size: 135.0 MB (135005940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:b04195bbdf3ec909799efb4f744158f912a37582fa3b7d965b273ff7e5d4038a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2014969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fd4022b1e86a9d46c81834b25cfc9728dfc9506d8673f01dfa2fa50164689f`

```dockerfile
```

-	Layers:
	-	`sha256:73f9c081625ee219788926176edf6a0bb932dd5fc414b41fe3740a2ccf272e90`  
		Last Modified: Tue, 25 Jun 2024 22:57:22 GMT  
		Size: 2.0 MB (2001451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a529962aa38374ed3190412a7f213f92b2c35d3b7dcc9e09ccd7751b995d10f`  
		Last Modified: Tue, 25 Jun 2024 22:57:23 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5cc77deec8a2a0ceef95078adae45548b7c667d1576cde1740b56477fdd0ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171511306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b87681eef4eb45f93bec661f72179920e0d72d24eab384ba7973f1af965d6f`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:bf8e9d1f2ecee34b45176bbe52a7d5ddb1addb4d7aad74aac2e430a39375078c`  
		Last Modified: Tue, 25 Jun 2024 23:50:35 GMT  
		Size: 135.5 MB (135476200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e29284b022d1303f72a6595de0d0529c6655da8676c50381d011d5aa9d9539be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2017444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4119e7219f13b5f9eeb5a6be0675c20ff3c0d66c4560ffda1db448eb6bb02e22`

```dockerfile
```

-	Layers:
	-	`sha256:d9c490db614852b58d942a0abd272d43a2fd0bf5863b51c1fd89a0837c98b311`  
		Last Modified: Tue, 25 Jun 2024 23:50:31 GMT  
		Size: 2.0 MB (2003886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79dc504b2ccfcccd2c78ec31fb01834dc645cc9625dbfc588150ef85eaa9205b`  
		Last Modified: Tue, 25 Jun 2024 23:50:31 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:2b4e008cf6948d1a11f78845291030d069db9595668ed9ce4d929028e6a7de95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161236050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7fda134be65e43c6665e70f7cb06fc15155cc23bed8e8ccf90e79463a825bd`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:e6bdd291cdc1c7ce3a43a7023e6e95c2b9eea5140b0abb7cbdd8e9a372771f58`  
		Last Modified: Tue, 25 Jun 2024 23:30:02 GMT  
		Size: 131.8 MB (131758206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a2c028c02feb964d160ec23383569141507c4a18628e50d025f64eec72d8bedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2013469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43597d2d47638a1339c19234a5902383520d85d1b0839b4d794ddcc19498b584`

```dockerfile
```

-	Layers:
	-	`sha256:1edc175a182eaad1aaf8f3246e899bdf831ad84d7847861a9c577c77ea4bfa0c`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 2.0 MB (1999951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84fa3d3baf9db902d25cd9cc267e2874741219683e814cc4e498de15b453e48c`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:e0c323fcf360f3998c9831a95b52c1e048048df044f1d71693056a7ee813694a
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
$ docker pull ibmjava@sha256:a8a959c23ce5b8d77936b2fce1e2f33b5d2cc4fe7daceee8fa48b8d0ff5df119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203215307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d319563b74ff06322e7f51b39fcd2eac8dcee444208e659c4a3843c9b07349fc`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6d7ddb94d08079895f4fabec6cc12c9acbb1f398d547dbfaa306cc2faf837`  
		Last Modified: Tue, 25 Jun 2024 22:57:25 GMT  
		Size: 1.5 MB (1469335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf32957134ad52256fcac2824cb56f06163e9eba54a44c9312ca67458220d8`  
		Last Modified: Tue, 25 Jun 2024 22:57:27 GMT  
		Size: 172.2 MB (172212218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:23efab1834ca487397c307c29b362a4f30d0180eede4008547bf87989c784d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2066960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bbc849255da33b9c004439fac42bac1bb33d21ddad38776d887c1c06d17862`

```dockerfile
```

-	Layers:
	-	`sha256:61cecfadceb961c7e0d0b8113edef133f87bcdaf07ae21ac297b3924be448d03`  
		Last Modified: Tue, 25 Jun 2024 22:57:26 GMT  
		Size: 2.1 MB (2054038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e38435ffa3e703e89e2e849304d40a327d331de9e55d2d183b60468c2a45bc5`  
		Last Modified: Tue, 25 Jun 2024 22:57:26 GMT  
		Size: 12.9 KB (12922 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:8db440d82d2cfa50057e7c69fb1171cf6e7bec41686085d017ff9c95578665e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208841101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19267522d340f26c418f6837ec8d94eaf2d64b11f6a66812098fe793aa09ecba`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:ad2f2b2bb92517562cc54a7709a1649468050868172a075982c9539f0882cc5e`  
		Last Modified: Tue, 25 Jun 2024 23:52:29 GMT  
		Size: 172.8 MB (172805995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:88bccdc63f96a800fb81cadad4c205581b69425c9d14911f48f1a281021f4267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21db540e988ddb268ee3eab84cd5b499767dc45b2d54ebda0a0602bc45094bb2`

```dockerfile
```

-	Layers:
	-	`sha256:157e24d73638ac7bd92608084c85eecc4ba1f920c48109ea26415eb9acff3025`  
		Last Modified: Tue, 25 Jun 2024 23:52:24 GMT  
		Size: 2.1 MB (2056461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46f5777f5d04514482930a0f6ff24ed60d5648cef4e961496395b7f726c4f2eb`  
		Last Modified: Tue, 25 Jun 2024 23:52:24 GMT  
		Size: 13.0 KB (12952 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:0645e8b60e71f613d08e293195d77b2bbe76f8c7d898286d2042a21ed9a2e35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191519123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c32a6c27e28c805dddca01ae89778b1ff723eb1bfc6f84e0f64261d6676a5fb`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:4682166c6f2936c53cc51970d9c062706c3618580e5db67faa6dee70be84f899`  
		Last Modified: Tue, 25 Jun 2024 23:31:34 GMT  
		Size: 162.0 MB (162041279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:fd21008e1b9acd37b396b7569b897c27444f047b969607bb170552073b10b8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2040688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a46215bb2dd86a04bdda1cd109c0e81c68420cccdf35081202584df4cb62e`

```dockerfile
```

-	Layers:
	-	`sha256:30bee264f47343be57ca6b825938db56bf71524dbfd16920e8e6cefa7b87e527`  
		Last Modified: Tue, 25 Jun 2024 23:31:32 GMT  
		Size: 2.0 MB (2027764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:176e686f83fe08e660bb840f75571a8ad02d240b6a60194e367b8465cf90bc3a`  
		Last Modified: Tue, 25 Jun 2024 23:31:32 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

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

### `ibmjava:sfj` - linux; amd64

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

### `ibmjava:sfj` - unknown; unknown

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

### `ibmjava:sfj` - linux; ppc64le

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

### `ibmjava:sfj` - unknown; unknown

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

### `ibmjava:sfj` - linux; s390x

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

### `ibmjava:sfj` - unknown; unknown

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
