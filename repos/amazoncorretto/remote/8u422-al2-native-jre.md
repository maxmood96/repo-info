## `amazoncorretto:8u422-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:5f508a4a872559ac6634198194264466f25005e2d3c1c4e1c094d05ed932eeab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d09b5550f86b26d8a04491418079535a4d2808277cf91b871d324e27ed7fca57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171786002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061f7d67e66a54676c722ca2aa3bd757d01246862b4f715823e72fa87df2632f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
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
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ad47f4277e5b54148f0cda384fc25d96e2ceb172a8a25e79f96dd79c38596`  
		Last Modified: Thu, 18 Jul 2024 21:49:29 GMT  
		Size: 109.1 MB (109138076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:36bd36794e7c5debe01475b8fa32de14be7270c7290160eeee0dc625ab615283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7506981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ecd335ed05e0614108386d368b05b3f97a8b728eba66417482cd53cd087df6`

```dockerfile
```

-	Layers:
	-	`sha256:6e4ab967f788c6b8aaea97d6816f132950d1b112529d36217b21befac36d4051`  
		Last Modified: Thu, 18 Jul 2024 21:49:27 GMT  
		Size: 7.5 MB (7497672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd4f97a977f3a532e7f2fe0f281127def0b09157d893724186ebbb66113e89f2`  
		Last Modified: Thu, 18 Jul 2024 21:49:27 GMT  
		Size: 9.3 KB (9309 bytes)  
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
