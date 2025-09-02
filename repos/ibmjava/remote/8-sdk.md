## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:3d5169eba2ed944b6a91f726e4925ea1afc59f57cfedb66b9a327d39d1901718
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
$ docker pull ibmjava@sha256:bdd1b055170b360e7f8649b823e0a8ff862c4e99d1ee068b0363b7a08a1adbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203659481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34ce942f311e6b5994347dd6e4eee0daec3e50c645839ec51b373fd9d711a02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Aug 2025 06:32:13 GMT
ARG RELEASE
# Tue, 05 Aug 2025 06:32:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Aug 2025 06:32:13 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 05 Aug 2025 06:32:13 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4925416b3fb5d495f6e16de06049a93d55c4ffcd482f3769be69cd528bce2a`  
		Last Modified: Tue, 02 Sep 2025 00:30:01 GMT  
		Size: 1.4 MB (1449997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966e6ffb26b3bd7bf9da02dadbea4e2548a48c8e55284d07eed977269d9847d`  
		Last Modified: Tue, 02 Sep 2025 02:16:40 GMT  
		Size: 172.7 MB (172672549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2159ce2ea36b1faebcae485d911892b0f00b3d8d55c2fd6c6ab7729fe8b861d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920e22e8b795cda192cfd7d3c93a45592d2c15150a143d3cd001ac4cbd93bdb8`

```dockerfile
```

-	Layers:
	-	`sha256:e06c610f86cd3a9f44fb9bbca8cdf54b27220472b35df83e9124d5218607a9d3`  
		Last Modified: Tue, 02 Sep 2025 02:01:35 GMT  
		Size: 3.1 MB (3083862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdbcb287d4d614d45d719c0e0ab5d2b68c051ac27e3d05ccb3d4c0177d26e24`  
		Last Modified: Tue, 02 Sep 2025 02:01:36 GMT  
		Size: 12.6 KB (12641 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1e86e6da9c3d0628c22a79554382f4046073124f8bc7a8bd37572f5c98a1176f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209795573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a7ffdd882315282737991187aa858b558e300b102463d8953f6664a52b688c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a1e9cd76df11cf884d2a1f9ade58772e0f6f878920b9ef002ff05b94bbbe60`  
		Last Modified: Tue, 12 Aug 2025 20:15:54 GMT  
		Size: 173.8 MB (173816259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a98532efc4d173d65a1b144acf49feaf5991d98f2df96e836dc399cc91180c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d8d29c3b9b6e350f085e580acd5348080b29cb99f860b2f27d383dbbfbd2c2`

```dockerfile
```

-	Layers:
	-	`sha256:8b9486f4423ba6c45e98c9d03eb847f33fd7a952a09f4902f2da744e989b73ff`  
		Last Modified: Tue, 12 Aug 2025 20:01:41 GMT  
		Size: 3.1 MB (3069795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f3c0c3c64f6f94b6a5f23f3feedfb4cc76a07070d2f419acb73753beaa32b2`  
		Last Modified: Tue, 12 Aug 2025 20:01:43 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:eac2eb64c9519846f4e2aa976c89b9ebfc152d15e05b17c7e7e91e507cfa8b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192089413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae4c04bbb7eaee743d1919fef6e25b366d4a1d29323e698c1ba43efa278852a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Aug 2025 06:32:13 GMT
ARG RELEASE
# Tue, 05 Aug 2025 06:32:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Aug 2025 06:32:13 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 05 Aug 2025 06:32:13 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bf2d3d267a3b9732481174fcba7d138507ff103bf415dc927e0315a8dba6ad`  
		Last Modified: Mon, 01 Sep 2025 23:52:51 GMT  
		Size: 1.5 MB (1455714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf75f4285bceea437dd2508c5cdd620dbfdb7dc3b7bf472e76865541425d1baa`  
		Last Modified: Tue, 02 Sep 2025 00:12:49 GMT  
		Size: 162.6 MB (162630031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c3b640300db1267ad64d8a7d6a614aed0f9fd0b29d2c5efd44af671488fca2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2769817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a592085325f58a777344244d0b1fd646e4b236d1db387ff4f37366d78fcaff4`

```dockerfile
```

-	Layers:
	-	`sha256:9ad71dc9cb160f54ee15536b3119a8db88bc03f8b6dfaa9bcfac97d5562b6071`  
		Last Modified: Tue, 02 Sep 2025 02:01:43 GMT  
		Size: 2.8 MB (2757178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a5eac4e7c10732a4f27a5a6e3cdfb70dd73bf0b9523cfc83ece96cf40590af`  
		Last Modified: Tue, 02 Sep 2025 02:01:44 GMT  
		Size: 12.6 KB (12639 bytes)  
		MIME: application/vnd.in-toto+json
