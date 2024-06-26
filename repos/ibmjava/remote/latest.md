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
