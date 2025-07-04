## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:dc8508bac711c37688139bc049bd78fc7f0a572a5ffa7261860b0179fe4bedac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c54eff4d09330046808ac1a7cd942b68f106ef59abbf197d1e5995bcf6dd72ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130793875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1240488ad2b60566c48fc5eb3a671883acbf3b151d3dea7646ae12a4b16047c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a00db81cfbfcbbcc0cbe194011d1372b5452428d24845777fa6177ed15ce473c`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 53.8 MB (53840211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93f6cc8c0ecf0e04c304530682f4a61079aa543c88b8550421ef308d26d31fd`  
		Last Modified: Thu, 03 Jul 2025 23:07:04 GMT  
		Size: 77.0 MB (76953664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:90101366c455740b11946b31ac12b49128624390d83a22c4fe0655e034f28f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc0e97cdd7e33b2feed872daf802c4a330415c06308425a7da7da8196e13a1b`

```dockerfile
```

-	Layers:
	-	`sha256:b832219ebb97f1f6660f1aef018c048dc79271b2e98d572fef5ea88057a3e95f`  
		Last Modified: Fri, 04 Jul 2025 00:47:37 GMT  
		Size: 5.2 MB (5222877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c88f4666d75638efd74bbc63278eeb0c6c91b1519430f693dd560664d1965ca9`  
		Last Modified: Fri, 04 Jul 2025 00:47:38 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a834c06e1e75637dac1d1ef2c1d2c3f5367dcd447eaa946d013252227958317f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128653596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3d1998e48d57609c08886eb5b7819e61d8967cc09137fdbb92653cc8321ade`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b68a2c71c7b58af19b07b9fdd45891d076947f1a7f9813dd85852d06d522801`  
		Last Modified: Fri, 13 Jun 2025 19:55:49 GMT  
		Size: 76.2 MB (76171904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:699a3b7492e3cc51ef1fd483fa8ebc939e717556619c94f3e9b631e5ac8a9731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7800f52651a227ee1dd83f66f54e690cfe4cbc8bc98dbb981c4b9ac454d1d61d`

```dockerfile
```

-	Layers:
	-	`sha256:86fd3510dc8de9e457df6005b3e26d96365d5e4daa448c1b5630d3af7f2b331b`  
		Last Modified: Fri, 13 Jun 2025 21:47:38 GMT  
		Size: 5.2 MB (5222492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39ee2396c822316dc7c78c5d8152b855ff8f05b5317bb235d7bd036e901dc8b0`  
		Last Modified: Fri, 13 Jun 2025 21:47:39 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json
