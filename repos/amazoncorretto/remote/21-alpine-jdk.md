## `amazoncorretto:21-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:801b86a5da334ca9dfa60008e6e1171cf364ca6e81061fa161c681721c1c7018
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1766e7a7fc6c60827c325f31674a89a46ed51883776cfe388cde45a13629abef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165372344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157b7783fe98adcab2ae9c384f5cf5fe2d5ff098d49c87284c6ad35b2405ebf8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:06:54 GMT
ARG version=21.0.9.11.1
# Wed, 05 Nov 2025 01:06:54 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:06:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d4bc3368d3809cd8ad2e688cb5fe01f46190980ebdbfcac8e9822be3643f0c`  
		Last Modified: Wed, 05 Nov 2025 01:07:14 GMT  
		Size: 161.6 MB (161569892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f994424806ee4a7b585545e513e22a39001f06c1a4c83bc5de48a9333721bb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.0 KB (595019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a320d3bdf4c385f78df0bac96807d33439edba4f645e4cf66aa1ef6bf55fc81`

```dockerfile
```

-	Layers:
	-	`sha256:25b978b7a9f7f423c6135b6408a6f1a40327543ef3b8c60543010944c62395b3`  
		Last Modified: Sun, 04 Jan 2026 08:31:27 GMT  
		Size: 584.3 KB (584341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96d31a8750f412262e3c2f3be4b569d1499758a0f7a717b07f7b154d1512c3f3`  
		Last Modified: Sun, 04 Jan 2026 08:31:27 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:96dba0f62697e55be5c80af65f13718709d701276d014ae5b9bc0df9df2489ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163726568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e888f1784ff4ab017a75dce88e2b60d4891f8b4305cd2b2bd784b541ce2a381`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:21 GMT
ARG version=21.0.9.11.1
# Tue, 04 Nov 2025 23:16:21 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:21 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fd450f0185222facf50c3585803b24553a293cbfa900eb12641a7831d0da01`  
		Last Modified: Sun, 04 Jan 2026 01:36:57 GMT  
		Size: 159.6 MB (159588499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:32a07a6fe30dad0f2a39c038c2ef63cbe7cb71b2a66fed683bc71e3df00949cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.6 KB (594638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48857fc02dc5d5b3d6edc04f74f5a23da6958cf44bd463750e302219a1c1b3ca`

```dockerfile
```

-	Layers:
	-	`sha256:fd996e20d2f56753ca03bb7b161681ca610f59a274379779d36b49415c72952e`  
		Last Modified: Tue, 04 Nov 2025 23:16:37 GMT  
		Size: 583.8 KB (583808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187994aaaa97a175db74c047da827242b630cea289bcdda2b0791cea7a41247b`  
		Last Modified: Tue, 04 Nov 2025 23:16:37 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.in-toto+json
