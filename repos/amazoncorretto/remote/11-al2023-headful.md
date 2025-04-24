## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:3dfec05b3d86603431a6e01e10734d1b29e506a935ae40229f5a8d01c6bcd84e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ff668f4435aebdaa69cb98f059ce403f496de39094cb65725d7428f8c7e7e75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132928333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9001be8f6e7d037eef4cbe48ad5a420258bcf64107fd32ef70ac49192e7a643d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1cf9fb914831ab202ad1756fe44227d7c88c49394a5cc9749ad863e76989673c`  
		Last Modified: Thu, 17 Apr 2025 22:49:09 GMT  
		Size: 55.9 MB (55906521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0585805c1bb21371b4eefe11471773477b40089d5737976d796aca25b92562`  
		Last Modified: Thu, 24 Apr 2025 20:08:10 GMT  
		Size: 77.0 MB (77021812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:72cb8f9ab6c531b05a0c3e406dc9240de291fb90c467d501f8ac48791ccea851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5473739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f7217de1c802b6ef8b44a541ed4301aa83a55025c5d80fe5c0992186ab9bcf`

```dockerfile
```

-	Layers:
	-	`sha256:da65c18604af09d45635865632abb4cac86e5892961ebb58e3c68058ca2bd5e0`  
		Last Modified: Thu, 24 Apr 2025 20:08:09 GMT  
		Size: 5.5 MB (5464951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3af6ddf2414c2d079be9902dba5b1445870b44bfaf540f5d2668f97bf81926c`  
		Last Modified: Thu, 24 Apr 2025 20:08:09 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c29453216c38f58a92707f492b59d23597d0b6397cd166142df639dcec093b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131204716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b84667d31e4d14016669200eba8a7826c95c8ba825bdda08e2bbc5ce81e6f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:28 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:28 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2607cd4c0e32f00e7a4e2a2d91efbfb9cc75ec102edd25deae66333016c0507d`  
		Last Modified: Wed, 16 Apr 2025 00:03:31 GMT  
		Size: 76.2 MB (76243707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b26226278cbd2f8d88cafbaf2ed722c75abf4d4abad5ed27ce69f9c29f0d49c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5473439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc6e492875dcb5444731ddf00d3179a569bc31b8f7fd3be7bf039685bad3641`

```dockerfile
```

-	Layers:
	-	`sha256:6adf93209a493f6e4e9d3479e2e2b9436abda3398d341ad5ef241c32942f9825`  
		Last Modified: Wed, 16 Apr 2025 00:03:29 GMT  
		Size: 5.5 MB (5464572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1455c2742f52b2ed147be77afb021eb6a973b32ef373379c29d0239634a17709`  
		Last Modified: Wed, 16 Apr 2025 00:03:29 GMT  
		Size: 8.9 KB (8867 bytes)  
		MIME: application/vnd.in-toto+json
