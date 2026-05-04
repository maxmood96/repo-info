## `amazoncorretto:8u492-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:d0ab9cfb23ade5959e025ebb8f83989ac1db09c8d22df22059684af636e2b3a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e41849eb5499d23f453ff0a566063180088d864d015b6381c049dff9c34e5666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188220164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae91038e7ba34a9ce67ad879e090b6c0764b04a226af464496ee2e130b03b1e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:50 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:11:50 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:11:50 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5095e5b012d39181c05f5ef0f4a179871dd263ab50f88a50cbee672704de93d1`  
		Last Modified: Mon, 04 May 2026 20:12:15 GMT  
		Size: 125.4 MB (125360155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0d51ab4dbe4961086f164f71bee2bfa4d755b7b661d20c9c432d88809240230e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593eb175559ec46b6c449dce1f88389355e6f4fe750b671114bf77c631c04bee`

```dockerfile
```

-	Layers:
	-	`sha256:40511e3ac75c8c3aa50a950b351f1ddc8ffdbc780418d7cc8e1df914454bccc8`  
		Last Modified: Mon, 04 May 2026 20:12:13 GMT  
		Size: 8.0 MB (7977515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6c45126f3a631f6b4c2b79b09024e95afcaa90fdf31f1e5504f4fad9c3432d`  
		Last Modified: Mon, 04 May 2026 20:12:12 GMT  
		Size: 9.7 KB (9711 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5f8d85c808e60eb44e7b7508fc4b7a549ee54d95cd4e9652decb0a5537e48745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132500535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2072862eb2bdceb292406dfa67c3d346c755f23ccd4ea8aa690414da15f9c06f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:03 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:11:03 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:11:03 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f76833d6d63eb52a46160aee5a492b5412751e31632638c217480ef134c2bf3`  
		Last Modified: Mon, 04 May 2026 20:11:20 GMT  
		Size: 67.7 MB (67705004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9367c22ea97a2817981eb337658f8e1f612ee9c8d0d0e017e8ec47fbe7079aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e749181d59779cc69b686e7e4e0d7fde44f5109b20ce339fe3b83e34b0b01ab`

```dockerfile
```

-	Layers:
	-	`sha256:44c443a6f91eb48a15f270dbb110bf9e66e2715f8ce2b368a8b1883000a404b0`  
		Last Modified: Mon, 04 May 2026 20:11:18 GMT  
		Size: 6.1 MB (6083038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e81027015694bb6c9bef8c3da07a11c124001128b1ae272e2f00d609ddc237b`  
		Last Modified: Mon, 04 May 2026 20:11:18 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json
