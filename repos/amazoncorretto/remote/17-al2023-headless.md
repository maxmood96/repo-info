## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:db12b8826472afa8c136e6974d97bb20067f4fdbed625d3de8acd835bfeee949
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ee950e46e9c2c8c13cc79194291731b5738c09a2db50b0adb8991622218a1eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136387584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaea9e79e6778b97534e0a4a6be4a771d305df3efb222ca09586cca17758d199`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:13:45 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:13:45 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:13:45 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:13:45 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:13:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dc76c1e0134d2b2a84a0bc83c7ce1bba2a22125739bd0a771533df6f1a4650`  
		Last Modified: Mon, 02 Mar 2026 23:14:02 GMT  
		Size: 82.4 MB (82354744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7a240351d6ce2d0177c61a5976799492ac8549f1af7f9fff22918e7f0d9896b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0389a03c36697f3644714db498d4d7900082b2ed55fdfbdfc9d1c5aa95a5e432`

```dockerfile
```

-	Layers:
	-	`sha256:6787c284f433004f4131238e18a0ae0efdf114f9571999a60867c2ea792563e2`  
		Last Modified: Mon, 02 Mar 2026 23:14:00 GMT  
		Size: 5.2 MB (5182966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6a25a16e35a718bec9830ac8a7d85121804750868a00c36f4ac7f44ff347cd`  
		Last Modified: Mon, 02 Mar 2026 23:14:00 GMT  
		Size: 8.7 KB (8707 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d22c052e9da9e2f4b050f2c735852587962775fb028ed647feb58f5e986c01a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134706082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac61b6d74b1b2d02689b1bf467cb487081998b91f8b595f9290a57d6d81b91a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:37 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:14:37 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:14:37 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:14:37 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127b23e3c2dac2cb84a943163ab8e4e66753007b5967f46c04e699ac51280098`  
		Last Modified: Mon, 02 Mar 2026 23:14:55 GMT  
		Size: 81.8 MB (81764763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bb9742ab25633b63ae1985e793c737f4a48739386a39565463c14eee69ce39d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a5633808ccc0aedb81dd1eb7032ce02cdc6d5e0fce0118ab1fd91d633b716c`

```dockerfile
```

-	Layers:
	-	`sha256:93424f5ccda9c5f6791b9a7dce2585471af08009fd9b34813823385ebe2b2338`  
		Last Modified: Mon, 02 Mar 2026 23:14:54 GMT  
		Size: 5.2 MB (5181754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b72d2b123e74addb856c63fd4e0ad71ab24a0f7e864c188044f6f9cbbaf8b8`  
		Last Modified: Mon, 02 Mar 2026 23:14:53 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json
