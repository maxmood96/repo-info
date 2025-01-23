## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:6c29a2a8bac4f2e59204b9395d3ffbdb58f438e22d0c1c48229b4efba91e4e9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:05d50cb62be5732942bfaca7a998096b1b65cdfd030287f59f04aa9c18ac60ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145535133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126671533519ef04de4fb9d33cc0cf0e1d0117628f464b6fad5e831f36a534d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68657a8f14726c6bd4ffebcb2e2b7a3bb4db564ce5884ad236dbee1b185a307c`  
		Last Modified: Wed, 08 Jan 2025 18:10:18 GMT  
		Size: 141.9 MB (141908873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2e3b789236e2c28627e46564453c7de4eefb179d7e4b94eee98e8127bfd2b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.5 KB (395496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1410fae83bd1c7658e6a97b4bebed851a295fed52b49be59678af0139cbfc7f9`

```dockerfile
```

-	Layers:
	-	`sha256:fef513aa863733df72333e15159ac48a90847dd2857de01fbb85dfc39f2b3a21`  
		Last Modified: Wed, 08 Jan 2025 18:10:16 GMT  
		Size: 384.8 KB (384771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c777320544aab7b966a75344a2b9ce92056550093bb477280390d474087b7f4`  
		Last Modified: Wed, 08 Jan 2025 18:10:16 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine-full` - linux; arm64 variant v8

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
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97df340b6260232b1135514dea309917ad91b4b2de7be5cd024bc6a5e22b99f9`  
		Last Modified: Thu, 23 Jan 2025 18:41:00 GMT  
		Size: 140.0 MB (140035031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-full` - unknown; unknown

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
		Last Modified: Thu, 23 Jan 2025 18:40:56 GMT  
		Size: 384.9 KB (384875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0e18c38c7124bc525f5ef19e516cb50963a23c537a14aeb23c5959772e7672`  
		Last Modified: Thu, 23 Jan 2025 18:40:59 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.in-toto+json
