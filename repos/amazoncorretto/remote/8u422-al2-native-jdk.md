## `amazoncorretto:8u422-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:fbde816f176cae878bb142f7566aefb05e069cda8921f30f8c37ce1d34f16832
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a195b41dd2558d5ba5bc5334fc9d5db4abad91b43497f4bb9eb99b4b2de2ac3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187944706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fcb9ed54871663a914eb9880e1a8839e520a9fa97c4f7287a6716f2c89738af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d96c7b757c3cdc0a389751a9083b02ab0787ff69c25e2bf64b62a4e186e9a47`  
		Last Modified: Thu, 25 Jul 2024 21:02:39 GMT  
		Size: 125.3 MB (125265540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6e284ae26a5f121821e28c90aaedbde8bc75fbbf4b70f0a9b933e7ed73a9ef92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d742ba6a37a686d9232c22d624068e6ee17c9165f401b4dfd1fdf3967d583557`

```dockerfile
```

-	Layers:
	-	`sha256:c42dcf4b3964807fade0e9bb3208aaf2dee8426d1609efb9414be7208e8b3d27`  
		Last Modified: Thu, 25 Jul 2024 21:02:37 GMT  
		Size: 8.0 MB (7971152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e65401ef4d834bc101b851725b9ae2267ba004d06c010c3047568ab71928a503`  
		Last Modified: Thu, 25 Jul 2024 21:02:36 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c0bc74543a8e6a5dedff4c276aeb9c9d526e44c0e36f5c3e8343c9230e4c8bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132121024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744927f3f77cac778b1d404e7d1215e1c2eb1646be182750cba3c07fae8b313d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb52a7416df2151690df2d3c8f9bfcfb66a837a4e274eb6b6152a54a4e6eaaf0`  
		Last Modified: Fri, 23 Aug 2024 02:18:42 GMT  
		Size: 67.5 MB (67533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c408bf7c2867febe797903a2ffaea35c2fda5e652bf5f9bbf7d42ecfe54c2ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4bba11619e5180de21b4ba0abc59108664809616e004ba0fbb90d93fcc36e5`

```dockerfile
```

-	Layers:
	-	`sha256:eb833b81c1fdf14c761286db79bce58892a590b48c79128a4512c7c611dcaaf9`  
		Last Modified: Fri, 23 Aug 2024 02:18:40 GMT  
		Size: 6.1 MB (6077709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039885578ce552fbba93a1985284633fcfd55e6d2c4bfbfe833ac1c5245f4d57`  
		Last Modified: Fri, 23 Aug 2024 02:18:40 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.in-toto+json
