## `golang:tip-20251227-alpine`

```console
$ docker pull golang@sha256:aec9bd475d55f12028ae7a9d8262ed3a449c325126f42e65bfaa76aac959a220
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20251227-alpine` - linux; amd64

```console
$ docker pull golang@sha256:945826f3ad4c12a803a4b964b24ec57fddde72e4d6c8940840dacdc4d8731615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99200960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4be00790e1515b01851198746187bb86d989d93d9f26cad3c5e9040b25dc7f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:16:30 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:30 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:30 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:16:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:16:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2a51d04da4c0e3401dc6a0431ea04237337f9819c2520e9fcf7d3ea52d8e5d`  
		Last Modified: Mon, 29 Dec 2025 22:16:57 GMT  
		Size: 296.1 KB (296088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c54e75f0355977f49fd303fcd47e9c421e5cb4ce0639b9b1710d2f526d135`  
		Last Modified: Mon, 29 Dec 2025 22:17:03 GMT  
		Size: 95.0 MB (95044613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bbb483f8415b7d3195772bc8a6eb0179beaa842545719979ffd4b207f7f7c`  
		Last Modified: Mon, 29 Dec 2025 22:16:56 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f15d3e18f139d666bea8eebb5b90ff5c8fe0bd05cad8c2386553edb8d1e4fbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be86ed6421926eb8cf70f7053151a878af3acfffee7c545cdc84f8a295c85a0`

```dockerfile
```

-	Layers:
	-	`sha256:52e97f89089bbbf6ccc520e5d2d83fb3cabf5cfc652dd64be05e82c4fb2c0a83`  
		Last Modified: Tue, 30 Dec 2025 00:25:52 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:000535f6e3466e99acd9c3917393ebb8df3d130664e808c51cb1df1cccbae71b`  
		Last Modified: Tue, 30 Dec 2025 00:25:53 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:7ffc34415e2cf6bdd00e63def63f5e2725e90ee290541c14e805ce624c39c7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95260301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f057403e3ad80008d947029055f499ebdd18c09e05d42abbff7603cd83d48c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:15:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:18:05 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:18:05 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:18:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:18:05 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:18:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:18:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc0033a4700273f2acb6186f55cb4d6f40c45a0ce19ff8f31cf1a96766afa80`  
		Last Modified: Mon, 29 Dec 2025 22:18:29 GMT  
		Size: 297.3 KB (297272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f655f252e9ea0da9647bd4425fda60ae8c3fdfd44e08b5203fb635166f3abd4`  
		Last Modified: Mon, 29 Dec 2025 22:18:35 GMT  
		Size: 91.4 MB (91394440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59d5dcb4d3f943130052c266ac2058bd1333a38dfb0cfb1d68785cd88ba3a4`  
		Last Modified: Mon, 29 Dec 2025 22:18:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1065f57b945273a103c9c7860ef8cdf9195d63ed88111fbe9e7e07c97ff91a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28093efe0e6e2d95c55f50afad68d754c8d9dbd5c772eff50e3522f214a5f8f9`

```dockerfile
```

-	Layers:
	-	`sha256:738ac880bf24bd5b23bb070b7546f108053f0d86f254890de3b8046207ad7dde`  
		Last Modified: Tue, 30 Dec 2025 00:25:56 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:b5a4f4935ead9cbe9759ca5f6434a88e8a0afb5fd5e2b18a22081bfb760d0b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a1f9be029848421e9c122e9104dd1471120ac95fb2774d28f438cd717886f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:17:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:17:20 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:17:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:17:20 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:17:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:17:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c6e6d2fc0896d66dc465e5557162b2e1b9da4627c071fb31effff4bf9ab334`  
		Last Modified: Mon, 29 Dec 2025 22:17:44 GMT  
		Size: 296.2 KB (296200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a592f218adec4eba0bdf6f4ba76e47643fbd079be331ecdb85fd7600664dc026`  
		Last Modified: Mon, 29 Dec 2025 22:16:40 GMT  
		Size: 91.1 MB (91114533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2742ee7c13bfe8c772baf17bca2993f9fac6887cf45819fc0f1c7fbff8fba5`  
		Last Modified: Mon, 29 Dec 2025 22:17:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:81545b122bd78d89c08baa3425db6dfccab118d2e58fb81fd3078ef15c1339b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642a8ec4af731c808c5329002e5c284fed5c6aab01af18be86c905128a5cc3b6`

```dockerfile
```

-	Layers:
	-	`sha256:74676baade6b71f7e5b2bbcf8fe471351bdc457f80945e15fa4ff5c280421281`  
		Last Modified: Tue, 30 Dec 2025 00:25:59 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea24f3d7a9eb64787bf676cdacc974f2ac38a887395f487c5bb5f2483d727024`  
		Last Modified: Tue, 30 Dec 2025 00:25:59 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b427a78bd2e1cbacc6225b1f7270b120b4aa34c6978083a73cd6bb7a498f5a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94619731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e3a6df1f970ea71905ef9eb238369e424d1e3fe1e9678ca3ab63c2a20e765c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:34 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:16:13 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:13 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:13 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:16:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:16:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026ece913eb73716bcfa9e022c78c1a484a60d8922da05283d1bc3ce8c3551cb`  
		Last Modified: Mon, 29 Dec 2025 22:16:40 GMT  
		Size: 298.9 KB (298851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff2a18ac08f0eac3e3d9e16d67bcab1f49cd95a40840a22cede89724436815`  
		Last Modified: Mon, 29 Dec 2025 22:16:45 GMT  
		Size: 90.1 MB (90124983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065f5ed300fb96fecd1504a911fa770497e2efa5c0a3c97955f7255b9b49ed24`  
		Last Modified: Mon, 29 Dec 2025 22:16:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:31aebc5c0f4fda2271f6c13aa1cfc69c61842fb49d324b2b341699f58f3a1f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba84b5b2556e7007a98cb54d26a26fda8b3c65e4c5916a75fc2d493fc01695c`

```dockerfile
```

-	Layers:
	-	`sha256:ce1177d1376974280463a0621f697a46f2b6f2d711478ac56c3af6bd32e2184c`  
		Last Modified: Tue, 30 Dec 2025 00:26:03 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df04821dd72d4f107d5582ff4560c77ce8e4242763f1088ae3f97156aac3cfb1`  
		Last Modified: Tue, 30 Dec 2025 00:26:03 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-alpine` - linux; 386

```console
$ docker pull golang@sha256:0d42f0e13ea70e5bb53015bf481a6cd8d734f0231cf08b148817e73705dd7b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96921635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cea7ba3faf4811ea3b93484848acb9cd778014e6810b960559def883385511f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:15:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:17:56 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:17:56 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:17:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:17:56 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:17:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:17:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04ff55e8368b323190ca1ae2379040f6b10de19b288784b92eb671bcf8e743`  
		Last Modified: Mon, 29 Dec 2025 22:18:19 GMT  
		Size: 296.7 KB (296672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b6f0074455116012c1ba771d20edb2ec10d2462257d60366f8ccb9b9224a99`  
		Last Modified: Mon, 29 Dec 2025 22:17:35 GMT  
		Size: 92.9 MB (92938705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f78e5e6aaa0673af678b026c7b2f928f6a3386b11b4497a71c13dcb2ab4137f`  
		Last Modified: Mon, 29 Dec 2025 22:18:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:323bb3c7dce55bd0687ecd19867a5c77e811cd01b06d97774d2d1f770a364b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54b80c89d5f096c720a9a9c60082defd28f7a3e26bfa79bce5c1aedd0129e7f`

```dockerfile
```

-	Layers:
	-	`sha256:4b7b40492d625758ee379bc1f72aef592e5eaf1a029e018e5ede0fb7334e194a`  
		Last Modified: Tue, 30 Dec 2025 00:26:06 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ade66b435fe3d99961cca4a945f000310ac743a2a123e7ccd72429925506f1e`  
		Last Modified: Tue, 30 Dec 2025 00:26:07 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:128d1ec24a4209ad4ea71cb0902ce602116ddc1daef2933d2bf92a4da73cbd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95785172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4487d7a7f0440b6b401e3e9faf2f9e107dee07d0256002f2009006b18fd3bf0b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:16:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:29 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:29 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:21:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:21:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251744709998ea3415429d77aa83c1ba367b71bf12c4b11c84d3ff1d0c4b550`  
		Last Modified: Thu, 18 Dec 2025 01:37:40 GMT  
		Size: 299.3 KB (299257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d98e6a9db6f27c232427cc65a14243d3dc0a9f5145a0455e78bccfb2bf7249c`  
		Last Modified: Mon, 29 Dec 2025 22:17:47 GMT  
		Size: 91.7 MB (91658002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7797902765900745d104403f9d5038789b447c5467b052719e6b8b29fb26039`  
		Last Modified: Mon, 29 Dec 2025 22:21:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f3808a34c5654d98d56a3cbf3c700ae5f2cea32791b4a1bcc2e04a61eebcdacc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (219980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e219615c288c6cd511ae233ea829d30a64812cdc961eeeefa325d4a3f43ec5`

```dockerfile
```

-	Layers:
	-	`sha256:2fc433bac980ba759ff3b66c6157fde0275860e10c984c88d01af97e05d3e1a2`  
		Last Modified: Tue, 30 Dec 2025 00:26:10 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca1e152dc6dd369a62c2c73293162f76b04b9cb40fac6b01a28e355ee61aa4a`  
		Last Modified: Tue, 30 Dec 2025 00:26:11 GMT  
		Size: 25.0 KB (24980 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:87c292fae4b77d593c5882bed14f6bdace315a446fd5d636e047cc4242894263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96188147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95a1aa0837d77aeee85763d86e0ad54b94c72857a5330119179f15943067566`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:47:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:59:48 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:59:48 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:59:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:59:48 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 23:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 23:44:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c358a50d2f39217ca62c3bf8831f5ece762bf2d424204f727fa6a6f9f5124f1`  
		Last Modified: Fri, 19 Dec 2025 05:50:24 GMT  
		Size: 296.5 KB (296519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b4b43eddab816a91e4e75ac1e1a8a3a105423311aff668e1c7594d9f8bed52`  
		Last Modified: Mon, 29 Dec 2025 23:07:05 GMT  
		Size: 92.3 MB (92307532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86b501b1221c30bf1643176c021c8f5c411db764ec1d5f0e56b09485529ae1a`  
		Last Modified: Mon, 29 Dec 2025 23:45:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:32c31e53ebabed71cca433e12f422bbeed101ca38f616adb7517e3f9cde5780e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260f99932a94c2b25913154ec6650fcc2c054ffc87b5a387e99c52cfd630859b`

```dockerfile
```

-	Layers:
	-	`sha256:dec6279b05af38bf1587338b4e6686641847d82968179e8c284ec09b45dc559a`  
		Last Modified: Tue, 30 Dec 2025 00:26:14 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7163c899e6168500a4592f7c6277ba22e5b418f6b3b1ed0881163b244513190`  
		Last Modified: Tue, 30 Dec 2025 00:26:15 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251227-alpine` - linux; s390x

```console
$ docker pull golang@sha256:585b0251e73f51235bcc37105e23a8a3bb6250ba26beae2b4435770e70646695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98225519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ab91af4a7cb0882e90186b482761f1de50ace563e7454a690fabf47e318c2d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:14:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:16:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:37 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:37 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:16:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:16:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7224d7d29671ca737c9ec945a7373478caed2bbfb74b122f8685b8c92149198`  
		Last Modified: Thu, 18 Dec 2025 01:15:01 GMT  
		Size: 297.2 KB (297192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ce8a7fa174e9abbfa1259cfd0fba44c900e27f7f4a5ae1c83f6fe0801a275`  
		Last Modified: Mon, 29 Dec 2025 22:17:17 GMT  
		Size: 94.2 MB (94203858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131acb80d1ed965f3d8582c2a3f7b6e01cfb55ef3b7c663804a64f85b73dc99a`  
		Last Modified: Mon, 29 Dec 2025 22:17:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251227-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:83337bff742d582551ef81fa716349fb66faf51093551e9f7447228421cdbc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7e73658a05bffe45b00d87e40c2e65a8c315cc0378036df5da18cfd2446e45`

```dockerfile
```

-	Layers:
	-	`sha256:8cfd0fcd97eb61447d27f15d3bfedb8d47b9b1454804114111e3be2d9d49167b`  
		Last Modified: Tue, 30 Dec 2025 00:26:18 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f723b0d85426c855c29e2ac2790c5fa2b6e239f710651ac72b8ff19372016a`  
		Last Modified: Tue, 30 Dec 2025 00:26:19 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
