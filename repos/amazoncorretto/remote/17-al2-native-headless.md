## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:70325cfbd0498b5ea553ee7cfc2c2d8455b4322be140721a9ef97ce5f7f7da21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:04a8a8b47794804b14f81b07b4218c39ba406e85ce6a81c33fdfbff313a06f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150486609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e491e0df56fc4fe8254908a097ed10b9abbb03ab2c5937b125bb6b40e1a559e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:fcc68e74b985a5b6eee4c73b52bbf6b5465b7b43a029c51e8950289a9262b97b`  
		Last Modified: Fri, 19 Sep 2025 15:29:12 GMT  
		Size: 62.9 MB (62933841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd0d80722fcebcf2d71e2f38dbe43e6325f098e5a6ef21583dcf8ebc2bcce85`  
		Last Modified: Thu, 25 Sep 2025 02:16:09 GMT  
		Size: 87.6 MB (87552768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dd909b64ad9630f4d4ea0935d2c4ced4e87485e314370f9252cb2629da491a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a8ab88500840f7cb5e577a1bdbb7b3dce72bda92edd37420d737cb0c336253`

```dockerfile
```

-	Layers:
	-	`sha256:cfb7a04014aa29ba783d342555f9c5c5a0b52ef0106634265f14875af6fe9548`  
		Last Modified: Thu, 25 Sep 2025 03:49:00 GMT  
		Size: 5.6 MB (5631755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d9de243eda57b6d236cb02dc60228a3bdc8e0879ff61776e803f3225726fc5`  
		Last Modified: Thu, 25 Sep 2025 03:49:01 GMT  
		Size: 9.3 KB (9335 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4b58f6f4d0fb5a42cdda45180b741ce38c998e4d351f9cc1c11efdef5aba58b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144581907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e60418c929d5400f5db2a10b98fe0bc9e761c78dcf135679b83ceb4e51572e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:43d39e1e5d32e8ac06f789363477524a09029961f1236d4dc3927f200c572bee`  
		Last Modified: Fri, 19 Sep 2025 23:24:58 GMT  
		Size: 64.8 MB (64793147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143344ce45dcf1777561bb02e01eb390abea3b73d70e8adf4934508c4b441f56`  
		Last Modified: Wed, 24 Sep 2025 21:13:23 GMT  
		Size: 79.8 MB (79788760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:16b4406a8c84a1e8f963b23e6bd0b70c8d19697454c7ef914f120084405368cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c598415e0e114a72001774f1fe21e7ab7bbf3316e0aa5f973e1b249450f481`

```dockerfile
```

-	Layers:
	-	`sha256:3a7ffc37c36260dc289fcc131d5fc239123abf6df9a08d4762f10eceb488557c`  
		Last Modified: Thu, 25 Sep 2025 03:49:06 GMT  
		Size: 5.4 MB (5448031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5b60de983df13ffba22259807e375d1b55f21a3ff547ae1ed7d7cecddf98ddf`  
		Last Modified: Thu, 25 Sep 2025 03:49:07 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json
