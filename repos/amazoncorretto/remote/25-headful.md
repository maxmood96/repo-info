## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:95a37efa5d087c9d77b6252e5e1b65b05045625249ce1278dd6674b5589bb494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:df11940310624cd96ac7654933e5991f939b2df58e062a7172a015552f934935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158903487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78fae5cffc4714738fb1d9797ba1b9d9ee83ee1770b8edf34989d1a35fabd52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:49:43 GMT
ARG version=25.0.2.10-1
# Mon, 13 Apr 2026 22:49:43 GMT
ARG package_version=1
# Mon, 13 Apr 2026 22:49:43 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:49:43 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:49:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0e3c1113673735409b32f254aaf79d2a700211b4cb9c616aa39ffc00ca59cc`  
		Last Modified: Mon, 13 Apr 2026 22:50:04 GMT  
		Size: 104.3 MB (104332233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dbb9946f7adfdab50e4cb0cfbaed39322d92f86c63f8b8fc34c95b320652baf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5236031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee2699441c52f9000ada36236af3a3adb9fe9e7d78c5a469fa429991bf6f093`

```dockerfile
```

-	Layers:
	-	`sha256:9223f35850cba0c6a96ab10645056803001fe4c2880941cea2b0580b619114ad`  
		Last Modified: Mon, 13 Apr 2026 22:50:01 GMT  
		Size: 5.2 MB (5226662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4940660840400d00e7d8bf54417eb44bf17bee29a1826dc0db3ea6786e423e21`  
		Last Modified: Mon, 13 Apr 2026 22:50:01 GMT  
		Size: 9.4 KB (9369 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:821737d634d5058a5772e5164b82c50b1d4d1731058596311da9e90b7ad0611c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156704621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89a290a5987e612afde3dcd1fb00053cc210bbe2664d4725ac69c6572951dc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:12:20 GMT
ARG version=25.0.2.10-1
# Mon, 13 Apr 2026 23:12:20 GMT
ARG package_version=1
# Mon, 13 Apr 2026 23:12:20 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:12:20 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:12:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498e824260ead0efc4494eabd72be2f86ab6bf8dee50bb7dcd2d9b98b674168`  
		Last Modified: Mon, 13 Apr 2026 23:12:41 GMT  
		Size: 103.3 MB (103261882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:55b845d1ccd3b61699d33e85bcbd0fb2616a7aadbff250553fd04ae1d9f1c5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da437465ad911e789a152ec4789efc0fbabba440104d5a96e3a7e878d3b46a08`

```dockerfile
```

-	Layers:
	-	`sha256:109fad1482635b56d4580e4688f356e71c2d8b550c405a441f3836184cb79366`  
		Last Modified: Mon, 13 Apr 2026 23:12:38 GMT  
		Size: 5.2 MB (5225476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb998370e06e7d7734be4abb9aa4e531ee7d9b9031f93142ffc721104f447be`  
		Last Modified: Mon, 13 Apr 2026 23:12:38 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
