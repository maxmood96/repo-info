## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:451bfd60816af47d3bb3afa420b3db8deab8fc2f87a4fab4df7d4cab4c5170d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f2d04601efeeda19f81e93748a848959210eb433686d4aa430bf49ac85a52fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154352757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652b2895a6146f92e371083d5bfd2398ba730b0d1dc5dfbc9472dd98b3f71772`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:28 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:05 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:12:05 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 22 May 2026 21:12:05 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:45dd431b24e3561020a83f5e29dd2642d9ec2f2788c6826e5b1e9ee25ee38759`  
		Last Modified: Sat, 16 May 2026 04:14:19 GMT  
		Size: 63.0 MB (62951975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8793ef5ff529caf61777ed01c5f119483cae765fa7f2cc77771dd5ae33dae9`  
		Last Modified: Fri, 22 May 2026 21:12:24 GMT  
		Size: 91.4 MB (91400782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6a36b84150e2fc50bd15a8b2b632c4caab803dff34884714ba229f9ac4d5c51a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5876330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9f229fce2879f7c81fbc9102fd7e7027824f26008acc4e89afd935b5ef0587`

```dockerfile
```

-	Layers:
	-	`sha256:5a56eb6aa78c9033e2e52c33f65da156c7a5cea8b8dc3601e6693fb50b615947`  
		Last Modified: Fri, 22 May 2026 21:12:22 GMT  
		Size: 5.9 MB (5866740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d685860e66bb42fbb13e818cf1948c626a1a9383fe583e905619bc31098b27a`  
		Last Modified: Fri, 22 May 2026 21:12:22 GMT  
		Size: 9.6 KB (9590 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ddebb12b91f0f2fc753136354c7c875af2fc05bc97a05351c8ab15cd59a48706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146882852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f0b26bb2f576e42430059ba865a665cb8d7a675b9af5fd74d7cbf38f49e6cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:43 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:32 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:32 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 22 May 2026 21:11:32 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9b55de233aca71116430038a4df795c9fbcd988648b5d3ff05692945d681a5dc`  
		Last Modified: Sat, 16 May 2026 15:07:44 GMT  
		Size: 64.8 MB (64790017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a040c0846939615373f61ff08ac0b7a7116858315ef39536e7132e2a4e80cbf`  
		Last Modified: Fri, 22 May 2026 21:11:50 GMT  
		Size: 82.1 MB (82092835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61bf88f0687a911e4cb16728776964935c6c975da592be43b8bd322b8a7eb1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5668154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09217bc46b13c6b653d67766f5af1352822adb903b17e5619e81e093262e653f`

```dockerfile
```

-	Layers:
	-	`sha256:f552637620a15e0c52787cd7aaf00d8c073946b78fc641887959b2b378ca2515`  
		Last Modified: Fri, 22 May 2026 21:11:48 GMT  
		Size: 5.7 MB (5658484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e90b3693f731d1aac5787f89b9134fc1977dfad014e38b1e38152661abaeeb22`  
		Last Modified: Fri, 22 May 2026 21:11:47 GMT  
		Size: 9.7 KB (9670 bytes)  
		MIME: application/vnd.in-toto+json
