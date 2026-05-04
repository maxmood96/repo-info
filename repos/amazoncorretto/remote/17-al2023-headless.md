## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:88bf81eb3194616da149571ace97e29b2102c4f291826e23c468e827ab0ed3dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2cbda2c587795bc5fdd3f03e24d91dd3c53865a3943b28ad801609b2698757f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137064291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1801b769ec53ac07cb9755ba27f2375ad276cd44d651772063b505567170ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:20 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:12:20 GMT
ARG package_version=1
# Mon, 04 May 2026 20:12:20 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:12:20 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f283494b19ea73c71312960048cef239b9c24f1e4e9b0968054c793b29a3f0b7`  
		Last Modified: Mon, 04 May 2026 20:12:37 GMT  
		Size: 82.5 MB (82487538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b4b34ecdeea947a03d33971a9ca141a15c15df89208b0e98624c492603934a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5199045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b30861ab17fb7d95ee6207e2739add284585ec250362e787a71e48a45c30506`

```dockerfile
```

-	Layers:
	-	`sha256:3a1eeda53a9758445f33c4c27746215aec5feb50bf7b0045820d6b8b6daab483`  
		Last Modified: Mon, 04 May 2026 20:12:35 GMT  
		Size: 5.2 MB (5190163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d94be328bfafdf51897eedd83de9d6261d119d7d2e3e45fc52033e74ba2b534`  
		Last Modified: Mon, 04 May 2026 20:12:34 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fa52db3db2a8b3be19c6bcf7a3f763146a747b21b26d92ae959dfefcaecd0c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135354587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b054fd6f9f4169ae6dbfaa720ba6ddb8fd544100c8c3310d7346930bd90b8200`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:51 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:11:51 GMT
ARG package_version=1
# Mon, 04 May 2026 20:11:51 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:51 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ffaee3eb317f27eb064a3a2682ff85efeedad8260d2af625bc395c0fbe1b3e`  
		Last Modified: Mon, 04 May 2026 20:12:11 GMT  
		Size: 81.9 MB (81897817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3deec365b4a4d5d7032e0434e3404b26ccebad92bec6fdf8402346b4e312b008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5197914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26503c435d3cfcfe66c1c3e90fbd00919e7f6d209c33a5286372768e68f690fa`

```dockerfile
```

-	Layers:
	-	`sha256:b1eeb703547b5bf80441edc10eb7630f242d8b08f2dcddb461764658694596bc`  
		Last Modified: Mon, 04 May 2026 20:12:08 GMT  
		Size: 5.2 MB (5188952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11baac4d44194e10463359ace28c807533d4aa4dbdc3b577aed208f91fd40f83`  
		Last Modified: Mon, 04 May 2026 20:12:08 GMT  
		Size: 9.0 KB (8962 bytes)  
		MIME: application/vnd.in-toto+json
