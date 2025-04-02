## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4f9d086c45580732d86e49bdf58682a41c6f18f59202e1f50691c202d6a2df11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e939855d870fb4c214e656c9cdc37f24d3cde35b834f4d5c3880a62834ef53dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144978652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7721757bd18c4a5b2702e873d8a363bca1e1f240746b08e9edd6ca88b9e13c83`
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
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a3286bd9bec83bebe73074cfb78535138d76fbee37470904a133467c3129d6`  
		Last Modified: Wed, 02 Apr 2025 00:01:25 GMT  
		Size: 89.1 MB (89071599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c206ff4884be5b1b993007ff9e21a914b0d341fc9deeac0192e9d89dcb0606eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5436142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be5cec3707429e5160bb63763ba92ec947120341e753c6b3f29e150d8792c41`

```dockerfile
```

-	Layers:
	-	`sha256:0c1779b3ed4b3f5528f63d41006778488288539b83315e1faf4e6a5a53fed910`  
		Last Modified: Wed, 02 Apr 2025 00:01:24 GMT  
		Size: 5.4 MB (5427394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a342c7205f153873db88a05f24290bfff2568bdc0b9d3188f55e32e24cc0a3e8`  
		Last Modified: Wed, 02 Apr 2025 00:01:24 GMT  
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
