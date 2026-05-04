## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:b48165097c6ff93938f21b333c10416da83095b0737fec93dde12c82cc9830e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:19abc44e639fe60666b453f27818310f82660f862dd4b23ebd0c58c5c58d36ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154197116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bc9c0bb277140267193449058ff4390218e6125db11d827703c45253e32ac1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:40 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:12:40 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:12:40 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb75b23077792d007666eae963afaf504e047c68d3a3efb0d6f474122fd843ed`  
		Last Modified: Mon, 04 May 2026 20:12:59 GMT  
		Size: 91.3 MB (91337107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:154aa0a29ab57f75846da4a522fc9fc5ed53cc82a70d6f60f633d255ce9af050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5876330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bb9d54e9a03c24f6a323d0d6a43f913edf2d4b8c86bf392435cf0f6a55540c`

```dockerfile
```

-	Layers:
	-	`sha256:59ed3d5905c8c2a6ad351b9a9672c4f5fcf602e0d7c03ee2e7f39e12f57cf799`  
		Last Modified: Mon, 04 May 2026 20:12:58 GMT  
		Size: 5.9 MB (5866740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:126d5765d251d40fcf03514b55d7e53bfeaa12d24648e99b317e9d74b2667cec`  
		Last Modified: Mon, 04 May 2026 20:12:57 GMT  
		Size: 9.6 KB (9590 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0ebb53caf62bcf4758742c90b674757f45e0fa04f5b0cdb8d8e001fa984b1946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146896704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b9a43f3e5e1de65208bbbb74cc066e78048d1d3a7a3e13b99560aab5702dcd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:23 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:12:23 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:12:23 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8622c08cd4d3a7e5cf1962b57ecb16cd22bc700dd044fbb892a2c5ccaba10564`  
		Last Modified: Mon, 04 May 2026 20:12:41 GMT  
		Size: 82.1 MB (82101173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f155c93719e160421e485c88a3d71f7ca73f14746dfa017609b84c92d2c7c93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5668154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea5b47f9a67be53ed9065d56593e47989bdf37dddc466addf21b272ab727fae`

```dockerfile
```

-	Layers:
	-	`sha256:140b8e83e55ff659433facd57a52547a57dcb4436174ab2316a82ab5cafedf77`  
		Last Modified: Mon, 04 May 2026 20:12:39 GMT  
		Size: 5.7 MB (5658484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d74f313db208b1266c1ec6b62fb0a3e41de081d23580453064ff07c6a8cd2e`  
		Last Modified: Mon, 04 May 2026 20:12:38 GMT  
		Size: 9.7 KB (9670 bytes)  
		MIME: application/vnd.in-toto+json
