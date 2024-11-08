## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:a2a0e05017e763a808bbbbe73eecabc707d4696de7997d076d548f0f4d272c05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6be059237bea8f985744a2d52428c7f7a656bc003b9450b82f8a526933172e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217578688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82853dddab97b5178461c17f4612b30e0441a83747f6ede55948caff72e9e278`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8430d4c5a00587f0a8dc4c62f82455c123b54b9016d43897ee77c496c018a8bd`  
		Last Modified: Wed, 06 Nov 2024 20:48:04 GMT  
		Size: 62.7 MB (62681042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2590fcc8201373236858981f9e3960f4b15ddf01dd626ff79be70ec4f67248e5`  
		Last Modified: Thu, 07 Nov 2024 21:48:04 GMT  
		Size: 154.9 MB (154897646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8be270997e72c10c220b99364f0829cbbfee87a8614e44b6acc1a56809de4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5688089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f8463394e4f8dde0328383bc0039291e58bce0628adf3eb94ea397fd459541`

```dockerfile
```

-	Layers:
	-	`sha256:718521e8c9cc41784aa645064248d0ed34dcdb12c651df5a7b2fdae3ee8101f2`  
		Last Modified: Thu, 07 Nov 2024 21:48:02 GMT  
		Size: 5.7 MB (5678758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff8bfa36fb40d6595e8edcf56c5426e15d9786d54f32bd46e24c626da84e51f`  
		Last Modified: Thu, 07 Nov 2024 21:48:02 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:51607f45bade1daa8e366341c315ec40be829b60ad6e867d964553e1ea8b1952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211824151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d9fc8dffc9b4afaa8016021027268032292cc82f8109ed65d15e8c2abe790f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0a62aca1c7d7ec3e0e098bf23685d8f0fcd19e33577a91dafc6dd30bef06deca`  
		Last Modified: Wed, 06 Nov 2024 20:48:17 GMT  
		Size: 64.6 MB (64588571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d591b3668e7a14c93cc4ed7151a421f3af9bf897b73b43db26b0f201396886f`  
		Last Modified: Thu, 07 Nov 2024 21:54:30 GMT  
		Size: 147.2 MB (147235580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a4418cd1c36c34b567c38bcc5a68b7778afed7ba0f9164e593a00509344403d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5506339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706f96350cf6905b33911a4ff80d4dea962d2c85e8913b3b3a6b9e23881bb996`

```dockerfile
```

-	Layers:
	-	`sha256:735043bb5de859d6ab2702d9d33e34b66969ac6f95575c1ac1c0ed6dfb174e95`  
		Last Modified: Thu, 07 Nov 2024 21:54:26 GMT  
		Size: 5.5 MB (5496929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b16940a5a4ed7a65d0c911e81cc84d4d529de432c12211d8f7bd6f1829c126`  
		Last Modified: Thu, 07 Nov 2024 21:54:25 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json
