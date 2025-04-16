## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:eb9fba1758a4896b90cec521a3e1cdc0bced5b9dfd0bb9eb65b2163746abe5ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d017317dc8ebe4dfc4ecef70737c16327ac0342d0c5ba9b3df88f7cd6436061c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (145000849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f81e91602dade4cccbb40c342915ff2407558203db3396fa2fcdb95ca1da4c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:23 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:23 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3ac3105e3ec784b882ea1b6520bddd7b0058147258bc57289255c6b962ccb`  
		Last Modified: Tue, 15 Apr 2025 23:56:03 GMT  
		Size: 89.1 MB (89093796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eef372671f18ada8731436178f5b45e41887e2348485a04258549e6c4d627c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5436142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395507bb7e55cbbc75201312df00f5a5452a8ef3b07cd1783be64b826cb7ee90`

```dockerfile
```

-	Layers:
	-	`sha256:1f649f9f74dca18a9e115deacc09b1b5627290175c7079b372d2dbf1b3d42762`  
		Last Modified: Tue, 15 Apr 2025 23:56:01 GMT  
		Size: 5.4 MB (5427394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:416d71c2ef0d49df9842b32e88ae8410fff026d61d271ec93f822a30f0a8f01a`  
		Last Modified: Tue, 15 Apr 2025 23:56:00 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:16608371d34e75e658e1792e9800a8d50a62f238863f5c3ee42f0bbc6a62b540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143169171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33751148b0e4ac9b1d6e1469a67b9768896f250f61a08af84c685053a586d507`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=21.0.6.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9207d081aa42cef9c0298c0ddb95bd0dd766f31043b2c9fee3f0c8f112b19934`  
		Last Modified: Wed, 02 Apr 2025 00:33:58 GMT  
		Size: 88.2 MB (88208162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:17a5a9fb59c80a038c09929ddb5a19780845c4e83d3cda5fb5cd7894a0ca833b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5435012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4fb7d3a0e9d233d6bd26b4a5672f615e4d7bcc85e136e21667db1b92a03696`

```dockerfile
```

-	Layers:
	-	`sha256:9c0eccafbf3575159dbb72c89209dcbfbc27c4f5126f04bef48523c26b80023d`  
		Last Modified: Wed, 02 Apr 2025 00:33:55 GMT  
		Size: 5.4 MB (5426184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8392ab53af337eb0c0392616c7be7910b2d546ad4762c09f9d3296223501cfa3`  
		Last Modified: Wed, 02 Apr 2025 00:33:55 GMT  
		Size: 8.8 KB (8828 bytes)  
		MIME: application/vnd.in-toto+json
