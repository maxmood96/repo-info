## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:9235483c7197eac70f14d06700217f9fe1a3dfdc96e5df6b5300f193a8c9fc64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3eef89f9167b2d34e8ff3a710c3852a3ed9bfe9f870e7c0dbc481cecef051d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153950340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feed5f22f064ba7392c0890392b6673b603d864be99deb015d5a77f5ba5aee7b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:07f9ec6a4553009171ec20ecdc638afd0eaac432b31f9e1b569f6e4fe9454d93`  
		Last Modified: Mon, 21 Apr 2025 21:48:34 GMT  
		Size: 62.8 MB (62761722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24b8132eaea284321f9c9e5a919cbed970e2f9535ebb5e564418b031dcb51b4`  
		Last Modified: Thu, 24 Apr 2025 20:08:22 GMT  
		Size: 91.2 MB (91188618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d010433741496181d5e6e3aafb7bf065dbc59dba1b73a87c1eba175582080bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5860939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91b41ad63d8ce41f116f6ab4fdda913446b0f4163b8f2f9c07b9378c01d4dac`

```dockerfile
```

-	Layers:
	-	`sha256:8aa12014551a50c339cea4c08701e1e69088f2c794e269e90331371c4502355b`  
		Last Modified: Thu, 24 Apr 2025 20:08:20 GMT  
		Size: 5.9 MB (5851468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73696033d10e00823d87992b1e1cbcc17c2b542b6f53abd83c749f50c2441d87`  
		Last Modified: Thu, 24 Apr 2025 20:08:20 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ef06e53bb8b3ce67d07a6e99995ad3ad3bb7f0f599f96d96badb63e46185d747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146442452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ac95ba54ed9ab36051dde668214c5008d999803a7886bd314b218fdaa51565`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af22006daf85108dec3a22b0675372242eb49e6ef21b63b1f61aebe287d1287`  
		Last Modified: Wed, 16 Apr 2025 00:12:02 GMT  
		Size: 81.9 MB (81876630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:65fe98b1f02e16fb9f37cc3d092ef6adb5aa3601572625a5c5295125988dc90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5650876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fa054b7bb36c941744b8d285f3a7bb51f050648b3cad4cdfcad5f2984d8c84`

```dockerfile
```

-	Layers:
	-	`sha256:cc1c487538ee7fa3e28cac407edb494231f1eaa13d23b90f3632c1ef30b66ab6`  
		Last Modified: Wed, 16 Apr 2025 00:12:00 GMT  
		Size: 5.6 MB (5641325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2cebc93a9d7f4eae18e729f080c6922f3a2ee2752f3708ab61df6f37292145`  
		Last Modified: Wed, 16 Apr 2025 00:12:00 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json
