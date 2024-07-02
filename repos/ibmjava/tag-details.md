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
$ docker pull ibmjava@sha256:f10dd21b2707f0b4f4ca80956e3272ff92d576de74dfd0ac9378304ba4057364
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
$ docker pull ibmjava@sha256:5b81c9e1fe45fd3e2a5bcdc48b886e4a0a7c51d0a68bc76aa61a6f8b4e081216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165991959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519ee26f94919aa3a6b7541e157ff63c621a60b3bef25157813f407d0227a42f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad37218bc956fdddeacd0ff6a9c47df9d4479440ce4cd460da448cca0c28a`  
		Last Modified: Tue, 02 Jul 2024 03:03:41 GMT  
		Size: 1.4 MB (1438241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba472852db631f821c233a385189185488282c173d367733a7581860cf2392`  
		Last Modified: Tue, 02 Jul 2024 03:03:45 GMT  
		Size: 135.0 MB (135019663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:62f6931071aea87e1e856066f297f471db2388fc5a3627c43b3736cd77273ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2014972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b519666619711976579dadd61a0ed7636573f549853b411f9c7fbc3c2afb653e`

```dockerfile
```

-	Layers:
	-	`sha256:c33092cc2c77a3b1d0f41f80f1800634da486b17c34cb4e183b12794d2afd03b`  
		Last Modified: Tue, 02 Jul 2024 03:03:41 GMT  
		Size: 2.0 MB (2001455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ceb1e3e67148bbbf33efbdfd51e649af706e288a82b3ac12983041ca1534f02`  
		Last Modified: Tue, 02 Jul 2024 03:03:40 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1e0617375a5a8c0d1a80b984c54eae3f97ac4e54e3dcb1535c48eeb01f40e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171478469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f2112036213949d04f2d0b81c15f4c86e9367260578c740537e4e9a24c5970`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73fe39aa7190a4c3d9ca1d0ac575d106d4b883ca1d2e6fbd1bc4a27f3ead93`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 1.5 MB (1523343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c039e649d90526676156eadaf6e5be4448cf66e08ffc5813ca1cfb7f5f8936`  
		Last Modified: Tue, 02 Jul 2024 10:41:29 GMT  
		Size: 135.5 MB (135494045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a59a03fe697ae41fb38dacf743be7998c6d29c5da4b914383c4ef782b088cee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2017448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcc56fd6b86beaafe1bb4ab6e7187f01dc5e0f909e63fe6d14aa43763e867eb`

```dockerfile
```

-	Layers:
	-	`sha256:ce6cf1b91acd608d2d9027b78102214232f90d51275a18ab1ae291a86c0193ca`  
		Last Modified: Tue, 02 Jul 2024 10:41:26 GMT  
		Size: 2.0 MB (2003890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550e1104c5d1739ba7b7e8993f0494900e224fefe8268d87771cf14500a80271`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:85385c1c1fe64ae152f45f34ae4f8818cc1f2ac411be2d325c7c374b3ba023c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161217993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4968a71f9d423f3bc2c9b3cf37cb13a2bc6c958db6361fcdd3d80d92551b018b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ad7703edfb983f72e74e56d3ba233db0435a1290037a46c332cd69db5ad6f`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 1.4 MB (1441883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f543b0489a8d3dd976994e8c395210f934f9cd74749fb1adb7dc0b3f915eb`  
		Last Modified: Tue, 02 Jul 2024 06:07:58 GMT  
		Size: 131.8 MB (131775570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ab5cc224dc474f320c99b545144ee3a270eb6ccaa41c511eb49085ff07c34a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2013473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d27ba34d0e309881642eec5aad6ddfe21cb823f662630dddaad5f4bffc36f31`

```dockerfile
```

-	Layers:
	-	`sha256:960d3da45dd01d9b304e33d891dd31cb1d13c6f32101e9413966927004716835`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 2.0 MB (1999955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41126b46ec01e5f6f2a3b5aff607dba48bd3b4d5923a9378a7cfc4e3026a02f1`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:f10dd21b2707f0b4f4ca80956e3272ff92d576de74dfd0ac9378304ba4057364
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
$ docker pull ibmjava@sha256:5b81c9e1fe45fd3e2a5bcdc48b886e4a0a7c51d0a68bc76aa61a6f8b4e081216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165991959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519ee26f94919aa3a6b7541e157ff63c621a60b3bef25157813f407d0227a42f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad37218bc956fdddeacd0ff6a9c47df9d4479440ce4cd460da448cca0c28a`  
		Last Modified: Tue, 02 Jul 2024 03:03:41 GMT  
		Size: 1.4 MB (1438241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba472852db631f821c233a385189185488282c173d367733a7581860cf2392`  
		Last Modified: Tue, 02 Jul 2024 03:03:45 GMT  
		Size: 135.0 MB (135019663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:62f6931071aea87e1e856066f297f471db2388fc5a3627c43b3736cd77273ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2014972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b519666619711976579dadd61a0ed7636573f549853b411f9c7fbc3c2afb653e`

```dockerfile
```

-	Layers:
	-	`sha256:c33092cc2c77a3b1d0f41f80f1800634da486b17c34cb4e183b12794d2afd03b`  
		Last Modified: Tue, 02 Jul 2024 03:03:41 GMT  
		Size: 2.0 MB (2001455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ceb1e3e67148bbbf33efbdfd51e649af706e288a82b3ac12983041ca1534f02`  
		Last Modified: Tue, 02 Jul 2024 03:03:40 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1e0617375a5a8c0d1a80b984c54eae3f97ac4e54e3dcb1535c48eeb01f40e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171478469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f2112036213949d04f2d0b81c15f4c86e9367260578c740537e4e9a24c5970`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73fe39aa7190a4c3d9ca1d0ac575d106d4b883ca1d2e6fbd1bc4a27f3ead93`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 1.5 MB (1523343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c039e649d90526676156eadaf6e5be4448cf66e08ffc5813ca1cfb7f5f8936`  
		Last Modified: Tue, 02 Jul 2024 10:41:29 GMT  
		Size: 135.5 MB (135494045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a59a03fe697ae41fb38dacf743be7998c6d29c5da4b914383c4ef782b088cee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2017448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcc56fd6b86beaafe1bb4ab6e7187f01dc5e0f909e63fe6d14aa43763e867eb`

```dockerfile
```

-	Layers:
	-	`sha256:ce6cf1b91acd608d2d9027b78102214232f90d51275a18ab1ae291a86c0193ca`  
		Last Modified: Tue, 02 Jul 2024 10:41:26 GMT  
		Size: 2.0 MB (2003890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550e1104c5d1739ba7b7e8993f0494900e224fefe8268d87771cf14500a80271`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:85385c1c1fe64ae152f45f34ae4f8818cc1f2ac411be2d325c7c374b3ba023c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161217993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4968a71f9d423f3bc2c9b3cf37cb13a2bc6c958db6361fcdd3d80d92551b018b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ad7703edfb983f72e74e56d3ba233db0435a1290037a46c332cd69db5ad6f`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 1.4 MB (1441883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f543b0489a8d3dd976994e8c395210f934f9cd74749fb1adb7dc0b3f915eb`  
		Last Modified: Tue, 02 Jul 2024 06:07:58 GMT  
		Size: 131.8 MB (131775570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ab5cc224dc474f320c99b545144ee3a270eb6ccaa41c511eb49085ff07c34a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2013473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d27ba34d0e309881642eec5aad6ddfe21cb823f662630dddaad5f4bffc36f31`

```dockerfile
```

-	Layers:
	-	`sha256:960d3da45dd01d9b304e33d891dd31cb1d13c6f32101e9413966927004716835`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 2.0 MB (1999955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41126b46ec01e5f6f2a3b5aff607dba48bd3b4d5923a9378a7cfc4e3026a02f1`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:78607f513c2dc76820545d4e2c44e52dc0cc54acfa1e33aadca0e44526fb56ef
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
$ docker pull ibmjava@sha256:91ca2ffccc51557311f5dcdee4d7c831de53d45b5e12f25861c8115e233f0c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203206747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d82acfbe43bb8920de0e508715f185c9562dfba2c1ed61e0c816fefe5986e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b7314d6b7e39503736d64744c95bb7467e6ebc8d9db88102350cc0a3d3203b`  
		Last Modified: Tue, 02 Jul 2024 03:03:46 GMT  
		Size: 1.4 MB (1438198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc12a4a066686684a17d23642ac15591656eb5dcf84e0b48ec2c8e313f4a6f4`  
		Last Modified: Tue, 02 Jul 2024 03:03:51 GMT  
		Size: 172.2 MB (172234494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5c8e97c2a72e9a565076616383e958504c4824ae6294b9f546d4d5ef4be57f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2066966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a627510d4038312970084b63777a1028ca89ccbecac257deaa607a743e6910`

```dockerfile
```

-	Layers:
	-	`sha256:88e9103518bbe84b3c6304d3607b0260934033b764b45b294ce00d027157e6b4`  
		Last Modified: Tue, 02 Jul 2024 03:03:46 GMT  
		Size: 2.1 MB (2054042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ce3e626e177f4e827744d06c94f43e72fa6c17113e995ea4cc4cd99f2635ffe`  
		Last Modified: Tue, 02 Jul 2024 03:03:46 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:3ac17471af77f2a50bd1d332ac342f1a2a1f20f9b558149d7f5702e7d3a56332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208821980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db23902f7bbef78d53e88444d2b6ddcd8b549f1b7dd8ccfff077453a0265807`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73fe39aa7190a4c3d9ca1d0ac575d106d4b883ca1d2e6fbd1bc4a27f3ead93`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 1.5 MB (1523343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda8a2e556b382b88d02908324730e69009b01e5e240a3af3678b37eef9605d`  
		Last Modified: Tue, 02 Jul 2024 10:43:15 GMT  
		Size: 172.8 MB (172837556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:922010024ee5f69774255c45b8a3027fedb4b73ea86a429dac3b89284fd43d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bdac27546af5151de093ce857bf1de25935cdad0aa1cb26beb426763e5e016`

```dockerfile
```

-	Layers:
	-	`sha256:bc129738d4d56802ce433d708d78d355daa12efcf971c4e67946278d500ecad2`  
		Last Modified: Tue, 02 Jul 2024 10:43:11 GMT  
		Size: 2.1 MB (2056465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db9f2a5779eccfe8290fe166115273a8e182b8d43d761707bb7654ab0f2c614`  
		Last Modified: Tue, 02 Jul 2024 10:43:10 GMT  
		Size: 13.0 KB (12951 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:8b07a0beef7f5e86ae956280e61047b71ceca19ec00e842872c2b5a950201cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191505886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e78af679d6287b78b8b50e01887f1d64d5cec12c08490cbe06e802b55124940`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ad7703edfb983f72e74e56d3ba233db0435a1290037a46c332cd69db5ad6f`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 1.4 MB (1441883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d1fd7bbb6820dbd609cec245157a4e8cd714516c71223faf3c244075fdac`  
		Last Modified: Tue, 02 Jul 2024 06:09:43 GMT  
		Size: 162.1 MB (162063463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:644868b5def57f26af86ba5d508c2021f870b47e842790439d644f8569c07854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2040692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cb6c3af75b3764b92eedd8fa8adf5077539410fbb4fc19edb0b051bf850bc0`

```dockerfile
```

-	Layers:
	-	`sha256:6d76576342c539c313eaab6a3d6754278dfe8e0776bf392ba55dbeedb2e4bd1d`  
		Last Modified: Tue, 02 Jul 2024 06:09:40 GMT  
		Size: 2.0 MB (2027768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71df1d3ff4ea65d5bddbe1ba47d82ad4b257e7a292935e80a0fac51d430b5a51`  
		Last Modified: Tue, 02 Jul 2024 06:09:40 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:e9b85602c603b5670da49b84febb1c000df34713f4f59f126a7a324fc9a27825
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
$ docker pull ibmjava@sha256:f620ed24152209545c0b4f7b928bbd180111e2ea2e0316f54b1680ccaedec686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100877325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee010bdb37e507abdbbb888c888409df3af703c6de6c00489eda582e759152dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90da020be5ddc6d70004d7bdcdfa83342a0fbfd3dfe6385dfe30771208d6d440`  
		Last Modified: Tue, 02 Jul 2024 03:03:35 GMT  
		Size: 1.4 MB (1438214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136dc9b12ccf44e211aa030068fff33eabb9e5e3340e62b68a1b6e1799393183`  
		Last Modified: Tue, 02 Jul 2024 03:03:37 GMT  
		Size: 69.9 MB (69905056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5de58ec3e9ed758d4a01c99ca36de4e66c5f127a02d830a8e3fe758ad897cf77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2000287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a02c2b1c7897c43eb2ec748bc0a2c8f502b01ec2b50dbd527b211e2fa9e6da`

```dockerfile
```

-	Layers:
	-	`sha256:ff0c07c46f1983a15846f61554dae1be46c23ead93c50161951ef83633c20d2c`  
		Last Modified: Tue, 02 Jul 2024 03:03:35 GMT  
		Size: 2.0 MB (1987361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:522a1f66a12eafdb653a9d106a076a5a5878a682deb21f9c940633a069351fc0`  
		Last Modified: Tue, 02 Jul 2024 03:03:34 GMT  
		Size: 12.9 KB (12926 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0d5d045b08de460a78c01bb22b4f084a79ee3fea0924fcd801a9f33c9413dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106387181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cef76435f0193c29a6092b42be63d1bed9fbbcec1e250c8c09e7c0fff3bd77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73fe39aa7190a4c3d9ca1d0ac575d106d4b883ca1d2e6fbd1bc4a27f3ead93`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 1.5 MB (1523343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbb798acd38de044e7bf8727b9dd61ad1609899a1e4ff4f2fc36c622fc33c4c`  
		Last Modified: Tue, 02 Jul 2024 10:42:14 GMT  
		Size: 70.4 MB (70402757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e4d9eac5d867c9dc4ab9d567c5ac2fa499f643fae2edfed8bf1f53a6e5695aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57b051515a2096f30d8c2780d52a7aa6b99924055461f9ceb0efaabc9ad8ee`

```dockerfile
```

-	Layers:
	-	`sha256:fc0b9584677f3eeb7e0bba688741f80044d76bcc05402b8298a327703c7e2268`  
		Last Modified: Tue, 02 Jul 2024 10:42:11 GMT  
		Size: 2.0 MB (1990745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7541558a22bbdd501160fe1e7cb10e323ad4dd37101ec0496984def61820e52f`  
		Last Modified: Tue, 02 Jul 2024 10:42:11 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:8499aa8d9aed6b946bc5138a96711cd2326890021172f5746e22505e60914789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99820889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac1bcf5dbe41d2e5d8ae68d712a92b0b85d9e8da733eddb0f93712969b07c03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ad7703edfb983f72e74e56d3ba233db0435a1290037a46c332cd69db5ad6f`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 1.4 MB (1441883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9022f0a929ddd0a81b214e1c27060e843e8f0f9acb691a3f97ba122b4df379be`  
		Last Modified: Tue, 02 Jul 2024 06:08:49 GMT  
		Size: 70.4 MB (70378466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f36a1017ab214c18be12b02d4c780a76e8794f5acb4b01a3798281e66eec8949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a0c93ecee68fb0da07588800d1cd1c4988d57d7d6652056bd03949667f5627`

```dockerfile
```

-	Layers:
	-	`sha256:ea54d3fdbd7f662221925892f30a92bf51dcd09524165561aab9c03a158e8c96`  
		Last Modified: Tue, 02 Jul 2024 06:08:48 GMT  
		Size: 2.0 MB (1988750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3015dfe8e5a282456ae431d795712034a9ca0a69fde429d36012fd5a795ab46`  
		Last Modified: Tue, 02 Jul 2024 06:08:48 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:f10dd21b2707f0b4f4ca80956e3272ff92d576de74dfd0ac9378304ba4057364
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
$ docker pull ibmjava@sha256:5b81c9e1fe45fd3e2a5bcdc48b886e4a0a7c51d0a68bc76aa61a6f8b4e081216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165991959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519ee26f94919aa3a6b7541e157ff63c621a60b3bef25157813f407d0227a42f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad37218bc956fdddeacd0ff6a9c47df9d4479440ce4cd460da448cca0c28a`  
		Last Modified: Tue, 02 Jul 2024 03:03:41 GMT  
		Size: 1.4 MB (1438241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba472852db631f821c233a385189185488282c173d367733a7581860cf2392`  
		Last Modified: Tue, 02 Jul 2024 03:03:45 GMT  
		Size: 135.0 MB (135019663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:62f6931071aea87e1e856066f297f471db2388fc5a3627c43b3736cd77273ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2014972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b519666619711976579dadd61a0ed7636573f549853b411f9c7fbc3c2afb653e`

```dockerfile
```

-	Layers:
	-	`sha256:c33092cc2c77a3b1d0f41f80f1800634da486b17c34cb4e183b12794d2afd03b`  
		Last Modified: Tue, 02 Jul 2024 03:03:41 GMT  
		Size: 2.0 MB (2001455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ceb1e3e67148bbbf33efbdfd51e649af706e288a82b3ac12983041ca1534f02`  
		Last Modified: Tue, 02 Jul 2024 03:03:40 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1e0617375a5a8c0d1a80b984c54eae3f97ac4e54e3dcb1535c48eeb01f40e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171478469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f2112036213949d04f2d0b81c15f4c86e9367260578c740537e4e9a24c5970`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73fe39aa7190a4c3d9ca1d0ac575d106d4b883ca1d2e6fbd1bc4a27f3ead93`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 1.5 MB (1523343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c039e649d90526676156eadaf6e5be4448cf66e08ffc5813ca1cfb7f5f8936`  
		Last Modified: Tue, 02 Jul 2024 10:41:29 GMT  
		Size: 135.5 MB (135494045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a59a03fe697ae41fb38dacf743be7998c6d29c5da4b914383c4ef782b088cee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2017448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcc56fd6b86beaafe1bb4ab6e7187f01dc5e0f909e63fe6d14aa43763e867eb`

```dockerfile
```

-	Layers:
	-	`sha256:ce6cf1b91acd608d2d9027b78102214232f90d51275a18ab1ae291a86c0193ca`  
		Last Modified: Tue, 02 Jul 2024 10:41:26 GMT  
		Size: 2.0 MB (2003890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550e1104c5d1739ba7b7e8993f0494900e224fefe8268d87771cf14500a80271`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:85385c1c1fe64ae152f45f34ae4f8818cc1f2ac411be2d325c7c374b3ba023c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161217993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4968a71f9d423f3bc2c9b3cf37cb13a2bc6c958db6361fcdd3d80d92551b018b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ad7703edfb983f72e74e56d3ba233db0435a1290037a46c332cd69db5ad6f`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 1.4 MB (1441883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f543b0489a8d3dd976994e8c395210f934f9cd74749fb1adb7dc0b3f915eb`  
		Last Modified: Tue, 02 Jul 2024 06:07:58 GMT  
		Size: 131.8 MB (131775570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ab5cc224dc474f320c99b545144ee3a270eb6ccaa41c511eb49085ff07c34a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2013473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d27ba34d0e309881642eec5aad6ddfe21cb823f662630dddaad5f4bffc36f31`

```dockerfile
```

-	Layers:
	-	`sha256:960d3da45dd01d9b304e33d891dd31cb1d13c6f32101e9413966927004716835`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 2.0 MB (1999955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41126b46ec01e5f6f2a3b5aff607dba48bd3b4d5923a9378a7cfc4e3026a02f1`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:f10dd21b2707f0b4f4ca80956e3272ff92d576de74dfd0ac9378304ba4057364
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
$ docker pull ibmjava@sha256:5b81c9e1fe45fd3e2a5bcdc48b886e4a0a7c51d0a68bc76aa61a6f8b4e081216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165991959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519ee26f94919aa3a6b7541e157ff63c621a60b3bef25157813f407d0227a42f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad37218bc956fdddeacd0ff6a9c47df9d4479440ce4cd460da448cca0c28a`  
		Last Modified: Tue, 02 Jul 2024 03:03:41 GMT  
		Size: 1.4 MB (1438241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba472852db631f821c233a385189185488282c173d367733a7581860cf2392`  
		Last Modified: Tue, 02 Jul 2024 03:03:45 GMT  
		Size: 135.0 MB (135019663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:62f6931071aea87e1e856066f297f471db2388fc5a3627c43b3736cd77273ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2014972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b519666619711976579dadd61a0ed7636573f549853b411f9c7fbc3c2afb653e`

```dockerfile
```

-	Layers:
	-	`sha256:c33092cc2c77a3b1d0f41f80f1800634da486b17c34cb4e183b12794d2afd03b`  
		Last Modified: Tue, 02 Jul 2024 03:03:41 GMT  
		Size: 2.0 MB (2001455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ceb1e3e67148bbbf33efbdfd51e649af706e288a82b3ac12983041ca1534f02`  
		Last Modified: Tue, 02 Jul 2024 03:03:40 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1e0617375a5a8c0d1a80b984c54eae3f97ac4e54e3dcb1535c48eeb01f40e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171478469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f2112036213949d04f2d0b81c15f4c86e9367260578c740537e4e9a24c5970`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73fe39aa7190a4c3d9ca1d0ac575d106d4b883ca1d2e6fbd1bc4a27f3ead93`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 1.5 MB (1523343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c039e649d90526676156eadaf6e5be4448cf66e08ffc5813ca1cfb7f5f8936`  
		Last Modified: Tue, 02 Jul 2024 10:41:29 GMT  
		Size: 135.5 MB (135494045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a59a03fe697ae41fb38dacf743be7998c6d29c5da4b914383c4ef782b088cee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2017448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcc56fd6b86beaafe1bb4ab6e7187f01dc5e0f909e63fe6d14aa43763e867eb`

```dockerfile
```

-	Layers:
	-	`sha256:ce6cf1b91acd608d2d9027b78102214232f90d51275a18ab1ae291a86c0193ca`  
		Last Modified: Tue, 02 Jul 2024 10:41:26 GMT  
		Size: 2.0 MB (2003890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550e1104c5d1739ba7b7e8993f0494900e224fefe8268d87771cf14500a80271`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:85385c1c1fe64ae152f45f34ae4f8818cc1f2ac411be2d325c7c374b3ba023c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161217993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4968a71f9d423f3bc2c9b3cf37cb13a2bc6c958db6361fcdd3d80d92551b018b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ad7703edfb983f72e74e56d3ba233db0435a1290037a46c332cd69db5ad6f`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 1.4 MB (1441883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f543b0489a8d3dd976994e8c395210f934f9cd74749fb1adb7dc0b3f915eb`  
		Last Modified: Tue, 02 Jul 2024 06:07:58 GMT  
		Size: 131.8 MB (131775570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ab5cc224dc474f320c99b545144ee3a270eb6ccaa41c511eb49085ff07c34a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2013473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d27ba34d0e309881642eec5aad6ddfe21cb823f662630dddaad5f4bffc36f31`

```dockerfile
```

-	Layers:
	-	`sha256:960d3da45dd01d9b304e33d891dd31cb1d13c6f32101e9413966927004716835`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 2.0 MB (1999955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41126b46ec01e5f6f2a3b5aff607dba48bd3b4d5923a9378a7cfc4e3026a02f1`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:78607f513c2dc76820545d4e2c44e52dc0cc54acfa1e33aadca0e44526fb56ef
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
$ docker pull ibmjava@sha256:91ca2ffccc51557311f5dcdee4d7c831de53d45b5e12f25861c8115e233f0c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203206747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d82acfbe43bb8920de0e508715f185c9562dfba2c1ed61e0c816fefe5986e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b7314d6b7e39503736d64744c95bb7467e6ebc8d9db88102350cc0a3d3203b`  
		Last Modified: Tue, 02 Jul 2024 03:03:46 GMT  
		Size: 1.4 MB (1438198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc12a4a066686684a17d23642ac15591656eb5dcf84e0b48ec2c8e313f4a6f4`  
		Last Modified: Tue, 02 Jul 2024 03:03:51 GMT  
		Size: 172.2 MB (172234494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5c8e97c2a72e9a565076616383e958504c4824ae6294b9f546d4d5ef4be57f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2066966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a627510d4038312970084b63777a1028ca89ccbecac257deaa607a743e6910`

```dockerfile
```

-	Layers:
	-	`sha256:88e9103518bbe84b3c6304d3607b0260934033b764b45b294ce00d027157e6b4`  
		Last Modified: Tue, 02 Jul 2024 03:03:46 GMT  
		Size: 2.1 MB (2054042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ce3e626e177f4e827744d06c94f43e72fa6c17113e995ea4cc4cd99f2635ffe`  
		Last Modified: Tue, 02 Jul 2024 03:03:46 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:3ac17471af77f2a50bd1d332ac342f1a2a1f20f9b558149d7f5702e7d3a56332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208821980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db23902f7bbef78d53e88444d2b6ddcd8b549f1b7dd8ccfff077453a0265807`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73fe39aa7190a4c3d9ca1d0ac575d106d4b883ca1d2e6fbd1bc4a27f3ead93`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 1.5 MB (1523343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda8a2e556b382b88d02908324730e69009b01e5e240a3af3678b37eef9605d`  
		Last Modified: Tue, 02 Jul 2024 10:43:15 GMT  
		Size: 172.8 MB (172837556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:922010024ee5f69774255c45b8a3027fedb4b73ea86a429dac3b89284fd43d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bdac27546af5151de093ce857bf1de25935cdad0aa1cb26beb426763e5e016`

```dockerfile
```

-	Layers:
	-	`sha256:bc129738d4d56802ce433d708d78d355daa12efcf971c4e67946278d500ecad2`  
		Last Modified: Tue, 02 Jul 2024 10:43:11 GMT  
		Size: 2.1 MB (2056465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db9f2a5779eccfe8290fe166115273a8e182b8d43d761707bb7654ab0f2c614`  
		Last Modified: Tue, 02 Jul 2024 10:43:10 GMT  
		Size: 13.0 KB (12951 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:8b07a0beef7f5e86ae956280e61047b71ceca19ec00e842872c2b5a950201cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191505886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e78af679d6287b78b8b50e01887f1d64d5cec12c08490cbe06e802b55124940`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ad7703edfb983f72e74e56d3ba233db0435a1290037a46c332cd69db5ad6f`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 1.4 MB (1441883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d1fd7bbb6820dbd609cec245157a4e8cd714516c71223faf3c244075fdac`  
		Last Modified: Tue, 02 Jul 2024 06:09:43 GMT  
		Size: 162.1 MB (162063463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:644868b5def57f26af86ba5d508c2021f870b47e842790439d644f8569c07854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2040692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cb6c3af75b3764b92eedd8fa8adf5077539410fbb4fc19edb0b051bf850bc0`

```dockerfile
```

-	Layers:
	-	`sha256:6d76576342c539c313eaab6a3d6754278dfe8e0776bf392ba55dbeedb2e4bd1d`  
		Last Modified: Tue, 02 Jul 2024 06:09:40 GMT  
		Size: 2.0 MB (2027768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71df1d3ff4ea65d5bddbe1ba47d82ad4b257e7a292935e80a0fac51d430b5a51`  
		Last Modified: Tue, 02 Jul 2024 06:09:40 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:e9b85602c603b5670da49b84febb1c000df34713f4f59f126a7a324fc9a27825
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
$ docker pull ibmjava@sha256:f620ed24152209545c0b4f7b928bbd180111e2ea2e0316f54b1680ccaedec686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100877325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee010bdb37e507abdbbb888c888409df3af703c6de6c00489eda582e759152dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90da020be5ddc6d70004d7bdcdfa83342a0fbfd3dfe6385dfe30771208d6d440`  
		Last Modified: Tue, 02 Jul 2024 03:03:35 GMT  
		Size: 1.4 MB (1438214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136dc9b12ccf44e211aa030068fff33eabb9e5e3340e62b68a1b6e1799393183`  
		Last Modified: Tue, 02 Jul 2024 03:03:37 GMT  
		Size: 69.9 MB (69905056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5de58ec3e9ed758d4a01c99ca36de4e66c5f127a02d830a8e3fe758ad897cf77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2000287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a02c2b1c7897c43eb2ec748bc0a2c8f502b01ec2b50dbd527b211e2fa9e6da`

```dockerfile
```

-	Layers:
	-	`sha256:ff0c07c46f1983a15846f61554dae1be46c23ead93c50161951ef83633c20d2c`  
		Last Modified: Tue, 02 Jul 2024 03:03:35 GMT  
		Size: 2.0 MB (1987361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:522a1f66a12eafdb653a9d106a076a5a5878a682deb21f9c940633a069351fc0`  
		Last Modified: Tue, 02 Jul 2024 03:03:34 GMT  
		Size: 12.9 KB (12926 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0d5d045b08de460a78c01bb22b4f084a79ee3fea0924fcd801a9f33c9413dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106387181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cef76435f0193c29a6092b42be63d1bed9fbbcec1e250c8c09e7c0fff3bd77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73fe39aa7190a4c3d9ca1d0ac575d106d4b883ca1d2e6fbd1bc4a27f3ead93`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 1.5 MB (1523343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbb798acd38de044e7bf8727b9dd61ad1609899a1e4ff4f2fc36c622fc33c4c`  
		Last Modified: Tue, 02 Jul 2024 10:42:14 GMT  
		Size: 70.4 MB (70402757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e4d9eac5d867c9dc4ab9d567c5ac2fa499f643fae2edfed8bf1f53a6e5695aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57b051515a2096f30d8c2780d52a7aa6b99924055461f9ceb0efaabc9ad8ee`

```dockerfile
```

-	Layers:
	-	`sha256:fc0b9584677f3eeb7e0bba688741f80044d76bcc05402b8298a327703c7e2268`  
		Last Modified: Tue, 02 Jul 2024 10:42:11 GMT  
		Size: 2.0 MB (1990745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7541558a22bbdd501160fe1e7cb10e323ad4dd37101ec0496984def61820e52f`  
		Last Modified: Tue, 02 Jul 2024 10:42:11 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:8499aa8d9aed6b946bc5138a96711cd2326890021172f5746e22505e60914789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99820889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac1bcf5dbe41d2e5d8ae68d712a92b0b85d9e8da733eddb0f93712969b07c03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ad7703edfb983f72e74e56d3ba233db0435a1290037a46c332cd69db5ad6f`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 1.4 MB (1441883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9022f0a929ddd0a81b214e1c27060e843e8f0f9acb691a3f97ba122b4df379be`  
		Last Modified: Tue, 02 Jul 2024 06:08:49 GMT  
		Size: 70.4 MB (70378466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f36a1017ab214c18be12b02d4c780a76e8794f5acb4b01a3798281e66eec8949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a0c93ecee68fb0da07588800d1cd1c4988d57d7d6652056bd03949667f5627`

```dockerfile
```

-	Layers:
	-	`sha256:ea54d3fdbd7f662221925892f30a92bf51dcd09524165561aab9c03a158e8c96`  
		Last Modified: Tue, 02 Jul 2024 06:08:48 GMT  
		Size: 2.0 MB (1988750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3015dfe8e5a282456ae431d795712034a9ca0a69fde429d36012fd5a795ab46`  
		Last Modified: Tue, 02 Jul 2024 06:08:48 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json
