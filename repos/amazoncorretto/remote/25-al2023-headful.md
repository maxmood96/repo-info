## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:2e62d3c9b0a150e57082b5aad02a575ee4fa1265b33da228689ccbcd72f4714c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:59d82fdd60bb171a913dea0fb2fea7a73db67c718e645315f953db40dfaf8833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159013833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd251ff6084dde38729b4949fcdb7e15622ee57a41acf11a9df6482931aab8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:34 GMT
ARG version=25.0.3.9-1
# Wed, 22 Apr 2026 21:35:34 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:34 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:34 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9055fd290922db3c3fd9470586062355f149eb0c0a562039fa4e8e7f6e42d1f`  
		Last Modified: Wed, 22 Apr 2026 21:35:54 GMT  
		Size: 104.4 MB (104442579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7ce4b6b4e3b46a02576c1d255d617c7b3a6f160e11f7f1add71508b3c237e70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5236843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cad5ed5d60ccb000712ef2be6203e4f5b2a13d112746486b9cfb5c43e140470`

```dockerfile
```

-	Layers:
	-	`sha256:d63162694dd99072e32dba225cad478eb0cecdca98c1695ad3dd7de6305defe8`  
		Last Modified: Wed, 22 Apr 2026 21:35:52 GMT  
		Size: 5.2 MB (5227475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:163e8ff94fee9bae84f3684b364d04518ec62799fddb3b3072a9a8c09bbcae0b`  
		Last Modified: Wed, 22 Apr 2026 21:35:51 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1cb839ac3f216ee7024f4b121948e323313b59f94341b4db63aa9625a9efe630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156837093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1e48ae5d62135b5e608cc61e4eccf0f21cb30dda84771e7d8be10b6f52b8d5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:36 GMT
ARG version=25.0.3.9-1
# Wed, 22 Apr 2026 21:35:36 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:36 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:36 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c1000b61ce1b6d610a8eef4c49c376c96d486086e6c52abaef389edfd6f43d`  
		Last Modified: Wed, 22 Apr 2026 21:35:58 GMT  
		Size: 103.4 MB (103394354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:32d7c8cb3035e8a2edad35dd0f6e59fe6b542d6988ed2f2c15e5f5df5401de2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e786601ae7e81d515cf9877b69f3063cf95c010afc35555b4409781a332e1d`

```dockerfile
```

-	Layers:
	-	`sha256:988512fcf975cdabeb7da908e115bde13311d13d2f5a4f4f76c08bb752bfc2cf`  
		Last Modified: Wed, 22 Apr 2026 21:35:55 GMT  
		Size: 5.2 MB (5226290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba05714e0bf17b81be5d2e8d6c60fce1169e0cd10cbe2cc375024029db68345e`  
		Last Modified: Wed, 22 Apr 2026 21:35:55 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json
