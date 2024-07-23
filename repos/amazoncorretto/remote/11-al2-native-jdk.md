## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:4dbd969b6923563377e1da2998859cb2c8da16debcb9dcd3af693997ce6573ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7546405f8c3b8f28d2b3aff6afb9f21f35a8106dab7014e1c30e328143cbd2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224761419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e09c1bf715093c216a955a68d92c41d94c12937e29ea4d330f419cc5d06c15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:23:24 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Jul 2024 21:23:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:37766f9d8ddf179208313163dc89d8d39dc16ba3be3bc46534855c244565cdd4`  
		Last Modified: Fri, 12 Jul 2024 13:12:20 GMT  
		Size: 62.6 MB (62649406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ce4b8817c0c6bfa0ac67cf9c10d67b4a8e3cdb25fd7161fe00f15d5dde7a88`  
		Last Modified: Tue, 23 Jul 2024 00:07:48 GMT  
		Size: 162.1 MB (162112013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:846909243e292b38ac5f75330922e7ecb6a5cb2167e0685ac2fd8445baf5b35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931acdbc3455c00cbfc7465fd47c45bf729c1a7788a446ef0db2573e8ea8279b`

```dockerfile
```

-	Layers:
	-	`sha256:4e4ed744063c0f41a99e9da14b1545b02f20063efc75e30fa39ef796731d94f7`  
		Last Modified: Tue, 23 Jul 2024 00:07:44 GMT  
		Size: 6.0 MB (5990309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c67a21866300b582ffaa33dd9a9f56786a807574b9514e6075c89ac52e88a74`  
		Last Modified: Tue, 23 Jul 2024 00:07:44 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:901b54eae64dc38578ecdbb7627c927787212665443250c69442c692ae787aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216876138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416dbb5677d073430f90b4104d44eb76a82964d4fe960d2c69dd9f2d5cc3c07e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9c67cb358d4965bfee42a7a7926eb24f420296caab09619e07c3fb50203bb2`  
		Last Modified: Thu, 18 Jul 2024 22:54:24 GMT  
		Size: 152.3 MB (152300827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:60a8ddfcebd1ebd35d1bf5612207fcbaa9b251fdc0f61fe5f888b5756fe418fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aaad457d11c458123a047b2c331286f694efd951c0e956b91c53fe1e96297d`

```dockerfile
```

-	Layers:
	-	`sha256:689b6781991a7360258488379b08794b723a2ad2de2165f140af124bb14fdcc8`  
		Last Modified: Thu, 18 Jul 2024 22:54:20 GMT  
		Size: 5.8 MB (5782684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8050639863bd7d344b322098c166818ce31d37f9a083eb94656139416ed9b190`  
		Last Modified: Thu, 18 Jul 2024 22:54:20 GMT  
		Size: 9.5 KB (9479 bytes)  
		MIME: application/vnd.in-toto+json
