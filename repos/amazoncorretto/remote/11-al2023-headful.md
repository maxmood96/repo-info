## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c4dd6bcba830eb225ca07dc242874bf557529cd23b313bd88f9db32fc3db39c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4d2b3160411deb010e31dbb6a1ec00499704414e36340a9d479e804b69f7f13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129168401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a290a48b0624cd6dc588d80b4f5941de90f1e57441224713143cdb496304189`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b60b6c892280988095a2507a148439d3b5fd7b108e66565a91cbdb1f0e543fa0`  
		Last Modified: Mon, 19 Aug 2024 23:08:46 GMT  
		Size: 52.3 MB (52325078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ea55c4dbf0bc29d5f15f7c3175c69067e6aa688b405c98c71e7522978445e6`  
		Last Modified: Fri, 23 Aug 2024 01:50:31 GMT  
		Size: 76.8 MB (76843323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:40069b9363237a1e559485fca960da15883134948e424032db4f5b4f36622f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cbdc2ced14233397f28f73a94dd5314c203cea3c7f9c97a41dd6152ef7deea`

```dockerfile
```

-	Layers:
	-	`sha256:cd54675ce6b5ee70dfe6c9ca6c5289bf66f749a6b0d0a6b3b56c718c27efe0d9`  
		Last Modified: Fri, 23 Aug 2024 01:50:29 GMT  
		Size: 5.2 MB (5223612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc7201941f6dee1784bc33055d32239038ded5d79de56554202f68768dfc87b6`  
		Last Modified: Fri, 23 Aug 2024 01:50:28 GMT  
		Size: 8.8 KB (8754 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:31dc250529fe22e53838c0d6af69bbabde6680c7817fa6ba1f686d9debcc039f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127428207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355508bdc83ab6ba613237a24ac4ee5ed54fcdc7f5398f952b3b753803433278`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:875f26d62c6d0f5a935b0c8548e8375f2a9b98d7669bf434dcd5b36e2114348a`  
		Last Modified: Tue, 20 Aug 2024 01:54:55 GMT  
		Size: 51.4 MB (51426298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f279fa847f04d29d016e724b1ba864ebe5c82541cbf63b84fc671aac78d79ea`  
		Last Modified: Fri, 23 Aug 2024 02:22:16 GMT  
		Size: 76.0 MB (76001909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4a6f26c15a03cb12d1205c5aede1dcf8aff8020da1e36f9bae6ee7343cac88b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df26e678970b302635533dff497b5426caf7beab684896fcc95f4b60597aec2`

```dockerfile
```

-	Layers:
	-	`sha256:5b262c9ba8b6186d67e35ac48d5ff773f0b651b31776e6e5fa66cfbe91977b79`  
		Last Modified: Fri, 23 Aug 2024 02:22:14 GMT  
		Size: 5.2 MB (5223232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e77125f3e4d9c4e3ca2f31d0046066d6fdf36dce6d4c13f227c03747209ccc5`  
		Last Modified: Fri, 23 Aug 2024 02:22:14 GMT  
		Size: 9.1 KB (9115 bytes)  
		MIME: application/vnd.in-toto+json
