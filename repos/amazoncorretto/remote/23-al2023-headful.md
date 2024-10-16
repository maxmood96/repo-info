## `amazoncorretto:23-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c3063adece90fc7c654ac17701c52d47f60ea6db5e9687726961585a2719f95c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:94bd1d5c9cedcc02e99b215bfed5da6282b892312a2db2ac03cce286663c5d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146103018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d981d2ea0839588656fe88ef945ac447c830844b8118b9bcdeffd63bbd4a6ca7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:49 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c581652f54ed5a2d5e289b27967efdb32439a315849f6fb91cf7d2c6a6da50`  
		Last Modified: Wed, 16 Oct 2024 17:57:38 GMT  
		Size: 93.8 MB (93777713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aee290847f57b762e7194bc73ee15b3d50118568f854f6e1c98c7b3dcaf94c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb9b87ecf6c20b32671308796d70de8eaac96842f9433146974124f7563616f`

```dockerfile
```

-	Layers:
	-	`sha256:a1c37b3cf975d11cbc129e48bafe66de9776ff7aacad38f3978f94824b6017d7`  
		Last Modified: Wed, 16 Oct 2024 17:57:37 GMT  
		Size: 5.2 MB (5214128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdcdcd17e784dcde9e302d684dbdb9c97646c260c1fda7bd1c783ad4345dc742`  
		Last Modified: Wed, 16 Oct 2024 17:57:37 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:089f5436d21d367633f66c49f7fb635c917eb7368f8c64de54533eaa9cfe217e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144138414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff0a5242a6ea6a925da929b3b988fb611b1797fdd8ba4b0ad2ed86345109c5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a0f2365f431805cb0e7698844a4f93a9f45fbe9a7f8fa7c6c953ed869cbc8`  
		Last Modified: Wed, 16 Oct 2024 18:43:11 GMT  
		Size: 92.7 MB (92712050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:efcd47c6fc51bb7692775757f383a3aa078e0d473f85881db6b2c2f573158247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33014dc058bac71f8fefca44aea8aca5a728938654873ce95125bc77e09c10a5`

```dockerfile
```

-	Layers:
	-	`sha256:52422946119a88c8f04acd65f7627ef0a2d594f578cc2fb36a4261ae77afc71a`  
		Last Modified: Wed, 16 Oct 2024 18:43:09 GMT  
		Size: 5.2 MB (5212117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e67133bb99db77f69b75c6e21c45244d3cc67347addaa402a6833669f0b973`  
		Last Modified: Wed, 16 Oct 2024 18:43:09 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.in-toto+json
