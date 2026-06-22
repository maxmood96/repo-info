## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4bb7159b0ee00d34da002076e7347bb9bcbdea67fb78faa964e13b5592e5b25f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2f6035f6b37138be76ca0ab0b4a03e1ed158aa61d621d36f72ba3a23ed508195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143931707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a90d9c7e5a26fd79871b86d9f480c7ebfb6e1d50ff96415b08ca2ccfee8ea69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:09 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:05:09 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:09 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:09 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e2a494e5ed62e2b3151c41d1c4434bbaad62c78ef21b8f0ca7864cebf444d0`  
		Last Modified: Mon, 22 Jun 2026 18:05:28 GMT  
		Size: 89.4 MB (89357524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3af4ab38945b318dd62015d56c9ede89fc02a80934235a8605997ef25de56974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acff5e0667fe0fbb767021fd3d1f6b4c3174c397c0590a6014635d30e48b08e3`

```dockerfile
```

-	Layers:
	-	`sha256:d481ab5ddbd12b5260f2826b18df418444057d159078fbe12e2d9e608e92ef33`  
		Last Modified: Mon, 22 Jun 2026 18:05:26 GMT  
		Size: 5.2 MB (5197547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e621a395488440f249f5429b561ffea31237963226e86863549fba39a53345`  
		Last Modified: Mon, 22 Jun 2026 18:05:26 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:90d7970239818994e21a21e86c9f8efa008bd3d8ad82e36c9fccce596f766d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141943636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94eae2fd1e82a9f9d8a3129db6045c26e14ed2a07dcdf0bd168e2ba9009560f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:09 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:15:09 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:09 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:09 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5147ce7cbd5e79f6dac5016ccaf2017ce79cf03bad756ca35efbae6e9670c06f`  
		Last Modified: Mon, 22 Jun 2026 18:15:29 GMT  
		Size: 88.5 MB (88492950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f514a3c601e0eb7420f8c374bd5e0fd3c6f6a6cfa38b62bfef2362468654dea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4d5f37175b49211afd05134cfcacf4a50f23f9cdd234b3aa8248866b18ba3`

```dockerfile
```

-	Layers:
	-	`sha256:f77fbd1bcc1255a5c4f91c5e301e4947aa8b8741d98e81b891a81a776497a5d9`  
		Last Modified: Mon, 22 Jun 2026 18:15:26 GMT  
		Size: 5.2 MB (5196338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33be492032041bfa45f8c34388c6eef2e14a32f6f15f1546d2d16cbfab4457ff`  
		Last Modified: Mon, 22 Jun 2026 18:15:26 GMT  
		Size: 9.0 KB (8962 bytes)  
		MIME: application/vnd.in-toto+json
