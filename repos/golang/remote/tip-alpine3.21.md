## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:25ad8ef9f920d88969aef842c665596ddda3083bd1c8fba262b1cf7c7da413ce
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:0ee9b22095e482b3097252441b20a7a46043c94792285ac536f5b8e373a4bda4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88528914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c300327cc2d3ed3fc26696c3538c7367c5a193f3172c3da8f01dd0e8a98f914c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef47253f3d4ec16a45ef8d58c35ca6d3d6c3c62b970c484b67df74f44dd53afa`  
		Last Modified: Tue, 07 Oct 2025 21:16:03 GMT  
		Size: 291.2 KB (291170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df330a3159ef2a0bf41805e9465d878d806cf4287e8fdd250ddbc3e024a94e45`  
		Last Modified: Mon, 06 Oct 2025 21:03:35 GMT  
		Size: 84.6 MB (84600016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbe4f9ce228f2a683a4ee539622d344326a44a8f64fb9f11b7d059be8c7b5d6`  
		Last Modified: Tue, 07 Oct 2025 21:16:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:c84b4a03df1b5e1ec9d81012faf22a160047eae81bc73eac729a2db33e9f0426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810685fd6b7a8beeb3727933f4c2d1467909100c3d0e2d61ff7b82c42608aca2`

```dockerfile
```

-	Layers:
	-	`sha256:3bf98f88823944bd30f13b1ff4117cce599db861ad571c4b75a8d6e899aa249a`  
		Last Modified: Tue, 07 Oct 2025 23:23:34 GMT  
		Size: 193.8 KB (193816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0679eec729ab6cd2b7773e8a23f7a3e1e285c634e8a20ec490042c89804503d6`  
		Last Modified: Tue, 07 Oct 2025 23:23:34 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:10d2a837bac629f59f32c6a7e34d2c855e73c844e1293dfbe6e5777d9d5b687a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85459023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783e48a63cd3e584a6c7fd4373f34a6fa7c9abca6eb4913980dcf9fcfccb7013`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092d2c734da81231ebc8b90e6e63cb0d93faae5cc787d677024f33dabd0ffdf0`  
		Last Modified: Wed, 08 Oct 2025 23:04:12 GMT  
		Size: 292.2 KB (292235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ca929e1e82e3da2a8d3fe64f9852116fdde16db4405daccb287d008513ea4`  
		Last Modified: Mon, 06 Oct 2025 21:06:14 GMT  
		Size: 81.8 MB (81801162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a3be72d481ca99c3c2d7998283904fe2fc9d072198c404eb651179d999ea9`  
		Last Modified: Wed, 08 Oct 2025 23:04:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:67427013db0d22b6a0fa3b0e5e5da3de8a0cf69b928eaa63a9c619ec0357703e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22336c013d3070c4e862af2464cf3301857baa729a5a6d20dfbeea8ff849e67`

```dockerfile
```

-	Layers:
	-	`sha256:0ee587b77338701a28a7a6b3e1d7eda1c0203c44630b5bdc25979af911e2e9e0`  
		Last Modified: Wed, 08 Oct 2025 23:24:48 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:81d1b5f5ef13d5559b3a7f5869ccdea2ea57b5b623b12a3ae6f7543083b3972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84938135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a4b6df60cc0b513b0c2d55647c972dacfd903c14ccd277a1ac4e23e4786c73`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93b3dca56fd32dbbb2ab9f4c55c793b57b77b34d4dc4e046053e7251e1b87b5`  
		Last Modified: Tue, 07 Oct 2025 20:15:08 GMT  
		Size: 291.2 KB (291214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113454a922f3bf5f9a74062c96cd1b1dd4f7636e5e5993fd895b9a087d38b9c4`  
		Last Modified: Mon, 06 Oct 2025 21:04:32 GMT  
		Size: 81.5 MB (81549892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94723e0976e372cc5b03c0aa94c6c3da666ac7ab93851f1764ef9d99b5eb0887`  
		Last Modified: Tue, 07 Oct 2025 20:15:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8af1b7e721e1e79a3eca568d278f315cb9a296c048fd83a9612eb6554fe7cb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 KB (218442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605d0ba0a501b42382bfa8c0300697873c48fa7791ff75cd2821438edefff6e0`

```dockerfile
```

-	Layers:
	-	`sha256:6cf889556074dc0b884e1fd8f6de2af978337b35203813d2eeee91b6e4d985b6`  
		Last Modified: Tue, 07 Oct 2025 20:28:56 GMT  
		Size: 193.8 KB (193822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1621d9f2e34519153f733de4f1e67a04044c5ebdb5f51b316d49a6196d74f502`  
		Last Modified: Tue, 07 Oct 2025 20:28:57 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ecdb7a36f1de36b2399d265287d1efa8b1ad711eba447abdf31199e38e794a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84818404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5047ffbe4657fcc3acfc4739decc5941e4576f1a93917277820d3171ff3dfa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e9b5859f62937bdd9fef0cce6cd47398c91676e6b9469b7d417cd1e41b964c`  
		Last Modified: Wed, 08 Oct 2025 23:27:44 GMT  
		Size: 294.0 KB (294043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae6f3de502e34feaea64f03c33850b0abe91d2931d0f357546a0b84a633dd1`  
		Last Modified: Mon, 06 Oct 2025 21:03:39 GMT  
		Size: 80.5 MB (80531850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771b4d7b4371a6b95f6ded092d572fb797451e5d075b067c58aa1e9678f5f962`  
		Last Modified: Wed, 08 Oct 2025 23:27:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:4632f157168c879648b8d2f462c7fa6419db7e5a65c7edcc69505cd5677d4ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1513d12254f9593a6f6ea19a0fb6cf017194eb68a97cc1135b7b8260770093bd`

```dockerfile
```

-	Layers:
	-	`sha256:c09207e8b71f6ea1a754fc51a72d956265cc124babe2a5d7612a024918bfb4c5`  
		Last Modified: Wed, 08 Oct 2025 23:24:53 GMT  
		Size: 192.8 KB (192765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37331be36fe24b4dc082bb245c2685092506bcd300248cc8e294bb190e5f98b1`  
		Last Modified: Wed, 08 Oct 2025 23:24:54 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:9a5a76b25cd81c513805a901d4947fcb8106707de4b46d3ab48d4c381a782369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86901919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd8840cd04e28640c7d6f098d1ae4536823f44e8a2fef74ffe4bc219bb3412`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fadf5cf8a274f2fb477f122d42d30a119c75b16d89149fc40eb8d477f3a0fad`  
		Last Modified: Wed, 08 Oct 2025 22:22:19 GMT  
		Size: 291.6 KB (291591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c0a8fc757d99c51188cdf4bad50d211862dd20e9507d39b31fbbec343ddd8`  
		Last Modified: Mon, 06 Oct 2025 21:03:40 GMT  
		Size: 83.1 MB (83145466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c0603edd52ea89d467a1043be9dd73a27079572acd96e0edce40c95e08a56`  
		Last Modified: Wed, 08 Oct 2025 22:22:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:f4ef9f8b538c4ef29187a623ae5ed2cec6c67e267f7d5abfcd053207558ea443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 KB (217179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed52e6eb3a6f6fdf98d770d9adae9ab95120662ec36bf245ccabcf7ce76d25de`

```dockerfile
```

-	Layers:
	-	`sha256:a604ff65520ba934f6ec3db6b73b6b97cd8eb91fb6bee06f513bfcf2f669c7bd`  
		Last Modified: Wed, 08 Oct 2025 23:24:57 GMT  
		Size: 192.7 KB (192704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c422032233cd80ad285addd346c3dc715f09313581e89cc1f0dcfcc8169582`  
		Last Modified: Wed, 08 Oct 2025 23:24:58 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:6d70ed32cafaa6b0f091032416dfc0c30bf43559e67b8ea665f96dc44ebcea2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85731294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ee4ebf45b57a7bd357b817f80d26887012ce2867cdbcd73327a47b74de4594`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c72ed30b4440614b477e3a87c9a33476b9d0b437a968436db8903fed6fcee5`  
		Last Modified: Mon, 06 Oct 2025 21:18:20 GMT  
		Size: 294.6 KB (294580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f43290ecdfba214453228a07057302573d0be977b7f6d3aeae38f2799df4e`  
		Last Modified: Mon, 06 Oct 2025 21:05:37 GMT  
		Size: 81.9 MB (81867431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f367c12de633d63608de38382a9238f9324c4e46b6f864fb05400d05da1351d5`  
		Last Modified: Tue, 07 Oct 2025 20:27:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:45c1fe170fe15665cb76e9a6970d36791ff80bc1c6c7275bd8b0c36f9069387d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 KB (216455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0000e0724bbb879a3603d5ad114f57bbf6aa684bbd2770fbc4d789d3fb813f3a`

```dockerfile
```

-	Layers:
	-	`sha256:2dcf6a93bad830b0b94ff4e55cddaa0dafc710d1991d6f619319c37481a0db90`  
		Last Modified: Tue, 07 Oct 2025 21:20:51 GMT  
		Size: 191.9 KB (191901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb405eb9c1cf0744ff276974b4495579c901c26d688f290cd02e174c233390e2`  
		Last Modified: Tue, 07 Oct 2025 21:20:52 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:dc8bf9f3076cfbe7e9a01b239d10b5a56a88a32f51db1953dcf3578d8ab575f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85874653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89baaab6b5d95c890e2fea78bf56944811bb4174b354d3ca72aa28593fd90530`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66587a4ead2af4b3777a88f71fff7f8fb2d28fecc6835536cfbd5f10d19b67b0`  
		Last Modified: Tue, 07 Oct 2025 14:56:06 GMT  
		Size: 291.5 KB (291518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fd0ce2ab28438bdf94f05f192ab71a6b801a6c5d6e3d4dc6d664c820e75f2c`  
		Last Modified: Tue, 07 Oct 2025 14:09:36 GMT  
		Size: 82.2 MB (82233887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0e9dc401db6b547151558896af20f8b9ccdb3710d93a2e2ad72eb60b1f06d2`  
		Last Modified: Tue, 07 Oct 2025 14:56:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:5c73ffc2198b8ba72913c1f13ea92606f05c195434eaa422acae18c8664076ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 KB (216451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c927f596322f9d5337ed6cf75e09f9fff53beea92607412588fe0f986378bc`

```dockerfile
```

-	Layers:
	-	`sha256:b3128de7a0f5ef8bf7d106a359c072e53e853f9023223805cb567fdd60001cd5`  
		Last Modified: Tue, 07 Oct 2025 23:23:47 GMT  
		Size: 191.9 KB (191897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b648f3056864bfa4b763783c826bec36cf0ead7dd73a80aa80bfcb94c4216d53`  
		Last Modified: Tue, 07 Oct 2025 23:23:48 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:882bdc027281d7f30df3f61927ffa91bdc9f3f18654303bb6589ad2739ea1a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86808411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c60cac187f0749caacc9d2a60724b1efaefd034bf25e6a45fc630124b8dab07`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c0d08c3945d6368d73f257f34ee298e8dee1cce97a4a8bd5b3c35a4f5ab3ee`  
		Last Modified: Mon, 06 Oct 2025 21:15:07 GMT  
		Size: 292.2 KB (292152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b71ba158c27a4a233d289bf79be8c87a013b440db0421d74c9dff9585ea4d5`  
		Last Modified: Mon, 06 Oct 2025 21:06:07 GMT  
		Size: 83.1 MB (83054001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf692584e9aa47cbe42a70d46bd3d03377a7e9efa4273e00b147892c34ae580`  
		Last Modified: Tue, 07 Oct 2025 20:39:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:4dd183fa31175b1776169a14a104e6eb40f7317d75bfa144f956936c3b3a41d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 KB (216373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de1409b769eb7316b04f06fc355ff69fb165b4485ff6706ccdbd5fc20ecd80d`

```dockerfile
```

-	Layers:
	-	`sha256:52eb04fc14de0daaae95e413bb12f0d58f31fa848b0bd4d4fbb2de13f0959dcc`  
		Last Modified: Tue, 07 Oct 2025 21:20:58 GMT  
		Size: 191.9 KB (191865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebb3213f1f4b1123651e17fec6857edcba443e85f04a65a6f4b8cb39a3ac5c0`  
		Last Modified: Tue, 07 Oct 2025 21:20:59 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
