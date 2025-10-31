## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:fdd648126ca923ab660ee6becda8fc6833b7299eafdd2c4c2b6cd69b5e8351f8
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
$ docker pull ibmjava@sha256:a75b9d7b4b9b43ef75b44a1be93df2b83243c2a3cb34fd948306fae050fa1f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166527972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c74e320bca0cc216ea6b6ad74eeda086eacd634e0e3f7a787a98a87b281246`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 30 Oct 2025 23:53:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 23:53:58 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 30 Oct 2025 23:54:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 30 Oct 2025 23:54:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23311177b9d27a75a99852778c82058eb31857a33e6c02ab885b46db249dfb6`  
		Last Modified: Thu, 30 Oct 2025 23:54:29 GMT  
		Size: 1.5 MB (1450037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66f1caeb7e84826796a497d9ceb42d9b8215b3a835f80f501735abb6593db75`  
		Last Modified: Fri, 31 Oct 2025 00:13:35 GMT  
		Size: 135.5 MB (135541117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a2369775533820ede1eeec13c77ae3a266a309f75ee83c988089a7eca7c33a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278df6763c94c8f54a8fdbb6cf5eb4dce1f3641cb191ab9b653f3f144a18e90f`

```dockerfile
```

-	Layers:
	-	`sha256:27ec4d7fe72becf8a657243b904b69fe3150dd43b252e3fa8c3409432843500d`  
		Last Modified: Fri, 31 Oct 2025 02:01:22 GMT  
		Size: 2.2 MB (2174120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a331f03acd81fef92e3dbadf53055d06a2b0cd0320771f49bc1f1638546ad08`  
		Last Modified: Fri, 31 Oct 2025 02:01:23 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:3bdc096d00b43ee375f771ddf8382fc010fd4fc8e873a8096f78a2b1dce1319a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172469934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000af13ae5df4a394508dafe3a26314fb33d51a14037a30e3ea4424cb38ef4c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:46:30 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 31 Oct 2025 00:46:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 00:46:30 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 31 Oct 2025 00:46:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 31 Oct 2025 00:46:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b2c2c5b1d0021029ccc4064df99950687160117bc008ac4bce5618b2dd9154`  
		Last Modified: Fri, 31 Oct 2025 00:47:22 GMT  
		Size: 1.5 MB (1536224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71758d1bf4a4ec11b0b439b7f4e5df0559ccc7ccaa49ca2ddd38186a648e5466`  
		Last Modified: Fri, 31 Oct 2025 02:39:40 GMT  
		Size: 136.5 MB (136486921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f7f58ba8e6db30e04f70800f9745145e1b8ab061c5badb42bec165fecc8a0849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31c09046cdceea920dd3d6fb29033aeec73e1eacfe6aa7776746e14c5338de`

```dockerfile
```

-	Layers:
	-	`sha256:651509291e87e154de2ae15dfa5e4f3d40b53235f1da9c04291f433f93561025`  
		Last Modified: Fri, 31 Oct 2025 02:01:27 GMT  
		Size: 2.2 MB (2177410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b52fa9c2734a9af5e2bb6d8c82230cc493c1f002e93252e8a5d8dc87651f493`  
		Last Modified: Fri, 31 Oct 2025 02:01:28 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:539e0eec1fedfbe195248cfca5699ebdd39e5be1be1e60c9b05dcb856c5f9faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162409745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2cef6ec69c443e0ba1ae20ec3dd153f5046003dc1865f14aada334707e80f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 22:32:22 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 30 Oct 2025 22:32:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 22:32:22 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 30 Oct 2025 22:32:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 30 Oct 2025 22:32:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a741b67c0dbf6d2e66e6ffe23e30ec9031bce057ebe9e2cb812bbb79480aa2d`  
		Last Modified: Thu, 30 Oct 2025 22:33:02 GMT  
		Size: 1.5 MB (1455880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a84a4d22587d870899aa47dbf78b8c505bacb62aff4ef27f67a3e726f2d3aa`  
		Last Modified: Fri, 31 Oct 2025 02:26:34 GMT  
		Size: 133.0 MB (132950452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:89cb92fc23175599d4a8ccbbef62c70035399c6696096c9667f7c94b352bc38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7166dcfded9bd2dbc67107d2dbfd88142462854ac30380c7a7d399c84e123a0`

```dockerfile
```

-	Layers:
	-	`sha256:72795cb0080107c7c62243efa21eb49b513b5b29ef82e8a3f49e3ab4705f7b7a`  
		Last Modified: Fri, 31 Oct 2025 00:21:22 GMT  
		Size: 2.2 MB (2174081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0af962c72d8bee56ac5893233e45de253d3edda399f86cb127c4bc73e9068800`  
		Last Modified: Fri, 31 Oct 2025 00:21:24 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json
