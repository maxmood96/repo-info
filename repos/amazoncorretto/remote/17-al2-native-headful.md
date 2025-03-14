## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:736426559e8e5595dbff8d6cade062117e272fd004afca94b4567e1ffa60a2da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:27f810a4e9d5606c66243adc19aa81a459fdfa149a17b87a81c961f03369cf91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153932762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d875851fcc512084de4c5ed401a4cad9fc586d3d31d3f384cb5cf9d0066f4934`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06bb3ad56dd182284e64499929da62fc86fadd091e7d5f71a70fc7ed8bc2dcd`  
		Last Modified: Thu, 13 Mar 2025 23:49:54 GMT  
		Size: 91.2 MB (91159924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:13208c21ecd1e9bf2b4570eeebd00fc174545520643a67b5574b9d34645fb0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06af1f677fa49dd8c9ba717b6666ba75a4c17684716dc34b41e616b6bf63a5bc`

```dockerfile
```

-	Layers:
	-	`sha256:e60d7824f3d1f014739a43524fc865b5f41658676d2549eebc4fd7aa3a8e8801`  
		Last Modified: Thu, 13 Mar 2025 23:49:53 GMT  
		Size: 5.8 MB (5849556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16ae5ff2b157bcf7be8e49091d629a95f10dfe6f75a15becf743c06834b46e63`  
		Last Modified: Thu, 13 Mar 2025 23:49:53 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d000a29f51da3eb17976c9828c103c3fbab1955d6e0bb198a28967fbcf30377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146343672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c477afc639d89c4a42d3c8f34013a0c907e2920c773c2a8be1f59262c8b468`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1756ffb1da431c865aab86b702f864e934727fe58d9a7eb92e679afddf6083a0`  
		Last Modified: Thu, 27 Feb 2025 21:19:46 GMT  
		Size: 81.8 MB (81822464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1028193614ecc76ae6e766d34ee305740844456e0c2fdea49b18f91a70f1d3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5650849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439ec3a2312de3e714b952a6f43e5ac6538b812c982748240899cfa4911563f0`

```dockerfile
```

-	Layers:
	-	`sha256:780a16f2c8a518d45f44a582909e0a86cb1a8f44f40e1c954e0eaff416265ba5`  
		Last Modified: Thu, 27 Feb 2025 21:19:44 GMT  
		Size: 5.6 MB (5641299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554b78f5917b267d4e965e5eabcaf4af87a1eb6002badd4fce75dcf9e0665eb9`  
		Last Modified: Thu, 27 Feb 2025 21:19:43 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json
