## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:fab827b49be75a374c64af03e3e4eddfbb16b44df1555912988c96e0b264e010
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8bfbc87412a37719b1f9b3d17c90197a88d6a6628d648a456363a857f3268e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172082874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c9564c012460603fe5ce4f7888dd7ce04e5d10de727887f1a78bf6c675e91d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:13 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:59:13 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 21 Jan 2026 18:59:13 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea7aded83d340474728f759b9c7ad6cf2ba7bd827ad112f1f6299ebb756535b`  
		Last Modified: Wed, 21 Jan 2026 18:59:35 GMT  
		Size: 109.1 MB (109142718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2f1f45ad154030401c27e6f2f50321b69c16c53e153718c1730b2371f082da2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dd09871420529db5ed04e75f067f6847f39850ff7d0d65571ed1000579ce4b`

```dockerfile
```

-	Layers:
	-	`sha256:9ac08bf836d343cceafc0d77fe3efb56c9823b8cef009f6ea79c413ca3bf312b`  
		Last Modified: Wed, 21 Jan 2026 18:59:33 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a34562be159a570461f1bb9c9b9a4dd4ecb4f8ca1211fa6f8c46c0eb8c201c2`  
		Last Modified: Wed, 21 Jan 2026 19:55:04 GMT  
		Size: 9.5 KB (9505 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c1a9b7729a14d4c6d180d21a833cd94c0e11639da2f8cd15e00faf5d0a7d871f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117741426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5592d403752f196700ed46124d2cac0d878f280874890ab93ec5b31c7602b72c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:23 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:59:23 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 21 Jan 2026 18:59:23 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 07:47:55 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e9e6d177b0dc862144886f0c37f2d2277940a325f87643da48589acb7a60de`  
		Last Modified: Wed, 21 Jan 2026 18:59:37 GMT  
		Size: 53.0 MB (52970992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:87149fdc5edd182b0c84d1f79ca15446ca4fb0919e6320b3498551365be53574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0129d2e3fb665166ad08026b980845cfed45f24410813181d4ad00012179025c`

```dockerfile
```

-	Layers:
	-	`sha256:5fc1bb365abefc983e3cf640cd89f6cb52d0a8639b19d9b57be653e026cc177f`  
		Last Modified: Wed, 21 Jan 2026 18:59:36 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2ee9f90e57bfc681b661e51cc287eda2ced59e10da5bdb10d84f1716f06a9a`  
		Last Modified: Wed, 21 Jan 2026 18:59:36 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
