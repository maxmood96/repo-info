## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:5647618563bf0e8f0fec1609651a4e5fc3895fe0cbe2fd972480a358aead094f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:94cff433ec5420a06b1cceed00afe537eb4c8cc85008020435ca2e5ff3314887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159012704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5151e6195f36a8eae74399b32b0a1144fd7683b236720ea41f26adcaa4857412`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:04:53 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:04:53 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:04:53 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:04:53 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:04:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d184fa9eb1b3af0c49066a74414a5c662e1618699425b8bad3f37f8d84ebdcc`  
		Last Modified: Mon, 22 Jun 2026 18:05:11 GMT  
		Size: 104.4 MB (104438521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4d89a7487de8ee82526a0a8427c4407babef992f5cdec9a22a486da82039d3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6d9a9c35aad8a45441b8437fc6b92beec76658cc6aced01c13c807aaf8f74c`

```dockerfile
```

-	Layers:
	-	`sha256:da41862e6cfd7ce1d786f4dc522cb5d168ae2028f31df30455aa30eb7c67bae2`  
		Last Modified: Mon, 22 Jun 2026 18:05:09 GMT  
		Size: 5.2 MB (5233233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c624242839e935b8f4e6d359b6fcc4b6a7dc8eeae575a9ca7a7fc59cd88855f1`  
		Last Modified: Mon, 22 Jun 2026 18:05:08 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a23a1dc574a680b0517f942d44995e7284a2111fff71a9172ceb90bde7c23112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156840013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9523ab85163f730ebf4146551f6971594d9c4ae5a730202dff26645b79226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:36 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:15:36 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:36 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:36 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2bec86eb8114c68be5da650918154ba280cc2aca986e2ceb61f9b717afe9aa`  
		Last Modified: Mon, 22 Jun 2026 18:15:57 GMT  
		Size: 103.4 MB (103389327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1aff5fac26c704794d7ace69960056ed86ebce67b913f125dc469929de3f7b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5241508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d255e338081c9f8d8ad4c77e27d46e7b528be4d14084b4790eba20128746294`

```dockerfile
```

-	Layers:
	-	`sha256:3d7b51cf9510cb3b5a9a3fe47616a0e3b3b8d7671988ad2624bbbe4112f42a49`  
		Last Modified: Mon, 22 Jun 2026 18:15:54 GMT  
		Size: 5.2 MB (5232048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6336c6694b54d5db6825a29345ee609fb62d3991aa1a8bcfeac82eb5635d0171`  
		Last Modified: Mon, 22 Jun 2026 18:15:54 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json
