## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:103d2a5be34c4c3a9b83c0d89ae35a371d5c6912765b5a63654ecf01d63c0095
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:32417788a805ae05ebd4fb06266ecb43af8ec2e6c9ed7d9a19b63f5e0fe0bbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172083241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aed6f9d8b5cf85c30aa0e92f5981be2c07e938e649bd8dd62972a8d024f1e34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:28 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:30:28 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:30:28 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44860ba25d72466144b9f209b8aae1212ac9a9ac732f679b72abc61af14eb7c`  
		Last Modified: Tue, 10 Feb 2026 18:30:49 GMT  
		Size: 109.1 MB (109124284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:745deedf02936d737dcb13c5b94d157198a75087c730571f605d7ecbd8b48f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45332a89fad14ff911ef5680d8ff947fd6ff3f5cd415d0368480e6093e673aed`

```dockerfile
```

-	Layers:
	-	`sha256:c42aa151ea7a30d28103ab5251d7383f39b733bc43ae2d469dc9de285b14c632`  
		Last Modified: Tue, 10 Feb 2026 18:30:47 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f8c5e7dbe03a16404d22d0d78488d9ce912ae32351724f76025d4824ee387a`  
		Last Modified: Tue, 10 Feb 2026 18:30:46 GMT  
		Size: 9.5 KB (9505 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0ecdb8ba093a5f3d4a4ccdcad1686a870d176cc37156a5a7c7763f6671d39ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117774814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c76fb71cca0313228dbf11d5c5cfb9b7793c1b615191356e3a135f16720e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:37 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:30:37 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:30:37 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55fe14de2179cfb45d85b36b9899fc908746aabd74fda41704fd5d4ff8550a7`  
		Last Modified: Tue, 10 Feb 2026 18:30:51 GMT  
		Size: 53.0 MB (52975338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:17333da865ee3b86630817785e9c95f595b7e8273430996508cea49b55997bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2c294253181831e138ef3cdc67c7aa4ec05b6b2ac1965d5d06937cc00feede`

```dockerfile
```

-	Layers:
	-	`sha256:d1835ec6ba8aad329fd024f6b651c14efc1898d4d4adbc294bf1ff4daa73194c`  
		Last Modified: Tue, 10 Feb 2026 18:30:50 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9b973a045de5de8b04ec109aae0107354d0cab9c5267a4e0856a447587e4d9`  
		Last Modified: Tue, 10 Feb 2026 18:30:50 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
