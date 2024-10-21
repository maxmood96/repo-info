## `amazoncorretto:23-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:1b4e49e8476c35704d5e0d53535976085485830f67d587f8335f22c97a42fe1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8f450137590fe1f15060ba66749d11dbc59e39be2aff7ed1ea83ef40120d1872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146142448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7593bd07974119866335d1935e49bc61ccccd8f43f9f911051e52ab730bbbb13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
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
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dcf92151ed7827c480bb70702ac6650c33b482a2353c1a9dcd44d39e7d7e3c`  
		Last Modified: Mon, 21 Oct 2024 18:57:14 GMT  
		Size: 93.8 MB (93798616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:552ac156fbbd9830758f7ac4c83cfbc5c69c83fd691347f7b161f92779923001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6469f86698aadd4e85a5769878c105dcb97b484d1ddd3837cbdf218d3e8d0a5b`

```dockerfile
```

-	Layers:
	-	`sha256:bbc0afe81c0b6500fc0343c9738a5d1dccd89701f204dbc2668ec0f4d0a5b02d`  
		Last Modified: Mon, 21 Oct 2024 18:57:12 GMT  
		Size: 5.2 MB (5214298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2869c20a6c312fe1cc376ba601fd36adb2097596476f86b235acd75f927bc78f`  
		Last Modified: Mon, 21 Oct 2024 18:57:12 GMT  
		Size: 9.2 KB (9248 bytes)  
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
