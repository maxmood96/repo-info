## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:2fbf977b8a57cc135783e4bcc8a4dccfa8bb3b38715fc18a59184252a57327b1
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
$ docker pull ibmjava@sha256:5e95c0be28a3668d08dbb1c35d778681a1d5336594068aa5afcde8533bb9a738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101795806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7aa0091ebe544e18e83ad6b302874c58b632246fd914117f93a008c804e5d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Jan 2026 22:29:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:29:09 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 15 Jan 2026 22:29:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Jan 2026 22:29:16 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e109ef74bff14f570183a8315236fe103addbb91141d21ea866e2c05e0a4cf`  
		Last Modified: Thu, 15 Jan 2026 22:29:35 GMT  
		Size: 1.5 MB (1450135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1858a72cb605ad99057911615e1d2a6b4c4b644664e5f6c68d54aae77ac7563c`  
		Last Modified: Thu, 15 Jan 2026 22:29:28 GMT  
		Size: 70.8 MB (70809004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:63188ffa83970b206885a3ac93d4f52e88d0b64f7d378f5578450f366855ef8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e2e0411527258b39a982987e4d1558fa9e0eca08ed8d633216b208fff6e5f3`

```dockerfile
```

-	Layers:
	-	`sha256:0dd089281d5f66ac29e2be40c1e7b026cb39dec5f456c9c707b8c2b4f86982a7`  
		Last Modified: Fri, 16 Jan 2026 00:02:59 GMT  
		Size: 2.2 MB (2156553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a0087d6a9d0691af87901084af6b64ea39e6d08bfa71147dcc340aadb5bfe9`  
		Last Modified: Fri, 16 Jan 2026 00:03:00 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:b6964ebf64cbcae2fc8ca54dbff7f0feab3d65db27f3c0750cc0ff0fb795bce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107727946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520c4c788d2b0efe91e91f16bf0437f861dddb6906bfc267c2673fcd813b7eee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:48:26 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Jan 2026 22:48:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:48:26 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 15 Jan 2026 22:48:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Jan 2026 22:48:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814f9357ec073065f6203180cb4350e2f9485621f356fdf6fd2a944386ce11b4`  
		Last Modified: Thu, 15 Jan 2026 22:49:11 GMT  
		Size: 1.5 MB (1536144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5fe6100cc025e978547c4526f6ea13107cfd5f48542519a90320b7def38a34`  
		Last Modified: Thu, 15 Jan 2026 22:49:21 GMT  
		Size: 71.7 MB (71744840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0e1bc5b7a0328bb811b81c3039e05ae8de69f1bd94581140e0279b0bbb5930dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cd7229a3aa998b927847fac5d637dd0cdbffd07c81574d3e96bb95d60727e4`

```dockerfile
```

-	Layers:
	-	`sha256:ef09e54764cdbed55a58f6c210fd976b40d9a14673fe70a201d0ddd1ca100639`  
		Last Modified: Fri, 16 Jan 2026 00:03:05 GMT  
		Size: 2.2 MB (2161054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df89aaea895a4a575bcb34afac656b6329ce1a7857477e6790d942ae62728cc2`  
		Last Modified: Thu, 15 Jan 2026 22:49:03 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:3fc6889a078588d8d04f72467bda7ebc6ef3a1f8a178e88dbdf961dd0d3489a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101310339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54549dabce2908476ff2cc9184fadd0c17158d8a1a53b3010d583f02b7fbf51d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:47 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Jan 2026 22:19:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:47 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 15 Jan 2026 22:20:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Jan 2026 22:20:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc737025d563a0d3cad996a8e2fb563804d52c9ac7514476c4798f787daf5a5`  
		Last Modified: Thu, 15 Jan 2026 22:20:32 GMT  
		Size: 1.5 MB (1455738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f0c433de4cbc299fc1d6ad399bf994d6d3d3ee7617a9d93487649e92230fe`  
		Last Modified: Thu, 15 Jan 2026 22:20:41 GMT  
		Size: 71.9 MB (71851463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6531e8a5cfffe7fa7e1084d074dc307cc3afb5916f56bfe3b11088101c611424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9cc0f8c98e12ebe4bc55643b2fbaf14a94d2ec2a393e3e9d2de6785c771447`

```dockerfile
```

-	Layers:
	-	`sha256:4e814f1d6f79338ba8ba783f9789f0aa12408ac112199405a4730c7830dc5242`  
		Last Modified: Fri, 16 Jan 2026 00:03:09 GMT  
		Size: 2.2 MB (2160175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea2a0c125113c0931a692540d8b287522346b6dd77363228e3c9751b9ad1d6c8`  
		Last Modified: Fri, 16 Jan 2026 00:03:10 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json
