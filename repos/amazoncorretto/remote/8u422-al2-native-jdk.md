## `amazoncorretto:8u422-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:295f7c7eac16cb2d6a81bdb548a1f863bc501c14837d9742b1a2b256b70f67a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b98482452462c18a980503ef48029207a31882a9ffb39d27d127f9acc7e4e43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187958073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcbb7d780cf936dc9646e71fe744c111ba1177ea83df9d842c716d307c8618e`
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
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850bd3afe14eb8c20378733c541bb7651e07b2321d12cf6380d6bcf871590c6`  
		Last Modified: Sat, 07 Sep 2024 01:06:13 GMT  
		Size: 125.3 MB (125262526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:22e59afffc1115d45b0875e0fe61e78a9bff8d0c65bfc6bf5f7f3c215f95ed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5aa2a3a0f78bc2244eac2bb335cf082343ee49fa3a471c86b0cc630ed9520c`

```dockerfile
```

-	Layers:
	-	`sha256:58ba6fb8e99a05ef1d52bed7f20281e60b6b388991dd0fc25cb22c17d055a556`  
		Last Modified: Sat, 07 Sep 2024 01:06:10 GMT  
		Size: 8.0 MB (7971184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1f64e06027102343204337aec080ba915a0f3fcc80536006ce1e57963ceb43`  
		Last Modified: Sat, 07 Sep 2024 01:06:09 GMT  
		Size: 9.6 KB (9559 bytes)  
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
