## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c0974cabdbcfa8d709dfd51c20d9638c83b8a6987c3253762d8133feac0d78cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:04d92c23a4dc105f34b253d4d11e17d9b988f791dbbaafd94757bd924be5a03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142830991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b5dc2547f2938217d7ee64a3ebbbb2007cd551d53c71de0a2ef7404f780383`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3821c16409786f1ee4132fa3756ee9d21cf2179e76c5031fb90dcc0f38500c51`  
		Last Modified: Thu, 13 Mar 2025 22:53:09 GMT  
		Size: 89.7 MB (89704115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c59c5abcef1276486349e7d59103df2fbcc4e7cbfa05f0b2731731f77ac14b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5195505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776d2491692fc43b3b9b7cf0337baa495641f0a7b6c8583adf34210402880adf`

```dockerfile
```

-	Layers:
	-	`sha256:e87d6ae74a0ed86cf924d82829b54e626a195924e3f01f30142c01208b2b208d`  
		Last Modified: Thu, 13 Mar 2025 22:53:08 GMT  
		Size: 5.2 MB (5186578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff827d7ba172cd436f4e2d88c7b0cd005f3915f2cb1e95ca7d0af7c77ae02d44`  
		Last Modified: Thu, 13 Mar 2025 22:53:08 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:baf75925d72c904dc867423390df393d377b782e5c110a8c7abaf6a41763dff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141091684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433fef335c356e0b24b6046fd453a5ba511352ffed619ee0741dcb9e2d05c97d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7b74bfc22eeb23b856feb114d6c45af8f6f133640963927a938d191062b251`  
		Last Modified: Fri, 14 Mar 2025 00:12:40 GMT  
		Size: 88.8 MB (88845706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:956aadae92ad91ec113ac2e139ff455d1382d4e5ec663e5bccac51a0d7b1a0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36d5dc40de3431e22a15ec0a246cf8586439eb7bd6aa56576825c16dfc6d8ba`

```dockerfile
```

-	Layers:
	-	`sha256:bc83a6025acfff5abbfc607e912d9dbf235249bc1fa5e052bce4a68dcd711657`  
		Last Modified: Fri, 14 Mar 2025 00:12:38 GMT  
		Size: 5.2 MB (5185371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f055d58d781ac83d7458bf15e23d34797e1ae49b8a37e936f0721363aa2231bc`  
		Last Modified: Fri, 14 Mar 2025 00:12:38 GMT  
		Size: 9.0 KB (9006 bytes)  
		MIME: application/vnd.in-toto+json
