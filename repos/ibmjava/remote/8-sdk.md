## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:fb61891017e4fdce49d5f4e0adb1a2ff4ac5802be8550d6ddf2589f4b5484bd3
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
$ docker pull ibmjava@sha256:20ce1aa6043684518b8f36ad5de615b54a0da228964e4fa8005dcfd11f85bc7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203707877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45afbe4c0240d62c6f579260e86168dad586c8031132812553f3c0f1f3a38b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Dec 2024 08:06:01 GMT
ARG RELEASE
# Mon, 09 Dec 2024 08:06:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Dec 2024 08:06:01 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 09 Dec 2024 08:06:01 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1dabcd183e1eb7782bdcc6e59949d1ed67fa36b2439d067e9be496035bc72f08';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='31c3f9d11b6fc3762b69ebbe77d874c71b6b5674f8b0a88f6fecd34a837cb87c';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2a9c26d50180f269380728cdea3f8feaa4150dc56fe41b9f8ea8e0ae83240288';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='36a02072cffb1a868c72d58693d4e9eca8f6b1cec92318763a08da512c3eb602';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b544760ef2447ffbaab4c77390e5c51299750cfbccd61aa9628cd5e227e7b41c`  
		Last Modified: Tue, 04 Feb 2025 04:25:12 GMT  
		Size: 1.5 MB (1450008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5865c7aa5f137e675e48c06955f0ece55d2336ff4f644ed7c7f88f2e86f57407`  
		Last Modified: Tue, 04 Feb 2025 04:25:14 GMT  
		Size: 172.7 MB (172721928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4f7c69a0c29e6515be8a08d2609e62ebe622a5ea85fd07ec0eac20696932203b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310ff88ef89450dd02c7d92da49d167b55f8ba7b1d897f6e1638cc2b6c9d2f1a`

```dockerfile
```

-	Layers:
	-	`sha256:26f3a8447cc77be47ad0ee6030b41d8940fb665457d75dd0c43413b4cfcf994d`  
		Last Modified: Tue, 04 Feb 2025 04:25:12 GMT  
		Size: 3.0 MB (2960372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a19c85ff101e665c0664a0611d69aca94b97939ace86bb711859bd59ce7d34`  
		Last Modified: Tue, 04 Feb 2025 04:25:11 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:e5d70b45ab527923a17a463b6ed155089f73abf47e470f56808a5c75504c9280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209746540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc24b3829127db11a823111b760774bbed6ccdff05842390e164bdcc276123c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Dec 2024 08:06:01 GMT
ARG RELEASE
# Mon, 09 Dec 2024 08:06:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Dec 2024 08:06:01 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Mon, 09 Dec 2024 08:06:01 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1dabcd183e1eb7782bdcc6e59949d1ed67fa36b2439d067e9be496035bc72f08';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='31c3f9d11b6fc3762b69ebbe77d874c71b6b5674f8b0a88f6fecd34a837cb87c';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2a9c26d50180f269380728cdea3f8feaa4150dc56fe41b9f8ea8e0ae83240288';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='36a02072cffb1a868c72d58693d4e9eca8f6b1cec92318763a08da512c3eb602';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
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
	-	`sha256:b02d88eeda303267366a56c66993189b82b30c3cc8e566147cbe2e43ba95773d`  
		Last Modified: Tue, 04 Feb 2025 08:25:23 GMT  
		Size: 173.8 MB (173762568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8524bf430bf566cc78a556c1c21a9146bd83597f1d1a71b1b96e0582eb4e4912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd1162d0d023c46eb05bc32dc21be38d8622b78552e1acc9bdbd877436cffbb`

```dockerfile
```

-	Layers:
	-	`sha256:11d5ff48f077acb5b474955d7696d185a317d09710a1d9f30752c7860c58b1a0`  
		Last Modified: Tue, 04 Feb 2025 08:25:17 GMT  
		Size: 2.9 MB (2946207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba860689eb357598bfe58adc7682cf157d42befe90fe8e62a14032d6c1d2bb5d`  
		Last Modified: Tue, 04 Feb 2025 08:25:17 GMT  
		Size: 13.2 KB (13212 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:c389916625d7e03e1c9fe3a5b74c81bf213e961e2e5d7d458c42c010bff76c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192300297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206fdd06075e0f3889d59dfd5f811055b6f3a32dc7b299d1d2536f8315b1e460`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Dec 2024 08:06:01 GMT
ARG RELEASE
# Mon, 09 Dec 2024 08:06:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Dec 2024 08:06:01 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Mon, 09 Dec 2024 08:06:01 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1dabcd183e1eb7782bdcc6e59949d1ed67fa36b2439d067e9be496035bc72f08';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='31c3f9d11b6fc3762b69ebbe77d874c71b6b5674f8b0a88f6fecd34a837cb87c';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2a9c26d50180f269380728cdea3f8feaa4150dc56fe41b9f8ea8e0ae83240288';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='36a02072cffb1a868c72d58693d4e9eca8f6b1cec92318763a08da512c3eb602';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd4605c2f3ea5db01805ac2f6f0f57e95cff85dce667f56133b28c0f20728ce`  
		Last Modified: Tue, 04 Feb 2025 08:30:44 GMT  
		Size: 1.5 MB (1455537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9cd7133929941ba71f7271b4f6fbe2424a46bae0e5c17adf844f65ab30082`  
		Last Modified: Tue, 04 Feb 2025 08:33:47 GMT  
		Size: 162.8 MB (162843829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:d93a48d6890ada9bcc90d8b019daf5291d70dc5b43158d661777b75e742b2f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2649257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f1034ff11bf3f7d642952cc70b0dc6e8e316b35189276281af1d40020cb35a`

```dockerfile
```

-	Layers:
	-	`sha256:4a32a6fe3a144c95f6d1159cc622ff25cec799523c1772cb6d96c02e2a1d43d1`  
		Last Modified: Tue, 04 Feb 2025 08:33:44 GMT  
		Size: 2.6 MB (2636080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d233b65eba91471649991d538f887590c20176e2e55e168203b9a90839974fc2`  
		Last Modified: Tue, 04 Feb 2025 08:33:44 GMT  
		Size: 13.2 KB (13177 bytes)  
		MIME: application/vnd.in-toto+json
