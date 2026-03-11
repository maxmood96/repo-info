## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:27325a6d2ebde1498f07ec27102c6d00fba40128003512b3658e93f323f292fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a14bed5e16ed1723af378a519a3a31ae7e8087158475d1b925bddffcb67584b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217305311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fec5ca75abd4d6456134260293826637fcde0f6da4391c95ed1736cdc9b737`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:04 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:33:04 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 11 Mar 2026 18:33:04 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b445307cb522af0dfc2b7b1173ba1e5824626fb2e45b1c508cee58bbc38b0b`  
		Last Modified: Wed, 11 Mar 2026 18:33:24 GMT  
		Size: 154.3 MB (154348801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:717052336ec7d8d4fb0577d9dbb60a97f6d0f87e6516c4a76d926f3faf3ddf33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d17b84458b6477fb2f5fb6b7f25f56e961d27eddd4cf1629072a7dd9284b7a`

```dockerfile
```

-	Layers:
	-	`sha256:58e2b29cada89e350557c37683645be2a2ae1eae2cd2785adbd5b905fe804cec`  
		Last Modified: Wed, 11 Mar 2026 18:33:20 GMT  
		Size: 5.7 MB (5683305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51924494733b9f4d92161e9eef0be1b2b86eb0535bc8a992be36e302430e7a1b`  
		Last Modified: Wed, 11 Mar 2026 18:33:20 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3fc6a054df16292de5171151c70dc30b2ec8c52293ed431e6921eeb0df69182c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211403751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa9e8dfb78e37ba0dba94817e47ee5ebe46940dce9a65c58b9463debad7c17a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:32 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:32 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 11 Mar 2026 18:32:32 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4db4b34afc738b1d8585e11342e7d57b9681050d6f23293daa783c3b35f98e`  
		Last Modified: Wed, 11 Mar 2026 18:32:53 GMT  
		Size: 146.6 MB (146600602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d9295ad5515e4fda691bd338d77f7395a85858bd4ef9df5a35b06d6a13e6b6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892ec1bf5d959094eace8c4b350dc083c0383e9a569e109339df87b2de70a60f`

```dockerfile
```

-	Layers:
	-	`sha256:0710e0d0b3c67d248ea5e02a48db8b378cb50eaedc378f4ee53cd9ab3e833f02`  
		Last Modified: Wed, 11 Mar 2026 18:32:50 GMT  
		Size: 5.5 MB (5501773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b017368f44b36f168d485e17e7a113165f8f23d9aad62f848aab3fdd18239ca`  
		Last Modified: Wed, 11 Mar 2026 18:32:50 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json
