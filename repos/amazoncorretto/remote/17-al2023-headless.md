## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:69e85b1626f31c454e11b7dc5240b898a424268e63516a09d8f6bfc88d4c1255
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d34e5548763d6b20311a6649664c00bf5f8ffa011e6c2a6544e6a11b0573d8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135279588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0800ccdfbc4e1ec25e688ea762d78831ea1ffbd8c197fbf0a87445fcae656bd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c39403805d14ea9206d459c7237fde4409dfba8f90d59f96dd1e004a37ab934`  
		Last Modified: Fri, 20 Dec 2024 22:32:47 GMT  
		Size: 82.1 MB (82123275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5bdc63f45d4a1aee17cb5786fbf0c163855eecb28ab1758b749f57ee7c8f33cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5dce2c432994f68aa24c510b8c4daa057e244bfbd8081847bead22a8fff5bd`

```dockerfile
```

-	Layers:
	-	`sha256:9fe7e8d9c913229d62c0bc58c5d6d3991e78714baac70e5e6eaaee21a5024de7`  
		Last Modified: Fri, 20 Dec 2024 22:32:46 GMT  
		Size: 5.2 MB (5179424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e419995bc8dab9da3c101bb4c1c4de9c562a627dd50526e6f152806ffd790af`  
		Last Modified: Fri, 20 Dec 2024 22:32:46 GMT  
		Size: 8.8 KB (8756 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:19b40264113143883718e67facb3cfa61d4da2388f2e8fa7aeedabf4eb884237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133795591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c268c42af85222ab9effc395062936fe8c66b82dc6bec88709a9545280d37313`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:98ab3ce9b55607064b358289eeb810db43f69e016067c07e7136a807475f6f27`  
		Size: 52.3 MB (52276382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1ddf588e8083df7d1c0f3bd3bf5b409846c59a4a8a1abd2525660c05ebc96`  
		Last Modified: Sat, 21 Dec 2024 01:45:03 GMT  
		Size: 81.5 MB (81519209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:65a994ca9411dc817717ff7837bd00383de3d442affb22d68d20c60762b0ab82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5187048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13c1260ab73b71200b0172b2c125f1ee9366d7cebfcf84e549c922a7b02ca43`

```dockerfile
```

-	Layers:
	-	`sha256:564354cb199ac6423f1908652f7ec4caebdc7ee179b9a788fce4c2e53fad7df0`  
		Last Modified: Sat, 21 Dec 2024 01:45:01 GMT  
		Size: 5.2 MB (5178212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0508f40029183b8d37391826e3c20bc07269d8114eee3b33b63a50cd0156323`  
		Last Modified: Sat, 21 Dec 2024 01:45:00 GMT  
		Size: 8.8 KB (8836 bytes)  
		MIME: application/vnd.in-toto+json
