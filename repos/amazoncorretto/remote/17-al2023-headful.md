## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:e5c92aebffad334dd1a78820ee9753a703f5797354873110cbac527b75981545
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
$ docker pull amazoncorretto@sha256:ae34968828e1e7c1d3a2ecf17d8e4d224ed505e5d2fd9b91d9d726000fa70341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134541618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875698245949eaecaf85201ac9fc5efe1ee906c16173759ba141fbf0ef4750ac`
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
	-	`sha256:92a376874570d50aaa72a4435a5b15fdfcdc3099600b45751b2c0705bd2c65f2`  
		Last Modified: Thu, 27 Mar 2025 02:43:04 GMT  
		Size: 52.2 MB (52247990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f0e1409da158a554a86a9884a4a3806c1401c6bc03aa0de69f96594b0801fc`  
		Last Modified: Fri, 28 Mar 2025 00:15:54 GMT  
		Size: 82.3 MB (82293628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aaf4007030c9603d6820f017a5755f4c3bbb781bd7b41b65d3c276fb71a7606e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbe358676468eaf1589b666a598f9c4e8dd517b8d37a99d9a28371ac411c549`

```dockerfile
```

-	Layers:
	-	`sha256:232f3047bc42bfb76039bb6eb1c0e963f87d92fb1350983db12820fc25f2863a`  
		Last Modified: Fri, 28 Mar 2025 00:15:52 GMT  
		Size: 5.2 MB (5183753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c2f22879a9476c6f78497197bdb4de200522cdcd77139ebb202fcc9eff4596`  
		Last Modified: Fri, 28 Mar 2025 00:15:52 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.in-toto+json
