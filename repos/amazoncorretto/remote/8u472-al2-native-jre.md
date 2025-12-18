## `amazoncorretto:8u472-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:8bbc099983c99bee6707fb151c06f4ea986980f02c26febb24724596c9b02613
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:98ab8ac4ed55afed35bde0374a0490e21f7317ff6a2d22b4c183b2f6c543c9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172059220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05422ca8824dc2726e0e01f035f2691b55d7f80f5d8309f2c0703e1fa1abbff1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:17:28 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:17:28 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 18 Dec 2025 01:17:28 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:17:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e5d9d74edc17203dce4061221bf6c21c4e2fe9ae24107a3bacab9cbd5e059a`  
		Last Modified: Thu, 18 Dec 2025 01:18:03 GMT  
		Size: 109.1 MB (109118245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f556ec9e41e14eaaf0bf043298d2ddfc810b3cc17a92cbe9bb337fb1f0baf748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1c99dd3d8a0f9303978e445680eff7c7b7bf7f064b489cbfe4b3210812a8fb`

```dockerfile
```

-	Layers:
	-	`sha256:1e94b59a479127dbcb67d5792ed695a49e721fa12d42282d87a5c63ab04710b4`  
		Last Modified: Thu, 18 Dec 2025 04:51:58 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68824534ddbef3d66c3a502f7649a5217c1dd7e7cce42172d93e18a9f5f7a95`  
		Last Modified: Thu, 18 Dec 2025 04:51:59 GMT  
		Size: 9.5 KB (9505 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cc4fe1091d19eb63765bf4bc3c08a80d790dc0989fb9508b4b83688c32aaa2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117736268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7b441bd9280c3ad8326a6a368be58449c1d547d5ae15edb8ea9abc7edca899`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:25:18 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:25:18 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 18 Dec 2025 01:25:18 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:25:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2058880cd8bedcc32090e18c34940c35630e757b8ac4d8cc7465a0dd1ddc96`  
		Last Modified: Thu, 18 Dec 2025 01:25:46 GMT  
		Size: 52.9 MB (52940513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d0ad8ee57346e50b852b85a3d9bf0d1c4c87b1e34f80a3464c4fa1df39aee856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a81299c8eee5a3484ff803cfd29a64f9e578afa077252e730b037e07a00749`

```dockerfile
```

-	Layers:
	-	`sha256:d1c43985eb0f3b8fa87d3e9fa47f9d82910af1dfb9a491f4c3e368425ee3bf8b`  
		Last Modified: Thu, 18 Dec 2025 04:52:08 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cd9f32ca13c364fe5bfc421a25f9b2ca2f5017c37588b50c97063e0f3b973f`  
		Last Modified: Thu, 18 Dec 2025 04:52:09 GMT  
		Size: 9.6 KB (9583 bytes)  
		MIME: application/vnd.in-toto+json
