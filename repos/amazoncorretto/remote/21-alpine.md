## `amazoncorretto:21-alpine`

```console
$ docker pull amazoncorretto@sha256:a5d354c8d10a4eecd4867df7d3787d9ae34c368a56c667f984bc0caee0a1b6b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:016b5a4d74cf71240f71ef5358afdc5cd793379b6a1aa8da7a094dda140d120e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165379996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5aa1730df25f8a1ae24c14c11066b17d19f3fd52a4aaca3092ce55b2573254a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0232a5c1ec36753528564a0c37c51dd325df2a291ba8a36a4d16515714648b`  
		Last Modified: Wed, 22 Oct 2025 00:52:18 GMT  
		Size: 161.6 MB (161577544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:475e7b16e152611b573a6c1e6ac9fd93938dce28ec94872a108b3f715b162a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.1 KB (595062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8075a3fabfa04564aff54aa4fb9286f2bbe40a9112d377e23b49ea7307cf1d7`

```dockerfile
```

-	Layers:
	-	`sha256:be86a69660d55666e135ce93442b5b1cbbf96afa756414c5352b306903e94aa9`  
		Last Modified: Wed, 22 Oct 2025 00:52:05 GMT  
		Size: 584.3 KB (584341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f17e056d43c90e3ffebccb3c93980d0ca9987d29e99018816c91ad791bfa7c`  
		Last Modified: Wed, 22 Oct 2025 00:52:06 GMT  
		Size: 10.7 KB (10721 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine` - linux; arm64 variant v8

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
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fd450f0185222facf50c3585803b24553a293cbfa900eb12641a7831d0da01`  
		Last Modified: Tue, 04 Nov 2025 23:25:34 GMT  
		Size: 159.6 MB (159588499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine` - unknown; unknown

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
		Last Modified: Wed, 05 Nov 2025 00:16:21 GMT  
		Size: 583.8 KB (583808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187994aaaa97a175db74c047da827242b630cea289bcdda2b0791cea7a41247b`  
		Last Modified: Wed, 05 Nov 2025 00:16:22 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.in-toto+json
