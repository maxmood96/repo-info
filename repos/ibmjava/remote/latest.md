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
