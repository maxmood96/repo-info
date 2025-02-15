## `amazoncorretto:11-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:4cd6af6942dc8a1a76f116af81eca0b29fd405a5b0cb65f08c51b4bce3d39c4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5cf8afa04d32804ab5122a932215b17dffb7dd7921a6ded9826969d0202b236d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145538649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12a91e868146eaf07145de0af7f3ceb4c9013556b3a4fd4c6ca7f3644359f77`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:0ca9254609025b1114ba67a28f9fbb47cde5e1840bbc65ff9d2fc9e9980ad0af`  
		Last Modified: Sat, 15 Feb 2025 00:03:43 GMT  
		Size: 141.9 MB (141911752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9a12308250152058e900a9110eada08a89f6c2ba9c7e85c95f440de32f5c4fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.9 KB (392880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f3f4f7aba512d53650e167812645810d150627733dfc91a7ec70143d06c2b8`

```dockerfile
```

-	Layers:
	-	`sha256:1b28b92a44be654b582c4cc39c148cafd2c1e3512a714f9f02fc5431b2348d14`  
		Last Modified: Fri, 14 Feb 2025 22:47:36 GMT  
		Size: 383.5 KB (383463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2c1e003fe85a41c5232f11705061c48e98cd826b4bf1ffc764ff7aefe84318`  
		Last Modified: Fri, 14 Feb 2025 22:47:36 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:75d59a6863f9713b76d9d560bceff3110587b48f88b26d5d5bec62127caba36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144125800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8ccec01f8566bcaf99474c2f6496cf4e54c5d2a58cde187017505c0dfc3a61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:97df340b6260232b1135514dea309917ad91b4b2de7be5cd024bc6a5e22b99f9`  
		Last Modified: Tue, 11 Feb 2025 10:11:20 GMT  
		Size: 140.0 MB (140035031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:31a87c73353d9b2e8c72bb09219432e1f3224eb386f7550e815ae956168b383e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 KB (395751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d51d97b45ad4f87adb14730fff633ce9cd362edffea91160bbdc42e339cdbe0`

```dockerfile
```

-	Layers:
	-	`sha256:320d6701d5336d039b5351d10a681ba7491ef1476edce1f648c22a12e46f86c9`  
		Last Modified: Tue, 11 Feb 2025 10:11:14 GMT  
		Size: 384.9 KB (384875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0e18c38c7124bc525f5ef19e516cb50963a23c537a14aeb23c5959772e7672`  
		Last Modified: Fri, 14 Feb 2025 22:47:37 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.in-toto+json
