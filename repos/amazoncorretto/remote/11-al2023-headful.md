## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:af282779654da73f27892de90f16e6e9eeb12edc21476682d8c4b8e388273a60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dc03e692c4337351d9b52b01bcd453f62bf9c2759a01c1caf0f2743eba06b395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129172014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2410ecebf9bafb0cfca57b3919ddd0d28fb7e7115dfe005a5bfa05330acbfb54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:1c9e0f4db95e1ae683b8f16b1ecfc5d8693ad4e5e379a2386e2870f38383c7d8 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:860904071dc658e37de73aa1556e7badfb13bef4747965ea3bd1049e8ff87dcd`  
		Last Modified: Thu, 04 Jul 2024 00:20:13 GMT  
		Size: 52.3 MB (52319623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88f5bd38d019fea526145f1adedc8925bcf60d776e32ad989d7e8518f72b286`  
		Last Modified: Fri, 05 Jul 2024 19:56:24 GMT  
		Size: 76.9 MB (76852391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:79b7c51d405c044dc7fa307947d9e91241b6c69ecaa88e5fd219ac78c6355564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700da83f814be3fe9026f8824b5d0b45f58c3a7be788cc234115c2e983deccb0`

```dockerfile
```

-	Layers:
	-	`sha256:0ae70acfaedad5490c5ee43375fda3f6709003c2e473b55bebb339ffbe860c6e`  
		Last Modified: Fri, 05 Jul 2024 19:56:24 GMT  
		Size: 5.2 MB (5195463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca6a80655f4a508024aa5fbc85203ab5af677973f8311534b99fbca723441cf`  
		Last Modified: Fri, 05 Jul 2024 19:56:23 GMT  
		Size: 8.6 KB (8558 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9373d82b5ec90f0beaf3812022fbffa275eb5bb02b0d488ba3276964a80887e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127422629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a49acadd7d7cdd87e0a4478788a80ee2bb7a58e2b4f13f43b730f6681195274`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:a2f5453af1f2210c7b49fadc5acdaaa335139ac35c64847d2f5879056f91a03d in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f95af119e05065dbdff89fbd219657362e32f7ec50d632e28754e75b5a13806e`  
		Last Modified: Thu, 04 Jul 2024 00:39:44 GMT  
		Size: 51.4 MB (51407040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd6c9f0c8cf529479ae975e842cc944f74745488852caaf18866c6ba972a356`  
		Last Modified: Fri, 05 Jul 2024 20:05:55 GMT  
		Size: 76.0 MB (76015589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6d01bdad2bfb73963a38c42f8efd2457b78f2036a7b1e9cfe0ad8ce00ff60abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfaca2e478671de76c8ff46f104e908e253f6bc3c25fd1321e379dcb015de75`

```dockerfile
```

-	Layers:
	-	`sha256:0d621db3eff57789aa4722be5e48e07cf0d086ff8bcf7b01061c81f90d57a00a`  
		Last Modified: Fri, 05 Jul 2024 20:05:53 GMT  
		Size: 5.2 MB (5195082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1e5d38b7e2a1c6b9002ef4589891209f3c486aef37fc5cd5df30eed96f7a19`  
		Last Modified: Fri, 05 Jul 2024 20:05:53 GMT  
		Size: 8.8 KB (8839 bytes)  
		MIME: application/vnd.in-toto+json
