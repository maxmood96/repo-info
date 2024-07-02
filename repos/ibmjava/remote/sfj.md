## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:c3f37e52e68c249c3bdd56bf9b0d245bed9d2b6ebf77873df8df71662dc769d9
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
$ docker pull ibmjava@sha256:235f4749cfd4a9b11948a781da9e66f390da40d22d12a9e13d87c57bb339674f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100877046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9631de094f5caef24e4cbee09cdef6bb53397e6aaae579eb378f806e99b53ee2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecbfd7b6c160400ea9952aefaa2a5a399e6210ef5d0ab6c65e59c9779f319d1`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 1.4 MB (1438223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29995a467d55c0447a2742539da59d117bd5b2ca72b96d8a4f8d9a62cf664a1d`  
		Last Modified: Mon, 01 Jul 2024 23:55:05 GMT  
		Size: 69.9 MB (69905069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:7751b54473ef6d57b0f7b70c86504c6c9f3c272337553a85ff7889f71cb76e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2002033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2a71faa7ae03aa4b78ba36977170bc3152d1ed35c3ba12cc62ce9ae42fd718`

```dockerfile
```

-	Layers:
	-	`sha256:825ed06a15a3205e38a2f4f99634dafd45719a5b41d9dcdcdb682a6cebdde4d1`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 2.0 MB (1989106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1da54cf03571f3a4c7a06be97eb66617a00b6e9db8e0d6c94746bafb84444e8`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:b2dcb62f57ee446f5b404533ab220303a4a33f5b0f2aa0f23cf1d90a09c6e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106386730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97be7d66e1ecc2d3201b283e69d6b7a61b4b90a80d660569a2d95541a628b459`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
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
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931c5e4dd486c8b6e739d1d63a66784037fbac8a7c6db683ddc9bb274e70188f`  
		Last Modified: Mon, 01 Jul 2024 23:59:09 GMT  
		Size: 70.4 MB (70402761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:d77c1db7362b0a00bfb31e50086d7d3fcc8ece0c2b375ca7ae57ee8ad0418eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be2c20a74fdfda27f7caf6245c17571b4e57ae4a608e63933999da1be4778f4`

```dockerfile
```

-	Layers:
	-	`sha256:452a2cea572a876e34d1756b41eed27b5aa0d809474a6b60ad723e68cb842074`  
		Last Modified: Mon, 01 Jul 2024 23:59:07 GMT  
		Size: 2.0 MB (1992490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12331d57dc50061d1126e4f2ffda4c621d60c42f63d332b0eda7fca81cd3218e`  
		Last Modified: Mon, 01 Jul 2024 23:59:07 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:56918331a479357a9046b00bfa9cac113eb2520de73b55152ac3825cb3bfdbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99820949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b538fc5f45c5b721c9ec7505f035a37ec2fe2499c3a30557ea55c9cf5cab7355`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
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
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c0ce8c3e76419e27c7140d29d7a13681b1f997591505a180fe442203298be`  
		Last Modified: Mon, 01 Jul 2024 23:57:41 GMT  
		Size: 70.4 MB (70378471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3dec87ba4700cb91f457fef6ea168eb7db55f658cb4b2f1ce1d20dd5063ba8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1493ec3d9d626aaf22d92c5ee30fcd2125a3a3bce808394dbce22ac82b5713f9`

```dockerfile
```

-	Layers:
	-	`sha256:31dc3e5f49697201b3b49326f2e3e31452cc851a83984e925ffe09307db6c2b6`  
		Last Modified: Mon, 01 Jul 2024 23:57:40 GMT  
		Size: 2.0 MB (1990495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbcb45fa29ce20bae53eda2f5ba6f6c85f09148ebcc0dc8c1706cbcc9dbfaeb9`  
		Last Modified: Mon, 01 Jul 2024 23:57:39 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json
