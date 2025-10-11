## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:9f5d1515cd3b7d17420172b89930a08c356fe82490cc039ba6af8b9070590f7a
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
$ docker pull golang@sha256:ee8f2fd1bc1c58459b298d1dac47f73b64c7c47c83bff391579e79b65902b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88533864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510b7af469690051d7dea0a0237e9f556510fc6f484b1e71ac8e0ced06ba31f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01cb87a4b07776e019c3edd7b6cf49bfb6fca564db3893451c7171ff2da5489`  
		Last Modified: Wed, 08 Oct 2025 23:40:04 GMT  
		Size: 291.1 KB (291121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df330a3159ef2a0bf41805e9465d878d806cf4287e8fdd250ddbc3e024a94e45`  
		Last Modified: Mon, 06 Oct 2025 21:03:35 GMT  
		Size: 84.6 MB (84600016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08929cd0a8f49433e1ad9057dbf452952efaa3ce4de04f830d442db3095881da`  
		Last Modified: Wed, 08 Oct 2025 23:40:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e8a55f9c69066c85a333ff0f6be0859f9d8d7d9d9634254188f4429551ea2352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 KB (217240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9eb74fcde650000a52ce1da6756903414a45350ea949ca4dc8fbe4eb187466f`

```dockerfile
```

-	Layers:
	-	`sha256:709069fb51ffc8f4cc3e4a722bf5066b6c68b39a7cda7c1b5cb7b94161a89bc4`  
		Last Modified: Thu, 09 Oct 2025 02:24:21 GMT  
		Size: 192.7 KB (192733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba98ce62a598f8bfcab79cd13a4288cffabb38e907085ac0a24859a94a46e46b`  
		Last Modified: Thu, 09 Oct 2025 02:24:22 GMT  
		Size: 24.5 KB (24507 bytes)  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
$ docker pull golang@sha256:6d5c12a7d0948899485c092481cd2622766ee6ef613930afb9873ddfa34d53c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84939814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b5841b2f97c692b6ab0304496828a8b2dd3475e622bbf3e2bfa4bcbefd778e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
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
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e681b034640886cdb3bd316f094fbcb8eb8932b99f5264030781bc1fb2330af`  
		Last Modified: Wed, 08 Oct 2025 23:52:01 GMT  
		Size: 291.2 KB (291153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113454a922f3bf5f9a74062c96cd1b1dd4f7636e5e5993fd895b9a087d38b9c4`  
		Last Modified: Mon, 06 Oct 2025 21:04:32 GMT  
		Size: 81.5 MB (81549892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3209b2d3df68dc88866a4888afce9d5d36665004b2c182e7ae15b5258a5bb0f`  
		Last Modified: Wed, 08 Oct 2025 23:52:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:375dd7663bd2827ac1c9f642abcb01fb45daf14dd24b0d1cc7cf5e974ac139df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f437aa4b2d1c1d48e6c24cc05f53cf013380719c3e1545d3273169e5e9418fc9`

```dockerfile
```

-	Layers:
	-	`sha256:7bec7ffdf5d977b1f3281a67c699d12b7e1801afb392ca79c3f3f0f547838faa`  
		Last Modified: Thu, 09 Oct 2025 02:24:27 GMT  
		Size: 192.7 KB (192739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0a13c4b96ed386cb8be19bb7890c319fce716d0a457702b85ba7b60a952571c`  
		Last Modified: Thu, 09 Oct 2025 02:24:27 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
$ docker pull golang@sha256:233c46624c05fc2f529e0519ee2962394def828bc798ce313518b5a8587f1fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85736182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8875a5698d084311845f4d7efff05797aadb28d0f6ae681a74bf5ae32793ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
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
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73de5935c27bbf53bedf5cf444a1a2d137f0c9fa6be0ac31ba3a0af17a0953`  
		Last Modified: Thu, 09 Oct 2025 03:31:32 GMT  
		Size: 294.5 KB (294519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f43290ecdfba214453228a07057302573d0be977b7f6d3aeae38f2799df4e`  
		Last Modified: Mon, 06 Oct 2025 21:05:37 GMT  
		Size: 81.9 MB (81867431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01766ef2689ff5e9fdbbffad1fd0056a7aa67c24befb1be70bbab287163ef13`  
		Last Modified: Thu, 09 Oct 2025 06:10:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a4fbb7ac8953e93ea128d5f83c87fc311d3ca910d6ff5f867603dc9422522fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 KB (215371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a59f0aba7072de742046e47893886f8832ae93eb6075a806f82c9b0aadfd5`

```dockerfile
```

-	Layers:
	-	`sha256:bc34c201cf8ef739fa2a1905266940a95f88ce0dc8e189921098c83edc561658`  
		Last Modified: Thu, 09 Oct 2025 08:23:44 GMT  
		Size: 190.8 KB (190818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:910766ff5ba9fc67c6f783efbfe000900b3d2292203428019e923c26708ac683`  
		Last Modified: Thu, 09 Oct 2025 08:23:45 GMT  
		Size: 24.6 KB (24553 bytes)  
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
		Last Modified: Fri, 10 Oct 2025 10:59:07 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
$ docker pull golang@sha256:8d168778cd4e98c165cd6fb9e89738e33ff01e5bbd834b5265ea2ad3cb2a13ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86812692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5787eaf1575a097f19e594eb0149de96a3781c9e7c45a3f82709fe9662069e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 06 Oct 2025 05:23:19 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
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
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cc4c05838d57ecfe671b31e7400d015d24d81c7ce717be366103b575ebe388`  
		Last Modified: Thu, 09 Oct 2025 07:53:30 GMT  
		Size: 292.1 KB (292099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b71ba158c27a4a233d289bf79be8c87a013b440db0421d74c9dff9585ea4d5`  
		Last Modified: Mon, 06 Oct 2025 21:06:07 GMT  
		Size: 83.1 MB (83054001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbbfe96fb0f234138683f39d7b1f8bd95455306244a1dbedb72dc65b4fe694e`  
		Last Modified: Thu, 09 Oct 2025 15:30:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8512f2ad907d1b214864fb4f4682bc306efdedeaf85e1a6914e9a4575d1e6d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 KB (215290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9c3ff5961a62e20a1eae14fde12ceb863096a0277d184d5d1f440f8cd31a98`

```dockerfile
```

-	Layers:
	-	`sha256:96ec5d5c772f396e027603bf7edf8358b076d36ac661d91140f4ac49b10b43d1`  
		Last Modified: Thu, 09 Oct 2025 17:23:35 GMT  
		Size: 190.8 KB (190782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a3c750e0e40128555de4681caeacab5e76c1d08528996557317b45ca226a9f8`  
		Last Modified: Thu, 09 Oct 2025 17:23:36 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
