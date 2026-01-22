## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:cea7aa629f2283add6db056d84f675bbfc8bb12cab57e2816c3b79c0dcd4f7d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ac27d0f705eb2a0ee984e27395d2b5219a76b960f8ed5b51ff509a35ad1b3974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158357199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcd3755e11e421bfa29be410556b208543505e5f1bc516e14e52108bc72aae0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:01:45 GMT
ARG version=25.0.2.10-1
# Wed, 21 Jan 2026 19:01:45 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:01:45 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:01:45 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e071b042ea5d549c6fe9bed51235c303540530fbcbdcc2ddc23c6d72fa649885`  
		Last Modified: Wed, 21 Jan 2026 19:02:03 GMT  
		Size: 104.3 MB (104335995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1da4bacf7b01cfae3bd0ec47ab1f8b710b956dd2d01cf2e2edc766d9273a5fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e832ca0b335088fb07812185e1fa0fdc4b98ebc135899d529d2d4535573ddadb`

```dockerfile
```

-	Layers:
	-	`sha256:c7b0f6913e628d3c7b72f585afdd6f588bc664ceb602936eca0227366055f0dd`  
		Last Modified: Wed, 21 Jan 2026 19:53:51 GMT  
		Size: 5.2 MB (5220218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5884fb4cdd27d863d257b344bdfa5534646eccef574d19b71f2af50a85a8fd0`  
		Last Modified: Wed, 21 Jan 2026 19:53:48 GMT  
		Size: 9.2 KB (9210 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0f75bcd43842f46eb09c210e317537955f719756446d83be24b1f5e1913444dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156178920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233528ccffe55812c2f04a29ab26dbd75a4be92d85c96f715b55f09beb2de310`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:02:06 GMT
ARG version=25.0.2.10-1
# Wed, 21 Jan 2026 19:02:06 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:02:06 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:02:06 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:02:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f555f016a1c3c05ce62d401c957235d63c2f059c70f95f10cbb14442553a2205`  
		Last Modified: Wed, 21 Jan 2026 22:21:04 GMT  
		Size: 103.3 MB (103264563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a3f42590170cda485d147ede535b25289a9fddbc42702c6c5b9b34d643de2870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca81c4462fc598209a572a8b42679268ee47321ae0245569c857ee9119f4c38`

```dockerfile
```

-	Layers:
	-	`sha256:0f43bcad28fa31b070f0510a44828f4c5c833c62cdce15fa23c8bd097d0d5e33`  
		Last Modified: Wed, 21 Jan 2026 19:53:27 GMT  
		Size: 5.2 MB (5219032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574644a8c1ad175adab7006cf1bd2973d34f11cdbdd911093dbf35e25d575d5f`  
		Last Modified: Wed, 21 Jan 2026 19:53:31 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json
