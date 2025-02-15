## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:4f5d2401fdac4d70d42f55933ad6d4cb3979f062736ffc0f03572ff0a122a9c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:1180c0e7f7cdd28bba4e44e8426d90a0835787275f1e535d0d9b029041850878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339237509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eacbf9fbac22d7e5532459b50384f4e0e04690cedd9fca681ce27f28c8afdc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 04:23:03 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 08:47:02 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 09:04:02 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac1e880ac4262e770b5ee1b650408d9e84a0e6d2c3bdf9c7a04145be483029d`  
		Last Modified: Sat, 15 Feb 2025 02:33:00 GMT  
		Size: 86.0 MB (85971755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f767e601eda3139d3a2c86388748ee052ac66ea4515fdb8e54673dc9e44217`  
		Last Modified: Sat, 15 Feb 2025 03:10:47 GMT  
		Size: 129.2 MB (129216535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a314e8948e2c109faf84065014a3ba9c99704683923f935c4463b366a7f99ddc`  
		Last Modified: Sat, 15 Feb 2025 02:32:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:21ed9b8666dbf091d25a850e35ca95757c55cbeadff583150c345244d33a5775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1b085194a092b8a19f361d4d24181e640aecda31920fac65971ff6b0d679d5`

```dockerfile
```

-	Layers:
	-	`sha256:fc1eaab41313d71e63991e05ad8f9b1a898b479a286a21189534162780a8d6d9`  
		Last Modified: Sat, 15 Feb 2025 03:23:43 GMT  
		Size: 10.3 MB (10267086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5f26d54c740cc34dccc496d06a932cc0e9e11f9936b91fde72927c62baa20ab`  
		Last Modified: Sat, 15 Feb 2025 03:23:43 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:b4ecd4a8208df840e988c91548e2876ed495508aa01715ef522f1d39de90a661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.0 MB (340038815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa18d85860b2c76acace45df6933e7d76bc2d1c7cbe827482f899cd4ab34f672`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 05:01:41 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 10:05:13 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 22:03:52 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963712fa0dd1a90ffb6870292b18b942f0e2af189f276f807c9c784ebb52e548`  
		Last Modified: Sat, 15 Feb 2025 02:33:36 GMT  
		Size: 87.4 MB (87397951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b2ede4bc0ff1c223f32b8ba810862b4e27669e273d5c1e6c5993b5698ec335`  
		Last Modified: Sat, 15 Feb 2025 03:10:29 GMT  
		Size: 125.9 MB (125872820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378bb5c3e258d29e009a1eefce158ab51099ab7ec88ad1e4595d30a6877a7ea`  
		Last Modified: Sat, 15 Feb 2025 02:33:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:0af4a618497d1bbd04976198d8cbcd31400488e6796a32ef76b63c1c6a458455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846dd9d9357539e6d4d779d75b7a70f9b3a47b5d0af0c2216356450b19b92c5b`

```dockerfile
```

-	Layers:
	-	`sha256:893ee86e09c99440684f4ad6a9e8b00c1a977c97403c213a63978b338fc019db`  
		Last Modified: Sat, 15 Feb 2025 03:23:48 GMT  
		Size: 10.3 MB (10256877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee0f5fce9ab6746052fb42381d1273f4609bebea3300379e82132413e9a5677`  
		Last Modified: Sat, 15 Feb 2025 03:23:49 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
