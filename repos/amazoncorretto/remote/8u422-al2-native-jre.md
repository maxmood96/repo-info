## `amazoncorretto:8u422-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:0cb25364e6db1341ae72c57ec6a194e21dcee9ff8523454ef128f57725fd501a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bfd02641fbefccfacd66f3dcb4c01b9b764ae611aba5409f0546763155a47916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171850785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82a0ad5c65b1f51f5eb38baa2b721fc61efaf227da4398b984d77439a6fe62a`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c91bf364720aa675eb26c6599e062fca09cf8bafb6d8f079db9292d77dc7361`  
		Last Modified: Thu, 25 Jul 2024 21:01:35 GMT  
		Size: 109.2 MB (109171619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e55d46d95639a93fb1c7e884fccdeda166179a57cdff60fbb73d11c851aba699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2111bb055b25ee9e08641e4b56ace41d9deb68a59b132ec9f334b21c5685878a`

```dockerfile
```

-	Layers:
	-	`sha256:8aca6ac1371243592f0d921249bc2128da07bb296308a20923f482c3919b104a`  
		Last Modified: Thu, 25 Jul 2024 21:01:32 GMT  
		Size: 7.5 MB (7497672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc4688f60d140fb4fc9941581a65bb29faf589aa5d4e02bb872c83530763de72`  
		Last Modified: Thu, 25 Jul 2024 21:01:31 GMT  
		Size: 9.5 KB (9514 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e701e87d62fd4fecb86b18829765c645227d76d09337ee27a48c343c6c1185ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117522015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98594f0faf3c75a140726ce98635da2e75e4c07df1daa62382cc963022f56dd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ff75a69d67f95351011b419ef9ec511e78334535db850551b97b310ec56fd7`  
		Last Modified: Thu, 18 Jul 2024 22:50:29 GMT  
		Size: 52.9 MB (52946704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e32fc8e003d5cf284f0ec03cfa725b1589a9d29d47850b9cb3e4549d40498830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8127cc79d013040b43078cf749e16fb00b0a1bb9608a8250fcba9597aaf22fb`

```dockerfile
```

-	Layers:
	-	`sha256:0cc848dbe8d199847bc9a92ff7e560bccf8ba35a0d94a05ff82ae8f53896eb85`  
		Last Modified: Thu, 18 Jul 2024 22:50:28 GMT  
		Size: 5.6 MB (5613416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250cb839b5e57415632f7b591881527e99a3386bc6da4707a36be59436a40de3`  
		Last Modified: Thu, 18 Jul 2024 22:50:27 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.in-toto+json
