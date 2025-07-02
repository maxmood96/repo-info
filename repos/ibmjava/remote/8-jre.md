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
