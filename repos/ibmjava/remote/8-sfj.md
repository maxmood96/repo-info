## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:e9b85602c603b5670da49b84febb1c000df34713f4f59f126a7a324fc9a27825
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
$ docker pull ibmjava@sha256:f620ed24152209545c0b4f7b928bbd180111e2ea2e0316f54b1680ccaedec686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100877325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee010bdb37e507abdbbb888c888409df3af703c6de6c00489eda582e759152dc`
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
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90da020be5ddc6d70004d7bdcdfa83342a0fbfd3dfe6385dfe30771208d6d440`  
		Last Modified: Tue, 02 Jul 2024 03:03:35 GMT  
		Size: 1.4 MB (1438214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136dc9b12ccf44e211aa030068fff33eabb9e5e3340e62b68a1b6e1799393183`  
		Last Modified: Tue, 02 Jul 2024 03:03:37 GMT  
		Size: 69.9 MB (69905056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5de58ec3e9ed758d4a01c99ca36de4e66c5f127a02d830a8e3fe758ad897cf77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2000287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a02c2b1c7897c43eb2ec748bc0a2c8f502b01ec2b50dbd527b211e2fa9e6da`

```dockerfile
```

-	Layers:
	-	`sha256:ff0c07c46f1983a15846f61554dae1be46c23ead93c50161951ef83633c20d2c`  
		Last Modified: Tue, 02 Jul 2024 03:03:35 GMT  
		Size: 2.0 MB (1987361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:522a1f66a12eafdb653a9d106a076a5a5878a682deb21f9c940633a069351fc0`  
		Last Modified: Tue, 02 Jul 2024 03:03:34 GMT  
		Size: 12.9 KB (12926 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0d5d045b08de460a78c01bb22b4f084a79ee3fea0924fcd801a9f33c9413dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106387181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cef76435f0193c29a6092b42be63d1bed9fbbcec1e250c8c09e7c0fff3bd77`
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
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73fe39aa7190a4c3d9ca1d0ac575d106d4b883ca1d2e6fbd1bc4a27f3ead93`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 1.5 MB (1523343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbb798acd38de044e7bf8727b9dd61ad1609899a1e4ff4f2fc36c622fc33c4c`  
		Last Modified: Tue, 02 Jul 2024 10:42:14 GMT  
		Size: 70.4 MB (70402757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e4d9eac5d867c9dc4ab9d567c5ac2fa499f643fae2edfed8bf1f53a6e5695aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57b051515a2096f30d8c2780d52a7aa6b99924055461f9ceb0efaabc9ad8ee`

```dockerfile
```

-	Layers:
	-	`sha256:fc0b9584677f3eeb7e0bba688741f80044d76bcc05402b8298a327703c7e2268`  
		Last Modified: Tue, 02 Jul 2024 10:42:11 GMT  
		Size: 2.0 MB (1990745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7541558a22bbdd501160fe1e7cb10e323ad4dd37101ec0496984def61820e52f`  
		Last Modified: Tue, 02 Jul 2024 10:42:11 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:8499aa8d9aed6b946bc5138a96711cd2326890021172f5746e22505e60914789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99820889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac1bcf5dbe41d2e5d8ae68d712a92b0b85d9e8da733eddb0f93712969b07c03`
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
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ad7703edfb983f72e74e56d3ba233db0435a1290037a46c332cd69db5ad6f`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 1.4 MB (1441883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9022f0a929ddd0a81b214e1c27060e843e8f0f9acb691a3f97ba122b4df379be`  
		Last Modified: Tue, 02 Jul 2024 06:08:49 GMT  
		Size: 70.4 MB (70378466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f36a1017ab214c18be12b02d4c780a76e8794f5acb4b01a3798281e66eec8949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a0c93ecee68fb0da07588800d1cd1c4988d57d7d6652056bd03949667f5627`

```dockerfile
```

-	Layers:
	-	`sha256:ea54d3fdbd7f662221925892f30a92bf51dcd09524165561aab9c03a158e8c96`  
		Last Modified: Tue, 02 Jul 2024 06:08:48 GMT  
		Size: 2.0 MB (1988750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3015dfe8e5a282456ae431d795712034a9ca0a69fde429d36012fd5a795ab46`  
		Last Modified: Tue, 02 Jul 2024 06:08:48 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json
