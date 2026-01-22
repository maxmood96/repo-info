## `amazoncorretto:21-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:f0edc0ff034f8ea77f5a9185cf7397c1bf424e6b54dabe665c996ee1ebc197d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2ffdbe5063e35a3325b8ee7bd6eeb25781aa239fbefe23e58c2dea32fdd514e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165229590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7f08a13d7a85b493be04b3728585fc9bf3900a69410e81bad13b969a2ab86`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:03 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:03 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:03 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28856809d2f13e8bd26e4a434104ac9a11d93a78b3e156174a5829c1363ef544`  
		Last Modified: Wed, 21 Jan 2026 19:55:48 GMT  
		Size: 161.6 MB (161587021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4a873c0344c0407a66d9a10994129e0528de264af9995aed40542d3e624f08bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 KB (595836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906b51e91f0e247d7c5c40f5885d6456e2b34352ade5b48b22f54b79261f3cf`

```dockerfile
```

-	Layers:
	-	`sha256:690bfd47edf51acc9d0181bab7bb04f1a2ea202d79da3bfd7ff8aec7f13b8738`  
		Last Modified: Wed, 21 Jan 2026 19:01:17 GMT  
		Size: 586.5 KB (586462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77e02dafeee17cf72a74fdd829ad2ffb6d862be2cbef58d30650f159722ee827`  
		Last Modified: Wed, 21 Jan 2026 19:52:25 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f5bd30a10bf5843a1063e89228ac7ca61bcf05f75d330958da619f99fbaf9379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163599932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f613d9d00a1e1b362ba33c2f176628192c2fd32f2ef697434217abb0f518146d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:29 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:29 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:29 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899c345535776ba12acbb676363315fada31508e7338c5ed54bd739b29a3d2c5`  
		Last Modified: Wed, 21 Jan 2026 20:01:42 GMT  
		Size: 159.6 MB (159607579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9a8324f9329b5f0ca52a225a391b91084ec90138ecf9a981e424ebfbd4dc1ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 KB (595359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fc03e3672125a1d758534bf3d8f04e21babf1421101b4be87b2942b4db7fa7`

```dockerfile
```

-	Layers:
	-	`sha256:9d923fe0f26c1ad9f88bbabb9e650580609469be57f93440d6492274647f2738`  
		Last Modified: Wed, 21 Jan 2026 19:01:45 GMT  
		Size: 585.9 KB (585881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759c3b973702f66a672aaa218748a617f7816bc0890f54873fe29116270ac279`  
		Last Modified: Wed, 21 Jan 2026 19:01:45 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
