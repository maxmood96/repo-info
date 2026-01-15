## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:984b58a9997885a44142626c79cc4f34bbabc6bca82a8b4991f3e62fce235b67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9ef04710724c4bf63a8d3eecbb69bdf13edeebf8e533bb294b6cd62ffa5acb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158290202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50671144471d58003db02681fb5c05ec6a7cb444b708eaa83acf2776a91fb722`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:19:01 GMT
ARG version=25.0.1.9-1
# Thu, 18 Dec 2025 01:19:01 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:19:01 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:19:01 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:19:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34945620d86888cc3752678f7ceac4a6c6a4e2f2ee9082bc5f7233b3646d3464`  
		Last Modified: Thu, 18 Dec 2025 01:19:42 GMT  
		Size: 104.3 MB (104301742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b2af160604507555eca9e609575845f98de5155041451f90f3e286ef853288b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a442e6d3a1a15a21548be7da1ce31d6083ec96d510347332a12ef894db29e0`

```dockerfile
```

-	Layers:
	-	`sha256:a056adf9d9e52b04bac8c892528bdd4fd4f24522710124f8ef1d62a75b51b186`  
		Last Modified: Thu, 18 Dec 2025 04:51:01 GMT  
		Size: 5.2 MB (5220208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14011b9529448c93b9f599d21e311e9fa028b8aeed6838209e1ab897f26ec587`  
		Last Modified: Thu, 18 Dec 2025 04:51:02 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2a888730e367e0ea60e48728d58189ba6e1fd45ef5502effeb30da27715f806c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156116563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd096318cc103b269d9796fce1a7453d0d0d548aa2cd3957eb325b0ffdf47ba6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:27:29 GMT
ARG version=25.0.1.9-1
# Thu, 18 Dec 2025 01:27:29 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:27:29 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:27:29 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:27:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38750b32f37238ca4114b23a0df2121e2066e9a241bc852a4ab6bef1cccce92`  
		Last Modified: Thu, 18 Dec 2025 01:28:04 GMT  
		Size: 103.2 MB (103243113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:91498dc14e9632e37de076906b7df6e82bff9fcb8bf5a7038e93b93f2f886403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d06fd14773905aca0e2328bdce75068c2e4766f2401750cd0fa2d09dae7d550`

```dockerfile
```

-	Layers:
	-	`sha256:2881b120598b12bf7e9cfb23c83d0ba21398a77acf387ff8b2fd4c7407385d1c`  
		Last Modified: Thu, 18 Dec 2025 04:51:07 GMT  
		Size: 5.2 MB (5219022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd31e8d6a1ecb401738d15a8dec3ee5267a17636bd3053ef682aad75e39f2d1`  
		Last Modified: Thu, 18 Dec 2025 04:51:08 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.in-toto+json
