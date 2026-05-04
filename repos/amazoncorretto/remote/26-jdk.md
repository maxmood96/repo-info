## `amazoncorretto:26-jdk`

```console
$ docker pull amazoncorretto@sha256:0a499b6b0991632fee40d228c510cd01a67a55d89b480754ab99d82a83bafcba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7444d19d6471d1f4464dd016505e6777c37ac515204398d97e7b90b9b1487a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (248026036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854606a19a2ff20c220eba80f2366d055e7282785c7e34bc9c3dd64633434264`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:13:26 GMT
ARG version=26.0.1.8-1
# Mon, 04 May 2026 20:13:26 GMT
ARG package_version=1
# Mon, 04 May 2026 20:13:26 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:13:26 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:13:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1309365e6b1f8020444030bfd0ebcfcf96af7398376415cd84688acb669071`  
		Last Modified: Mon, 04 May 2026 20:13:51 GMT  
		Size: 193.4 MB (193449283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dc849b312eb121677d10c0cc361f1f0643267eb11f1625161bf53c971785d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e420bdf14a30c4ca8c98a35c4acd1dcd2335015f5e5c03bc4936a80ea7eca886`

```dockerfile
```

-	Layers:
	-	`sha256:c75ed3e1d5a1e009c8ac887255662c3365af19be331912097f5c36af51f95d17`  
		Last Modified: Mon, 04 May 2026 20:13:47 GMT  
		Size: 5.3 MB (5332742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e38b24afede78d927342506daac5319ca014ffe107f79164a6bbf528142fd7b`  
		Last Modified: Mon, 04 May 2026 20:13:46 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7009e1663cf25b22d594e2ad57105bbf75fc1b7e9b55e8ae55381f699eddde5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244730577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0101dfd1cab23fc3712b0104f7d8139578eab46b3478acfd068366de7bb7d99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:13:09 GMT
ARG version=26.0.1.8-1
# Mon, 04 May 2026 20:13:09 GMT
ARG package_version=1
# Mon, 04 May 2026 20:13:09 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:13:09 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:13:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3f209306d29a392a7bf9740c1d4f96184e9aa51cded6008821adef02da82e7`  
		Last Modified: Mon, 04 May 2026 20:13:36 GMT  
		Size: 191.3 MB (191273807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5bbfce883a0b8fa0339bbc1f17d5365c13f655c5d82e5d2cc4456667cca396f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876bba15c2bde096337f72f9101704da0dbbcc26720ae26e7352e4a841a1e741`

```dockerfile
```

-	Layers:
	-	`sha256:499182567c2a54915f0b6ec59f4c2efb030fd89fc06bf52a97fbfcfa59c4c828`  
		Last Modified: Mon, 04 May 2026 20:13:31 GMT  
		Size: 5.3 MB (5331718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a5056bd2f3783d8bd7887e570864036d4154686f482fa2e55175b08f5dd251`  
		Last Modified: Mon, 04 May 2026 20:13:31 GMT  
		Size: 10.8 KB (10778 bytes)  
		MIME: application/vnd.in-toto+json
