## `amazoncorretto:8u442-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:5e494c9fe28d0ee6f1235e0138ec1392992b77b3cad55b0716d7a9ffa5b09895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-al2-native-jre` - linux; arm64 variant v8

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

### `amazoncorretto:8u442-al2-native-jre` - unknown; unknown

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
