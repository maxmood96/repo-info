## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:8378fad5a3f1bcdcc7d9ed6bf73b6eeef427c0dee0654c40cb97c91de975aba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d8ebad340446269599e7d9022ea3a1517a966300cb96b3c396edf5f5a35566e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187889929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a0df6108c7c3b8105e3b21189a897fb2e7d66eb0d268d7b8a5f12c74cf0009`
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
	-	`sha256:6eeabd86b075e80cf303c4a0348cf048d31ba6ae2d42b051bb230016153f8809`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 62.7 MB (62659944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e518343556a05e624f54f47e2cdc0d5b6c6e6054b3ded9a426ab35feb7e9d60a`  
		Last Modified: Fri, 23 Aug 2024 01:50:44 GMT  
		Size: 125.2 MB (125229985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:81f10fdf2b3e5386057cae0be9c04cee5730f13b4fcc3ec4cabaf60450ee1838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ead06dfad920b80fdb72d37fb1b58c19af4ffdbf1773a3ee0413fb85369b7b`

```dockerfile
```

-	Layers:
	-	`sha256:437335503b1ec0da4b6e16ee2e86515fe938455e982db30f3a2703654913442c`  
		Last Modified: Fri, 23 Aug 2024 01:50:43 GMT  
		Size: 8.0 MB (7971184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7f6cf28da5c3293858db37c1d505fabf22e2d317cc2430298eb79d2d09b464`  
		Last Modified: Fri, 23 Aug 2024 01:50:42 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

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

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

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
