## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:fa851c291064837287401ef40131e797825b9ac5bd0d2874bcefe778ef160663
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d0613caa40c061fe8c178cc1a7278463b333bed955ff299cab0593363cba24b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172062191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7063715293a2e869b291fac04939c144768cda9a72ab76535aa68e0ad9bbfdd7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:06 GMT
ARG version=1.8.0_472.b08-1
# Thu, 15 Jan 2026 22:09:06 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 15 Jan 2026 22:09:06 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:09:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:13:55 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc003f01e4811c0b57016376f309088e583f04ee68fde0077acef26b6ee8c9c`  
		Last Modified: Thu, 15 Jan 2026 22:09:45 GMT  
		Size: 109.1 MB (109122035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cf458e5bfb6b97e87fa5b319784d120bb8ee848fd0be36e09d85b7b5fecac1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda9d86ce6a399594a61d81c1544ab0b1da5d0a36a0e154b71862c09d4364f6a`

```dockerfile
```

-	Layers:
	-	`sha256:312e35349f260aecd32cfd9c156e528073918ebefb1db047b8f7ad727ed96fd3`  
		Last Modified: Thu, 15 Jan 2026 22:52:39 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daaee3c2b300818d493caf65ddb54be7e55019fd08cf9808928da69a93311c9b`  
		Last Modified: Thu, 15 Jan 2026 22:09:25 GMT  
		Size: 9.5 KB (9505 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:be61d20f7c4ceae5d845eb572001c2b6633e32648adb1182257fc0dff6380ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117704447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e1699da0a8304054c462f67395c08fb67d41d8cb23996ab0cd1146bf1cc75c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:17 GMT
ARG version=1.8.0_472.b08-1
# Thu, 15 Jan 2026 22:08:17 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 15 Jan 2026 22:08:17 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 07:47:55 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10c6309ea52ef8d882b54d9ae77b56578e6d80df0b8323c9c4ba49f585bdeb0`  
		Last Modified: Thu, 15 Jan 2026 22:09:06 GMT  
		Size: 52.9 MB (52934013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:797225d73f6ed0e22ca45a306a2353db5206418122c100d4bdd2cad4b35fc511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2430209b719a6e3ccb1a227f3dc2231fa6a84cc7b5762839c6b5153d6613a17`

```dockerfile
```

-	Layers:
	-	`sha256:6d2f5736260c0282fb462f84b977f4e9c2b044e300f7722533d253ee3c98cbe0`  
		Last Modified: Thu, 15 Jan 2026 22:52:50 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d82c6a6ac9265e36af07038210e912665fa1e9e90fafdd8d9067d9ca955511`  
		Last Modified: Thu, 15 Jan 2026 22:08:30 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
