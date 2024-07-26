## `amazoncorretto:22-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:052c03bc2ec8c5311d2feb79c689bf88f76e910fe8f32206dc37704e64a84cc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:28fe13e2a7b805657e6a42d2f735c025e9304623ac63c5a7fd754a0a276489cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140659500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4346af328bb87862d16ee7176bbf04833b7f61637c3c573231507653bbf3538`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff750bd26ab71a46c3b8ad5fa384df48e6dda50dcf63f864208a3754a071181`  
		Last Modified: Thu, 25 Jul 2024 21:02:24 GMT  
		Size: 88.3 MB (88345321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:338656c0d7ab6af44e837ec0f624cb06e52b73f096a7f2291b6023541391c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5195138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca6f7005d371b6a7d2113ba2cc7d579ee7ebb3725ca62f9017188e462f10592`

```dockerfile
```

-	Layers:
	-	`sha256:a455f34761990831bad75f07a19f719f40be2b05427291257db6287e84ed4e09`  
		Last Modified: Thu, 25 Jul 2024 21:02:22 GMT  
		Size: 5.2 MB (5186101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd31ba510a8f1cba12087f663269017b47d31fc1f73d303da6073ea85d0a0db`  
		Last Modified: Thu, 25 Jul 2024 21:02:22 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4c4c444a1c2b1453738d46e29dc39b9293988b5efdbfdde518851b4ac76a4b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138706428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898f556784baf49cbbd0f8e0574a817bd99bb9a94d0c96acadcfae5b75af6c47`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:69f1520adb0e35dcf91717c80b7867ab26fcf8ef8506b9831fcca72a1b38b618`  
		Last Modified: Tue, 23 Jul 2024 01:08:54 GMT  
		Size: 51.4 MB (51402016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75be6b25dcf28035ddd184e51a090bc86161c5a7f012d73c3825ef666266989a`  
		Last Modified: Fri, 26 Jul 2024 02:06:44 GMT  
		Size: 87.3 MB (87304412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b089bb116dac96f2bab280643d213f2cafb067705c41fef5dc29ae70abb8fe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5866374e11bbf414875e8c3ed610c7806e2894b021401a8ed02ffa4e2526b72d`

```dockerfile
```

-	Layers:
	-	`sha256:f23b77c47f202b48d48408494f61ad494f054122bfbedc189507023dec690245`  
		Last Modified: Fri, 26 Jul 2024 02:06:42 GMT  
		Size: 5.2 MB (5184085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe359824638316c2280a7b02d2fcb07c7ffdbf8640b7064c4bc5480f383881f`  
		Last Modified: Fri, 26 Jul 2024 02:06:41 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
