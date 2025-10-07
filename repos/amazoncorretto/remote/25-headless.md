## `amazoncorretto:25-headless`

```console
$ docker pull amazoncorretto@sha256:65cfbc029be04e69d7535b6c9399463766052411a537ebdf129b93a7e27df626
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1491921c2514658067bb2da6ff6848c935351ac7fe2c81d8d7290f2ddfd47690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157609937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e17a4a0a0ab8fefc0c20c4a35144f149e9826092f22c16084c8a77c512629d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38264826e72cb08a0f2c424b4ad3301faffbb5f8e5654ed84781518150faf5e1`  
		Last Modified: Mon, 06 Oct 2025 21:14:32 GMT  
		Size: 103.6 MB (103604806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b25e7ee4e7d767d2adc37d5b8faaace85a9dced76e4c96b13732575e729564c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd47259e559fad67205335edcc960f08f94550132a30a3a41dea3b4a5f697db`

```dockerfile
```

-	Layers:
	-	`sha256:703c1adba6a12c810a117f9c320d5ecfd48a0f2063ca740e7e9d5bb2aa6aca47`  
		Last Modified: Tue, 07 Oct 2025 00:51:56 GMT  
		Size: 5.2 MB (5194703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5dc686460340c27727822263810d922571d45d077e3f8f8bf70cf4d677d0438`  
		Last Modified: Tue, 07 Oct 2025 00:51:58 GMT  
		Size: 9.1 KB (9074 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a6040c99c6c84ef8844fe5d4b29f27f714710c40ee6f1dd81de0d255114cac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155412237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512bfc827a48b709189207761f1c3a068b9d524d76b6438a024ebe9099a5a456`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30290206abcea52b78fca353b0c677dc1c607ae3a468034a6febe4e1c18114f`  
		Last Modified: Mon, 06 Oct 2025 21:15:29 GMT  
		Size: 102.5 MB (102521034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6dab49e153aa7cb864c86531740dba0c9b42de5957ce02f8cf545d173461c450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e511c07e4f50c69738b2535c59c20d32fa6ccbbe2b57cd1879cd097fccc47e4`

```dockerfile
```

-	Layers:
	-	`sha256:0e83b1387f421041477f6fe9bd54830a4622f6ff84a0c15b16d99fce782e5707`  
		Last Modified: Tue, 07 Oct 2025 00:52:03 GMT  
		Size: 5.2 MB (5193514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561c10be51773d9e9d729fc104272ad35389bb190dc4e3d11715b4db9a4cc730`  
		Last Modified: Tue, 07 Oct 2025 00:52:03 GMT  
		Size: 9.2 KB (9166 bytes)  
		MIME: application/vnd.in-toto+json
