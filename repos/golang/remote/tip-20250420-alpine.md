## `golang:tip-20250420-alpine`

```console
$ docker pull golang@sha256:8951da7edd26733a29760b526a5fdcef3d89f95e9f5a3df704a61fc3011db1e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-20250420-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:39ec63943e7b8e5e776a5951a61b84c248082d1bbaa0f8fd881a11d9ef27dc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125903098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddded95fca02d2038ae06409dd024787d7fa9d9c405fe5c182ab585102a1912`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:20 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7bf435709d1c27794da4aa58bbf1c4a90e82ff2338f06023036bd847c51bc`  
		Last Modified: Mon, 21 Apr 2025 22:36:52 GMT  
		Size: 122.2 MB (122241957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f92641ca33d600d20c6c4ddefa7ed5fd77ebf74e63eab906d908ebbdf3aadb`  
		Last Modified: Mon, 21 Apr 2025 22:36:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250420-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:559fd9fe1db3adfefa9176dd8e534567a0dcd570ce116690ee117a87a06c8e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1578aee7d442256c1f939576436657b19e7466985f6a27b1ffc09fdadbdb717e`

```dockerfile
```

-	Layers:
	-	`sha256:8ae1583b635707cce56ef259c6804a48d60263ba271952b9f1f75038cf5f0d7c`  
		Last Modified: Mon, 21 Apr 2025 22:36:49 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250420-alpine` - linux; 386

```console
$ docker pull golang@sha256:db68ba764484040d1e901bc350d207f755a0279a8fb420840de85082ce6af3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128802872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c7ce95adf8fd56cc20dde74a4499fca0615390f3da0531b45428343b7b898e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689995964c02ae5829f0ebbc101aa49deaad9cc40bcfc7378d2d077f9e20f4d1`  
		Last Modified: Mon, 21 Apr 2025 22:37:41 GMT  
		Size: 295.6 KB (295614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22385500e9d61ec2b239f5d3bd81241409c720a3ebb2a4cf2d458346f64bcc50`  
		Last Modified: Mon, 21 Apr 2025 22:37:44 GMT  
		Size: 125.0 MB (125043477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c3deee176fdd208576023f85d8f57fa91553c0c4cc82e38dfdd1bc2d6b855`  
		Last Modified: Mon, 21 Apr 2025 22:37:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250420-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:93dd14298bbcdead0bddd049a4ff24f13a4e39dc948298fa162075be8f5c7da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 KB (236833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42c8b05ca43e26b4bf6db300d56cf95860174d1a66adec83f31c672cfcb5b5`

```dockerfile
```

-	Layers:
	-	`sha256:cf95ba9138bf195b27c79f1416529201b52055187adc7099954daffa7e3b4c68`  
		Last Modified: Mon, 21 Apr 2025 22:37:41 GMT  
		Size: 211.7 KB (211734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6432774282d7c6795b2dd37112074ff2a80615cb8bbf066d66fe3029707b0f02`  
		Last Modified: Mon, 21 Apr 2025 22:37:41 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json
