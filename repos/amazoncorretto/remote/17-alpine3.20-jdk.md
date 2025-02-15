## `amazoncorretto:17-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:aedb7e9c299a6ecb8b19df35a862af49cf9104c6a04d076b32a5c56488f842de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:77980ab89485cd9103fd2cf526e35ea39efdaaa412037c5118d474e6699661b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149304568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5f66dac65810a9155e96beff12b28cdaf0a8ec5eee8551a5aa6b8d71e8e227`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0e9cf49a439c9ddc32e569232c6b6e1656b3e527ca85f0bd467aa815af8d46`  
		Last Modified: Fri, 14 Feb 2025 22:57:18 GMT  
		Size: 145.7 MB (145677671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eca857d499978269edea0c6e614601af6aa90cf85027917d03d236a9942db7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 KB (386079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10de6a4f6fb304757c52921d63e04f2babc1ae954fc2b19598e150c6685bedfc`

```dockerfile
```

-	Layers:
	-	`sha256:1db56d7ea03f4239d63a2f81830ebec9768ab40b553319f2935b12f1cf6d28b5`  
		Last Modified: Fri, 14 Feb 2025 22:48:14 GMT  
		Size: 376.7 KB (376663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59556c61100abfce8272d7eee91ee5aef39b555de4f4dab071697fb64cb28fb`  
		Last Modified: Fri, 14 Feb 2025 22:48:14 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6554290c6cc021a19548e21470752a47b066197587263c312bd2e093536d46fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148111671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994b525b664575c693b10eb4fba81a8a314c626d71bbd04ff8ef2401ed4c552b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbfd5bba38b947d2ea3a0b77869ef0e6f42408ae61bf467f85d73d093edf4e`  
		Last Modified: Tue, 04 Feb 2025 21:02:57 GMT  
		Size: 144.0 MB (144020902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5cd2c607bcf8b84685540471ec3a45434b34741cc3125eb2abed864161e44fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 KB (388314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7829d69e066c24bfe7d209edf61af81c49048e10c2ef5c3fde6e2a3f98c3c90`

```dockerfile
```

-	Layers:
	-	`sha256:62e32a01b3c9756c040e81e2c323a6567e10ad2d35a761bbc02d8a8051e0eadd`  
		Last Modified: Fri, 14 Feb 2025 22:48:16 GMT  
		Size: 377.4 KB (377438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99bbd23312ee4e1f9f080bbf3a866445aac021fa52f1c00d36b534324ed6d4b8`  
		Last Modified: Fri, 14 Feb 2025 22:48:16 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.in-toto+json
