## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:045a357aded815577fcd3354acbd26dba12687142930441fa9f92106feb93d83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d8e9c218c9f9aa58a6fa1012c1c1fc476547f858a8b1803512ea03f363a71214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137055916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4974e60559ada59af6e0048ec2d00294a18d222db98f607e549aa0e627ffdbb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de87407ab93d55ae3ab096a06d670dca33318b7eccaac5f4ab8e4a930fed46e5`  
		Last Modified: Mon, 06 Oct 2025 21:12:20 GMT  
		Size: 83.1 MB (83050785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b3a9bc06cda98695a9703f068059823adb0eb052fb7d6d6da5c1c0459b4f7187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7673cc80d7a783b5e97c540990228a4168c2f6158bda73f672c5ace5822f63c7`

```dockerfile
```

-	Layers:
	-	`sha256:10ac375a5b96b331eeb11361f26695bedf0020ff4f482f37e1895590387b5d9e`  
		Last Modified: Tue, 07 Oct 2025 00:49:13 GMT  
		Size: 5.2 MB (5208245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5115293b470fe1d85b947a71cf21f744c9dad0c35359e735a969b59b24b711`  
		Last Modified: Tue, 07 Oct 2025 00:49:14 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:13b4f2c46def994a70987627c8cefa37e46ee5e7ef73b926fa061e0ec3c6cf50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135369448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0afb95e32a594bc50e98a40ee7e0c8fef1629fc2fe80e8885f9ba0382e8c5a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccdaa874ec8c754e819d698415f9fc93d7f88fdf85722ec7da3132e5385c97d`  
		Last Modified: Mon, 06 Oct 2025 21:13:07 GMT  
		Size: 82.5 MB (82478245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a74e92180f8ea394f4ca09d908cd148344b218a5c472cfcb5015829afdc8e601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2e31aa92439c0fbba52b28b464b2458174fc65bc74dce4d6710666f6b4ae49`

```dockerfile
```

-	Layers:
	-	`sha256:a247d59a05b179b3b9cd4a491f6ccad1650a8b696b5e37cabedb9362fba7ce9c`  
		Last Modified: Tue, 07 Oct 2025 00:49:19 GMT  
		Size: 5.2 MB (5207036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f4fd043874461cfd3f4081cfe20f26f16fe0d36e719f76940b2adede2dc8fc`  
		Last Modified: Tue, 07 Oct 2025 00:49:20 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
