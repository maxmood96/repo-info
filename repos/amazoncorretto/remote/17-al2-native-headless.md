## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:01d8ab62928413bdb737f28426951a36ed51cfb32598f18466548e7e1ea78204
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:63c14a8315edb1ab011cc2c4792da587b4c641ea6061d0fa806ad8f0cfdacff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150549565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6346e7b5a58046275eeb24397fc93cb92d28efc31c3eac061bc967951b9a78f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:46 GMT
ARG version=17.0.18.9-1
# Wed, 11 Mar 2026 18:33:46 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 11 Mar 2026 18:33:46 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48682dc7b83d4dbf871bcb42154fdbd3ac3ee27a581b4e3f9985f2d0884769ff`  
		Last Modified: Wed, 11 Mar 2026 18:34:05 GMT  
		Size: 87.6 MB (87593055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f359c31a05db763571cc0bb2774b16d264d725053e8c49731b07f3609f6a7211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298a429ea89275d335730e9689d52523d9998e97c16b790f03daf9c432b44f53`

```dockerfile
```

-	Layers:
	-	`sha256:c752238428900dafe9b017712f9cfb38bfe829073e3088fd857b54c5338ab848`  
		Last Modified: Wed, 11 Mar 2026 18:34:03 GMT  
		Size: 5.6 MB (5631759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad591286c9c49f8b84df423c25601a94c580fec6bf0b39e4bbec31ca8d5270c`  
		Last Modified: Wed, 11 Mar 2026 18:34:03 GMT  
		Size: 9.3 KB (9293 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6c80d1eb010b8329b17d5ed08276ef09a43dd56773144083dcb12169a13ee0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144631997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b010cb8f574e34473f1da402600a5ac64bca583bc87f54fb9712050c36c8a17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:14 GMT
ARG version=17.0.18.9-1
# Wed, 11 Mar 2026 18:33:14 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 11 Mar 2026 18:33:14 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5492f8438a8af75664dea63fa90e78684c48b2bf662d57301e843f820f2756a0`  
		Last Modified: Wed, 11 Mar 2026 18:33:32 GMT  
		Size: 79.8 MB (79828848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6d8cd8f9b2d5df8377e9808f31c11c40f80c70b6dd4f00846b9072a74a99a7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfd2fb6ae1049cfecd442b363326c717c58e402cba313cc34b2f852e5ff0ab7`

```dockerfile
```

-	Layers:
	-	`sha256:65a294c9a6e0f4bb08edcb312ac481061c3ecfaa9d01b1d793e76110155191d7`  
		Last Modified: Wed, 11 Mar 2026 18:33:30 GMT  
		Size: 5.4 MB (5448035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058033235bc4961fd78965cd86812a46d6c9553750d7bdb95c861455f8cd3303`  
		Last Modified: Wed, 11 Mar 2026 18:33:29 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json
