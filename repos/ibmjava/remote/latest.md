## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:584c689279773de7717506dc1fe3986b1425dc53e77ab4f333ca597b0e49ef8d
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
$ docker pull ibmjava@sha256:feea3e0f32f6a4ca527a95dbac4dbc092beb477bdedf3904f5ed0b691222f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171478023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad2908bb593ed2f32181d25e5c8c99b408d283ff97fe030f2f8bd243423bc84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
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
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fb31235783601bd59538e24e276a9e82866c05187cf11f6d7f103ee2da2a7f`  
		Last Modified: Mon, 01 Jul 2024 23:58:28 GMT  
		Size: 135.5 MB (135494054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:965a639b56106ba77fac71d5b0b2e2f8114a828582516f98cef43a205c3b8ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2019193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d60b0f9f418e28f7812400eee4286a6eab36af7568d7a56f1825867be648fc`

```dockerfile
```

-	Layers:
	-	`sha256:13e00de8f3ffacd80d684cdd1efe9581c3ea60f160e70e62f633bfd2165b0a9d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 2.0 MB (2005635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0bde9dec7dad702d9174dc7c6f4269c8aba29f158a8a8b5ea457a772046d3f`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:9caddcc5130f064ad583b38d25b35976f8fa1d80f01c3c0e7dfcd9ce63fb6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161218052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302e9342effe91a3bed89461e74f1f5cf68904a23e3c1a403e5e2030f0237df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
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
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765dbfcb4c1b46ddc1850a42907c8b085aae31b3a7011bec428c88f2e42058a1`  
		Last Modified: Mon, 01 Jul 2024 23:57:01 GMT  
		Size: 131.8 MB (131775574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4f3474545b0c985f4aabffabb11929af627fcc7bc9984eb5a81f2572054d747f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2015218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0185f46eade1974b889ef4ecafd65120663a10cf324092cdfc0d238d5eddee51`

```dockerfile
```

-	Layers:
	-	`sha256:7ddd66171008f794aa45628f5209edffdaf8b58e16d506534ebfb47b176a71d4`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 2.0 MB (2001700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b51474b2177138891a5eea1e84b78f256d5a57f71d918dfef4e81b36e03a059`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json
