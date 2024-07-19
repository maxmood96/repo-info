## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:38e171826fb982092ce3398a2c899cd6d283f429c13f508f01fdfd25327e4cea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:193df28fcbb7cbb652ccac1973b7ca88c390817a19fa8b952dfdbc4def974f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224759439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210f9b365fd34c32d0245c6da401015ee1cc4a41597ac653afab2ab455a337dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
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
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc34703ecf17ed008a133f625f0dbbfdb2f6052c7452b4febb0593dc4e8aff85`  
		Last Modified: Thu, 18 Jul 2024 21:49:45 GMT  
		Size: 162.1 MB (162111513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:91021785c08d5b7581b690445a8a05cd86fbee76f029380c53dbfd9f95cc8ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fec5480066fa4449cd9ae1d8e93e22c59af049c2dfd1b828b7d81e2c50438f7`

```dockerfile
```

-	Layers:
	-	`sha256:8a30097ddb0fbf0d8fdf26e6369bb37a8b12331d766e25229e7ea25eca3d5f2d`  
		Last Modified: Thu, 18 Jul 2024 21:49:41 GMT  
		Size: 6.0 MB (5990309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5dc8d94f14bb6c296e88322d8fe8735eefd7c079d644a9bfece5049944d1edf`  
		Last Modified: Thu, 18 Jul 2024 21:49:41 GMT  
		Size: 9.2 KB (9201 bytes)  
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
