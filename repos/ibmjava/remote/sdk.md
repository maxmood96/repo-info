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
