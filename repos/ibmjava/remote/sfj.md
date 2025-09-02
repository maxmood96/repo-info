## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:4ec5ec676425fb478f0ae549cde3d361a5f790ef7de8479cfe0477971ce237b6
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
$ docker pull ibmjava@sha256:421e9751c5046f12ab49d6d12d3d8654c0a89579837e85dbc4648a2bcbfa69cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101766416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26540ccbd2f59c970e4f5088dc74ad20ec3dfba7049664773770f5c61184c032`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Aug 2025 06:32:13 GMT
ARG RELEASE
# Tue, 05 Aug 2025 06:32:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Aug 2025 06:32:13 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 05 Aug 2025 06:32:13 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e82fa24af564814fde5b9935935ddcee4a20f1a264469802f41069e3b38f8bf8';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3ccbe3ca1ffd097f40b06e7c4f31f4a38de361e5c8116ffd4a030df5f5303519';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bcf97b069ac7fbc7dffee303e1934917668d73af2a9b426ccb1b91e76e46eee0';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32a47164cccb60875bfbeb72e9958b1e034a28f541fcdf8d48ea0644f90fe68`  
		Last Modified: Tue, 02 Sep 2025 00:22:44 GMT  
		Size: 1.5 MB (1450049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fdabea96d3f18620dc327314c98f105a69f987d632c9abaad397b0f7f5b91a`  
		Last Modified: Tue, 02 Sep 2025 00:22:49 GMT  
		Size: 70.8 MB (70779432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6a57215ed0426a6fca3ff90c7df9887d0f3f16f1b9a65d6b6ed7d479dbd203af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0200874f13b896930601b0de2a330edcd00609428a8db2b1c8d44f401c52a785`

```dockerfile
```

-	Layers:
	-	`sha256:41a9b1f0987302eeb27dad1d8476f64daa90ecae8b655cb7edcadcc248ac0011`  
		Last Modified: Tue, 02 Sep 2025 02:01:38 GMT  
		Size: 2.2 MB (2155973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726293ddc801daca0087b5a060adaf6fe883f5e20f60a48a3c01e2f02e1b3365`  
		Last Modified: Tue, 02 Sep 2025 02:01:39 GMT  
		Size: 12.6 KB (12644 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:3ed20ad26dfd89ec186f0a0bf8230a51b7165663efa07acf75aca8f60ffac88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107698386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527f40f8ee02deb02dac137a48a587ec32b0f39dce93ad6113bebddc5b930eff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Aug 2025 06:32:13 GMT
ARG RELEASE
# Tue, 05 Aug 2025 06:32:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Aug 2025 06:32:13 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 05 Aug 2025 06:32:13 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e82fa24af564814fde5b9935935ddcee4a20f1a264469802f41069e3b38f8bf8';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3ccbe3ca1ffd097f40b06e7c4f31f4a38de361e5c8116ffd4a030df5f5303519';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bcf97b069ac7fbc7dffee303e1934917668d73af2a9b426ccb1b91e76e46eee0';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d192c8447a05338f6be98b961be219ec48c73dbb11447b3a780880ae17380635`  
		Last Modified: Tue, 02 Sep 2025 01:06:08 GMT  
		Size: 71.7 MB (71718947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2652fe157619a79ff3d3c62120fe19a555d42e4033454da9c2e4c83131bc7cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c372c3c689591f2289094a351c6e394032bcb7313323c9aef94dfbda0fcc32c6`

```dockerfile
```

-	Layers:
	-	`sha256:381da016d3c8fb8579a1592e08d3f7132f2df31e7ba200b238a820c092b81864`  
		Last Modified: Tue, 02 Sep 2025 02:01:43 GMT  
		Size: 2.2 MB (2160474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935b4dc739528a61c5c49f2b648c2a3f75defde0504bcf049f8b53a0fadf1743`  
		Last Modified: Tue, 02 Sep 2025 02:01:44 GMT  
		Size: 12.7 KB (12678 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:20d52c2de78f59918db1f7a34a8f09c557b7c989a5a58121abf70718a8c62f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100737258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d418cbf31bec35432c9a84a00559a252dad30f1d92628662dc42a2fd8a7a47`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Aug 2025 06:32:13 GMT
ARG RELEASE
# Tue, 05 Aug 2025 06:32:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Aug 2025 06:32:13 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 05 Aug 2025 06:32:13 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e82fa24af564814fde5b9935935ddcee4a20f1a264469802f41069e3b38f8bf8';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3ccbe3ca1ffd097f40b06e7c4f31f4a38de361e5c8116ffd4a030df5f5303519';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bcf97b069ac7fbc7dffee303e1934917668d73af2a9b426ccb1b91e76e46eee0';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bf2d3d267a3b9732481174fcba7d138507ff103bf415dc927e0315a8dba6ad`  
		Last Modified: Mon, 01 Sep 2025 23:52:51 GMT  
		Size: 1.5 MB (1455714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db04bd8db0b57abc54e137234d96efaa921cecd085e12a2ea94ec0b383ff8f8`  
		Last Modified: Mon, 01 Sep 2025 23:53:44 GMT  
		Size: 71.3 MB (71277876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:1fb5cdc1dc41b357874051a92cc0902a5e82d3a5cc7bf01c373d6cff85d8a378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f615e26c002061730cf7eb599d06a449bae7b74e0e7c4e4d04ee5a83035ae2`

```dockerfile
```

-	Layers:
	-	`sha256:5b03e02ac2a9c92d55aa2e74937b070a6ca70d6fd41a7605fb3271439bb7b123`  
		Last Modified: Tue, 02 Sep 2025 02:01:47 GMT  
		Size: 2.2 MB (2159595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee1f77bc2cc02f04d1557a8bf888bddf19977a0bbff514d157f440fd74eaf4b`  
		Last Modified: Tue, 02 Sep 2025 02:01:48 GMT  
		Size: 12.6 KB (12644 bytes)  
		MIME: application/vnd.in-toto+json
