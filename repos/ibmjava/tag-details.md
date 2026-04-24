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
$ docker pull ibmjava@sha256:651980e2d1fe409d28b15b45323bfb1ca7ea5f97daa4d322e8b854de2ba3a1c8
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
$ docker pull ibmjava@sha256:340b0090627884f4a5276c27350d741ab83dc7b8000466c375df33fc1a77a433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167420303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fa9ee32ed49f4062c6953b6b2e658b685db5a24277134ac64da4c59423db8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:54 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:27:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:27:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd87c806116a3327741f8989fb20f94e5b7e156ca698501e1e0b0514c15176cc`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878328ea0ba0a45102b59e8522909701c56daf777fb1204159b1ca3caa8fc60e`  
		Last Modified: Fri, 24 Apr 2026 17:27:52 GMT  
		Size: 136.2 MB (136233737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ed58169ea93ee8fe0f275a63d5bde4614d114a02134a20bfa737617e9edc91d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47846e80dce9901543fb6d52795875dfe7c508067b41aaccc697f57d11866cf`

```dockerfile
```

-	Layers:
	-	`sha256:b5f3e27cb7c81ef1412ab2d56029fbea2f0d2fa54889161cd4b9d4b3dbed2e33`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b389c09cae44fb089b9f17d90586f89284a7a440afc09f2d8a221aaebca912a3`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:60dae3b0a022378e3baa297d9bad3a9b4db9d5f8133939ecf843089198cc63ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173334378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c638b2f03ca371a7eb320ffb9608d7694643db2f4adcd11c1fcccd0785dc7b0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:26:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:26:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cb20336fdd807d5eb118e9f46bf10d1be4c8f6c65d63dab7ffea533b4e49b6`  
		Last Modified: Fri, 24 Apr 2026 17:26:46 GMT  
		Size: 137.1 MB (137149796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4a294ea82ff396dfce45966cea0ece1312ec4ad607c1c69526480b4a076f0f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d09d91aedb63d4023458ab4fdfa178290a18a60b060506402b9643045e485c`

```dockerfile
```

-	Layers:
	-	`sha256:4d835488e19183223c297298362c94b17f293e448bb991149c7c6c4649d9ee32`  
		Last Modified: Fri, 24 Apr 2026 17:26:42 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6784fa7c4b56c95ce0389902f22286c926c8f0bf2164ddca2110a810d16a4f4`  
		Last Modified: Fri, 24 Apr 2026 17:26:41 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:9b9ee11bc6c4fadcd57bbbfd53366edb6e260546c309549719e1af6e7d8a57f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164278947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c8dcde081d4c54cc9843f8fa1faeec3c1220a674ff820bf2dcb242181a53f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:43 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a9e5555a5ddb3d1f5fa6bd9012ab52c8310c1a58ba719057c7f5485b1c7428`  
		Last Modified: Fri, 24 Apr 2026 17:31:07 GMT  
		Size: 1.5 MB (1455956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a00fabe9237f71da51910a55fc0a18f318d99767ece360367101320254dade`  
		Last Modified: Fri, 24 Apr 2026 17:31:21 GMT  
		Size: 134.6 MB (134620692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2e3b6c0a79815b8029f3c91032eff0a71a077e50e59eabe52ddef43cc40030a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb48d29a3e4df86572eb849cf461c65cea9b98a8e2840b3c17a792a93b28f85a`

```dockerfile
```

-	Layers:
	-	`sha256:d48e10f8ceaa466569fc23d26c4930d7fda7e912e50ffd153b819ca47b8742f1`  
		Last Modified: Fri, 24 Apr 2026 17:31:07 GMT  
		Size: 2.2 MB (2174063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e2422b331efa3edd8c0b1aeb684b7a15bfe80af7997e5cdee3ebac76856665`  
		Last Modified: Fri, 24 Apr 2026 17:31:03 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:651980e2d1fe409d28b15b45323bfb1ca7ea5f97daa4d322e8b854de2ba3a1c8
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
$ docker pull ibmjava@sha256:340b0090627884f4a5276c27350d741ab83dc7b8000466c375df33fc1a77a433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167420303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fa9ee32ed49f4062c6953b6b2e658b685db5a24277134ac64da4c59423db8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:54 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:27:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:27:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd87c806116a3327741f8989fb20f94e5b7e156ca698501e1e0b0514c15176cc`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878328ea0ba0a45102b59e8522909701c56daf777fb1204159b1ca3caa8fc60e`  
		Last Modified: Fri, 24 Apr 2026 17:27:52 GMT  
		Size: 136.2 MB (136233737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ed58169ea93ee8fe0f275a63d5bde4614d114a02134a20bfa737617e9edc91d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47846e80dce9901543fb6d52795875dfe7c508067b41aaccc697f57d11866cf`

```dockerfile
```

-	Layers:
	-	`sha256:b5f3e27cb7c81ef1412ab2d56029fbea2f0d2fa54889161cd4b9d4b3dbed2e33`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b389c09cae44fb089b9f17d90586f89284a7a440afc09f2d8a221aaebca912a3`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:60dae3b0a022378e3baa297d9bad3a9b4db9d5f8133939ecf843089198cc63ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173334378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c638b2f03ca371a7eb320ffb9608d7694643db2f4adcd11c1fcccd0785dc7b0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:26:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:26:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cb20336fdd807d5eb118e9f46bf10d1be4c8f6c65d63dab7ffea533b4e49b6`  
		Last Modified: Fri, 24 Apr 2026 17:26:46 GMT  
		Size: 137.1 MB (137149796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4a294ea82ff396dfce45966cea0ece1312ec4ad607c1c69526480b4a076f0f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d09d91aedb63d4023458ab4fdfa178290a18a60b060506402b9643045e485c`

```dockerfile
```

-	Layers:
	-	`sha256:4d835488e19183223c297298362c94b17f293e448bb991149c7c6c4649d9ee32`  
		Last Modified: Fri, 24 Apr 2026 17:26:42 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6784fa7c4b56c95ce0389902f22286c926c8f0bf2164ddca2110a810d16a4f4`  
		Last Modified: Fri, 24 Apr 2026 17:26:41 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:9b9ee11bc6c4fadcd57bbbfd53366edb6e260546c309549719e1af6e7d8a57f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164278947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c8dcde081d4c54cc9843f8fa1faeec3c1220a674ff820bf2dcb242181a53f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:43 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a9e5555a5ddb3d1f5fa6bd9012ab52c8310c1a58ba719057c7f5485b1c7428`  
		Last Modified: Fri, 24 Apr 2026 17:31:07 GMT  
		Size: 1.5 MB (1455956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a00fabe9237f71da51910a55fc0a18f318d99767ece360367101320254dade`  
		Last Modified: Fri, 24 Apr 2026 17:31:21 GMT  
		Size: 134.6 MB (134620692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2e3b6c0a79815b8029f3c91032eff0a71a077e50e59eabe52ddef43cc40030a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb48d29a3e4df86572eb849cf461c65cea9b98a8e2840b3c17a792a93b28f85a`

```dockerfile
```

-	Layers:
	-	`sha256:d48e10f8ceaa466569fc23d26c4930d7fda7e912e50ffd153b819ca47b8742f1`  
		Last Modified: Fri, 24 Apr 2026 17:31:07 GMT  
		Size: 2.2 MB (2174063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e2422b331efa3edd8c0b1aeb684b7a15bfe80af7997e5cdee3ebac76856665`  
		Last Modified: Fri, 24 Apr 2026 17:31:03 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:1404efae6d95a96688dc58afb47a2afa95242b2baf730de74dd688e5f53cb121
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
$ docker pull ibmjava@sha256:9b1161b5997708d69456ffefe711060b0685003a718a5959d5b85375da5cc061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204707915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79996c84f0736757f63244b16fd497c36881d752b0e18dd2453d9120c9a53e1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:54 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:50 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd87c806116a3327741f8989fb20f94e5b7e156ca698501e1e0b0514c15176cc`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da11bf882625bc0731870fe51d67be8846835897063fdf7fbe2617b1a03e93`  
		Last Modified: Fri, 24 Apr 2026 17:29:10 GMT  
		Size: 173.5 MB (173521349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:45700dc05c34a9716c88c91d29db5679f43e8ff656dc81407744ab39c28171a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1976f38d39862ae8eb753f1f592043f3f45cbd6a3c73acee46f5e07f3831dfa2`

```dockerfile
```

-	Layers:
	-	`sha256:4685c695f7b699126f04c0133c6f05db0c8092762b2599d18d9fbdc415dc41aa`  
		Last Modified: Fri, 24 Apr 2026 17:29:06 GMT  
		Size: 3.1 MB (3085059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1d4c19363db2ec5c457921a18518fdc1b0c704368555bde399a36f22a8226a`  
		Last Modified: Fri, 24 Apr 2026 17:29:06 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:3cd62e59e8ac469bec05bbd31d2586260abfb38968b00020cb63727009b5bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210829577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244f1472f52f0660860e5c83bd857c6d650fdc27d9e85977c41aefb8a84ce5ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:27:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:27:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2132eaca12df4dc2a7b0af262a8068d86a7122d98ccc02571ca194fca2fb9e83`  
		Last Modified: Fri, 24 Apr 2026 17:28:02 GMT  
		Size: 174.6 MB (174644995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:648e9b3bb1e063fc9a77657904e3c3679a9af72a63a02eafad60f4e5b60c4a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513215ed1fe85c669bbbca9beb60df20ac0b233725aa806169610f5562009769`

```dockerfile
```

-	Layers:
	-	`sha256:fe2c542a9494fcebe3022bc6fb0348723ce899268dc778b1bc2eaa7523295b0b`  
		Last Modified: Fri, 24 Apr 2026 17:27:59 GMT  
		Size: 3.1 MB (3071008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31851a69dcf03f352b961db6065aa6700bdb371137b792bfc5e4650826622af6`  
		Last Modified: Fri, 24 Apr 2026 17:27:58 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:6bde71d20c9b03076df1700c452f830b1bc451f8fc04f363d94e177deedd3189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194827646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e38a8d9e206d1097635fb25f299c08692f008d8683b22a26a0a609814d26c9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:59:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:17 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:50 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a94005458eecbf59d36fdcb472759320381954eb3b9e0a8ea9c1e920dc2a0`  
		Last Modified: Wed, 15 Apr 2026 21:00:37 GMT  
		Size: 1.5 MB (1455873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d965b2264e89cbb2ca1fd752191cb709cc08ea307b3d630dd92092bcc30f153b`  
		Last Modified: Fri, 24 Apr 2026 17:30:11 GMT  
		Size: 165.2 MB (165169474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:666ff2484eff1711ff3f4ff50ee0f8d8a28b6a47b9fac3c9279dea5db248d931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6eb9845959b3fa0d5c2070645a6cca71486ee13fe72ea94165d45a60540bac`

```dockerfile
```

-	Layers:
	-	`sha256:5ef4874ad01ae0cb3663f01a0ca21317c72acf77f59b8e0513f712d5a59b4214`  
		Last Modified: Fri, 24 Apr 2026 17:29:56 GMT  
		Size: 2.8 MB (2758361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e21a593ba4aa71089bc08fb484ed9d46aa64d44ad80fb00e6c327dc3be099a`  
		Last Modified: Fri, 24 Apr 2026 17:29:53 GMT  
		Size: 12.6 KB (12597 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:0dbb057ba5a16072c4c2362b8a473d4a01ebbcaae9db2155934809a114a87203
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
$ docker pull ibmjava@sha256:1678f4ebcdbe99b0c21541643b7986ccdd88e288064ca2392afafe8ecd83775d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102358232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b6bca4b98100a69ef9d612febfa73225e1936f33ada229c8baee7d5a563d95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:27:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:27:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:27:55 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a0d80514b8219bde29705f38ed9b2738489539c787898f6f7c506254c1a958`  
		Last Modified: Fri, 24 Apr 2026 17:28:34 GMT  
		Size: 1.5 MB (1450085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf1299181d5f5c89288edc76bc3524391830db8eeb6d97afb0e960842e1bb36`  
		Last Modified: Fri, 24 Apr 2026 17:28:38 GMT  
		Size: 71.2 MB (71171649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e43d9e3a487f9af90d640bc304f1e05b6f058c0fa32045ec013db4ca729c589d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f915df40306b5a30c4a12cabbfb4741179c525f583a3573c7ef50ff8ba7c0dd3`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f91ccbdb31be34553b4d3ba5467547f4b51ba453da425dfb2bdf38fd1e5b9`  
		Last Modified: Fri, 24 Apr 2026 17:28:34 GMT  
		Size: 2.2 MB (2156549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3d8752b7ecfb858c84437b30a56ca1ab6d731a0ffe7546e8ad0f72b4e16184`  
		Last Modified: Fri, 24 Apr 2026 17:28:34 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:72b1f13a06250a12ff8eec92056f932358070d8bc51f36eaa02eac2eed527c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108299917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8378fdaebd67b0d5baf6e0108d794f3e98c5ef645019c0ac9eb4581bae769b5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:25:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:25:55 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb02b7620f1c9a312232aae8d2b12e460397a04548ba64d41301281d6ccd3d1`  
		Last Modified: Fri, 24 Apr 2026 17:26:21 GMT  
		Size: 72.1 MB (72115335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0b1c4089116e98b80594155afa0e01110bd351fc166d4a717ce3d90e62a9acbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16b373f284321e73f50454fe1f5859551ce0ea4e4e8beed53047dd06bc2b591`

```dockerfile
```

-	Layers:
	-	`sha256:1f152ea86f4edd743f02e6484c10b34f789a2e4a1d83f66cc5711cc064962d0a`  
		Last Modified: Fri, 24 Apr 2026 17:26:19 GMT  
		Size: 2.2 MB (2161050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f7c70c427b34e9a67b6ec46f9e0848a9facacb75ba0332c9e9ac3a673f8125`  
		Last Modified: Fri, 24 Apr 2026 17:26:19 GMT  
		Size: 12.6 KB (12634 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:016a4fae381bd1666202808d37d16c2168c1ae91e4e2998a5c6451ef05f79a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102890298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ed624af855a75673af5df09a0e59cbb5c909fb41c9616bdb2e301d348987c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:59:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:17 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:26:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:26:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a94005458eecbf59d36fdcb472759320381954eb3b9e0a8ea9c1e920dc2a0`  
		Last Modified: Wed, 15 Apr 2026 21:00:37 GMT  
		Size: 1.5 MB (1455873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb1befb7a4f3a44bb6b445ca487f754e3d05dcea256b474aef455a0abfc2535`  
		Last Modified: Fri, 24 Apr 2026 17:29:12 GMT  
		Size: 73.2 MB (73232126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:724200d1cf109c31a8f7b3a100827a2d30468a9575c2e6946814797c90c2d246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71ec594cbde2b248bb2eca2da15e95be8b49b6bbc0d3601c072634bad0dbc8d`

```dockerfile
```

-	Layers:
	-	`sha256:4bbb3b6725faf8ef76c5fc348e8fd02a7bf2d8cce61b96c96db55ae9789a36cf`  
		Last Modified: Fri, 24 Apr 2026 17:28:53 GMT  
		Size: 2.2 MB (2160171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ceb848da9744c4e5dab51fd313bc648d16c13086f11010f0791ef38da761810`  
		Last Modified: Fri, 24 Apr 2026 17:28:52 GMT  
		Size: 12.6 KB (12600 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:651980e2d1fe409d28b15b45323bfb1ca7ea5f97daa4d322e8b854de2ba3a1c8
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
$ docker pull ibmjava@sha256:340b0090627884f4a5276c27350d741ab83dc7b8000466c375df33fc1a77a433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167420303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fa9ee32ed49f4062c6953b6b2e658b685db5a24277134ac64da4c59423db8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:54 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:27:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:27:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd87c806116a3327741f8989fb20f94e5b7e156ca698501e1e0b0514c15176cc`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878328ea0ba0a45102b59e8522909701c56daf777fb1204159b1ca3caa8fc60e`  
		Last Modified: Fri, 24 Apr 2026 17:27:52 GMT  
		Size: 136.2 MB (136233737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ed58169ea93ee8fe0f275a63d5bde4614d114a02134a20bfa737617e9edc91d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47846e80dce9901543fb6d52795875dfe7c508067b41aaccc697f57d11866cf`

```dockerfile
```

-	Layers:
	-	`sha256:b5f3e27cb7c81ef1412ab2d56029fbea2f0d2fa54889161cd4b9d4b3dbed2e33`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b389c09cae44fb089b9f17d90586f89284a7a440afc09f2d8a221aaebca912a3`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:60dae3b0a022378e3baa297d9bad3a9b4db9d5f8133939ecf843089198cc63ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173334378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c638b2f03ca371a7eb320ffb9608d7694643db2f4adcd11c1fcccd0785dc7b0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:26:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:26:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cb20336fdd807d5eb118e9f46bf10d1be4c8f6c65d63dab7ffea533b4e49b6`  
		Last Modified: Fri, 24 Apr 2026 17:26:46 GMT  
		Size: 137.1 MB (137149796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4a294ea82ff396dfce45966cea0ece1312ec4ad607c1c69526480b4a076f0f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d09d91aedb63d4023458ab4fdfa178290a18a60b060506402b9643045e485c`

```dockerfile
```

-	Layers:
	-	`sha256:4d835488e19183223c297298362c94b17f293e448bb991149c7c6c4649d9ee32`  
		Last Modified: Fri, 24 Apr 2026 17:26:42 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6784fa7c4b56c95ce0389902f22286c926c8f0bf2164ddca2110a810d16a4f4`  
		Last Modified: Fri, 24 Apr 2026 17:26:41 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:9b9ee11bc6c4fadcd57bbbfd53366edb6e260546c309549719e1af6e7d8a57f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164278947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c8dcde081d4c54cc9843f8fa1faeec3c1220a674ff820bf2dcb242181a53f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:43 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a9e5555a5ddb3d1f5fa6bd9012ab52c8310c1a58ba719057c7f5485b1c7428`  
		Last Modified: Fri, 24 Apr 2026 17:31:07 GMT  
		Size: 1.5 MB (1455956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a00fabe9237f71da51910a55fc0a18f318d99767ece360367101320254dade`  
		Last Modified: Fri, 24 Apr 2026 17:31:21 GMT  
		Size: 134.6 MB (134620692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2e3b6c0a79815b8029f3c91032eff0a71a077e50e59eabe52ddef43cc40030a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb48d29a3e4df86572eb849cf461c65cea9b98a8e2840b3c17a792a93b28f85a`

```dockerfile
```

-	Layers:
	-	`sha256:d48e10f8ceaa466569fc23d26c4930d7fda7e912e50ffd153b819ca47b8742f1`  
		Last Modified: Fri, 24 Apr 2026 17:31:07 GMT  
		Size: 2.2 MB (2174063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e2422b331efa3edd8c0b1aeb684b7a15bfe80af7997e5cdee3ebac76856665`  
		Last Modified: Fri, 24 Apr 2026 17:31:03 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:651980e2d1fe409d28b15b45323bfb1ca7ea5f97daa4d322e8b854de2ba3a1c8
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
$ docker pull ibmjava@sha256:340b0090627884f4a5276c27350d741ab83dc7b8000466c375df33fc1a77a433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167420303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fa9ee32ed49f4062c6953b6b2e658b685db5a24277134ac64da4c59423db8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:54 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:27:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:27:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd87c806116a3327741f8989fb20f94e5b7e156ca698501e1e0b0514c15176cc`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878328ea0ba0a45102b59e8522909701c56daf777fb1204159b1ca3caa8fc60e`  
		Last Modified: Fri, 24 Apr 2026 17:27:52 GMT  
		Size: 136.2 MB (136233737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ed58169ea93ee8fe0f275a63d5bde4614d114a02134a20bfa737617e9edc91d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47846e80dce9901543fb6d52795875dfe7c508067b41aaccc697f57d11866cf`

```dockerfile
```

-	Layers:
	-	`sha256:b5f3e27cb7c81ef1412ab2d56029fbea2f0d2fa54889161cd4b9d4b3dbed2e33`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b389c09cae44fb089b9f17d90586f89284a7a440afc09f2d8a221aaebca912a3`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:60dae3b0a022378e3baa297d9bad3a9b4db9d5f8133939ecf843089198cc63ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173334378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c638b2f03ca371a7eb320ffb9608d7694643db2f4adcd11c1fcccd0785dc7b0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:26:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:26:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cb20336fdd807d5eb118e9f46bf10d1be4c8f6c65d63dab7ffea533b4e49b6`  
		Last Modified: Fri, 24 Apr 2026 17:26:46 GMT  
		Size: 137.1 MB (137149796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4a294ea82ff396dfce45966cea0ece1312ec4ad607c1c69526480b4a076f0f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d09d91aedb63d4023458ab4fdfa178290a18a60b060506402b9643045e485c`

```dockerfile
```

-	Layers:
	-	`sha256:4d835488e19183223c297298362c94b17f293e448bb991149c7c6c4649d9ee32`  
		Last Modified: Fri, 24 Apr 2026 17:26:42 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6784fa7c4b56c95ce0389902f22286c926c8f0bf2164ddca2110a810d16a4f4`  
		Last Modified: Fri, 24 Apr 2026 17:26:41 GMT  
		Size: 13.2 KB (13238 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:9b9ee11bc6c4fadcd57bbbfd53366edb6e260546c309549719e1af6e7d8a57f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164278947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c8dcde081d4c54cc9843f8fa1faeec3c1220a674ff820bf2dcb242181a53f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:43 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a9e5555a5ddb3d1f5fa6bd9012ab52c8310c1a58ba719057c7f5485b1c7428`  
		Last Modified: Fri, 24 Apr 2026 17:31:07 GMT  
		Size: 1.5 MB (1455956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a00fabe9237f71da51910a55fc0a18f318d99767ece360367101320254dade`  
		Last Modified: Fri, 24 Apr 2026 17:31:21 GMT  
		Size: 134.6 MB (134620692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2e3b6c0a79815b8029f3c91032eff0a71a077e50e59eabe52ddef43cc40030a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb48d29a3e4df86572eb849cf461c65cea9b98a8e2840b3c17a792a93b28f85a`

```dockerfile
```

-	Layers:
	-	`sha256:d48e10f8ceaa466569fc23d26c4930d7fda7e912e50ffd153b819ca47b8742f1`  
		Last Modified: Fri, 24 Apr 2026 17:31:07 GMT  
		Size: 2.2 MB (2174063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e2422b331efa3edd8c0b1aeb684b7a15bfe80af7997e5cdee3ebac76856665`  
		Last Modified: Fri, 24 Apr 2026 17:31:03 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:1404efae6d95a96688dc58afb47a2afa95242b2baf730de74dd688e5f53cb121
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
$ docker pull ibmjava@sha256:9b1161b5997708d69456ffefe711060b0685003a718a5959d5b85375da5cc061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204707915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79996c84f0736757f63244b16fd497c36881d752b0e18dd2453d9120c9a53e1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:54 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:50 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd87c806116a3327741f8989fb20f94e5b7e156ca698501e1e0b0514c15176cc`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da11bf882625bc0731870fe51d67be8846835897063fdf7fbe2617b1a03e93`  
		Last Modified: Fri, 24 Apr 2026 17:29:10 GMT  
		Size: 173.5 MB (173521349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:45700dc05c34a9716c88c91d29db5679f43e8ff656dc81407744ab39c28171a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1976f38d39862ae8eb753f1f592043f3f45cbd6a3c73acee46f5e07f3831dfa2`

```dockerfile
```

-	Layers:
	-	`sha256:4685c695f7b699126f04c0133c6f05db0c8092762b2599d18d9fbdc415dc41aa`  
		Last Modified: Fri, 24 Apr 2026 17:29:06 GMT  
		Size: 3.1 MB (3085059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1d4c19363db2ec5c457921a18518fdc1b0c704368555bde399a36f22a8226a`  
		Last Modified: Fri, 24 Apr 2026 17:29:06 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:3cd62e59e8ac469bec05bbd31d2586260abfb38968b00020cb63727009b5bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210829577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244f1472f52f0660860e5c83bd857c6d650fdc27d9e85977c41aefb8a84ce5ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:27:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:27:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2132eaca12df4dc2a7b0af262a8068d86a7122d98ccc02571ca194fca2fb9e83`  
		Last Modified: Fri, 24 Apr 2026 17:28:02 GMT  
		Size: 174.6 MB (174644995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:648e9b3bb1e063fc9a77657904e3c3679a9af72a63a02eafad60f4e5b60c4a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513215ed1fe85c669bbbca9beb60df20ac0b233725aa806169610f5562009769`

```dockerfile
```

-	Layers:
	-	`sha256:fe2c542a9494fcebe3022bc6fb0348723ce899268dc778b1bc2eaa7523295b0b`  
		Last Modified: Fri, 24 Apr 2026 17:27:59 GMT  
		Size: 3.1 MB (3071008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31851a69dcf03f352b961db6065aa6700bdb371137b792bfc5e4650826622af6`  
		Last Modified: Fri, 24 Apr 2026 17:27:58 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:6bde71d20c9b03076df1700c452f830b1bc451f8fc04f363d94e177deedd3189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194827646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e38a8d9e206d1097635fb25f299c08692f008d8683b22a26a0a609814d26c9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:59:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:17 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:50 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a94005458eecbf59d36fdcb472759320381954eb3b9e0a8ea9c1e920dc2a0`  
		Last Modified: Wed, 15 Apr 2026 21:00:37 GMT  
		Size: 1.5 MB (1455873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d965b2264e89cbb2ca1fd752191cb709cc08ea307b3d630dd92092bcc30f153b`  
		Last Modified: Fri, 24 Apr 2026 17:30:11 GMT  
		Size: 165.2 MB (165169474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:666ff2484eff1711ff3f4ff50ee0f8d8a28b6a47b9fac3c9279dea5db248d931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6eb9845959b3fa0d5c2070645a6cca71486ee13fe72ea94165d45a60540bac`

```dockerfile
```

-	Layers:
	-	`sha256:5ef4874ad01ae0cb3663f01a0ca21317c72acf77f59b8e0513f712d5a59b4214`  
		Last Modified: Fri, 24 Apr 2026 17:29:56 GMT  
		Size: 2.8 MB (2758361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e21a593ba4aa71089bc08fb484ed9d46aa64d44ad80fb00e6c327dc3be099a`  
		Last Modified: Fri, 24 Apr 2026 17:29:53 GMT  
		Size: 12.6 KB (12597 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:0dbb057ba5a16072c4c2362b8a473d4a01ebbcaae9db2155934809a114a87203
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
$ docker pull ibmjava@sha256:1678f4ebcdbe99b0c21541643b7986ccdd88e288064ca2392afafe8ecd83775d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102358232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b6bca4b98100a69ef9d612febfa73225e1936f33ada229c8baee7d5a563d95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:27:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:27:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:27:55 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a0d80514b8219bde29705f38ed9b2738489539c787898f6f7c506254c1a958`  
		Last Modified: Fri, 24 Apr 2026 17:28:34 GMT  
		Size: 1.5 MB (1450085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf1299181d5f5c89288edc76bc3524391830db8eeb6d97afb0e960842e1bb36`  
		Last Modified: Fri, 24 Apr 2026 17:28:38 GMT  
		Size: 71.2 MB (71171649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e43d9e3a487f9af90d640bc304f1e05b6f058c0fa32045ec013db4ca729c589d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f915df40306b5a30c4a12cabbfb4741179c525f583a3573c7ef50ff8ba7c0dd3`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f91ccbdb31be34553b4d3ba5467547f4b51ba453da425dfb2bdf38fd1e5b9`  
		Last Modified: Fri, 24 Apr 2026 17:28:34 GMT  
		Size: 2.2 MB (2156549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3d8752b7ecfb858c84437b30a56ca1ab6d731a0ffe7546e8ad0f72b4e16184`  
		Last Modified: Fri, 24 Apr 2026 17:28:34 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:72b1f13a06250a12ff8eec92056f932358070d8bc51f36eaa02eac2eed527c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108299917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8378fdaebd67b0d5baf6e0108d794f3e98c5ef645019c0ac9eb4581bae769b5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:25:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:25:55 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb02b7620f1c9a312232aae8d2b12e460397a04548ba64d41301281d6ccd3d1`  
		Last Modified: Fri, 24 Apr 2026 17:26:21 GMT  
		Size: 72.1 MB (72115335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0b1c4089116e98b80594155afa0e01110bd351fc166d4a717ce3d90e62a9acbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16b373f284321e73f50454fe1f5859551ce0ea4e4e8beed53047dd06bc2b591`

```dockerfile
```

-	Layers:
	-	`sha256:1f152ea86f4edd743f02e6484c10b34f789a2e4a1d83f66cc5711cc064962d0a`  
		Last Modified: Fri, 24 Apr 2026 17:26:19 GMT  
		Size: 2.2 MB (2161050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f7c70c427b34e9a67b6ec46f9e0848a9facacb75ba0332c9e9ac3a673f8125`  
		Last Modified: Fri, 24 Apr 2026 17:26:19 GMT  
		Size: 12.6 KB (12634 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:016a4fae381bd1666202808d37d16c2168c1ae91e4e2998a5c6451ef05f79a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102890298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ed624af855a75673af5df09a0e59cbb5c909fb41c9616bdb2e301d348987c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:59:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:17 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:26:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:26:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a94005458eecbf59d36fdcb472759320381954eb3b9e0a8ea9c1e920dc2a0`  
		Last Modified: Wed, 15 Apr 2026 21:00:37 GMT  
		Size: 1.5 MB (1455873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb1befb7a4f3a44bb6b445ca487f754e3d05dcea256b474aef455a0abfc2535`  
		Last Modified: Fri, 24 Apr 2026 17:29:12 GMT  
		Size: 73.2 MB (73232126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:724200d1cf109c31a8f7b3a100827a2d30468a9575c2e6946814797c90c2d246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71ec594cbde2b248bb2eca2da15e95be8b49b6bbc0d3601c072634bad0dbc8d`

```dockerfile
```

-	Layers:
	-	`sha256:4bbb3b6725faf8ef76c5fc348e8fd02a7bf2d8cce61b96c96db55ae9789a36cf`  
		Last Modified: Fri, 24 Apr 2026 17:28:53 GMT  
		Size: 2.2 MB (2160171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ceb848da9744c4e5dab51fd313bc648d16c13086f11010f0791ef38da761810`  
		Last Modified: Fri, 24 Apr 2026 17:28:52 GMT  
		Size: 12.6 KB (12600 bytes)  
		MIME: application/vnd.in-toto+json
