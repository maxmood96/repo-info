## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:056e039474036b98272134794546302360e4e686bfce52bce2124738dfdc6014
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c1ea1f3702925f3b4f92aed29dcf090833dab2fe3e83ebe11fac4505a9476120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150538327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41272d47c80895fb2dd1098d68d0108306c5840ddc155e04728b0aa6683e465d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:15:07 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 22:15:07 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 06 Nov 2025 22:15:07 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:15:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3caad92509f14215a0a19b9d29cd180809c63252a0b74d8911ec71295e38a8b`  
		Last Modified: Thu, 06 Nov 2025 22:15:39 GMT  
		Size: 87.6 MB (87604193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:24fec446e32762b22e5c2b816377dcd3344831d0b26466ef23263a72a01dfa52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44c20f5243986efd1810b34bd9798d027b26c1827767dc6eb662a30d5e5d923`

```dockerfile
```

-	Layers:
	-	`sha256:7a16096a954d4325f11716359c2ada0b4b2eb8d03a71dc7504d551e5de2688be`  
		Last Modified: Fri, 07 Nov 2025 01:49:02 GMT  
		Size: 5.6 MB (5631759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e96086c47783db64f98eb11373b2270c6801a3cc3a91e9d73ebf53281b5bf0c6`  
		Last Modified: Fri, 07 Nov 2025 01:49:03 GMT  
		Size: 9.3 KB (9293 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:56849b2ca28479dfad826e1bde5f3557a4bc58d94e2bc69e897473afa6b7164d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144623820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902b7d85e8c7d7f77183bde14fee75c2de2b6143111fa74b931430c65b4ee44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:53 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 22:13:53 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 06 Nov 2025 22:13:53 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b90df2139b75b357dc5190eb81494ac9d1335fa95f2955d86bc73b8e4f89ec`  
		Last Modified: Thu, 06 Nov 2025 22:14:25 GMT  
		Size: 79.8 MB (79830524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:26fed698c5ef82d1748e8a4eef4f7df834424de3a1c9f0bd76612bc163a0bc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c13fd1f243d70ef52bb239e108fa0b4f201292837187b34edb4725bb8f426`

```dockerfile
```

-	Layers:
	-	`sha256:8814ff166bc825f7fa2d3bae73e0f0b38f32b8168daa7ff3a5730f76b7083955`  
		Last Modified: Fri, 07 Nov 2025 01:49:08 GMT  
		Size: 5.4 MB (5448035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e58aec591d80e193c12d1acb15474fcf9800cd2231ee2a33705488a02b1c59a`  
		Last Modified: Fri, 07 Nov 2025 01:49:09 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json
