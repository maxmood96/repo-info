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
$ docker pull ibmjava@sha256:f37d1d1f91eec98e1114eb107a9a6c4a476fd043d3fa610638e6d1c7e3388e95
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
$ docker pull ibmjava@sha256:c14c0c8624f9adeb98403d4f7e0f29b9f9fcb7d749a017f30509a95bcc38e549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166767887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b767b04ad6e539d5eebf9214bd586f04efe73406e1a68129b33ee8c35cf690`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0d473605c46f9db355df7236218d24a2ef5b47874d4f24c615233869c1c3402a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2085991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8331766c1fdb10942e1d910875375c150f121b74857b3c20756186debc594029`

```dockerfile
```

-	Layers:
	-	`sha256:ea6fecaaeaf2d545dac3687c0cc7d201ebcbde2158f47af8e1206e20589107f2`  
		Last Modified: Tue, 03 Jun 2025 16:10:44 GMT  
		Size: 2.1 MB (2072219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e543936ae15ce4ff2d91919fd56109bc15876e24d318dd6207119383d0ec108`  
		Last Modified: Tue, 03 Jun 2025 16:10:44 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0dfc49e54b96cab01b2d9f0faa2ac9cb8bdd23a307f8cd404b5361d8803d4bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172607671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa126710509d5aad12f8d37bf40215d1e00cc81ff6e7d8b88ebf45461da61da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f581f4e6d076b9a3a2abd7d2780b110e85ed22e65b4361103dcee628dbec2ac6`  
		Last Modified: Wed, 02 Jul 2025 03:54:24 GMT  
		Size: 136.6 MB (136628814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0490dd8aaa1965e6afcc222939705f3e1ced67fc582f169ed11c978716f95ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2dfc34f191c32be6112f2902d9b2aad5a4b67319cb0efebf9ed18a1dacac18`

```dockerfile
```

-	Layers:
	-	`sha256:7f59357e19d60da8dd7a215ac4eef83e815c18200f5322df6251115c864980b7`  
		Last Modified: Wed, 02 Jul 2025 05:01:25 GMT  
		Size: 2.2 MB (2176798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b9ee117cfb64fc03034ecce80400b9922d3c7ac1397bd1dd4b4c9ab95407e1`  
		Last Modified: Wed, 02 Jul 2025 05:01:26 GMT  
		Size: 13.8 KB (13816 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:62c7820523f9938e81649f8b9986ab5fdeb8ce9d4dec6185843c21ad4ad5192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162268182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25163082133c9fa7ad7385757e18830a2946267df8435f55f3341648f74db5da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c8815ff3b76bc5d8ae6bf80bbcf7593d004650d9bc9a7dd2369668cacaa2f75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2085952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af14d337299fdcf1e40c9ba82ffceb90455d97cf954b7e4b124712fdef46d634`

```dockerfile
```

-	Layers:
	-	`sha256:ae0933ed6a39894e27c061aee0a8c345fe400e24824a7325e2ea25e1b67ea4fa`  
		Last Modified: Tue, 03 Jun 2025 16:11:29 GMT  
		Size: 2.1 MB (2072180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd20a67b3b7569a6b50f48d5d786c7c7d318e1ff2a89fa994ba37b940b4c65ae`  
		Last Modified: Tue, 03 Jun 2025 16:11:29 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:f37d1d1f91eec98e1114eb107a9a6c4a476fd043d3fa610638e6d1c7e3388e95
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
$ docker pull ibmjava@sha256:c14c0c8624f9adeb98403d4f7e0f29b9f9fcb7d749a017f30509a95bcc38e549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166767887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b767b04ad6e539d5eebf9214bd586f04efe73406e1a68129b33ee8c35cf690`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0d473605c46f9db355df7236218d24a2ef5b47874d4f24c615233869c1c3402a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2085991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8331766c1fdb10942e1d910875375c150f121b74857b3c20756186debc594029`

```dockerfile
```

-	Layers:
	-	`sha256:ea6fecaaeaf2d545dac3687c0cc7d201ebcbde2158f47af8e1206e20589107f2`  
		Last Modified: Tue, 03 Jun 2025 16:10:44 GMT  
		Size: 2.1 MB (2072219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e543936ae15ce4ff2d91919fd56109bc15876e24d318dd6207119383d0ec108`  
		Last Modified: Tue, 03 Jun 2025 16:10:44 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0dfc49e54b96cab01b2d9f0faa2ac9cb8bdd23a307f8cd404b5361d8803d4bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172607671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa126710509d5aad12f8d37bf40215d1e00cc81ff6e7d8b88ebf45461da61da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f581f4e6d076b9a3a2abd7d2780b110e85ed22e65b4361103dcee628dbec2ac6`  
		Last Modified: Wed, 02 Jul 2025 03:54:24 GMT  
		Size: 136.6 MB (136628814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0490dd8aaa1965e6afcc222939705f3e1ced67fc582f169ed11c978716f95ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2dfc34f191c32be6112f2902d9b2aad5a4b67319cb0efebf9ed18a1dacac18`

```dockerfile
```

-	Layers:
	-	`sha256:7f59357e19d60da8dd7a215ac4eef83e815c18200f5322df6251115c864980b7`  
		Last Modified: Wed, 02 Jul 2025 05:01:25 GMT  
		Size: 2.2 MB (2176798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b9ee117cfb64fc03034ecce80400b9922d3c7ac1397bd1dd4b4c9ab95407e1`  
		Last Modified: Wed, 02 Jul 2025 05:01:26 GMT  
		Size: 13.8 KB (13816 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:62c7820523f9938e81649f8b9986ab5fdeb8ce9d4dec6185843c21ad4ad5192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162268182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25163082133c9fa7ad7385757e18830a2946267df8435f55f3341648f74db5da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c8815ff3b76bc5d8ae6bf80bbcf7593d004650d9bc9a7dd2369668cacaa2f75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2085952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af14d337299fdcf1e40c9ba82ffceb90455d97cf954b7e4b124712fdef46d634`

```dockerfile
```

-	Layers:
	-	`sha256:ae0933ed6a39894e27c061aee0a8c345fe400e24824a7325e2ea25e1b67ea4fa`  
		Last Modified: Tue, 03 Jun 2025 16:11:29 GMT  
		Size: 2.1 MB (2072180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd20a67b3b7569a6b50f48d5d786c7c7d318e1ff2a89fa994ba37b940b4c65ae`  
		Last Modified: Tue, 03 Jun 2025 16:11:29 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:d96ad62260ccd3cff64bf75fcc06f7951d22ece10557f9bf2f5c1ee2a481eb46
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
$ docker pull ibmjava@sha256:e6dc6d758b9e48640eb15800d8cce961ef194c7d5bcf137ca494bc01d63f26ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204168263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bbd844b9770b0c10e0b19adc84bd2f3049fc746f46de543c98198f0701f29e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f678ce4d9a60d6c998236f3e466663b67491d0de867f033ff45f466b1f53d30`  
		Last Modified: Wed, 02 Jul 2025 04:28:31 GMT  
		Size: 1.5 MB (1450007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dbef6e2a79b4a6f488821b533bbd58fc3e82c469e70b2a60b56adcdbb580e6`  
		Last Modified: Wed, 02 Jul 2025 05:05:05 GMT  
		Size: 173.2 MB (173182570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:59c2b50fdae01850d6a93ced94af2e3cac3610cf37f615ad08d156ce0d8e15ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd56d969318b3354dfcd60143885e906e6d50cd5ed5d500b2ae90ecffd5958c`

```dockerfile
```

-	Layers:
	-	`sha256:0f64110ce3adc02b2bec90987e68411cb8d6fff6b69394cab42711c1f547c4b4`  
		Last Modified: Wed, 02 Jul 2025 05:01:28 GMT  
		Size: 3.1 MB (3083828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be2a38af5c85fc51e9f3fe5aab1a30668a6461231a8e0bcd4710a88f31645f1`  
		Last Modified: Wed, 02 Jul 2025 05:01:29 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:e3365e40c4a63ab47e7997d00689a8750cead278ee316dadf0f1a3f7ee38b477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210217391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267afb8e32ffd3ef9ae2bccf716ee830296bbb97029f8e64dd766634e787329e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba99977cd9d6077fd4b307c3357787311ced4b3a091deff606c2244499c52dca`  
		Last Modified: Wed, 02 Jul 2025 05:05:40 GMT  
		Size: 174.2 MB (174238534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8e2cbe645208295d6ce8a67be9f3e35eafc43040b80a6af6c62fb6d25f4fdf7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420f9f75bab2dc52eea96bea822bf74dfdf79c4aeafc5e692c1c907b130ce32d`

```dockerfile
```

-	Layers:
	-	`sha256:2a580b888b091e828d99907782b577e4929fb7af8b70034b3c2f8704a7fccda0`  
		Last Modified: Wed, 02 Jul 2025 05:01:33 GMT  
		Size: 3.1 MB (3069777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:945afa5218986909835c1422d2582bc61260d20f147ee8cd3e743bf8e1842c55`  
		Last Modified: Wed, 02 Jul 2025 05:01:34 GMT  
		Size: 13.2 KB (13212 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:92c479b9321584afd388a500009071de71605089938119defa89d5a82ee4c74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192753473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd384000d924a2236616fec91fd4af7b135931b63869fe3a1b37fd79591ad5f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2d974b5413f042241053a768c76f997e675bc55e8e98836da09fd5211caf69`  
		Last Modified: Wed, 04 Jun 2025 01:56:26 GMT  
		Size: 163.3 MB (163297145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:86bad0987a14f67bfb89db9ee2684dc7c1f50acf6501ae85604317315bff7503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2669033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1348730ceea4c07afd5a1a64d53cbece01a0b205a6108b0fa6b00cb72d5451c`

```dockerfile
```

-	Layers:
	-	`sha256:74df62495bb96ef85a20d09412940687ef4e6fd3074c14dc90b4b4603424503e`  
		Last Modified: Wed, 04 Jun 2025 01:56:47 GMT  
		Size: 2.7 MB (2655855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d83a744ca31a81fdecced1884f246faa6ce3fb50139d3ec01cb389aabf576e`  
		Last Modified: Wed, 04 Jun 2025 01:56:48 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:5fedf567317236256496a5159eb4eef032ed7ad2c2707b5becf8fc0af33f1228
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
$ docker pull ibmjava@sha256:f958e2b42789067a30996418bd8c437523fbf41d5644fed195b1af8ee92acf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101478723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208bfd2b5bcc49248cfd829c7a6fce5275267ad114d1852ad35778ea1fa440c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98acd822b08706485046b4324f633237d583daebe53cebec36a620ccb812eefe`  
		Last Modified: Wed, 04 Jun 2025 01:54:19 GMT  
		Size: 1.5 MB (1450028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225c989849e787ac38a65d9d633ad373c2de4d843dc80de0a6e91e5a32c0d6b0`  
		Last Modified: Wed, 04 Jun 2025 01:54:24 GMT  
		Size: 70.5 MB (70495692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9fda182f6a32a51973d8f6feeea26ba584d03b4db71c0496f3d45053335a1b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2067831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756148d5f8906ca53804b08c33fa0888fee6e723ee16bf5a7916bb0a52acd6f5`

```dockerfile
```

-	Layers:
	-	`sha256:9d0d95f4621604b0c19165d24a9fc4c20748cf223ba73e8cd269b89bd4de48ee`  
		Last Modified: Wed, 04 Jun 2025 01:54:35 GMT  
		Size: 2.1 MB (2054650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc9efd7c6722bfb7265b6b546f9faacf0a6c438fedc711d1bab5d2ba38ec7fb`  
		Last Modified: Wed, 04 Jun 2025 01:54:37 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:f79d9191c2cfd63a96e6104b819c0a7e5fcaa6935ef4ae9e712668f0c03f94d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107307499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c70aece4bce65f968965847dc6fa280d3cfd62a5160edbf632c9d9b15729da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b508e78ad839eb5804b4140d689c487ab1a9a5ee9bf667cf9d4f054b0f8aa3c`  
		Last Modified: Wed, 02 Jul 2025 03:55:31 GMT  
		Size: 71.3 MB (71328642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3d952bf4ba0008d0443b61c87f05520f6967a47d4dadf989491a93cec747473c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9310ab59c178144de5d53c77bfe20c325f5f00e0f4293e4b036a8aa4558b4`

```dockerfile
```

-	Layers:
	-	`sha256:5d99fc4ae86321e2a3eb17e319204cf5633501cf2c3fe9242c24a88a74f84451`  
		Last Modified: Wed, 02 Jul 2025 05:01:39 GMT  
		Size: 2.2 MB (2160440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cb3a42bca34bb15e981eeb6605c067349398490bf65c4b242538754665e3fc`  
		Last Modified: Wed, 02 Jul 2025 05:01:39 GMT  
		Size: 13.2 KB (13215 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:4e5c003d1b009b2beda33874ee68dfc7243710c2242b3a7b291e7e10bf632750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100547913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f75624f0e6e8a9a79e53fbca4d95f467cd3fb10402f6939faae96e7331c119`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd00bf8dd828b872bf42377febdada4af95e394143d096bfd2a690a2f1efe9b`  
		Last Modified: Wed, 04 Jun 2025 01:55:03 GMT  
		Size: 71.1 MB (71091585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:91302eef63310f57829acda62e70498f97a6dc6f49f8a9f52c2d1de02e05ffd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32cbfb8c7e9cc23d596ac1f4417d4078163071d9dbba978e599d406b3014ab7a`

```dockerfile
```

-	Layers:
	-	`sha256:87d09cc5c97769d4a7126368b6f80358a3fe46ff88895a75b58c8830aff7f6fb`  
		Last Modified: Wed, 04 Jun 2025 01:55:16 GMT  
		Size: 2.1 MB (2058272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2e43e230ae0052e2a70067ed3e4979c04b79d6b524178ce32dc959fc1f1343`  
		Last Modified: Wed, 04 Jun 2025 01:55:17 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:f37d1d1f91eec98e1114eb107a9a6c4a476fd043d3fa610638e6d1c7e3388e95
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
$ docker pull ibmjava@sha256:c14c0c8624f9adeb98403d4f7e0f29b9f9fcb7d749a017f30509a95bcc38e549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166767887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b767b04ad6e539d5eebf9214bd586f04efe73406e1a68129b33ee8c35cf690`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0d473605c46f9db355df7236218d24a2ef5b47874d4f24c615233869c1c3402a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2085991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8331766c1fdb10942e1d910875375c150f121b74857b3c20756186debc594029`

```dockerfile
```

-	Layers:
	-	`sha256:ea6fecaaeaf2d545dac3687c0cc7d201ebcbde2158f47af8e1206e20589107f2`  
		Last Modified: Tue, 03 Jun 2025 16:10:44 GMT  
		Size: 2.1 MB (2072219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e543936ae15ce4ff2d91919fd56109bc15876e24d318dd6207119383d0ec108`  
		Last Modified: Tue, 03 Jun 2025 16:10:44 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0dfc49e54b96cab01b2d9f0faa2ac9cb8bdd23a307f8cd404b5361d8803d4bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172607671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa126710509d5aad12f8d37bf40215d1e00cc81ff6e7d8b88ebf45461da61da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f581f4e6d076b9a3a2abd7d2780b110e85ed22e65b4361103dcee628dbec2ac6`  
		Last Modified: Wed, 02 Jul 2025 03:54:24 GMT  
		Size: 136.6 MB (136628814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0490dd8aaa1965e6afcc222939705f3e1ced67fc582f169ed11c978716f95ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2dfc34f191c32be6112f2902d9b2aad5a4b67319cb0efebf9ed18a1dacac18`

```dockerfile
```

-	Layers:
	-	`sha256:7f59357e19d60da8dd7a215ac4eef83e815c18200f5322df6251115c864980b7`  
		Last Modified: Wed, 02 Jul 2025 05:01:25 GMT  
		Size: 2.2 MB (2176798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b9ee117cfb64fc03034ecce80400b9922d3c7ac1397bd1dd4b4c9ab95407e1`  
		Last Modified: Wed, 02 Jul 2025 05:01:26 GMT  
		Size: 13.8 KB (13816 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:62c7820523f9938e81649f8b9986ab5fdeb8ce9d4dec6185843c21ad4ad5192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162268182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25163082133c9fa7ad7385757e18830a2946267df8435f55f3341648f74db5da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c8815ff3b76bc5d8ae6bf80bbcf7593d004650d9bc9a7dd2369668cacaa2f75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2085952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af14d337299fdcf1e40c9ba82ffceb90455d97cf954b7e4b124712fdef46d634`

```dockerfile
```

-	Layers:
	-	`sha256:ae0933ed6a39894e27c061aee0a8c345fe400e24824a7325e2ea25e1b67ea4fa`  
		Last Modified: Tue, 03 Jun 2025 16:11:29 GMT  
		Size: 2.1 MB (2072180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd20a67b3b7569a6b50f48d5d786c7c7d318e1ff2a89fa994ba37b940b4c65ae`  
		Last Modified: Tue, 03 Jun 2025 16:11:29 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:f37d1d1f91eec98e1114eb107a9a6c4a476fd043d3fa610638e6d1c7e3388e95
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
$ docker pull ibmjava@sha256:c14c0c8624f9adeb98403d4f7e0f29b9f9fcb7d749a017f30509a95bcc38e549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166767887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b767b04ad6e539d5eebf9214bd586f04efe73406e1a68129b33ee8c35cf690`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0d473605c46f9db355df7236218d24a2ef5b47874d4f24c615233869c1c3402a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2085991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8331766c1fdb10942e1d910875375c150f121b74857b3c20756186debc594029`

```dockerfile
```

-	Layers:
	-	`sha256:ea6fecaaeaf2d545dac3687c0cc7d201ebcbde2158f47af8e1206e20589107f2`  
		Last Modified: Tue, 03 Jun 2025 16:10:44 GMT  
		Size: 2.1 MB (2072219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e543936ae15ce4ff2d91919fd56109bc15876e24d318dd6207119383d0ec108`  
		Last Modified: Tue, 03 Jun 2025 16:10:44 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0dfc49e54b96cab01b2d9f0faa2ac9cb8bdd23a307f8cd404b5361d8803d4bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172607671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa126710509d5aad12f8d37bf40215d1e00cc81ff6e7d8b88ebf45461da61da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f581f4e6d076b9a3a2abd7d2780b110e85ed22e65b4361103dcee628dbec2ac6`  
		Last Modified: Wed, 02 Jul 2025 03:54:24 GMT  
		Size: 136.6 MB (136628814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0490dd8aaa1965e6afcc222939705f3e1ced67fc582f169ed11c978716f95ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2dfc34f191c32be6112f2902d9b2aad5a4b67319cb0efebf9ed18a1dacac18`

```dockerfile
```

-	Layers:
	-	`sha256:7f59357e19d60da8dd7a215ac4eef83e815c18200f5322df6251115c864980b7`  
		Last Modified: Wed, 02 Jul 2025 05:01:25 GMT  
		Size: 2.2 MB (2176798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b9ee117cfb64fc03034ecce80400b9922d3c7ac1397bd1dd4b4c9ab95407e1`  
		Last Modified: Wed, 02 Jul 2025 05:01:26 GMT  
		Size: 13.8 KB (13816 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:62c7820523f9938e81649f8b9986ab5fdeb8ce9d4dec6185843c21ad4ad5192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162268182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25163082133c9fa7ad7385757e18830a2946267df8435f55f3341648f74db5da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c8815ff3b76bc5d8ae6bf80bbcf7593d004650d9bc9a7dd2369668cacaa2f75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2085952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af14d337299fdcf1e40c9ba82ffceb90455d97cf954b7e4b124712fdef46d634`

```dockerfile
```

-	Layers:
	-	`sha256:ae0933ed6a39894e27c061aee0a8c345fe400e24824a7325e2ea25e1b67ea4fa`  
		Last Modified: Tue, 03 Jun 2025 16:11:29 GMT  
		Size: 2.1 MB (2072180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd20a67b3b7569a6b50f48d5d786c7c7d318e1ff2a89fa994ba37b940b4c65ae`  
		Last Modified: Tue, 03 Jun 2025 16:11:29 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:53a37ba44ce75c4de5f6a4f9c1026ab230955a1c00ef35d6022121ec8d89b08c
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
$ docker pull ibmjava@sha256:20f9d44884baea081e43815f0c3d9d943b63d058f8283d43c8dd833df5f39825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204165671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f57f05b562f6be51de90aa3bb09397a9ee7c5dea890d78d4eb8be1223c9494`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1673ecf1f8cf29c7b6d44154073b2680ebb266fb061c00ce97737116e2f3ae`  
		Last Modified: Tue, 03 Jun 2025 13:40:34 GMT  
		Size: 1.5 MB (1450055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a185752a0304fcd0e6e7695a76b658b3b2519964cbb14da9e9c6023d3a2df39`  
		Last Modified: Tue, 03 Jun 2025 13:40:50 GMT  
		Size: 173.2 MB (173182613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a31d52ad4e81ff9d9bf4474de8008eeb09e626981d03af0303ca4ba335fbab39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2995717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f7f5edc90ce99963a574390b48faf8e194fcc849591142661f7e9274a911c9`

```dockerfile
```

-	Layers:
	-	`sha256:2b0f78e9080b325581210f9ae857d7eefe35ede6580979fc549aa51b4d1cb4ec`  
		Last Modified: Wed, 04 Jun 2025 01:55:40 GMT  
		Size: 3.0 MB (2982539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e749ad81944be5d3dcb8be2766d40da1a1d210a5b9e5176aed053ebfeda35c3`  
		Last Modified: Wed, 04 Jun 2025 01:55:41 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:e3365e40c4a63ab47e7997d00689a8750cead278ee316dadf0f1a3f7ee38b477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210217391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267afb8e32ffd3ef9ae2bccf716ee830296bbb97029f8e64dd766634e787329e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba99977cd9d6077fd4b307c3357787311ced4b3a091deff606c2244499c52dca`  
		Last Modified: Wed, 02 Jul 2025 05:05:40 GMT  
		Size: 174.2 MB (174238534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8e2cbe645208295d6ce8a67be9f3e35eafc43040b80a6af6c62fb6d25f4fdf7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420f9f75bab2dc52eea96bea822bf74dfdf79c4aeafc5e692c1c907b130ce32d`

```dockerfile
```

-	Layers:
	-	`sha256:2a580b888b091e828d99907782b577e4929fb7af8b70034b3c2f8704a7fccda0`  
		Last Modified: Wed, 02 Jul 2025 05:01:33 GMT  
		Size: 3.1 MB (3069777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:945afa5218986909835c1422d2582bc61260d20f147ee8cd3e743bf8e1842c55`  
		Last Modified: Wed, 02 Jul 2025 05:01:34 GMT  
		Size: 13.2 KB (13212 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:92c479b9321584afd388a500009071de71605089938119defa89d5a82ee4c74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192753473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd384000d924a2236616fec91fd4af7b135931b63869fe3a1b37fd79591ad5f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2d974b5413f042241053a768c76f997e675bc55e8e98836da09fd5211caf69`  
		Last Modified: Wed, 04 Jun 2025 01:56:26 GMT  
		Size: 163.3 MB (163297145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:86bad0987a14f67bfb89db9ee2684dc7c1f50acf6501ae85604317315bff7503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2669033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1348730ceea4c07afd5a1a64d53cbece01a0b205a6108b0fa6b00cb72d5451c`

```dockerfile
```

-	Layers:
	-	`sha256:74df62495bb96ef85a20d09412940687ef4e6fd3074c14dc90b4b4603424503e`  
		Last Modified: Wed, 04 Jun 2025 01:56:47 GMT  
		Size: 2.7 MB (2655855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d83a744ca31a81fdecced1884f246faa6ce3fb50139d3ec01cb389aabf576e`  
		Last Modified: Wed, 04 Jun 2025 01:56:48 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:5fedf567317236256496a5159eb4eef032ed7ad2c2707b5becf8fc0af33f1228
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
$ docker pull ibmjava@sha256:f958e2b42789067a30996418bd8c437523fbf41d5644fed195b1af8ee92acf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101478723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208bfd2b5bcc49248cfd829c7a6fce5275267ad114d1852ad35778ea1fa440c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98acd822b08706485046b4324f633237d583daebe53cebec36a620ccb812eefe`  
		Last Modified: Wed, 04 Jun 2025 01:54:19 GMT  
		Size: 1.5 MB (1450028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225c989849e787ac38a65d9d633ad373c2de4d843dc80de0a6e91e5a32c0d6b0`  
		Last Modified: Wed, 04 Jun 2025 01:54:24 GMT  
		Size: 70.5 MB (70495692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9fda182f6a32a51973d8f6feeea26ba584d03b4db71c0496f3d45053335a1b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2067831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756148d5f8906ca53804b08c33fa0888fee6e723ee16bf5a7916bb0a52acd6f5`

```dockerfile
```

-	Layers:
	-	`sha256:9d0d95f4621604b0c19165d24a9fc4c20748cf223ba73e8cd269b89bd4de48ee`  
		Last Modified: Wed, 04 Jun 2025 01:54:35 GMT  
		Size: 2.1 MB (2054650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc9efd7c6722bfb7265b6b546f9faacf0a6c438fedc711d1bab5d2ba38ec7fb`  
		Last Modified: Wed, 04 Jun 2025 01:54:37 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:f79d9191c2cfd63a96e6104b819c0a7e5fcaa6935ef4ae9e712668f0c03f94d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107307499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c70aece4bce65f968965847dc6fa280d3cfd62a5160edbf632c9d9b15729da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b508e78ad839eb5804b4140d689c487ab1a9a5ee9bf667cf9d4f054b0f8aa3c`  
		Last Modified: Wed, 02 Jul 2025 03:55:31 GMT  
		Size: 71.3 MB (71328642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3d952bf4ba0008d0443b61c87f05520f6967a47d4dadf989491a93cec747473c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9310ab59c178144de5d53c77bfe20c325f5f00e0f4293e4b036a8aa4558b4`

```dockerfile
```

-	Layers:
	-	`sha256:5d99fc4ae86321e2a3eb17e319204cf5633501cf2c3fe9242c24a88a74f84451`  
		Last Modified: Wed, 02 Jul 2025 05:01:39 GMT  
		Size: 2.2 MB (2160440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cb3a42bca34bb15e981eeb6605c067349398490bf65c4b242538754665e3fc`  
		Last Modified: Wed, 02 Jul 2025 05:01:39 GMT  
		Size: 13.2 KB (13215 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:4e5c003d1b009b2beda33874ee68dfc7243710c2242b3a7b291e7e10bf632750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100547913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f75624f0e6e8a9a79e53fbca4d95f467cd3fb10402f6939faae96e7331c119`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd00bf8dd828b872bf42377febdada4af95e394143d096bfd2a690a2f1efe9b`  
		Last Modified: Wed, 04 Jun 2025 01:55:03 GMT  
		Size: 71.1 MB (71091585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:91302eef63310f57829acda62e70498f97a6dc6f49f8a9f52c2d1de02e05ffd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32cbfb8c7e9cc23d596ac1f4417d4078163071d9dbba978e599d406b3014ab7a`

```dockerfile
```

-	Layers:
	-	`sha256:87d09cc5c97769d4a7126368b6f80358a3fe46ff88895a75b58c8830aff7f6fb`  
		Last Modified: Wed, 04 Jun 2025 01:55:16 GMT  
		Size: 2.1 MB (2058272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2e43e230ae0052e2a70067ed3e4979c04b79d6b524178ce32dc959fc1f1343`  
		Last Modified: Wed, 04 Jun 2025 01:55:17 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json
