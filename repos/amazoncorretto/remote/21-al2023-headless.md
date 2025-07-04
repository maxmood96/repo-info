## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:d894e82c9b643ae7935360609399b6c99c7dda13e0dfb2c4b08fed3c72dd0e52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6970b1a583098da0c8fca2527a9b08fbff229b41fe53b725fab4dcf17843e3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142861031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fa01ea7a3d403d0df87017a1d5a5a6ff2eb0c64affc0b83e2fff8b491f448c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a00db81cfbfcbbcc0cbe194011d1372b5452428d24845777fa6177ed15ce473c`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 53.8 MB (53840211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccca58db15b9c288d0812cd980a00a2977b9e5953cd813ebcb7619468247e134`  
		Last Modified: Thu, 03 Jul 2025 23:08:18 GMT  
		Size: 89.0 MB (89020820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:34807d24d9a41c45c18f34457c1bc1a53975b4c56a18a6b87342167bb72b5ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152191eba4f514024938bbfa7825890465e09fafd881ad3b523d73e779c3f5e1`

```dockerfile
```

-	Layers:
	-	`sha256:db788198f3699b5a58f2ee7727f45753054afffed5a33503ebceb366765b3866`  
		Last Modified: Fri, 04 Jul 2025 00:49:02 GMT  
		Size: 5.2 MB (5185143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8bb11a47c5bf1d80e322e9b56d369b1dc24ef7e61787bc950e0f1f0c78001a`  
		Last Modified: Fri, 04 Jul 2025 00:49:03 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f4220fbc4c53d653ea30479fe39ed83289b1f4dc4ea34fe1ecd77ea757ddb0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140646518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3c3f97d28f76511d479d51b9b07a5480974c8ef6764c6328f90ef3182c02f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898aacbcf0bfd7b51497ed8ec7d52303b85662a29bbcf78e295ab985ae0e3e0e`  
		Last Modified: Fri, 13 Jun 2025 21:54:48 GMT  
		Size: 88.2 MB (88164826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6d292a2c2b297fe429ae006d2b287c22d573ef8775eb55480487f775c2785218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff88135301ddffec583e5e45d95b5066539faf15f7694a300e298c6562cf24e`

```dockerfile
```

-	Layers:
	-	`sha256:818471f9d18550fc7c6971ca2e2a3434dd873f80bcd5bb832f3c1bbe3d903996`  
		Last Modified: Fri, 13 Jun 2025 21:48:57 GMT  
		Size: 5.2 MB (5183927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d02fbf70efd1150d57d0b1beccda4b88618eb565072685ea50c03ab744e4d148`  
		Last Modified: Fri, 13 Jun 2025 21:48:58 GMT  
		Size: 8.8 KB (8827 bytes)  
		MIME: application/vnd.in-toto+json
