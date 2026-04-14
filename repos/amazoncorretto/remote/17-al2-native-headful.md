## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:a4d3bd49516aee5bd5c09f252816122ec1eb55789642475fdbcb929cc12ae5df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eb490561240ad134fbbaae448027018d9ecc76ba84070f0612385c3d5b976b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154243575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696198bf2359896fe7f15e2f7e25b5b884d33c5c3e515731bdd59ba8ca1d13fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:57 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:49:04 GMT
ARG version=17.0.18.9-1
# Mon, 13 Apr 2026 22:49:04 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 13 Apr 2026 22:49:04 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:49:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68398da4c29cdf848ce1a984c634ccdfab78a35e5e3402180d543a429cdc7967`  
		Last Modified: Mon, 13 Apr 2026 22:49:23 GMT  
		Size: 91.3 MB (91288309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6e3996d4b902fdd5aeb68874dea561752721e881004ee2cd9a0f288f4f085115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5875499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac27e8263eb0fa66075187d868d3dddf01d2acbe4108d6d7bbbde17b516e819`

```dockerfile
```

-	Layers:
	-	`sha256:fdd7e0d5c1bf949776d821860c3bf5223d28d680d984e90744ea22131d2c7726`  
		Last Modified: Mon, 13 Apr 2026 22:49:21 GMT  
		Size: 5.9 MB (5865915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ed899a64c78cbd4596fe09f3f5ce789900370658d8bd5bbb8dcf31ef644a18`  
		Last Modified: Mon, 13 Apr 2026 22:49:21 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fc16993e6a02f7ca0f70f54788291c8ac1ec945ccf2d6c570deeca43a4942a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146791006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfe9695aa6f46ad16dd49c9d7dacf8c78a5cbae9311157d3b74a7d478ba7eb9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:22:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:22:09 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:11:47 GMT
ARG version=17.0.18.9-1
# Mon, 13 Apr 2026 23:11:47 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 13 Apr 2026 23:11:47 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:11:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e9ef1e3e2810479456d22a6e06c2d313a88489b79354a0803c785188185a9`  
		Last Modified: Mon, 13 Apr 2026 23:12:05 GMT  
		Size: 82.0 MB (81988031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:41337b714424e254c2d3cc2f5a639c5f3fb3d0fc3140fef9e0f9e486f9be7487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b0fd5f3baeeaf986bd03d5e671849b1773e8212e06f14fbaf9d90f78758639`

```dockerfile
```

-	Layers:
	-	`sha256:0a9c427996ab41c8c209e635c45a44f66004d3ebf15205e5700cf35f95432ab3`  
		Last Modified: Mon, 13 Apr 2026 23:12:03 GMT  
		Size: 5.7 MB (5657658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24fc67e10a99b616e7444d4ab3f0cc453a933f44d44f7121032562227a846be7`  
		Last Modified: Mon, 13 Apr 2026 23:12:03 GMT  
		Size: 9.7 KB (9665 bytes)  
		MIME: application/vnd.in-toto+json
