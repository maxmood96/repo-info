## `amazoncorretto:8u462-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:7438afeb516daf8e7b24a684529a9fc730c3aa8c0072e7f9c128d97585ccd1e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:360999e1869df6821722000419d809c03d52b884c2d29d5e02a364b2a51a1feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188268042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b657bc9070850f287626a1250ead18f00ffc3d407162772f6064718a23e2f69d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750ceb76f6a9cb88d7315eac762d3c4b345df5e01e1bf5e9730249081eb87def`  
		Last Modified: Mon, 25 Aug 2025 20:18:16 GMT  
		Size: 125.3 MB (125289917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b271aac7e273c6a97fc695bf3bc1acccf0fa56a0751208335b907ba8dc8433f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a11b6495d564efcd536059afd07cd7152575e0f995041290702101aa18b344`

```dockerfile
```

-	Layers:
	-	`sha256:a175c9e34a504c6946fc389cbba1439a44c0efe9b399b144e81d2dff2d3249c9`  
		Last Modified: Mon, 25 Aug 2025 21:50:09 GMT  
		Size: 8.0 MB (7977406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262ff73053beef76d0b76f16ed551e3394bd65ab7053b0706e4ae9c4cb7bdb2`  
		Last Modified: Mon, 25 Aug 2025 21:50:10 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:786059973b50fe168d7fc555888b2c3e12d8744c08ffd6b9b5cb350597e8926e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132340843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5260edb9ad387737a3fe50efbc619d45d8d5c73464e2e76ace9d51ee981c65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8159b54a0a1bfbf6a207a66823e8de25f22d7023df0e7eee6c7569f711c469`  
		Last Modified: Sat, 16 Aug 2025 05:12:05 GMT  
		Size: 67.5 MB (67546479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:616883ac717beeec1a7e6c5f362ae1f8a19248bd28f26555597d1bc981571827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ea0e1d50acd621cf0b19a1edd0656d401a7dcdf198e42cb7a96a51b896910f`

```dockerfile
```

-	Layers:
	-	`sha256:457ca8c67b3d4347c5cb17914f7c2b576062a4a13c8f815d3c65faedec768df3`  
		Last Modified: Thu, 14 Aug 2025 09:49:50 GMT  
		Size: 6.1 MB (6082937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c201ceaa1fec15c29f1bc7ed3b09c4b3d0f737ebc79b4c5abcab61e4ba3b29`  
		Last Modified: Thu, 14 Aug 2025 09:49:51 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
