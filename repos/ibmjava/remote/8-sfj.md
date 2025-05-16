## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:2601ddddac50dbc7c317da1811e3356c3441394726b91f9da448c24b746af4f2
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
$ docker pull ibmjava@sha256:6c2a688d5855cfc3d1845bc16ce4516f5a0add138597c4f791caf15b6a11bfb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101478466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c752f48f13b64d48c37527671bc44e19033f974b349d5ded31e01d653ae5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fce7ad64d8e7a6e537f46ad89e4578bc2bc7219954201134354c28360bed14`  
		Last Modified: Fri, 16 May 2025 19:59:23 GMT  
		Size: 1.5 MB (1450208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e28bd27d016252f68af84939c9ba6b1f15eb24d79800b7d9280b56ee614c89`  
		Last Modified: Fri, 16 May 2025 19:59:27 GMT  
		Size: 70.5 MB (70495644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e0339fd7b8ed0e3a9d21c87855ec6e2536f9bf46a83b263798e5342bf3ebad6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2047602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15481a73c6c9e0a8f31316aae1884c90dcd66c4c112084ad7ed40cda32f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:0c959c03c4030fdf817351c18fcabd8805c23dbfaaba9738f53f28b55c4b32fe`  
		Last Modified: Wed, 14 May 2025 19:35:01 GMT  
		Size: 2.0 MB (2034421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed15e5715112fd5a2cd433c56de13c9ed2a9c5504a635005f194cfba87e84b0`  
		Last Modified: Wed, 14 May 2025 19:35:00 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:b9d8cf73ed1812770b2c08ee06171ff8c84364664038f42b90c1db3667cf2fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107308043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fb0a1e978c2f1ea1aebea5f79764cbacf6822948c37c3638d2b4f961241989`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce266802d90bd81a35f2bfa06dda920a30ccaf77bd70a0f972e5ac85814cd8a`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4c6905e04c9184247640579fafa52e096976ddf445a8fb4f7068b37a97f105`  
		Last Modified: Wed, 14 May 2025 19:37:48 GMT  
		Size: 71.3 MB (71328625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:da12c3265d566874701cd5ff713424d6dd77b3e2abc1e5a08d420c8037dea192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2052021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29958454ad666049460ed204953cf7a937a999b6ecc4d65e6a34df5c727c2d1b`

```dockerfile
```

-	Layers:
	-	`sha256:c307d7361520511a758951b1750cdddb3824b83d49ccfa3d498028ee84900e88`  
		Last Modified: Wed, 14 May 2025 19:37:45 GMT  
		Size: 2.0 MB (2038808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243397b71c2380bde1bca649bad6b23ebd5fe7a4254a4cf5c24767d2e27f5d7c`  
		Last Modified: Wed, 14 May 2025 19:37:44 GMT  
		Size: 13.2 KB (13213 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:9a50cb7c83b39903272c273d4112b50e33c2b5934f7943c9b58c440ce505f472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100547274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cfc583b4b8cc4f57bc672be46f1bf7acdb7f8c250e5500bdfac0f279ad32bb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
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
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a80e8992168178f43fd2602a23cc2b2a1380dcba5882f3fbf1da5fe7f83ac5`  
		Last Modified: Fri, 09 May 2025 12:35:37 GMT  
		Size: 1.5 MB (1455700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a0f1fd0bd2f7bbc2ffdbb416daf60034b798141f7efecc1effec1fcb92d49c`  
		Last Modified: Wed, 14 May 2025 19:39:02 GMT  
		Size: 71.1 MB (71091590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f702c3bc00c05601fff77baa83b0b1f97d46d51e260664c369cdffa715cbe53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373c74f4df4e7141bcc97e62e380873f99d0d1dda2fe1938b3d91df69a795ea`

```dockerfile
```

-	Layers:
	-	`sha256:985fd38328266389a298f2d419903f609e0b18739c8936725e16bc4bce455e01`  
		Last Modified: Wed, 14 May 2025 19:39:00 GMT  
		Size: 2.0 MB (2038043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2b33f3e43440c3414fe7bf75a0a04cbe26ac913cd20d207203c9f5b9906e8f`  
		Last Modified: Wed, 14 May 2025 19:39:00 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json
