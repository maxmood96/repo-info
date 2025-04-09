## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:6838e6fb273dd40716338db2c106e09b2015097dd678fd388727e5e49a6e51cb
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
$ docker pull ibmjava@sha256:d6a7265a5c1dddceb25a6ae417fa0c8555506d1669e2f468b2410c03867178e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203889890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ce5a0f7586a8bf116f8960f585c666af55405a55ee8f405b1f44dc737409fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Feb 2025 09:27:08 GMT
ARG RELEASE
# Fri, 14 Feb 2025 09:27:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Feb 2025 09:27:08 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Fri, 14 Feb 2025 09:27:08 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e160359d8ef9f6b95400b0f6946e1ad5590c998300f10ac80576e68a624f5ee`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 1.5 MB (1450037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03d8575c7c900c1ac40fc6b6d512946ce651e0fb3883564d887013f164d0186`  
		Last Modified: Wed, 09 Apr 2025 01:18:55 GMT  
		Size: 172.9 MB (172907488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:422ad9740ca1f51d146a57c52f7bcda727b4a30b255371ad1b49979cc39a39fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d264201ed5c558a7f17952d06e543a75450e0695ffc3af936214b28b3d9f1289`

```dockerfile
```

-	Layers:
	-	`sha256:359202f8bd9abfc2584827afb339f435559012e613bd8592974f37de610d6ea2`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 3.0 MB (2959908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc8c6287d8981938b613ac5acb7739f90c763dc38c337365c6ab7b1d7bdd102`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:80e2ad6620f3f82d59d8810d86959ba8628a1b1f8d09bc02c7f5aaaac37839f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209925669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874bdacfaba22f9b5c03961584b2cedf0927330b1af5e042632e06b82d8cfa67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549562dbb9f45949b79117ad60c4bbdb1ae9a0fd0a32b6119b57bf804e7f1c77`  
		Last Modified: Tue, 04 Feb 2025 08:22:06 GMT  
		Size: 1.5 MB (1536037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be22b512b5a96a4fe3331474ad127315a608e672c8ea3e79391be0db725d01a`  
		Last Modified: Tue, 18 Feb 2025 21:33:04 GMT  
		Size: 173.9 MB (173941697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:58a59cc85849ba6df7406da683a9d18526cc9492f156957c03d49f6e2b8ebdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eac0af4ef39654c7e88b004b656163ec139f0c0fe2b993db35c7cbbf7bc334`

```dockerfile
```

-	Layers:
	-	`sha256:8b89649aebeca8f9c065960b792fbb3dea2c43fa44f4f88141f05fbc415d47b1`  
		Last Modified: Tue, 18 Feb 2025 21:32:59 GMT  
		Size: 2.9 MB (2945643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0821def02bb6c4a457d8cb01e9cc1842b2deb32a2bfcdd5561a69750214e5387`  
		Last Modified: Tue, 18 Feb 2025 21:32:58 GMT  
		Size: 13.2 KB (13212 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:8372ea0e8044ad3181ab73ca6132ed5976dbb87c17ce5548beba74100bd8376e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192506212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d933544add6a6bb2eec6e0ad75cd465815512658622c32a639745ef9b4a69d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:03 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:05 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Sun, 26 Jan 2025 05:32:05 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f4ed4c83fd203a93b2e2d3afc549f52d4e75a4e9c4ecade96808e6a2fe3ebb`  
		Last Modified: Tue, 18 Feb 2025 21:29:44 GMT  
		Size: 1.5 MB (1455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae97d923a9d8a7f083dca06b2b1940a95758b3f7b691117f2db3c03beddc5b0e`  
		Last Modified: Tue, 18 Feb 2025 21:32:46 GMT  
		Size: 163.0 MB (163049714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0db9ff1dd35933c8ccaba5cd1636613ff8b3349f21ab11308b4818c25558898e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2648693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cad2ff981e4a4ded66e115ed734096029e3e22b50e0c2085531a396fed3731`

```dockerfile
```

-	Layers:
	-	`sha256:44ac44987ef8c1727e8a4cec0873d1d6b6c4ef8de235f866865ad677d090059a`  
		Last Modified: Tue, 18 Feb 2025 21:32:45 GMT  
		Size: 2.6 MB (2635516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d80a9a448ce0a4b26ca082e699deb13e1a08c5f79ccc63aafeadb917f122191c`  
		Last Modified: Tue, 18 Feb 2025 21:32:44 GMT  
		Size: 13.2 KB (13177 bytes)  
		MIME: application/vnd.in-toto+json
