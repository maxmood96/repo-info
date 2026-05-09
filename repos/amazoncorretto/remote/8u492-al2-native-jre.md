## `amazoncorretto:8u492-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:67af64d288f49805b4469bfdd8c0b36ae663038ec7f387a1a8bd49689a76d651
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2182f779080ee99ca0cb359bc7e7c7d76434fa000e4d0c1414b8194c13ae1a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171946724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0047d30c6d38f5e1ebe24a0d1d2686b614ad1e5ecb29cd71ccf6eadf00cd975`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:56:20 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:56:20 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:25 GMT
ARG version=1.8.0_492.b09-2
# Sat, 09 May 2026 00:16:25 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 09 May 2026 00:16:25 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:3f708fc5705625846e206621966842bfead7ee5b8e4fc20aab0c77c563600126`  
		Last Modified: Wed, 06 May 2026 07:46:46 GMT  
		Size: 62.9 MB (62859738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3c03e563cc3c6e1e022c2c3855952601463844cfd4cd39c35f1c69c732577a`  
		Last Modified: Sat, 09 May 2026 00:16:47 GMT  
		Size: 109.1 MB (109086986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:14fefb0263c9daee99903dc9c916d8f3ce1943be0aa1a56867c13b15048a060a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31e3688f03a852ee1fdb73825ba5d6cbf23e17af6dd1b043ea5d42a3f7e4560`

```dockerfile
```

-	Layers:
	-	`sha256:aed868f906be917f2bef494ec0b6452f30f300622e2a0ede5e011a3243bc8918`  
		Last Modified: Sat, 09 May 2026 00:16:45 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407014c39eba4a3c25d144cefdd7fbe2c8462c691f4e6aea22eab3a1a7b079dd`  
		Last Modified: Sat, 09 May 2026 00:16:44 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8b46daa4fc202108f8532e7924965c484e3b325028651678a5be2bf7c22d7608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117772978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4446571ec80314a43556e33fae65f7bfbd18cb96a6f1759c2014aee6bc908ca6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:14 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:14:54 GMT
ARG version=1.8.0_492.b09-2
# Sat, 09 May 2026 00:14:54 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 09 May 2026 00:14:54 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:14:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:835dd3779a793c24eeba54a176badcbf0ecf82042603b5459dd57e14ad679d47`  
		Last Modified: Wed, 06 May 2026 07:46:52 GMT  
		Size: 64.8 MB (64808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4bb1ffa8d7d504d7023f719f74276e71a10addc73ab046b8f324f8607a5f2a`  
		Last Modified: Sat, 09 May 2026 00:15:11 GMT  
		Size: 53.0 MB (52964063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e3f6750f2d71675d60ebaec936a294bb82678c83aae87a4bd3c22eb22573e9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae7c8dc9a2060206ecdec3374d714309d31d34ac83eedd45d59ddae4adf5762`

```dockerfile
```

-	Layers:
	-	`sha256:205c56ecfdbc4a7f8885491734d65d76f4d8bdf041fa2c7aad91df9032e4ac4b`  
		Last Modified: Sat, 09 May 2026 00:15:08 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab35aabd15475dc7921011367af60cdfee401cd6be2704113760bc9068c9ed63`  
		Last Modified: Sat, 09 May 2026 00:15:07 GMT  
		Size: 9.8 KB (9752 bytes)  
		MIME: application/vnd.in-toto+json
