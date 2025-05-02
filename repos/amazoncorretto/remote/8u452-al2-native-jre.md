## `amazoncorretto:8u452-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:79cd03960b153a27172c48e3f1f283e14839030171ba2242312462a8ff1e6231
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u452-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f6cb857063ab7cb82254576ff1e77dc36087511711c171969582a96f344c3291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171858815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c628b1bdaeabc3622f4feed8a605146520a1ee88be713c62418c585ab6cca8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=1.8.0_452.b09-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:d95443c3dbb00d5bc2eae8f837647b2757c14518822de8c1758b9842856c04b8`  
		Last Modified: Thu, 01 May 2025 13:44:39 GMT  
		Size: 62.8 MB (62759330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f5b4d167d6aa56c8b233c03f7e085786836a369cff3e9834ca26fab4433149`  
		Last Modified: Thu, 01 May 2025 21:08:16 GMT  
		Size: 109.1 MB (109099485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:41610c5f52922236cebd20ef40806c8811dd5d69762b4f92f177a6a7dabbba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26005dd1c323e94e7c061f1c7459fcfbef3b826501d14dd0b7b737aa5c80f88`

```dockerfile
```

-	Layers:
	-	`sha256:606c0a7f2fad1abedad96be74a5805763e68121caa78532c28382840b7ffc7e2`  
		Last Modified: Thu, 01 May 2025 21:08:13 GMT  
		Size: 7.5 MB (7486555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0809ae41ce0f7aa049b3e5abc892a37e94f426fbed18869e7355394a5620a850`  
		Last Modified: Thu, 01 May 2025 21:08:13 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u452-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:800df07fc1b42e4ee9d6d5c9619ca2b5ff1aa3fb47bdd09aa52acefb925cece7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117540674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae93f1817d66e41b52d587804a43caa69f5c24135e87743b79a285e0dda7bea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=1.8.0_452.b09-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:08a465b69ed13c6a3d1f2674c3766151b11bcb021ca0e952f6a01f81b18fb3e8`  
		Last Modified: Thu, 01 May 2025 13:44:52 GMT  
		Size: 64.6 MB (64594727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce19ebe6fa59a27d0c6cff546878f8ebd198b95dfe60080a8da85162dd07d2dd`  
		Last Modified: Thu, 01 May 2025 21:09:00 GMT  
		Size: 52.9 MB (52945947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a6cac327c4d1098be12a07e3fb779b15c0cacc053aedffc46080ccde3ae72cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5615559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527e5a8d0a60dd4ac67931bd13af21f9dc8cf12d87cc88c899ba2b4767115d34`

```dockerfile
```

-	Layers:
	-	`sha256:473ea337b2bc0aeafbdd00c83930daf2120950b7bc1c7ffecc901fd3498da6e8`  
		Last Modified: Thu, 01 May 2025 21:08:58 GMT  
		Size: 5.6 MB (5605932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872af156e341f26817c35f60cbd64b4247933a451bc6b49461c6167f4a1889be`  
		Last Modified: Thu, 01 May 2025 21:08:58 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
