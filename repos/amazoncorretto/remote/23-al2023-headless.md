## `amazoncorretto:23-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:47df3e7347f4e803698ff8a0c02cff5c7da4f0ec1b7211d4fffeeef0e5b92f90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:38fca76a4de4bfbef97bb395d2ce3ae7918c8cf5ccd0aab97c318bb076bec8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146293363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acea41d6fc8dcd342bc8d5f99a5c4e1c163828d35de2daf74adf993399b9ef15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add3709262ace2959271f5bdd6d42704449c0529af2051a0d7b1c0eb4185b105`  
		Last Modified: Thu, 27 Feb 2025 21:08:35 GMT  
		Size: 93.1 MB (93141630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7abaeb5d5d133df90486fe3228c79457ad5330cbf02742e1a81927ba588772a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c58d3adf8f670929df563163b79af90c521ae950a8fd48b656a78db9d33950`

```dockerfile
```

-	Layers:
	-	`sha256:0f074908a81ce35ab5e1ca57c29832f48eda84a4bfa527b2188758434f6f4702`  
		Last Modified: Thu, 27 Feb 2025 21:08:33 GMT  
		Size: 5.2 MB (5164154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d94df4ac95ee1af64faeb0ef8b473d268c664bdee0b101b3c544e23129089a0`  
		Last Modified: Thu, 27 Feb 2025 21:08:33 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:690f85037ae179a004b70140187dda1fadeae2bdc35136f8959681e7eda3f278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144408480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e990f933613f7380fc77cbb7c753c60d6fd7036dfdf75f1fd4ad59716b6f97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6a5b8bb929cb2e230733e1ffd40f96a926f60841519bb84c519d2e8c0421c9`  
		Last Modified: Mon, 10 Feb 2025 20:30:29 GMT  
		Size: 92.1 MB (92137529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:260ab53e67af41b42b3998f9454a5b918e5efd9c74a2bbfa1a62096760c87371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12ff2644f935741241645ee524568ca8b738d4ba5735cd8be28c99bbdf45003`

```dockerfile
```

-	Layers:
	-	`sha256:494d559b98e35cba0c614c2bfce47861d65c929c7bcc84f87cee7fc93b46f06d`  
		Last Modified: Mon, 10 Feb 2025 20:30:27 GMT  
		Size: 5.2 MB (5162143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b61f5802a6844e45f6550be25ec274447ab4f0282aeb0de689faa6341d131f3`  
		Last Modified: Mon, 10 Feb 2025 20:30:26 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.in-toto+json
