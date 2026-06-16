## `amazoncorretto:17-alpine3.24-full`

```console
$ docker pull amazoncorretto@sha256:223ebda8690566648f5cc77a69d661ecf7c35a9f977fd7cbf0d19545491ad1c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.24-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a2e0b37400aae74bf0b89b6ce341dd4e34f2267db38a479c8242c48c3bee7dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152453315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693c25030ac8d26faa3befa4d4aafedb0627bb19b6978661141007c59544d79a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:25 GMT
ARG version=17.0.19.10.1
# Tue, 16 Jun 2026 00:19:25 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:25 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:19:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca623af35f11c167e66c0b2d9ab5d16b630814b00d63a79e81122b4b25532b7f`  
		Last Modified: Tue, 16 Jun 2026 00:19:43 GMT  
		Size: 148.6 MB (148606924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.24-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:698de994ebeef3141dd37581ce16c148bb56e96048067287adfac8322b306ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.6 KB (594569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18dacaa758b1ade617e0dbfe6458fcd06488b23eb14a1ffde31fceee9c4d4f4`

```dockerfile
```

-	Layers:
	-	`sha256:7628da57e2fdba1bbb266c92892b45600ef6c505a856ec8143045e83fe22aeb9`  
		Last Modified: Tue, 16 Jun 2026 00:19:39 GMT  
		Size: 583.9 KB (583882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed3418096aacda8d6ed5dd745b9b1675f28d95b150472c453b0f896006f44ee4`  
		Last Modified: Tue, 16 Jun 2026 00:19:39 GMT  
		Size: 10.7 KB (10687 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.24-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1265fe6624eba106642ca5e6ba5eececf6a41ac06048d896ba614419813e9479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151136589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea62bed6b3fc89a62b2f54edaa21d7154b2a4e50ab0de0161449a575d3ce3ce9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:34 GMT
ARG version=17.0.19.10.1
# Tue, 16 Jun 2026 00:17:34 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:34 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:17:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65be918273f7584173158de2c2356b09ef7f1f84bd03d633a3a88684025d512`  
		Last Modified: Tue, 16 Jun 2026 00:17:53 GMT  
		Size: 147.0 MB (146953552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.24-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f7dab3b2a7ef2c7b1fbea8a58df06f6bb3dbab1e59899397bdad57b7962ec635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.5 KB (593538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68641e5bcfde1bc90598690fb44db88b44c58f2d9c8e6368a867bc9093ec8e7`

```dockerfile
```

-	Layers:
	-	`sha256:5e1ea0bc891831fa9755342045e08cf75146a0b7a1eeafbad6305b55b40197b7`  
		Last Modified: Tue, 16 Jun 2026 00:17:49 GMT  
		Size: 582.7 KB (582699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e813cf47e75fc648ce58a3962f38a329d7b3dfd902af21e65b4b4663175cf5cc`  
		Last Modified: Tue, 16 Jun 2026 00:17:49 GMT  
		Size: 10.8 KB (10839 bytes)  
		MIME: application/vnd.in-toto+json
