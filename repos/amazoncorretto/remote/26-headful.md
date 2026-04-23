## `amazoncorretto:26-headful`

```console
$ docker pull amazoncorretto@sha256:0a22655b51edce6c1776bf250307ece57cfc628de96cb7a5d166480310b34c95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2a78a21d5e2cae7d50d3e7b526fefee69f2103dd12c130c27834a4d228d8fdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161115092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76168e44cd9db48c27d6d7b7fdba9759aedf88e48893e7eacfa254dcce81ce6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:52 GMT
ARG version=26.0.1.8-1
# Wed, 22 Apr 2026 21:35:52 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:52 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556d4c7d8fd6945cdaf3c6f2c5e36a78f3be20bc342c89bc6b9ead8c6bd7291f`  
		Last Modified: Wed, 22 Apr 2026 21:36:13 GMT  
		Size: 106.5 MB (106543838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6610fd7fbf335083b71ee069e3302eb2bad092a3c72640e0f83cac0717d2b224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5caa2eab57547ae6f57f71a8ae74945aa91670df537eabba12821ed70a8bbc4`

```dockerfile
```

-	Layers:
	-	`sha256:46c4c9e46b80f1e722d43882498c4fc8a52a0dda780e171c00aa933dd6ac10d9`  
		Last Modified: Wed, 22 Apr 2026 21:36:10 GMT  
		Size: 5.2 MB (5225833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c341ff86f002c397f801f5662c8592211ac5540c0d159ae42e1ecc8e9e6c286`  
		Last Modified: Wed, 22 Apr 2026 21:36:10 GMT  
		Size: 9.4 KB (9367 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3f36fbd55b4ae5fe44b523c0ca936b57bc93168d978ab6e6ccaafaeb1dcb8c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158876973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361bfa69442f9c0022592ff56d79adefc9cdb33a16e38835587e40c8fa465215`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:56 GMT
ARG version=26.0.1.8-1
# Wed, 22 Apr 2026 21:35:56 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:56 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6796f6ca8c1316afc60daaa015efe4ba6aada3babb464236bbbcd09eae8f4a24`  
		Last Modified: Wed, 22 Apr 2026 21:36:17 GMT  
		Size: 105.4 MB (105434234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de2e5d400b692a2f94a96ed1335c51708d4caefa7ddbe51c698fa550703fd3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ac7b8a97765e2bcd9928bfa74e73559bd9aafdfe9cf7724f227ef12b59ce42`

```dockerfile
```

-	Layers:
	-	`sha256:55561501293f76f32da5a1721536dd900697a62eabe6af42919fdf152e14a097`  
		Last Modified: Wed, 22 Apr 2026 21:36:15 GMT  
		Size: 5.2 MB (5224646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46948f71ed3bb2738e9a38c1d452e31060e67ec4d6fbf2eb63901436ed7cc77b`  
		Last Modified: Wed, 22 Apr 2026 21:36:14 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json
