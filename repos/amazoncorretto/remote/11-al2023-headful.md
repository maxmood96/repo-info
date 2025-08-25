## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:427fe83b2a51823e46c6cae892590eee758925211f4765086bd5ebd02d61de84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:914f2186c3ba3c3442d165617010abc341ee30724eab1f4f458708ac153f8ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130947615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbc00ed208d033e3d4c5aeb142dfa0d259df1890d6f6c61e105d72f04f255ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf9e01a394ddd2488d59726ae242efacd5eee036fcf1f7d81b8efacb402bebb`  
		Last Modified: Mon, 25 Aug 2025 20:18:09 GMT  
		Size: 77.1 MB (77078885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:298936e122f39dcf094a07221b43dd18364db18f9fb29f7200de6d6fa7855c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c18c18f5d28f0b5a2e7e4e8eaf4581d852abee2162bf03449d249d0398fdbc`

```dockerfile
```

-	Layers:
	-	`sha256:791babe5e64966828475c6c75fe12321ccaecf49ddea0b53b8433a96d3467e9d`  
		Last Modified: Mon, 25 Aug 2025 21:47:38 GMT  
		Size: 5.2 MB (5222168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0c28fcfaf95d9ac82b744a33df33753c9f49afc0c05ae22ae910d66ec3bfdb`  
		Last Modified: Mon, 25 Aug 2025 21:47:39 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fcf82f5236dd840b154afc079ae12ee564a9f77372bfad1b959bff916e1caa57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129026516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f590a697cc3b43e24cee988183ddd5385d29574c6bfe1ae0d82befce96e2ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f05d6a88ed2d518a9a127efb7208bc9ebf50700b69950670c616d55cbebc070`  
		Last Modified: Sat, 16 Aug 2025 05:57:30 GMT  
		Size: 76.3 MB (76300122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:79a7dcdc29bf2d385e8b9080455d13a1ac48bb7953c358439cf6ea5450cfc090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74079ea0c4e790c915195074d88d8158f4cd6eb6d82248391db7772fbc96c4a3`

```dockerfile
```

-	Layers:
	-	`sha256:710e65928e9ed8f9139f5289f46032970d8eff78acf108d172835f4159f1b5e7`  
		Last Modified: Thu, 14 Aug 2025 09:47:38 GMT  
		Size: 5.2 MB (5221789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec30631e59d72600ff271e0f7450fff723b1138d33b4ef025c66a29c86a4d3e`  
		Last Modified: Thu, 14 Aug 2025 09:47:39 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json
