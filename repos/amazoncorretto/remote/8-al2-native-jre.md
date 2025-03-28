## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:f0e273e455c190fdd382b0215c7d4601cb923649002905452c4e866124cd2784
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:83f0b3cf6ca9690377040f9569be2865ad80088e349a0518f9365e6833538caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171854235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539816226bf087ecc5d72ab47b0d86412681a1ac56f97a44e83ac7f90052d20d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=1.8.0_442.b06-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5355535d886da3065908ecc2f91808ff7d2ce5c31b8778ea6abbf6dce026f2c7`  
		Last Modified: Thu, 27 Mar 2025 23:58:40 GMT  
		Size: 109.1 MB (109101346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b68c9ad1f09aa24146af3d13f6dccaf6d7b342872f938802aef81d036acfd5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348bcd5b523f87c8bfc15692fd525d8d2e33776d421aabc51c148a320f61b5b7`

```dockerfile
```

-	Layers:
	-	`sha256:5246e7c8b9c15bf7fc7c4e9d833e28450fa84c17d923eec6cfc7c88825c2ed2c`  
		Last Modified: Thu, 27 Mar 2025 23:58:38 GMT  
		Size: 7.5 MB (7483409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f099ddc67aa23b3cbfcc0067e6c6040979220d91796558eb2b166a248bb666`  
		Last Modified: Thu, 27 Mar 2025 23:58:38 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a32ec9316d4a6c10d70f63820822e3accdb668f065b2cb5bc09a3d8bd35098ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117477453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12158f2d759caacc22211e243c201ed8eb5df84c5650515c5bb17f2f104a807`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=1.8.0_442.b06-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda5e4f56ea6ccd03bd817e56d0216bbbb2dd273bbab9b77756512c70c49116c`  
		Last Modified: Fri, 28 Mar 2025 00:06:17 GMT  
		Size: 52.9 MB (52911631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:37de798469401bf51d5f1de1e8dc1fed4d5351b34daac5cf28674fa91849a294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5b53a220fa1935a132b4743328d5df0ee5b97feeb12599b3465dd2a79c8196`

```dockerfile
```

-	Layers:
	-	`sha256:86e77f55c12fd31392129c5dff6b461822f1b3916689a86e9459597638aa2ce7`  
		Last Modified: Fri, 28 Mar 2025 00:06:15 GMT  
		Size: 5.6 MB (5602808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff69a9bc89e2c272abb36597fc481e95645ebc46fe266a5f212c1b034fcef99`  
		Last Modified: Fri, 28 Mar 2025 00:06:15 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
