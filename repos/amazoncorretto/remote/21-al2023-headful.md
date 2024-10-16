## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:3d2e593b4c25e48eec5c0550a7d292d9457ea6245b86457837a9c3d4a4940ab0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d1076f709f6b39cb90752743b05a5cd20e45cd530ce8d293defb31fe2b3e5f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141947841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d97cd50370d99b146a2631a3070174dce47bdee623c1c9c38608711b4b4542c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:49 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a313e9712a773a653d7b7df204b007beaada68024f65f87581c89f0e2c47383`  
		Last Modified: Wed, 16 Oct 2024 17:57:32 GMT  
		Size: 89.6 MB (89622536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:72addff36b54b7ef447f126493302e2699edbbba2cc0745e44c3ea43c0698bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f0477f719a6a0d38fe7f73b20765221c20b60114ddc7cc6b35141a2a979317`

```dockerfile
```

-	Layers:
	-	`sha256:c34923116d802dbc67838c1d488bf83baa69a95bcd537e04aa286a54e80f8fc1`  
		Last Modified: Wed, 16 Oct 2024 17:57:31 GMT  
		Size: 5.2 MB (5211309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a41d05e218bc66566846029df0e2c9795d55a50bf26e1d361f07af4bbd760b40`  
		Last Modified: Wed, 16 Oct 2024 17:57:31 GMT  
		Size: 8.9 KB (8936 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f9129ceaf785daaf38d702d2718ed411176ba6ee00215876acb26898f51c5fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140111891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ae763167238ba0e7b5a0a9b5e7beef8ae3124c60aa1999aaee0bebc9d331fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297b35094500b1ca957c3beedbc5298d8fae9f28d9dccb57ec00db2996d4d7b1`  
		Last Modified: Wed, 16 Oct 2024 18:35:38 GMT  
		Size: 88.7 MB (88685527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7ec7e60eb66458bf56fc2b69982946b2d2507e13d9847acfad2d77ed1eab22b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a789943ce515013833c50740ee009186c7566908a0a967ded332e6a59c47bdc3`

```dockerfile
```

-	Layers:
	-	`sha256:3403ab3ea17aeb3f4008f0416cfbb6401bf815a81ff4faf55653c39f35867dce`  
		Last Modified: Wed, 16 Oct 2024 18:35:36 GMT  
		Size: 5.2 MB (5210100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2abd94bdd07678524d2cc111efbe9c799dabf9e5045c690d33e352fb84a502`  
		Last Modified: Wed, 16 Oct 2024 18:35:35 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.in-toto+json
