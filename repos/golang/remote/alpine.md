## `golang:alpine`

```console
$ docker pull golang@sha256:f1fe698725f6ed14eb944dc587591f134632ed47fc0732ec27c7642adbe90618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:alpine` - linux; amd64

```console
$ docker pull golang@sha256:a52ec26b648564b6cef8adf7bea14348b499a32d08de3943823150ad268f0d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73044482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b740e4568193271cab03d8813e82bb40bbb300e05f663f2178d6ee3fbaf991e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667a4259027594465efe0982aec566a89095e879511d0716b4ae322f291e393d`  
		Last Modified: Tue, 14 May 2024 22:59:10 GMT  
		Size: 292.9 KB (292900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e347f261431f4a9affbd78ee6f59a7486c17be94c7c8274be137aab626f0555`  
		Last Modified: Tue, 14 May 2024 22:59:11 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db27d6512129ba324acd616fd920202156dfadb8ccae8ffd1ec862bd46277c98`  
		Last Modified: Tue, 14 May 2024 22:59:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b813c5abc473e740e85b634140585df96eb060037547e33a4437481f1f3fda04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 KB (229111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca9b35d67da609fd861af56fb096bfb9d9df96c49a09cbac2a71e89845a5d3b`

```dockerfile
```

-	Layers:
	-	`sha256:6d1b1af0163962959a21bd6cf158722eec8f7ece7bb42d14edd651103eabdb86`  
		Last Modified: Tue, 14 May 2024 22:59:11 GMT  
		Size: 205.0 KB (205047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d1314f30561d7169cd119be1c8572d2a7cfd97760030c529510c99c0e8d326`  
		Last Modified: Tue, 14 May 2024 22:59:10 GMT  
		Size: 24.1 KB (24064 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:b34e66c3961169336bb03ad1548ae874571c1f74a74577fe1b43cc36c80613c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71175107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68310480aebfa05a75a050c8a799c31efe8ac700eb79aa9767567733be0ed002`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad27ef8f58290014492c74a7b2f956cb2cb25394a5098ce6da1e33844d12639`  
		Last Modified: Tue, 14 May 2024 23:01:50 GMT  
		Size: 294.3 KB (294336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87622d8ade59df0daad35a20a0a1b816a8c25ed474cf6048473d6bbd0d46f2`  
		Last Modified: Tue, 14 May 2024 23:01:52 GMT  
		Size: 67.7 MB (67715217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310eb826c90e6f890ea6ae063ba343178643fcf5b69c5543af729af28cef52af`  
		Last Modified: Tue, 14 May 2024 23:01:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ede38240e04f2650dd1b2db98d49228eaf375739134fdc75dba27d1d9129a6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 KB (23807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cb3e1217a5184955d1165a6cda0761b72b8f09ed28ae75f33da4b0883f1dfe`

```dockerfile
```

-	Layers:
	-	`sha256:5ec34ab1776beab827b2374e57e985e06f4893d91786c7dd2c43609af01c7b77`  
		Last Modified: Tue, 14 May 2024 23:01:50 GMT  
		Size: 23.8 KB (23807 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:20b4a52834614903826fc043859f35653a4c568098b3ac5a1e28dc85994f089c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70927455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddaa325fb310831bde97c498bdf3a7b8cc5e084cd3848f891f49c808acd8f98`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5bc8c8a85a004d09793602cc73eb5cdd7e51489747e55adbda95159c328a70`  
		Last Modified: Wed, 15 May 2024 08:38:49 GMT  
		Size: 293.2 KB (293185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd578652b0fd72238bc2565adcc2bf2716995c086d72609492506b36ddec660`  
		Last Modified: Wed, 15 May 2024 08:36:50 GMT  
		Size: 67.7 MB (67715213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2149779e1ffef1096a27b02d94b473a272e256d5c015ce287a5ca9a26bc0171`  
		Last Modified: Wed, 15 May 2024 08:38:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e95360c59613517ad8544fbd1c9c42af4fbeb3538a4ec24c12b0ef36f22fa800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 KB (229107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4334dc07c9c4a2f3881cdb281972e3973a96996d5b2688a0bc7d6bd109e254`

```dockerfile
```

-	Layers:
	-	`sha256:ce7c85b82f26648565c904781ed7c8670935430c86b8f402fca263cf581313f3`  
		Last Modified: Wed, 15 May 2024 08:38:49 GMT  
		Size: 205.1 KB (205081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844714ec76764617fd1395ed8dcf25e4331a9f0732e6637fbb1413e53353ecff`  
		Last Modified: Wed, 15 May 2024 08:38:48 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8d1654b2a3b86c5c7e4f53f2028b78ac7908b9e29bc18f01ae4cf578d01419cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69915980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47435cf6488c31f9fc75d0e7579bd00ef23934081bd610d1b9f27fdb943ecce4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e3f50b898a3ae6cfe23ad1a18c4fb0bf0e08bb7feb5503a4b7d6a65e6f31bd`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 296.1 KB (296070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df936e3f0526d99820dadd5ba236ab92b125bf8f10cf6f450093350d9d53af4`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:22c03a5b12bc2b66393386ac38b23ca722fd3cc0dcb7d1bbd0e731839a97216a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 KB (228982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4072648c026afcb8a34f422c7100706682fda10101f4960de624290a98421753`

```dockerfile
```

-	Layers:
	-	`sha256:b8b1359a78ead7806e03d3e6b8be725ccd62fe0739a85299db881b98a6acbe87`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 205.1 KB (205066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb62db786336498e2892bbd7afc131a056a9ded197194e18088e63bc77296c0`  
		Last Modified: Wed, 15 May 2024 09:55:59 GMT  
		Size: 23.9 KB (23916 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; 386

```console
$ docker pull golang@sha256:f6f94bd7469a1aeacc39b95a47e882054fda464a85b7e922ef8b8bd28086fb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70881140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f81ee6a8ff66da850f0a80ade203fa17c3aa4c1def9db68400b79b95c0753a5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c94b8b9760e0847d05f366c417e7166fd3c393351c2f1eabc669aef908b46a`  
		Last Modified: Tue, 14 May 2024 22:57:13 GMT  
		Size: 293.6 KB (293566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e4b9e273af1abd1d111e520ed84244c384ff0228d35080912b63c411128c82`  
		Last Modified: Tue, 14 May 2024 22:57:16 GMT  
		Size: 67.3 MB (67343328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942c8820933d61ac7d9a29280a115b995ef7ee91ce63aa6d0ba7d69cdece6f89`  
		Last Modified: Tue, 14 May 2024 22:57:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:35e4ca635ba322e36a8356f1285ae5a80b6abb677689da6481184a94572404fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 KB (228979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a7e020eafabd0380300fc83e137a1496ea6dbc0208b4b3d4caa9a99f491601`

```dockerfile
```

-	Layers:
	-	`sha256:70e211f267708a594453380d82a9641fd3ddf8616397d1eb209e13b8bf1cab37`  
		Last Modified: Tue, 14 May 2024 22:57:13 GMT  
		Size: 205.0 KB (204968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:943b9f3363de4f70b8828443027813e165c0e584ed4a483722d3623aa4ba07c4`  
		Last Modified: Tue, 14 May 2024 22:57:13 GMT  
		Size: 24.0 KB (24011 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:66906aeebaf2d2e4c78bb39784b783d77246e455c17395d646f57b7b140354ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70085062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6247326d46566e3b6eb30059ae26bb56c0a4a0a4ca62d2ee6eb2db804c9c0a02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d82ce8dbc35c2b54369f84f5d1cdca1f43f171bafaa35b9ece60118143b6960`  
		Last Modified: Wed, 15 May 2024 04:46:37 GMT  
		Size: 296.5 KB (296495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a09e6cada02540e54f2e6e8c59f80c9960dc5c4559a3d96a1cc4bcca469ff9e`  
		Last Modified: Wed, 15 May 2024 04:44:01 GMT  
		Size: 66.4 MB (66430056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f690359b53e53fdcdeaa9654150463f063113662b6108d3988eef4548dec7c`  
		Last Modified: Wed, 15 May 2024 04:46:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a63d2fb17361b3f07519111bc2d832ec5e2159f3bfe144f3ea14e469ae623652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 KB (227148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe1d5d5d1f7dcd4377674b848b70f778ab20e23452370b7828ad5586795cf23`

```dockerfile
```

-	Layers:
	-	`sha256:5b6e13df040a73bd7afecf419ed0d024167290c565920d249fb8ca868cbbd4bf`  
		Last Modified: Wed, 15 May 2024 04:46:37 GMT  
		Size: 203.2 KB (203185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c1e0edb1c99bffaac347b13878e824eed860cceebc6072892fa4cb3b2bf6c6`  
		Last Modified: Wed, 15 May 2024 04:46:36 GMT  
		Size: 24.0 KB (23963 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; s390x

```console
$ docker pull golang@sha256:0e5bf747efb8a48b77e96bece4ba3a02ecf5d28c2b3daf2144bddcfc5a848a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71935986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbe972317b1bf6233bca9a319fed2c3b57fbdd6bed22da237ed8622886c9bad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 16:32:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 May 2024 16:32:49 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 16:32:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 May 2024 16:32:49 GMT
ENV GOPATH=/go
# Tue, 07 May 2024 16:32:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 May 2024 16:32:49 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 07 May 2024 16:32:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 May 2024 16:32:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc57cebd6cab112aa720ede5bce8aa42592bcc9ea99aa91ade3eb03d2ecbbce8`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 294.1 KB (294116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b913ee17a483cc427f632db9240a13b45ee66ca5d56d622dcfedef41eaa6cd`  
		Last Modified: Wed, 15 May 2024 02:44:08 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382b267d7cbedb48e683f15d12454c6aa505137bf49f9e3258cbdb09690fc056`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6bb3dfd9218309f0a526787a94534b73fc6f45f0f60c19d5377551d81d70a073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 KB (226989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7337811b79414e4bbd74a8eaa285168231fca74c9af13b40a96b30be94fb652c`

```dockerfile
```

-	Layers:
	-	`sha256:d98603c001669642404e9484bcaa6adacfce98d0d7a38c1a12950971d187d088`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 203.1 KB (203091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21a6895d5759b60d87b16ae5b0133aaf02bbb9bd486561a67b452c2accc9703d`  
		Last Modified: Wed, 15 May 2024 02:46:59 GMT  
		Size: 23.9 KB (23898 bytes)  
		MIME: application/vnd.in-toto+json
