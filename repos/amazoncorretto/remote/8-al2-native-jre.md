## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:e4901d299136607272d6ba0d1d3075a1bf546ea9a8ff2ab844ba73f82cf24094
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fb46d08d35b09d4566c77c0164599f237a8cda4466a73dc423ba3e708d92b039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171725247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c258a4af63ede09eace3aff3564e84536a19d2e7f8b171c9d311a8f3b37d0e62`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:24 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=1.8.0_442.b06-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cfe9bbed5cb4d66219c202304ceba075fb3a446026759f6103ba7d5efbac2e`  
		Last Modified: Thu, 23 Jan 2025 18:27:32 GMT  
		Size: 109.1 MB (109089417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9128f74aa6aedcf0aa8df6aceac50a9ca1f58e4d29b6fcbfd86ab24ec73d162b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6370f1e561ffe71d5b568d421d21676773a216dd7d3268e743c65a8e6c144955`

```dockerfile
```

-	Layers:
	-	`sha256:c3259587f32eb1499290c615c57836ecdc127de341153ca91325bdc72c2aa958`  
		Last Modified: Thu, 23 Jan 2025 18:27:31 GMT  
		Size: 7.5 MB (7483483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5d24b944e76764e7e1b42bed729b427f975c392e3d4e4d1625b76d9c0c78257`  
		Last Modified: Thu, 23 Jan 2025 18:27:30 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c2eaa22238ee425e9c3102c49de14c64e10741e8ed63675aac1b9e1de30d92c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117508519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468723f08e37688b8649fd684516de3a4e7866c643f6555d9ae4a620c1a77b97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=1.8.0_442.b06-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b5eb1da8a227c899973b4e0b22c80691b470dbed6d999eca9acdef75fb367b`  
		Last Modified: Thu, 23 Jan 2025 18:30:27 GMT  
		Size: 52.9 MB (52918214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:df6feec8e00ae39a4fe4be1f008ab3bc51097aa771be25f97b0dcb6cee94c08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd85707d951116409e31902173946fb20bc761a9a4b22ed548138a91df974335`

```dockerfile
```

-	Layers:
	-	`sha256:8d1694c4f153a8936671191d6746e578ff8c722bf303bb1f95166b81b3101141`  
		Last Modified: Thu, 23 Jan 2025 18:30:26 GMT  
		Size: 5.6 MB (5602804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce84ed87ad2e14a72a7de5427089970874ca7e5aa43dda707c7822010c0e4b0`  
		Last Modified: Thu, 23 Jan 2025 18:30:25 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
