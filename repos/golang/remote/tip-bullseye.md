## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:4d2787c2e2db73825171829c864c3665a7347b5a26b625fe8462af4e499856f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:3394eb9be71e37d9b7c447122fb038d63be3ba7ce740611782725d48182e09fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293498281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a945a81e4ddda93ecb9f262cd1a41befd4f1e40204c544eaf243b43e2a44b02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3bd1a042194ae6d1dd79cd616350ddd097936baccecc5e8d0d2f0d414857e0`  
		Last Modified: Mon, 16 Jun 2025 17:54:48 GMT  
		Size: 86.0 MB (86021879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd9226ac30cafc0afd46b4cd0a61efa6a788bc8ead02212a127058aeb6d31`  
		Last Modified: Mon, 16 Jun 2025 17:54:27 GMT  
		Size: 83.2 MB (83198960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2d3761b24f5694e19cb987ef597f340cc618e8e4a84d76836b5969318c8ba`  
		Last Modified: Mon, 16 Jun 2025 17:54:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:a6e850eda2e6a299bc0378de5a3336a9f2a468c55468e0db657be30a637ab485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10509221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2252bc7d80559a7b2f6ea6b575b1cc716a0ab3e1aba972632a353d66352999c9`

```dockerfile
```

-	Layers:
	-	`sha256:e7d3f6e672ef2f1753052c03dadb249849670fd381b7f9c2a94a56222a8a228f`  
		Last Modified: Mon, 16 Jun 2025 20:24:53 GMT  
		Size: 10.5 MB (10482164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85c3231e6f7f5b4e8969241c6acc3198482c7fd96f5b041963cafd6626d09cab`  
		Last Modified: Mon, 16 Jun 2025 20:24:53 GMT  
		Size: 27.1 KB (27057 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:79660e7dce1be24867f5054435c5ff7c37c4b577a579ea699d14e9aa33ea438e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259774789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e24928da2cb3cd34d0512d83a3e6fa44e44daa06513baa65c00dca055ebb64`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f7feeb0b6a1c7b2f8058fc4bcf8523950540bd39c01231df0b01c7791add68`  
		Last Modified: Wed, 11 Jun 2025 18:28:34 GMT  
		Size: 64.9 MB (64942390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61657cadfce4d144c231832da5fb28f3562535b7ef7b3db141bedf56ff930a8`  
		Last Modified: Mon, 16 Jun 2025 17:55:24 GMT  
		Size: 80.3 MB (80276791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d660f0acf9f8d0a6975f05281c789cd19a6c5e19e9eb4bd4222b3a6f36bc14e`  
		Last Modified: Mon, 16 Jun 2025 18:15:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:32f18ff18cc25452321848eff5622fcf59f59ba221350bbcb5776641f36f2c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10316330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867961d38d0291df9a7f9e33081453c6ce9f19a1ccadb6df94bd348c846cdf8f`

```dockerfile
```

-	Layers:
	-	`sha256:94655a51875ebd65ad34d96dbc9310635589d0f558ea84ddc85dc2eea3f952a2`  
		Last Modified: Mon, 16 Jun 2025 20:25:02 GMT  
		Size: 10.3 MB (10289165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:216d37a96b5e412f323d3f07ca28a0e7057e5ddb762b1c551f7dd669457d8e86`  
		Last Modified: Mon, 16 Jun 2025 20:25:03 GMT  
		Size: 27.2 KB (27165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:77f40b8321e0bf47b1cd467219e41a6147f2f0c8f0dbab28937f879815bf1b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283459880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b891cce17e1abae2502d1cc3ffc5e07f805d01beb2d55731f43d3b39872b65b9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44d5956aed85d3d6d2c696b8489053af4a6a4d168314e425819189773cd2fb`  
		Last Modified: Wed, 11 Jun 2025 23:10:33 GMT  
		Size: 81.4 MB (81431904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474322652bdf8738a818f3dc1b43a8c6cbcdf6326e806a2a5c83973b4d105379`  
		Last Modified: Mon, 16 Jun 2025 20:49:17 GMT  
		Size: 79.2 MB (79171869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e606d0e497807b2cbb15ca82d564d04001f93176c351be4851015bd5213fa`  
		Last Modified: Mon, 16 Jun 2025 18:06:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5237dcc87da3456343752da802c57c324fc4c6cf5bd36d9d3f3ffc7a3d5e597b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5633af3e44ed6a3b485ebe89ebb9c65a6be827c9d52501ce62d505bfe16a8674`

```dockerfile
```

-	Layers:
	-	`sha256:391648d8a95b770c5f2e9b291be84b2a0c8104e916c2cb3e82fbdf6e3c8ee5a9`  
		Last Modified: Mon, 16 Jun 2025 20:25:11 GMT  
		Size: 10.5 MB (10483447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c901a5c34bfe1f6049241eed08534e36e13fe6b3fb7115fc6e860b98b33119`  
		Last Modified: Mon, 16 Jun 2025 20:25:12 GMT  
		Size: 27.2 KB (27193 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:554f823f0429e24c751ea518c2eca8e892f73f604423e1c9d799d3eda04a5147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296382927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65eca6beba83a9e1dea405d7fda9198adecd4cd04f5260205c42cda5a12e8a8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a34392e433938214bbf2cba34365a474d819c470686803059c6d8390cf680`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 56.0 MB (56049939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71be4b42262b42192cdebaf03549dc559058a911c2b3ac46387a5a1fd9675e3c`  
		Last Modified: Mon, 16 Jun 2025 17:55:29 GMT  
		Size: 87.4 MB (87448047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e76dfda8e65144da912c18e6b785a2d25e1b2cffef4d19df66cebc068e773e6`  
		Last Modified: Mon, 16 Jun 2025 17:55:19 GMT  
		Size: 81.9 MB (81926154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d17e4709261db99db8af64616b2d556ac1d7a3a3c293d34290a2abe548e783`  
		Last Modified: Mon, 16 Jun 2025 17:55:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:278becb0ae0d5969bcc0a3703562a87ce7616db4031a7341316cbe554a7ee951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473c74fd7c7e0d2840d4daefd0b3369b45e79e5bc20740e73f2eaae96878baa9`

```dockerfile
```

-	Layers:
	-	`sha256:64117e7b1f1a7ef20eabd07d9496e431ce9a38b21f98987124188a2e9f205fcc`  
		Last Modified: Mon, 16 Jun 2025 20:25:20 GMT  
		Size: 10.5 MB (10471501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0fc654bf5efe23f86e209034e55f3886d7c3e2f3dc4b683864cb3d5f1503799`  
		Last Modified: Mon, 16 Jun 2025 20:25:21 GMT  
		Size: 27.0 KB (27024 bytes)  
		MIME: application/vnd.in-toto+json
