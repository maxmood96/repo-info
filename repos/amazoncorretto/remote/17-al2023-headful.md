## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6604753150a66e9f8657c1a8d706731e4c94a9444f4e961f8c0a9791e4f2e8a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:98cb0673e9f4b144ec52830f993b09927a61a9668920cff63b7a70c34f1ac280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135433820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74faf6de90dc30639c243cf1d72758f7f44a318f221e4a039df1083abcf90381`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:50 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9a0f8ca95549caa504c79acef976bd6b204271a0f61eacfa1a045c2ce6bb0d43`  
		Last Modified: Tue, 17 Sep 2024 02:04:40 GMT  
		Size: 52.3 MB (52324958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d882194d42457942930f2722571bcf2a8d163227f530d8816e50550d9bea839`  
		Last Modified: Tue, 24 Sep 2024 01:56:43 GMT  
		Size: 83.1 MB (83108862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:43e5cb4a0928187503541f070ca2480953454ef91c13646d094a617e1e2362ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edb12bdbe3be8ee18a3a35f8a829843ba2d7451c00a7c80ae7bf35cbe0d3ac5`

```dockerfile
```

-	Layers:
	-	`sha256:4d67e436311597b33a1a17687f4110e5ce09b26f614cc3466d1db5ea9f7d3ba0`  
		Last Modified: Tue, 24 Sep 2024 01:56:42 GMT  
		Size: 8.7 KB (8681 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:15a856d451238cc7be5534a44cd686cdeddef7476a77627d54a2df7fc7062a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133868331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4a272ac3d968d10b63bab94be58c69ef85f07656ab05ce0612db5e6e064d60`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df96cdb6cdfe82582c4384aa1b9b851e2712c7aad7a547d91f5d42b637b982d`  
		Last Modified: Tue, 24 Sep 2024 02:38:40 GMT  
		Size: 82.4 MB (82442339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d3f575753c6031be63091633872c6c32015a02a23bed4c079b6e8c5cbfed15f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d82ce6ef11be4377551aefda3135dd8c95b1196f1c7c2c5606f6461fc6ea3a7`

```dockerfile
```

-	Layers:
	-	`sha256:11c9a9fa14d509b5bd8be16d35bb2b08b894defe40ae3b653f7dc855b83289da`  
		Last Modified: Tue, 24 Sep 2024 02:38:38 GMT  
		Size: 5.2 MB (5207632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b55d7e5efedab0c53ee0975c2241fe7a6f9bc3ab586187bf966cee503cf83b9`  
		Last Modified: Tue, 24 Sep 2024 02:38:38 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.in-toto+json
