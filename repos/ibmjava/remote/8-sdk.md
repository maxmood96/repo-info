## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:025fbd71060d205512a5a5bffb53a5a1eb8ff19a757bcf6a0bc3533a3cc8748e
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
$ docker pull ibmjava@sha256:54f79b627664ae0e80eb7ae04384f2fa1357ebcbb6a56eb68da16a94f9c5e18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203106503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125cc8fd6e3a281bafbca09aea97c34ef2299f6ad9251b5f2fbc7cb9fa1d94d4`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c22e75fb9dfc02c2b846fdb7ea830b729536ea6e69c37adbe23e490a2a5b387`  
		Last Modified: Tue, 17 Sep 2024 00:59:30 GMT  
		Size: 1.4 MB (1438138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae95ac88ac0804bc3b7ca3e44688c77636d9eed729564f2ccecbc336cb0f2c0`  
		Last Modified: Tue, 17 Sep 2024 00:59:33 GMT  
		Size: 172.1 MB (172132677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8377ba027f8013d1dac2f8002a7d1903c2dc77ef2b4611771e206135d24557f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2097570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7600ced5ca2c2a9ea9522a334cb6894f7e6e57c711eb67d5dd00d64867bb518`

```dockerfile
```

-	Layers:
	-	`sha256:a3b584aa0fa4d6b4f33b5bde45b947ea752def99596508f4920bfb0d40836600`  
		Last Modified: Tue, 17 Sep 2024 00:59:31 GMT  
		Size: 2.1 MB (2084647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2916dd73c4c459966010fc72bcb4cee16d8f5fd2a344ba52c4f8ad1c9156c6`  
		Last Modified: Tue, 17 Sep 2024 00:59:30 GMT  
		Size: 12.9 KB (12923 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:155be61a85304135f4a5fb0f202646d634cbdee31c08a4ef9c8a7e27ece00edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208720340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13772ce0a1db0497acf4672fee866ae4754d57a6d3377863218e59f2ae1d5ac`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:62636db2ac4815fe48801a3b62ed8d568ad28ca0e2330b3a84e227a61b023a72`  
		Last Modified: Tue, 17 Sep 2024 01:34:57 GMT  
		Size: 172.7 MB (172748853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c2b38ddd2c7793409ae9a705e5ea064ac88a7dacbd2544e261597dec16045faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2099736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd743695dda4a33158a39e94c2b9c3d12ac078513a87cdb0e57538c91c2c49`

```dockerfile
```

-	Layers:
	-	`sha256:bab4ee37005b1b2035b044667cc6e94910a2180f324feb400fcf22d6b9c68aae`  
		Last Modified: Tue, 17 Sep 2024 01:34:52 GMT  
		Size: 2.1 MB (2086784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d518a06071241da6083182ba063a703ceb6093cb1710e14ac3d3668c8af31af`  
		Last Modified: Tue, 17 Sep 2024 01:34:52 GMT  
		Size: 13.0 KB (12952 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:bd645f51b108228ea5eaddd74e4c4083ae4ccf297907e2e5670def952e7f3e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191654678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367306913f020efe1b31489ba569fd2288a37d305e7f96bcde6099ad9e4b6ec2`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:f675c68607c669df079bb79b19cf6109bef13663f5009617064a4ba0e4f20d89`  
		Last Modified: Tue, 17 Sep 2024 02:15:19 GMT  
		Size: 162.2 MB (162211289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0db96ed97fe7aedc9794860187b6abdbebe84cc0f564e5fb692a3bdbf85781ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5055449e053b6aba44ca9879c4f1e4b02692690aa3e362a466e771e2a341cbd`

```dockerfile
```

-	Layers:
	-	`sha256:6488eeca981afe31c0bf835c2826096870f806d4044bbfccd063e914c89219ed`  
		Last Modified: Tue, 17 Sep 2024 02:15:17 GMT  
		Size: 2.1 MB (2059444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa95e8866e05bbc9232fc741a41b7cd64d8cf47ede29bfadf2b5b1d03a552f12`  
		Last Modified: Tue, 17 Sep 2024 02:15:17 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json
