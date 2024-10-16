## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:51129e437f7cbae044c4951d363e9597f238a4f61194a146b2800e312e814573
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:38faed9f95b13f3a5c1ce75cd77f39e734d9fb635bc6a4a71eb830769dade0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129183345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd270bd77db9d650204b87eda1793f33f5121faa0cce4a8b0bfa30069b6eb58`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:4371f60118337fd4a0e87771e20d3b3c79dbc4625e7cbffa61b0e766f1ec9428`  
		Last Modified: Wed, 16 Oct 2024 17:56:29 GMT  
		Size: 76.9 MB (76858040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aa719841a92d47382bec06404ad9e68320f7549dd90723df1cc94a07fe0c4666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a2d150415d74745f5fb5d3c788809667d7cd16104090644de46e243fd1d2c4`

```dockerfile
```

-	Layers:
	-	`sha256:65076a9a568b18b907c4ecd62d43c4089af2fc9247dbcee141511fba7a777a24`  
		Last Modified: Wed, 16 Oct 2024 17:56:27 GMT  
		Size: 5.2 MB (5223625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be415143e9903c8f2fafe7c654ab382078779b08d8b16d61a5c045ef3ba22e1`  
		Last Modified: Wed, 16 Oct 2024 17:56:26 GMT  
		Size: 8.8 KB (8792 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:75dba342263bd0c4f92cb8f536cf6063c1198b316d2cf058693b902c4c9839b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127442462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76790ad9d06b95f7312e456d58ed9ca9ab0a97791f003bec70f5aaf733ebfca6`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:593075dbfc00b6738acddb20ca3f19d0c71d1de2852f2c33a30052e8b26dda8e`  
		Last Modified: Wed, 16 Oct 2024 18:14:32 GMT  
		Size: 76.0 MB (76016098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:06ab65cdc09a0550f2febda29c6dd11b28ba405d6e01aecbf2896ff942db962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b93b27734d237ca89b5e08f7d491b2df2f36dabbf185e3e1be82cff7ecaefa`

```dockerfile
```

-	Layers:
	-	`sha256:8e6324fcd1b7c194228890afef6bbd617ee5f1def6567bef7a988e5accfed09b`  
		Last Modified: Wed, 16 Oct 2024 18:14:30 GMT  
		Size: 5.2 MB (5223245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4887211cc161b640d74d77002d006d83a008357c74c45636517064c7bcff1b9`  
		Last Modified: Wed, 16 Oct 2024 18:14:30 GMT  
		Size: 8.9 KB (8872 bytes)  
		MIME: application/vnd.in-toto+json
