## `amazoncorretto:8u492-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:f69a55a0e72748e7980c8996f0a354b3ef7c2d76f57731b622b38b933c644185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:929eb3730bd4d5ab037c1d4e2cefb198234337652f77ffa052298e46036bae8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171942402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b5d034d2d5f42c3047e09e02daa21f7a5d5a3e3ee4abedb3f9538fc0bc41c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:34 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:11:34 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:11:34 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f9f535e55ab72143801ad81b39158663c293eb69a9c2be4cab2c04f818e6f`  
		Last Modified: Mon, 04 May 2026 20:11:55 GMT  
		Size: 109.1 MB (109082393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9d35d6af4048dd4ef7a8b8bef66507590b2f1e6dce2905bf309aa2138449e5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4516428b49b141b539fb0546ff392766a6ef00f10435189229a8b3d12acde323`

```dockerfile
```

-	Layers:
	-	`sha256:285505661d6d593137b2445142bc242b6edbf17ccb629c219beaf2f274a4afa1`  
		Last Modified: Mon, 04 May 2026 20:11:52 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6d487ddc9ad5875dce8f229364f6fd914a285c85d3faa094d49ffea8657652`  
		Last Modified: Mon, 04 May 2026 20:11:52 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:742fca6274a77baa13f613740946fda1808e61e36b1a239c8589e1ce590ee133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117764711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099279eb9c1117d7301eedc07d0a2bcc3e45de8fe8dcf35e92aeb4d8cf1c78e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:10:49 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:10:49 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:10:49 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:10:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178ad43a7b0d533b7e01080b2f8d1b48503f68fef5d45f6a50eed18449ce852c`  
		Last Modified: Mon, 04 May 2026 20:11:04 GMT  
		Size: 53.0 MB (52969180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1273ccf1f2eeb30fd509bdaaae8ad7725079141f7f186cd54a3872de10e991e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adcf00cabb3b26dee0965e0d35665a828d007257af2cdc7bc42415f95495ddb`

```dockerfile
```

-	Layers:
	-	`sha256:edca833d1f6bbe83f15165b96e15f0c3949100eea699404c7977e221c8fb3345`  
		Last Modified: Mon, 04 May 2026 20:11:03 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b288ddd3c48a8a2dd58bd482509dede685e21ac6b981564952bd476d274630`  
		Last Modified: Mon, 04 May 2026 20:11:02 GMT  
		Size: 9.8 KB (9752 bytes)  
		MIME: application/vnd.in-toto+json
