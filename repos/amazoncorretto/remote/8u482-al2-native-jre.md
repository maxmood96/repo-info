## `amazoncorretto:8u482-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:3e08c92ea0a5d30a4bcaed7694c16212607ea2c239b08ae9a5fc62d8e5b66eee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ff7b72d062ece253b26e7a011766c1416d902bae6b8709b87b5b455ae787c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172089732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af73b1b9eccc21f08261857f8ba0dd6342a59ed80e6dcf0083ab94115072038`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:23:57 GMT
ARG version=1.8.0_482.b08-1
# Wed, 15 Apr 2026 21:23:57 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 15 Apr 2026 21:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:23:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f99d4bad1ce2ade55e95140173f9deea1a7612d0f93ae0f3645db712a9b28`  
		Last Modified: Wed, 15 Apr 2026 21:24:24 GMT  
		Size: 109.1 MB (109134466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d62524facbac23721a524427f7caa7d9bd151acbdce307266e2e7e99e63c33d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeeb716596b90ba7a683ff06016ef59fa9ff697504b18e829005d47785420cab`

```dockerfile
```

-	Layers:
	-	`sha256:ec6d85635af9496a160c44153777847767d9c82a5e3e1ef6d8b2ff93eb5f7f07`  
		Last Modified: Wed, 15 Apr 2026 21:24:21 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb1d7e1e2d818b3260b692b94e1ed73ca6643e2398344887ca9420e68900339`  
		Last Modified: Wed, 15 Apr 2026 21:24:20 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c5537df5e149c71652c0a660f6666b56893a6fee099bc991d874d3abf76eb98d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117771860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642ec135543f033bc9f095dbf21a796cd15facb38f2e7b35b40e0dad035a15cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:38:11 GMT
ARG version=1.8.0_482.b08-1
# Wed, 15 Apr 2026 21:38:11 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 15 Apr 2026 21:38:11 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:38:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7335b0edd6075c7c296171a5d9c8d86fc0d958687d22eb1adca4044f9e815b8`  
		Last Modified: Wed, 15 Apr 2026 21:38:27 GMT  
		Size: 53.0 MB (52968885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:63a431487db9a956cfc88af4d33947f858bc4464d3474480310eb6a6bf001aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65802a672773eff4ea0c0d127af2f51e9e39d3c3babaf104741a91e29cf70693`

```dockerfile
```

-	Layers:
	-	`sha256:5612ea65068b6b3031f17f823bb85bf2748e634a7b71aeb2d99021216ee2bbee`  
		Last Modified: Wed, 15 Apr 2026 21:38:26 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1b02bd6ef48712f72fd9a27556dd922d5f4cd701a1ba4103205ad0fcc9348d`  
		Last Modified: Wed, 15 Apr 2026 21:38:25 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json
