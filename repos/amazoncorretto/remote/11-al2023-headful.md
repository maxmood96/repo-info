## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:823c1307cbe15f2cb70acd8fb9699f1c9fa869b04d93347993ec7c2a2d107d19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:241ba30cc8492d881810eef70ab4bd6f1292a9b90325d2fc0518382a824e7f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129168313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a85bf73451e76fac288d34d9c8542224fd69b2b85f46e0c3c8716da9fcde738`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:50 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9a0f8ca95549caa504c79acef976bd6b204271a0f61eacfa1a045c2ce6bb0d43`  
		Last Modified: Tue, 17 Sep 2024 02:04:40 GMT  
		Size: 52.3 MB (52324958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80399069863487bfe43cd09f8eb510a70903539f138962449a0c8f6d53d04012`  
		Last Modified: Tue, 24 Sep 2024 01:56:47 GMT  
		Size: 76.8 MB (76843355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:48d100f1c20e2c4a823d44b17de8c33b44032d0df82ba136555e0817459f3749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 KB (8535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79a8172189d6a9a3a9eb99c89c4e8901465671a11230a7c6a5616f7392b9ccf`

```dockerfile
```

-	Layers:
	-	`sha256:0aace7159a9cb896c3b77877065000a8b6a2ca3075d1233bc39d6b8bf549a619`  
		Last Modified: Tue, 24 Sep 2024 01:56:45 GMT  
		Size: 8.5 KB (8535 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b0c4225a191297cb3a17f94741bbad056de891325263a6bb65a3b06813fdfebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127427764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e105791d4121f374d62a002d21ab8b11b1ca8a9a31dddad2dc2dee103c89f5d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85721c68c49773fce59670d3470ce36fef963e35a0beb74e3c12fdd9e0bc559a`  
		Last Modified: Tue, 24 Sep 2024 02:32:55 GMT  
		Size: 76.0 MB (76001772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3cdf70941d1f02a2dda356795c10dbd66a75726020c5af1c242a18154399f2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cacdf950ebd0c229dbaca85bd13671e8a7b9d1c55f7b4fa3f641acf8f1b573`

```dockerfile
```

-	Layers:
	-	`sha256:ec58dacb2298070c03724b5d54fd385136e44dd6bdfb51d15de10a602bf1f88d`  
		Last Modified: Tue, 24 Sep 2024 02:32:53 GMT  
		Size: 5.2 MB (5223232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e0a026e630144c54bd615e7e1acfa1e3524ba69d69242bfa099a9b56e8df13`  
		Last Modified: Tue, 24 Sep 2024 02:32:53 GMT  
		Size: 9.1 KB (9115 bytes)  
		MIME: application/vnd.in-toto+json
