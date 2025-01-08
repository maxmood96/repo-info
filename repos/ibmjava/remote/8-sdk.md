## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:a4fe5321c6ca3de2a926cf62d4403a99dec18fd17c2dd7d8a813f8af261053a2
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
$ docker pull ibmjava@sha256:ad40127a9cb7644a8840bad89c5036952c5a37c2c602910df0f15f9f1dc4873a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203707324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06fbde8b6f29b73f24767e3bd1d4ffa1413c43221b9a9315645050c7fdef6b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690120052cd6d21f254e5b212f4fb92130cf8eefd618b563c0646438b1a4f1f8`  
		Last Modified: Mon, 09 Dec 2024 19:29:07 GMT  
		Size: 1.4 MB (1449633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e897e8a3ce3964a6f11856395edebeef9c3e457e8dfd5945b32d3f714c640a53`  
		Last Modified: Mon, 09 Dec 2024 19:29:11 GMT  
		Size: 172.7 MB (172722003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f58c06154f94c6cfa7a84463499dfb9aae2db334daf411261291dff9d34417a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2975412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af5a785d5d471c51caca242bee7284433f4a99fb5c1abc0e90dedaba0062959`

```dockerfile
```

-	Layers:
	-	`sha256:f90da5c0e1b0b0aee9f2cc75137e859fe45c320f44cb47975d0649ade6d6f18d`  
		Size: 3.0 MB (2962234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46f3970ac6b57e31c08a3d518064fd9ae43b155629b2e5982bba1df4fed3d8b9`  
		Last Modified: Mon, 09 Dec 2024 19:29:06 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:999a1f87c1aa701b9b1b5efeded133e271c89f79448bd2f131f8221d8c89bacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209734067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c2874d497c370ad59aac163c568f0ab75b93617392f2a903bf6948415b2b36`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66afe9d4f948d68f54ec6defff14cff5750f89a8e79d8b5e4e8e2cb5d07ea235`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 173.8 MB (173762580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:dd844f786a96c658b63df350fed7012435af9caad46fab830035418519d641ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2955372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0586c2b50657aeb67d0e4a0927e53cd42d3f8bee28aa52eb5c7b2f55563a46`

```dockerfile
```

-	Layers:
	-	`sha256:422ba8a5eeb7217706206d64bbc7051714f5c603d1df043fc0d4d4028f764fd5`  
		Size: 2.9 MB (2942160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa50e59fac267236465ef4d5cc7b4db37a876e8618e537e6c2bc23ddb247cc6b`  
		Last Modified: Mon, 09 Dec 2024 19:31:58 GMT  
		Size: 13.2 KB (13212 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:16fa692d6c60bc9b7abe2f38c589e882dc607651c59a506c32bf89dff0743e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192287190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bbc40d559f37f53caf6a925b9223f731d3a84efbb8bb56aab60104480a4fba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
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
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4400326614b568e7fa5e271ba2b12f9fc40b2d302626d86d824d5b3330bc3e8`  
		Last Modified: Tue, 10 Dec 2024 02:26:24 GMT  
		Size: 162.8 MB (162843801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a291ee3ff11abaa193c97e73071426461530b051df61991fe6e5e2414863a9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2644882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8277c518e05957425ee1b0ff5255ba45a21412da7552850f2a37a03a19891d90`

```dockerfile
```

-	Layers:
	-	`sha256:410ba7837a2cadeb3a32d0ee9d8c61dcc7f3ac4750aa490182771517176c2175`  
		Last Modified: Tue, 10 Dec 2024 02:26:21 GMT  
		Size: 2.6 MB (2631704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edfc0d07849bda6c9e8c4a0c3a6ac392024198ceb7c20c5c2cb67f0717b779ed`  
		Last Modified: Tue, 10 Dec 2024 02:26:21 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json
