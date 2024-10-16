## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:2223ac89a1329350da4190b7e43338320a183dcf2990e550e404046a1f277d91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:684d383051551933730d8f362e7b1b94b91a0bfbb202a34c155461f1157ee7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128493376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223369f3f2dcbd544a90af3815c1fb0f2d83ed272257a3991ed5f1659f44db86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:49 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a29aaf0aba7591583343123d54c149aec296f4ec57948e1f022b2ef95b99259`  
		Last Modified: Wed, 16 Oct 2024 17:56:18 GMT  
		Size: 76.2 MB (76168071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bc1e5371731cb2ad7d84de7b18a5c5ba8e0e2c415d5fa4d6ae5f76779104b92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1320d189f9089e3b22bbd2960a0e5d34fc34daae708143e4ed56f603d5c41e5`

```dockerfile
```

-	Layers:
	-	`sha256:479a1e0dacf3f3fd9ec6f5be5c3fc1146d63e02d7e2e5a70fdabbd84f8f63953`  
		Last Modified: Wed, 16 Oct 2024 17:56:17 GMT  
		Size: 5.2 MB (5198512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0937aa468be8f218a85d4d4d4e3fa5f2f85b5d6b7bd033a8a054a8b1e4ca167d`  
		Last Modified: Wed, 16 Oct 2024 17:56:17 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a979af530c4fb9cfa86347fe2158666c4b82786b4f0e76a9eeb9c6c2ba75441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126739615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa3cf0d7bcaff18c1ae1648edbad2c74bea336351dcebe37e5ecf3e7b924aff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12c21ea3d396a00732b4442985ea1495b026893cd26c52a9572bae1c65961b6`  
		Last Modified: Wed, 16 Oct 2024 18:13:44 GMT  
		Size: 75.3 MB (75313251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d132eefd2bcdca46cdba02ed86c169d3c0e01868edd7a9571ce4656ca6d2eaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23a22fef594b67d15a412a33dbc818063c85c2c8f1eff58e8ed654efa02eed3`

```dockerfile
```

-	Layers:
	-	`sha256:a9ba52127a40ec23737ee62018f143454b4a722bed67d2ce8fcef5f9d1355b99`  
		Last Modified: Wed, 16 Oct 2024 18:13:42 GMT  
		Size: 5.2 MB (5198129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78f9194c5869cc5b9f90663ab7ddbc3b5b27d470704deead3b31723deaddac8`  
		Last Modified: Wed, 16 Oct 2024 18:13:41 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
