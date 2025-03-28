## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:486635f047e100161be5470fafbee2eff5ed16d085ab04955c6b938945b7e671
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:39afa311c50217afbc42d52d63756d5b30ea673071ebc818529031d624701f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135971915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89045a14c30c36c894c5101a05b045943ed4d19382b4b60b0b8ab609a13b6d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbebe96b900bf7a70003d644679af2d1b124df67f61ec5f6ffcca5dac0726ada`  
		Last Modified: Thu, 27 Mar 2025 23:58:50 GMT  
		Size: 82.8 MB (82848626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0c2d0378342cdbc0e65bd19d611e5f11d12a759e32e7d01c1a47df8c5b93264e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db9a6884b2d37da437c8038b1cc538662529ee8341c21a9211de2d682b54b86`

```dockerfile
```

-	Layers:
	-	`sha256:f9b061e2c69e9872f42412103b365fdcacb0aa92f78671fe4b69de85a22dbaff`  
		Last Modified: Thu, 27 Mar 2025 23:58:48 GMT  
		Size: 5.2 MB (5184962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6bbab604dc721a1a70426da1bf34f386159669ac421609c753ff26b78bc0489`  
		Last Modified: Thu, 27 Mar 2025 23:58:47 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:84a297d8eadba97c07791e245b0c4a4e45414077104f28cdb94697f32bf0212c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134547654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdec45a9c6aa71299342ae60ebe6a2d15b795d133923885b0f06edb85b157006`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ab750feac752895d7d179c4ea7bed1e98b0f15dfbc12c1c080209851aa00e`  
		Last Modified: Fri, 14 Mar 2025 01:13:43 GMT  
		Size: 82.3 MB (82301676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61d10b8a59b37f59e40ed01dd3e4ab4f9b134ad85a28d97afa3b578ca656eaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faab3333e624155c3bc160546f521fd4007a33dcd065b5f34fc64344f43630b6`

```dockerfile
```

-	Layers:
	-	`sha256:0ca61c51b79e4e0b2871d61fa84b221e872eb3c27f70105811a079b82932e03a`  
		Last Modified: Fri, 14 Mar 2025 01:13:41 GMT  
		Size: 5.2 MB (5183753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02086cae6e086bef2c2283a0ae2731978b7dc6c8607e72b08a5e93f16d9833b6`  
		Last Modified: Fri, 14 Mar 2025 01:13:40 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
