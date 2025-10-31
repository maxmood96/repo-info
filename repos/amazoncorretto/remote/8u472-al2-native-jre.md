## `amazoncorretto:8u472-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:e5d91106659dd4e08896e6a57f1be44bd398625e8f194b6e6a352d5423d0934b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f4f4fc85feb690039859455203fccb28017c9679cf514e5bf85e1b1d25cfcb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (172041228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5987906edfdc91f8be1a9ceccb8f5cd7cc5b64a585f898767a1b27cac4a03e8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:21 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:21 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:11:21 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15af8eb3706ca5c6f311227a15ef45dff4a34e0f0270f0769462235fdb3ddf82`  
		Last Modified: Fri, 31 Oct 2025 00:12:06 GMT  
		Size: 109.1 MB (109107160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b369328668953a1e9e1d02ff9977075d63876a09a7288222b85c7f209b1cafa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d34442d3f27fd2cede0a4d0eee936d47510d5fbd9e670a47db34cf4a05f430f`

```dockerfile
```

-	Layers:
	-	`sha256:16a88c9ab7bceac01b8f67c30cd7dc58789efde0b2c70eaaf6a7652fda3b0919`  
		Last Modified: Fri, 31 Oct 2025 02:45:13 GMT  
		Size: 7.5 MB (7504128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b91b08883a10d2976e7cabc097bfa58fc17f4dd782ec9e804487213501dfe2f`  
		Last Modified: Fri, 31 Oct 2025 02:45:11 GMT  
		Size: 9.5 KB (9505 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c62fd8b9a8f47a9666c2eca6d4191a7f01fab88a0742c3f61fe962705542eefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117733500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2674159c589862104236f4e5fb12bd8ebab168df744f66a7fa861e805437b581`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:44 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:44 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:11:44 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01549ae61a6ce8de8eefbabf5fac3f11969ddd4527ac7a202638f9b32ee46746`  
		Last Modified: Fri, 31 Oct 2025 00:12:12 GMT  
		Size: 52.9 MB (52940042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7546a90cca06495aee09930a3632230521d82783f33fb7f2534be635d35a75a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783a926a509b9fd04f0b291eb54e54ca482ebce1b277d2064f62a222a334eb61`

```dockerfile
```

-	Layers:
	-	`sha256:f2a82a112022687f7582451f2f8e3ed4605593e5d71f0f13bf9bd1525edf74d6`  
		Last Modified: Fri, 31 Oct 2025 03:51:57 GMT  
		Size: 5.6 MB (5618887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea68bf0d10f97285d33487ff9e3fb3ba95c974450847dd725e9df5ddef3d54d5`  
		Last Modified: Fri, 31 Oct 2025 03:51:58 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
