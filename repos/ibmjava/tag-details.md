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
$ docker pull ibmjava@sha256:e1c2be85ccce7b783002d9060d05f633f04e0d1b1537b0d66f0825d1a9b55ad6
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
$ docker pull ibmjava@sha256:bd48dc91eb6ff19f34485181d55cc01dd596d696acb642831cf6f2bbb2116b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166792954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b61abfc818ae1062699e4181e38e22689edadb4186fb4dcedaa9a5fcb4e4a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:38:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:38:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:38:00 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:38:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:38:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907aa1863e414cc3bd625d16f193eb2a7a696d737f29ea8028674b7ff063b7ea`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 1.5 MB (1450031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31583ab84185052af0267c732938b8d9abf260403c2b16db59ce3c029cb1306e`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 135.8 MB (135804403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6298cb084d30fbb1f9197a5a9c4b80575fbf04a9ee0fc2b75d2ef378a53a3029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624dd04aa3d68aa0805dfed5ec0415bfd434cf3673b5b42c0b0572b96b3e9e1b`

```dockerfile
```

-	Layers:
	-	`sha256:8975656e0276028fa94e8361562337a386c6b64683f6bb5f912766d543714049`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121859b9ce1a86f5b94bb9eaf8aeca84aeb7c1b5f605b19d9e3a398cfb755b2b`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 13.2 KB (13191 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:75da0fb44e4aa91f34eeb1326dba50ab501936cbd41b71a641f3c139504c4e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172739449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677bb812a6c55dcf30a828f65bb08ad77c5e4bb612f474f745a95da9561e0d65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:00:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:00:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b990e2f2714a48197073ae8696b1699afebaa89893fb7cfe4bbed983bbd1a3b0`  
		Last Modified: Tue, 17 Mar 2026 09:01:35 GMT  
		Size: 136.7 MB (136749908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:1181b3548ef88779e2237462473e330fdc6fe03b071aa0872be49c7f06c58a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5766a7b5ee6445c211eaa2bf3589187db78f66bb6f3eb2469817fefba6315d`

```dockerfile
```

-	Layers:
	-	`sha256:a3123ccfe4588cac0917d7458350552c7e28a70d0c73ed24bde3bab6025e6891`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a38b956b7552dfa76b9e2afdd7791985d53c69349e3bf6cc2eccf2389ff0ae77`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:8368192116d7473e5ac0836a468acad413c5f70c5c3e8acf74d5e30460938b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162733622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0febc3901a5954c8b9c42b42eb9726a66cc23eb55fe5825a1c8508922ac3e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:08 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:35:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:35:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ec19658856db1b8624bd8ebec866bdd80a75f89b9975fa0a83c84c0a82533d`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 1.5 MB (1455803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c4a63b925697e8ab7861cc42e5a891be2cb407053bb6155a9b92a251f0926`  
		Last Modified: Tue, 17 Mar 2026 02:35:36 GMT  
		Size: 133.3 MB (133270717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ebf9d17a7744cdfd13992002f394f9d8968de303e79ce58d174fdae43faf7818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c74e0796e68a0953d5e5f62e165d64bf65676e41c2888e44e762bf942fb9e1`

```dockerfile
```

-	Layers:
	-	`sha256:20739c7df9a65a070e38922bd2313919710a8e7f15d1afa4d6da15aa65a7b999`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 2.2 MB (2174077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f37183efaf4ebdc3b442dde92b3dc215d72f686dc2654ada87d25a5228f596e`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 13.2 KB (13191 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:e1c2be85ccce7b783002d9060d05f633f04e0d1b1537b0d66f0825d1a9b55ad6
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
$ docker pull ibmjava@sha256:bd48dc91eb6ff19f34485181d55cc01dd596d696acb642831cf6f2bbb2116b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166792954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b61abfc818ae1062699e4181e38e22689edadb4186fb4dcedaa9a5fcb4e4a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:38:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:38:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:38:00 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:38:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:38:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907aa1863e414cc3bd625d16f193eb2a7a696d737f29ea8028674b7ff063b7ea`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 1.5 MB (1450031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31583ab84185052af0267c732938b8d9abf260403c2b16db59ce3c029cb1306e`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 135.8 MB (135804403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6298cb084d30fbb1f9197a5a9c4b80575fbf04a9ee0fc2b75d2ef378a53a3029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624dd04aa3d68aa0805dfed5ec0415bfd434cf3673b5b42c0b0572b96b3e9e1b`

```dockerfile
```

-	Layers:
	-	`sha256:8975656e0276028fa94e8361562337a386c6b64683f6bb5f912766d543714049`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121859b9ce1a86f5b94bb9eaf8aeca84aeb7c1b5f605b19d9e3a398cfb755b2b`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 13.2 KB (13191 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:75da0fb44e4aa91f34eeb1326dba50ab501936cbd41b71a641f3c139504c4e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172739449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677bb812a6c55dcf30a828f65bb08ad77c5e4bb612f474f745a95da9561e0d65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:00:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:00:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b990e2f2714a48197073ae8696b1699afebaa89893fb7cfe4bbed983bbd1a3b0`  
		Last Modified: Tue, 17 Mar 2026 09:01:35 GMT  
		Size: 136.7 MB (136749908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:1181b3548ef88779e2237462473e330fdc6fe03b071aa0872be49c7f06c58a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5766a7b5ee6445c211eaa2bf3589187db78f66bb6f3eb2469817fefba6315d`

```dockerfile
```

-	Layers:
	-	`sha256:a3123ccfe4588cac0917d7458350552c7e28a70d0c73ed24bde3bab6025e6891`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a38b956b7552dfa76b9e2afdd7791985d53c69349e3bf6cc2eccf2389ff0ae77`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:8368192116d7473e5ac0836a468acad413c5f70c5c3e8acf74d5e30460938b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162733622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0febc3901a5954c8b9c42b42eb9726a66cc23eb55fe5825a1c8508922ac3e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:08 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:35:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:35:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ec19658856db1b8624bd8ebec866bdd80a75f89b9975fa0a83c84c0a82533d`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 1.5 MB (1455803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c4a63b925697e8ab7861cc42e5a891be2cb407053bb6155a9b92a251f0926`  
		Last Modified: Tue, 17 Mar 2026 02:35:36 GMT  
		Size: 133.3 MB (133270717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ebf9d17a7744cdfd13992002f394f9d8968de303e79ce58d174fdae43faf7818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c74e0796e68a0953d5e5f62e165d64bf65676e41c2888e44e762bf942fb9e1`

```dockerfile
```

-	Layers:
	-	`sha256:20739c7df9a65a070e38922bd2313919710a8e7f15d1afa4d6da15aa65a7b999`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 2.2 MB (2174077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f37183efaf4ebdc3b442dde92b3dc215d72f686dc2654ada87d25a5228f596e`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 13.2 KB (13191 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:9919ff473492a0184fce8cce2b2fd53432f0322b0b034d62742ecb02569ee1b8
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
$ docker pull ibmjava@sha256:946d2d248627fa9e970567797ae61e5e2a9cd8ecf8d929c671b2751469299ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204046815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1721eacf55c64231950a04f40fbd8a21c7cc4802f24b3fba630c99cf25f32021`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:39:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:39:02 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:39:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:39:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486a0cc1bc5c4630c334e3ef2214d1ad765d760a43a7054dcbfade82afe29283`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 1.5 MB (1450067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb898a25d9c64b330791cfa3f3d3639a8d6863cc4d6ffdcd61d7e5da57cd6dc9`  
		Last Modified: Tue, 17 Mar 2026 01:40:18 GMT  
		Size: 173.1 MB (173058228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:d599fc29fa420c298c20ec6869ed60bd22987bee06b91ba5a8490acb59b4a032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d06816b2c5090b8b4953d9e69ec806ff6cc12ca1d3f101f7d3cc324c71bc26a`

```dockerfile
```

-	Layers:
	-	`sha256:1abba04bccb36f420e6f4ee22e4a23042440a83ab6f2b368465162cf691e5fd7`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 3.1 MB (3084436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9960a7a2366fbf774d8607ecbdb6ebfaf5eb41f2c1ac61e814cc582e2123edf`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:d16d8cf237312580f6f205af6be4d2ece2a89eba342bf17eac2322cc3a65e713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210202250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea22ddad3670a5281b3b2a0831491bddda4757e44635130316e3143bfdf85ea7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:02:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:02:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c401a6ed6a34f2058c3b651c40d5634f706de4db2c5dd73a816a6e6481685f`  
		Last Modified: Tue, 17 Mar 2026 09:03:19 GMT  
		Size: 174.2 MB (174212709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a7bb4def5d76a47db3c990378b6e56cab368ed1befff06647f70c741fd2c7faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f06a00d8b7e5a8bc673ab3db92bf6632e14e2bca297a70023d65956fc23c57f`

```dockerfile
```

-	Layers:
	-	`sha256:795c9a1a2ee38481297b4715396321cfde2e2d3a5cb8b9220c8a088350f842a1`  
		Last Modified: Tue, 17 Mar 2026 09:03:15 GMT  
		Size: 3.1 MB (3070385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7fecdce5ec1ae5ded8cc72718f7123b7a88b2745230045f4810f9a7ec909534`  
		Last Modified: Tue, 17 Mar 2026 09:03:15 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:d50e878269877470450a35aff736acd2f2aaced18a630d7ce35a093d0380bbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193093413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05e41a6ed9be802ab076f6a3630756459b9bbefecf00d149f4bdf073f94b208`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:08 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:35:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:35:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ec19658856db1b8624bd8ebec866bdd80a75f89b9975fa0a83c84c0a82533d`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 1.5 MB (1455803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23bbc57d9e744b627543ae7ccf124d2070352c70ba38bb69f933a24bee3fbbe`  
		Last Modified: Tue, 17 Mar 2026 02:36:06 GMT  
		Size: 163.6 MB (163630508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9ea38da7c66eaf1b5d60b361e56cdddf6e548afab9fda3518c0679ba86c4874d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43d77909dfecf678182a48dc749aa1cb20f71d72cd6036f28287424791c355d`

```dockerfile
```

-	Layers:
	-	`sha256:ecb2014b00be73dc9dab90ff1f6429d00398d847d344f2d40b610ae298ffc65c`  
		Last Modified: Tue, 17 Mar 2026 02:36:02 GMT  
		Size: 2.8 MB (2757752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2263756a259b2e914ad46e2ff2a85d79c8e3019ce0e1483d9720b78b9824c52`  
		Last Modified: Tue, 17 Mar 2026 02:36:02 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:08d142fa029f34acb6fc7138b664f2866c17528afa66cdd8e37e8f5c33704c30
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
$ docker pull ibmjava@sha256:40eb55678154cbec43f955b29627c94489bdb980c375e17fd002497177d71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102032501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f59f5ba1d86d57d8192caeec156e72839f8015e23466e834b4e637c481fe180`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:38:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:38:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:38:21 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:38:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:38:49 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda6992acf7946bb49b19b813307ddce44be037dc956f72cbdefad5c0451011c`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 1.5 MB (1450004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6f4b5a9618d868ebd1368148ccc36913a08be266accd214995e162ae610cff`  
		Last Modified: Tue, 17 Mar 2026 01:39:00 GMT  
		Size: 71.0 MB (71043977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:113c8de52cfed403979b357e017553fb39c87e866902e72c142f3448b9509a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20578745d0e6efe0205ce7690683230fa3ba73b8c96d802b9fde147f212c854a`

```dockerfile
```

-	Layers:
	-	`sha256:39e638f4ad76558e1abc1522f4ee8d20807f100be1cda00c4ed3012e64a7c9c8`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 2.2 MB (2156549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21878a916161ded72eac50ef9bb13140ea347aaeac3a1d096c951e9a48fd088c`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:4a226ef900cb19af8d10b761688db8b599e05d4d78fc736f3b7b5bcc9389c851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107973118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69417ff2c11f5f058aeab9921034c20189da4fbc237a0c1f625f495198a56dac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:01:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2930a63157b00bf9aef8c2f7549bbcf8184530de6350d92d7787b15cf5a48668`  
		Last Modified: Tue, 17 Mar 2026 09:01:51 GMT  
		Size: 72.0 MB (71983577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:49097b98767c4fc1cae0e6c101e7f7b92ec696ddda329142a0a2362cde6eacf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4c235d56166ee198cd6aad97055aa0b2f9e34bc28a8b43ae3a6e087f7937d8`

```dockerfile
```

-	Layers:
	-	`sha256:163a666ec3e5b9e602de3b47db381f48e17dc1ed4a6da72900338601197d6024`  
		Last Modified: Tue, 17 Mar 2026 09:01:49 GMT  
		Size: 2.2 MB (2161050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:047260f196209b742c556aa8395c44856bc18bc1ef92d6919821ff536d3795fc`  
		Last Modified: Tue, 17 Mar 2026 09:01:49 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:848e4a88e781fe55d0159064ede17578f5bcb7d597f1dc39e175f3cac6bc5b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101548222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6b0cb963e9187490f69b2e7dbb3c7794de4f7e5643b36fd364bc1cfbf6415b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:31 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:31 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:34:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:34:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edcd91a41ee09197ac78b9446645d919d302d4e6bd111070c1d80415e1f6f5a`  
		Last Modified: Tue, 17 Mar 2026 02:35:09 GMT  
		Size: 1.5 MB (1455776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11b08ab3fd61ca7d95eeb83e30dfc381cef5518aff1e320af9178d2d24bd211`  
		Last Modified: Tue, 17 Mar 2026 02:35:11 GMT  
		Size: 72.1 MB (72085344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:44e72ef13cc6e7230ae50a8abe22a98e4d46705a849ffee8b998b5112eb7b81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd08ffb05a271ec84d6e4fecb3916910bf1f071339cf4e6331d9366b58acbf29`

```dockerfile
```

-	Layers:
	-	`sha256:5012b78f94d748a661594abcc798a8c428742b614ec665ee79a8e9a34e365d4a`  
		Last Modified: Tue, 17 Mar 2026 02:35:09 GMT  
		Size: 2.2 MB (2160171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5a06999fafd55e15280321d2ddd19a67729dce56f1a205c83eec31c5d9479e`  
		Last Modified: Tue, 17 Mar 2026 02:35:09 GMT  
		Size: 12.6 KB (12600 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:e1c2be85ccce7b783002d9060d05f633f04e0d1b1537b0d66f0825d1a9b55ad6
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
$ docker pull ibmjava@sha256:bd48dc91eb6ff19f34485181d55cc01dd596d696acb642831cf6f2bbb2116b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166792954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b61abfc818ae1062699e4181e38e22689edadb4186fb4dcedaa9a5fcb4e4a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:38:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:38:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:38:00 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:38:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:38:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907aa1863e414cc3bd625d16f193eb2a7a696d737f29ea8028674b7ff063b7ea`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 1.5 MB (1450031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31583ab84185052af0267c732938b8d9abf260403c2b16db59ce3c029cb1306e`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 135.8 MB (135804403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6298cb084d30fbb1f9197a5a9c4b80575fbf04a9ee0fc2b75d2ef378a53a3029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624dd04aa3d68aa0805dfed5ec0415bfd434cf3673b5b42c0b0572b96b3e9e1b`

```dockerfile
```

-	Layers:
	-	`sha256:8975656e0276028fa94e8361562337a386c6b64683f6bb5f912766d543714049`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121859b9ce1a86f5b94bb9eaf8aeca84aeb7c1b5f605b19d9e3a398cfb755b2b`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 13.2 KB (13191 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:75da0fb44e4aa91f34eeb1326dba50ab501936cbd41b71a641f3c139504c4e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172739449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677bb812a6c55dcf30a828f65bb08ad77c5e4bb612f474f745a95da9561e0d65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:00:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:00:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b990e2f2714a48197073ae8696b1699afebaa89893fb7cfe4bbed983bbd1a3b0`  
		Last Modified: Tue, 17 Mar 2026 09:01:35 GMT  
		Size: 136.7 MB (136749908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:1181b3548ef88779e2237462473e330fdc6fe03b071aa0872be49c7f06c58a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5766a7b5ee6445c211eaa2bf3589187db78f66bb6f3eb2469817fefba6315d`

```dockerfile
```

-	Layers:
	-	`sha256:a3123ccfe4588cac0917d7458350552c7e28a70d0c73ed24bde3bab6025e6891`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a38b956b7552dfa76b9e2afdd7791985d53c69349e3bf6cc2eccf2389ff0ae77`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:8368192116d7473e5ac0836a468acad413c5f70c5c3e8acf74d5e30460938b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162733622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0febc3901a5954c8b9c42b42eb9726a66cc23eb55fe5825a1c8508922ac3e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:08 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:35:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:35:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ec19658856db1b8624bd8ebec866bdd80a75f89b9975fa0a83c84c0a82533d`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 1.5 MB (1455803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c4a63b925697e8ab7861cc42e5a891be2cb407053bb6155a9b92a251f0926`  
		Last Modified: Tue, 17 Mar 2026 02:35:36 GMT  
		Size: 133.3 MB (133270717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ebf9d17a7744cdfd13992002f394f9d8968de303e79ce58d174fdae43faf7818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c74e0796e68a0953d5e5f62e165d64bf65676e41c2888e44e762bf942fb9e1`

```dockerfile
```

-	Layers:
	-	`sha256:20739c7df9a65a070e38922bd2313919710a8e7f15d1afa4d6da15aa65a7b999`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 2.2 MB (2174077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f37183efaf4ebdc3b442dde92b3dc215d72f686dc2654ada87d25a5228f596e`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 13.2 KB (13191 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:e1c2be85ccce7b783002d9060d05f633f04e0d1b1537b0d66f0825d1a9b55ad6
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
$ docker pull ibmjava@sha256:bd48dc91eb6ff19f34485181d55cc01dd596d696acb642831cf6f2bbb2116b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166792954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b61abfc818ae1062699e4181e38e22689edadb4186fb4dcedaa9a5fcb4e4a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:38:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:38:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:38:00 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:38:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:38:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907aa1863e414cc3bd625d16f193eb2a7a696d737f29ea8028674b7ff063b7ea`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 1.5 MB (1450031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31583ab84185052af0267c732938b8d9abf260403c2b16db59ce3c029cb1306e`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 135.8 MB (135804403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6298cb084d30fbb1f9197a5a9c4b80575fbf04a9ee0fc2b75d2ef378a53a3029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624dd04aa3d68aa0805dfed5ec0415bfd434cf3673b5b42c0b0572b96b3e9e1b`

```dockerfile
```

-	Layers:
	-	`sha256:8975656e0276028fa94e8361562337a386c6b64683f6bb5f912766d543714049`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121859b9ce1a86f5b94bb9eaf8aeca84aeb7c1b5f605b19d9e3a398cfb755b2b`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 13.2 KB (13191 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:75da0fb44e4aa91f34eeb1326dba50ab501936cbd41b71a641f3c139504c4e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172739449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677bb812a6c55dcf30a828f65bb08ad77c5e4bb612f474f745a95da9561e0d65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:00:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:00:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b990e2f2714a48197073ae8696b1699afebaa89893fb7cfe4bbed983bbd1a3b0`  
		Last Modified: Tue, 17 Mar 2026 09:01:35 GMT  
		Size: 136.7 MB (136749908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:1181b3548ef88779e2237462473e330fdc6fe03b071aa0872be49c7f06c58a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5766a7b5ee6445c211eaa2bf3589187db78f66bb6f3eb2469817fefba6315d`

```dockerfile
```

-	Layers:
	-	`sha256:a3123ccfe4588cac0917d7458350552c7e28a70d0c73ed24bde3bab6025e6891`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a38b956b7552dfa76b9e2afdd7791985d53c69349e3bf6cc2eccf2389ff0ae77`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:8368192116d7473e5ac0836a468acad413c5f70c5c3e8acf74d5e30460938b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162733622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0febc3901a5954c8b9c42b42eb9726a66cc23eb55fe5825a1c8508922ac3e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:08 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:35:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:35:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ec19658856db1b8624bd8ebec866bdd80a75f89b9975fa0a83c84c0a82533d`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 1.5 MB (1455803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c4a63b925697e8ab7861cc42e5a891be2cb407053bb6155a9b92a251f0926`  
		Last Modified: Tue, 17 Mar 2026 02:35:36 GMT  
		Size: 133.3 MB (133270717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ebf9d17a7744cdfd13992002f394f9d8968de303e79ce58d174fdae43faf7818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c74e0796e68a0953d5e5f62e165d64bf65676e41c2888e44e762bf942fb9e1`

```dockerfile
```

-	Layers:
	-	`sha256:20739c7df9a65a070e38922bd2313919710a8e7f15d1afa4d6da15aa65a7b999`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 2.2 MB (2174077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f37183efaf4ebdc3b442dde92b3dc215d72f686dc2654ada87d25a5228f596e`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 13.2 KB (13191 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:9919ff473492a0184fce8cce2b2fd53432f0322b0b034d62742ecb02569ee1b8
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
$ docker pull ibmjava@sha256:946d2d248627fa9e970567797ae61e5e2a9cd8ecf8d929c671b2751469299ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204046815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1721eacf55c64231950a04f40fbd8a21c7cc4802f24b3fba630c99cf25f32021`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:39:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:39:02 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:39:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:39:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486a0cc1bc5c4630c334e3ef2214d1ad765d760a43a7054dcbfade82afe29283`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 1.5 MB (1450067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb898a25d9c64b330791cfa3f3d3639a8d6863cc4d6ffdcd61d7e5da57cd6dc9`  
		Last Modified: Tue, 17 Mar 2026 01:40:18 GMT  
		Size: 173.1 MB (173058228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:d599fc29fa420c298c20ec6869ed60bd22987bee06b91ba5a8490acb59b4a032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d06816b2c5090b8b4953d9e69ec806ff6cc12ca1d3f101f7d3cc324c71bc26a`

```dockerfile
```

-	Layers:
	-	`sha256:1abba04bccb36f420e6f4ee22e4a23042440a83ab6f2b368465162cf691e5fd7`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 3.1 MB (3084436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9960a7a2366fbf774d8607ecbdb6ebfaf5eb41f2c1ac61e814cc582e2123edf`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:d16d8cf237312580f6f205af6be4d2ece2a89eba342bf17eac2322cc3a65e713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210202250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea22ddad3670a5281b3b2a0831491bddda4757e44635130316e3143bfdf85ea7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:02:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:02:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c401a6ed6a34f2058c3b651c40d5634f706de4db2c5dd73a816a6e6481685f`  
		Last Modified: Tue, 17 Mar 2026 09:03:19 GMT  
		Size: 174.2 MB (174212709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a7bb4def5d76a47db3c990378b6e56cab368ed1befff06647f70c741fd2c7faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f06a00d8b7e5a8bc673ab3db92bf6632e14e2bca297a70023d65956fc23c57f`

```dockerfile
```

-	Layers:
	-	`sha256:795c9a1a2ee38481297b4715396321cfde2e2d3a5cb8b9220c8a088350f842a1`  
		Last Modified: Tue, 17 Mar 2026 09:03:15 GMT  
		Size: 3.1 MB (3070385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7fecdce5ec1ae5ded8cc72718f7123b7a88b2745230045f4810f9a7ec909534`  
		Last Modified: Tue, 17 Mar 2026 09:03:15 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:d50e878269877470450a35aff736acd2f2aaced18a630d7ce35a093d0380bbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193093413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05e41a6ed9be802ab076f6a3630756459b9bbefecf00d149f4bdf073f94b208`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:08 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:35:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:35:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ec19658856db1b8624bd8ebec866bdd80a75f89b9975fa0a83c84c0a82533d`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 1.5 MB (1455803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23bbc57d9e744b627543ae7ccf124d2070352c70ba38bb69f933a24bee3fbbe`  
		Last Modified: Tue, 17 Mar 2026 02:36:06 GMT  
		Size: 163.6 MB (163630508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9ea38da7c66eaf1b5d60b361e56cdddf6e548afab9fda3518c0679ba86c4874d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43d77909dfecf678182a48dc749aa1cb20f71d72cd6036f28287424791c355d`

```dockerfile
```

-	Layers:
	-	`sha256:ecb2014b00be73dc9dab90ff1f6429d00398d847d344f2d40b610ae298ffc65c`  
		Last Modified: Tue, 17 Mar 2026 02:36:02 GMT  
		Size: 2.8 MB (2757752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2263756a259b2e914ad46e2ff2a85d79c8e3019ce0e1483d9720b78b9824c52`  
		Last Modified: Tue, 17 Mar 2026 02:36:02 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:08d142fa029f34acb6fc7138b664f2866c17528afa66cdd8e37e8f5c33704c30
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
$ docker pull ibmjava@sha256:40eb55678154cbec43f955b29627c94489bdb980c375e17fd002497177d71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102032501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f59f5ba1d86d57d8192caeec156e72839f8015e23466e834b4e637c481fe180`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:38:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:38:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:38:21 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:38:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:38:49 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda6992acf7946bb49b19b813307ddce44be037dc956f72cbdefad5c0451011c`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 1.5 MB (1450004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6f4b5a9618d868ebd1368148ccc36913a08be266accd214995e162ae610cff`  
		Last Modified: Tue, 17 Mar 2026 01:39:00 GMT  
		Size: 71.0 MB (71043977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:113c8de52cfed403979b357e017553fb39c87e866902e72c142f3448b9509a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20578745d0e6efe0205ce7690683230fa3ba73b8c96d802b9fde147f212c854a`

```dockerfile
```

-	Layers:
	-	`sha256:39e638f4ad76558e1abc1522f4ee8d20807f100be1cda00c4ed3012e64a7c9c8`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 2.2 MB (2156549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21878a916161ded72eac50ef9bb13140ea347aaeac3a1d096c951e9a48fd088c`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:4a226ef900cb19af8d10b761688db8b599e05d4d78fc736f3b7b5bcc9389c851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107973118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69417ff2c11f5f058aeab9921034c20189da4fbc237a0c1f625f495198a56dac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:01:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2930a63157b00bf9aef8c2f7549bbcf8184530de6350d92d7787b15cf5a48668`  
		Last Modified: Tue, 17 Mar 2026 09:01:51 GMT  
		Size: 72.0 MB (71983577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:49097b98767c4fc1cae0e6c101e7f7b92ec696ddda329142a0a2362cde6eacf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4c235d56166ee198cd6aad97055aa0b2f9e34bc28a8b43ae3a6e087f7937d8`

```dockerfile
```

-	Layers:
	-	`sha256:163a666ec3e5b9e602de3b47db381f48e17dc1ed4a6da72900338601197d6024`  
		Last Modified: Tue, 17 Mar 2026 09:01:49 GMT  
		Size: 2.2 MB (2161050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:047260f196209b742c556aa8395c44856bc18bc1ef92d6919821ff536d3795fc`  
		Last Modified: Tue, 17 Mar 2026 09:01:49 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:848e4a88e781fe55d0159064ede17578f5bcb7d597f1dc39e175f3cac6bc5b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101548222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6b0cb963e9187490f69b2e7dbb3c7794de4f7e5643b36fd364bc1cfbf6415b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:31 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:31 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:34:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:34:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edcd91a41ee09197ac78b9446645d919d302d4e6bd111070c1d80415e1f6f5a`  
		Last Modified: Tue, 17 Mar 2026 02:35:09 GMT  
		Size: 1.5 MB (1455776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11b08ab3fd61ca7d95eeb83e30dfc381cef5518aff1e320af9178d2d24bd211`  
		Last Modified: Tue, 17 Mar 2026 02:35:11 GMT  
		Size: 72.1 MB (72085344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:44e72ef13cc6e7230ae50a8abe22a98e4d46705a849ffee8b998b5112eb7b81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd08ffb05a271ec84d6e4fecb3916910bf1f071339cf4e6331d9366b58acbf29`

```dockerfile
```

-	Layers:
	-	`sha256:5012b78f94d748a661594abcc798a8c428742b614ec665ee79a8e9a34e365d4a`  
		Last Modified: Tue, 17 Mar 2026 02:35:09 GMT  
		Size: 2.2 MB (2160171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5a06999fafd55e15280321d2ddd19a67729dce56f1a205c83eec31c5d9479e`  
		Last Modified: Tue, 17 Mar 2026 02:35:09 GMT  
		Size: 12.6 KB (12600 bytes)  
		MIME: application/vnd.in-toto+json
