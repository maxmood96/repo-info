## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:5efc13115b4e2dc234e89616f8317307a52e0fb0811b93976149d9030a25b488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:54baf0d8624c787534ee2a0bd77fc52b0d20bebbb16c11bfc1ccec02f228af07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171786612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33811170a72e88f1e453c6976bc01749c0c27ae071daca1276b5829ec80780f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:23:24 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Jul 2024 21:23:24 GMT
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
	-	`sha256:37766f9d8ddf179208313163dc89d8d39dc16ba3be3bc46534855c244565cdd4`  
		Last Modified: Fri, 12 Jul 2024 13:12:20 GMT  
		Size: 62.6 MB (62649406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269c9c6c65c836a2d05a8fe551fa715ef922949fc0201780fb3ab3b24542bbe7`  
		Last Modified: Tue, 23 Jul 2024 00:07:48 GMT  
		Size: 109.1 MB (109137206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d767233b7de4326fe772abdac67338e10ef06874a0b1efe9ed5f5341f0ca5a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdf09fca46a669345b41c07dcc09afbfaa84a5b896d33f7d105e4b4bdb93594`

```dockerfile
```

-	Layers:
	-	`sha256:b267bf251100e43d8a5ee0cb8a50363f3754928c608aec38801ac72c10058194`  
		Last Modified: Tue, 23 Jul 2024 00:07:45 GMT  
		Size: 7.5 MB (7497672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea43d69a79b1a21b7d042e55732ef246ee2cf029d7a9aebb806414b21d9d4dac`  
		Last Modified: Tue, 23 Jul 2024 00:07:44 GMT  
		Size: 9.5 KB (9514 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

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

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

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
