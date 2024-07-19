## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:a0f60eea3bfc59a5b70aaa1c225c5293324eb8b8299dd241040d293761d7bfb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5d9b80b46a61628cd9ebd1af927979b6cf497094d522d45fc7638f67ec1f45d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150425117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8869a87a361492560b05822db3c1b761993a224f64c4864a2cda98b5943fe291`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abcfdd8d076d1d2817352700c1c2dc50ab6008c0379c8805765bdeb0b2a877c`  
		Last Modified: Thu, 18 Jul 2024 21:49:34 GMT  
		Size: 87.8 MB (87777191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8ed21c8db6969a7f75646b099affcb87392e9101c695a4746ef6dce342fdd080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5635159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c64b9093ee984a6ba8e73c851769ef20a8986ff8e0ed2ee1973db6912604a24`

```dockerfile
```

-	Layers:
	-	`sha256:6d1386c6b376c899a7be91771c558257b20420a605c028bb5f14db2f58434aad`  
		Last Modified: Thu, 18 Jul 2024 21:49:31 GMT  
		Size: 5.6 MB (5626062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0efc340e06b4d0ed1b8cd801771fc54cad494510d89c1860a5e0fc53efabd7b9`  
		Last Modified: Thu, 18 Jul 2024 21:49:31 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cacaa38bff2435adf7d45427b0bda06014a1d9576bff8845b111cccd0791c89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144653383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ce8070e5d0e322d63530f56073bc820881852d4560e8513416ce3168ef01aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aed87060011b4440169c496340411d672d9301885673fce1681a4a38185efce`  
		Last Modified: Thu, 18 Jul 2024 22:56:09 GMT  
		Size: 80.1 MB (80078072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:800973e68b586f4d25f8884f77e1f1f80b7cd49af62f4ab762f0cf48b93dc5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98416945f657e2dba9f22b58e2b3b0fb2af322cf1ecb4f3c485a346aec0c9fb0`

```dockerfile
```

-	Layers:
	-	`sha256:282e2731004b8211d7f5dabea062e2cdd0cf8da1670a327962395f136680a65e`  
		Last Modified: Thu, 18 Jul 2024 22:56:08 GMT  
		Size: 5.4 MB (5442037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c8809959eabdf69bc417afc692e847a16ecb4f4f6f9dbc6e324eba6774aff3`  
		Last Modified: Thu, 18 Jul 2024 22:56:07 GMT  
		Size: 9.4 KB (9375 bytes)  
		MIME: application/vnd.in-toto+json
