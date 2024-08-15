## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:fec3053ba7efe2029b2a4aa9ae629595455e459e8d2fecf740bf5952cebb8570
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
$ docker pull ibmjava@sha256:1c97b535f98e4dd1f95eb4903ad55ee6cb6f8ed8cc113adbeaf421b287b78aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203104882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f786e62d3a19362a4f564f6e121e5f6659853824dcf88563ee45196b0a1aa6`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8c18821fbc0471fedb2e8d7e260b39328bb46dca7050fb2f35e9978027721`  
		Last Modified: Thu, 15 Aug 2024 17:59:10 GMT  
		Size: 1.4 MB (1438186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f2f0b645d46a7ddb8e36fe968de9432ed457a1e721bd3319005b4c247aa897`  
		Last Modified: Thu, 15 Aug 2024 17:59:13 GMT  
		Size: 172.1 MB (172132641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:bc9c775650971d0f5dfeeb348b9acc36d3195896cbbd76506dd32951bea51ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2099459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd292538c5bfd0e919ac72ab92bacc5c46266991c976e0e1035b6258c8e3404`

```dockerfile
```

-	Layers:
	-	`sha256:54428d95b4915121f41e43910b6df8f13d1912566bbc2849cde09a0d06c1393b`  
		Last Modified: Thu, 15 Aug 2024 17:59:10 GMT  
		Size: 2.1 MB (2086535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e332ea5e3d95187f2fcc0f364e69421b62fd1213b192810b16c9c821f4efe875`  
		Last Modified: Thu, 15 Aug 2024 17:59:10 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:d528a87d018f00e6bd6f62db44f91121e3b77b8a33c71b1307cb89bd7f2c1abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208733330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4baeda25e2df0275986917a7821de39ee314f15e0372ea3e624f3c4bbc7f1857`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:5efe3d7f9fb24db3c2b24b72e305f514e257051c48eeaa8c6cec6b6568094e0c`  
		Last Modified: Thu, 15 Aug 2024 18:21:30 GMT  
		Size: 172.7 MB (172748974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4aeda80df4a172c22e2a1232a97d4153ff6c830abef60855e2532dd6871c8258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2101624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dffe94088f2a7af116028258dc9b741cac4560e7a92f33aaab237988f9ea30b`

```dockerfile
```

-	Layers:
	-	`sha256:2201a31e386621b4fafe5197dcf947c20952a84109b33e88125b3021f6cfc1b1`  
		Last Modified: Thu, 15 Aug 2024 18:21:25 GMT  
		Size: 2.1 MB (2088672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:418d439ad631c62c0b04f2bb077a23ea221dc37c1dde7652cc1f6593e18158e3`  
		Last Modified: Thu, 15 Aug 2024 18:21:24 GMT  
		Size: 13.0 KB (12952 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:dbea4b7d439ee7fb1eef66af006d0754b593221cc42bdb0a7229ab6482ae2b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191653846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb4cea3ebc9be2b47447a52296b2908cd673e780e7dae61cdeed2c01a10828`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:33ce16b6bf91c9e4b1366f1c72d845d0c3c81e5fbef3768e31d442000ba629f5`  
		Last Modified: Thu, 15 Aug 2024 18:14:23 GMT  
		Size: 162.2 MB (162211356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:aa7a2aab962c469e2da63b7e8acbe874c2e3545228e7feba4d1c95a59ceb5e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2074256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74bea6f1148a9c96cd3c813226a610e5010fe7de99c21654643bc28aabf5a2f`

```dockerfile
```

-	Layers:
	-	`sha256:1f1b08640d299d3009701a539057c71312074e1024873a09f8746d946f86528a`  
		Last Modified: Thu, 15 Aug 2024 18:14:20 GMT  
		Size: 2.1 MB (2061332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd6ecfbb084bdf0cd9d60e6a2d830b7a2455a110fdedf4343617c970e4e1f5c`  
		Last Modified: Thu, 15 Aug 2024 18:14:20 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json
