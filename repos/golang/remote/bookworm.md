## `golang:bookworm`

```console
$ docker pull golang@sha256:e41c702dbd95b11333fb914e8671eb61b198c33bf9e1f89ab90c7b13460b6b0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:bookworm` - linux; amd64

```console
$ docker pull golang@sha256:63faca1fd8d85713bc6730e51a31a1155d19703a1e2637627daeb60729573b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39037e2be1b348d071dea0628a94d1559c0c0102f44102632ca343473d63f5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Aug 2024 18:18:42 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Tue, 06 Aug 2024 18:18:42 GMT
CMD ["bash"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288f02cee7a92d575f9531397d0f4f9de025996c9d6e3b90dbe9a2d76dcec82d`  
		Last Modified: Tue, 13 Aug 2024 02:05:33 GMT  
		Size: 92.2 MB (92230622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c08045297c877b698a8fa5aa6b5d3ec88c34ba7415eb1f83746a1f6babd1cf`  
		Last Modified: Tue, 06 Aug 2024 22:56:12 GMT  
		Size: 69.4 MB (69362558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aa3786ec5fc20b549f7fe03f6b9e12fb2e1120b786fc611baca0c01fc4288e`  
		Last Modified: Tue, 13 Aug 2024 02:05:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3097c8c1341a6ff3757cbf0b8dc22d495ffedd811b7b72be21c47c93a135450d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf07197470983d4e8c36596207bd67e62a1cb8bdc2dcb3c0edf262eb6af46de1`

```dockerfile
```

-	Layers:
	-	`sha256:11ca4ac20c04380b26ea6d6ed0b32e0fe0d5660b604841c11adad3db77b742aa`  
		Last Modified: Tue, 13 Aug 2024 02:05:32 GMT  
		Size: 10.3 MB (10257409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70b1e06cf207562c4d7c1772c16da617341db898a406eb1a2c84cd67423b9121`  
		Last Modified: Tue, 13 Aug 2024 02:05:32 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:b7742dd9f0ac617036cce9bf7cd9e9e4ad7badfb65cff7d5f8d018ddb7142b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260143057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d96ba4365c8aeb819d4b314edeede449205f09f3224638e3d3bd2a09a396bf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Aug 2024 18:18:42 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Tue, 06 Aug 2024 18:18:42 GMT
CMD ["bash"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bc24d45690a515d5d64aeaa7be5994f7db1e902b9e4dadf7bbc9b27214008d`  
		Last Modified: Tue, 13 Aug 2024 11:29:59 GMT  
		Size: 66.1 MB (66089195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38353948ef7c4a85c3e42510197b5f321621d39f3094140f1496e3ba11d3156a`  
		Last Modified: Wed, 07 Aug 2024 00:08:57 GMT  
		Size: 67.7 MB (67728993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d9cd78b35f0a70606a0f561779ef60551ea655c1f70adc1f012f100fb3c38`  
		Last Modified: Tue, 13 Aug 2024 11:33:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:743dc39c22b4f0bcd13f9ccb870c0d15362770ba80a3e0f52182bf7ffb0d3d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10093801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eff5097d8cf86329bc0b99bd869e3407e981ab44249656b710675f9cade6d9`

```dockerfile
```

-	Layers:
	-	`sha256:3c773af711717b59a3a2f552b2b7ecac18e21ed4c02898ce1fcd68e2c214baa5`  
		Last Modified: Tue, 13 Aug 2024 11:33:07 GMT  
		Size: 10.1 MB (10066146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e84d0c864740eaf89922cf8c5c7822d2218718766316d1ff0b0caede1217d079`  
		Last Modified: Tue, 13 Aug 2024 11:33:06 GMT  
		Size: 27.7 KB (27655 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:bdd4ea901fda6637a0d791978310e87631f923c4c9581adbfb3719bc5ec491db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289742170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7220e195e6ea64f427b2d8a3cccd04e90d84644e3389f1ed67ce834b4bdf475`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Aug 2024 18:18:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Tue, 06 Aug 2024 18:18:42 GMT
CMD ["bash"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ed394a57fdf7a8b1057c80df7e753ad2e1f2dbce3af0d967d2a04f584591e6`  
		Last Modified: Tue, 13 Aug 2024 16:02:27 GMT  
		Size: 86.3 MB (86282871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edaf09ec107de8a2f93a55fc7fad71182aeefb0572c5f2e2f498d1ab1fd3b77`  
		Last Modified: Tue, 06 Aug 2024 22:56:17 GMT  
		Size: 66.3 MB (66283242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f6a6d8da17ef2ade29cbaedba7629db289f1cfd053fe8fb47b5f6290dcc185`  
		Last Modified: Tue, 13 Aug 2024 16:04:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4c26066a825e344f3cce6c0a1df4cb805f2bc582144a9aa928eb93e098a5b16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10313225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bbe7fa0c0816d68e23a21150ff15130a0745a1e59704b68584aeb78b7065ce`

```dockerfile
```

-	Layers:
	-	`sha256:27284288e092638b0a4e5152790f4c10f2f2a51e352988391cfedfc6f63f67ca`  
		Last Modified: Tue, 13 Aug 2024 16:04:17 GMT  
		Size: 10.3 MB (10285335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64089733272fbf41be55181e7b59165fe003717cd742c23bed03eb4b7f1d0f4b`  
		Last Modified: Tue, 13 Aug 2024 16:04:16 GMT  
		Size: 27.9 KB (27890 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; 386

```console
$ docker pull golang@sha256:8ae92b0f1598356df80f4e9bd682c4cdbae8f1a3fc9cee1f05ce88a00462f05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298451422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87dc27bc5cd8aaff4b6579229d92b391e75ded6308e66d5c2ed84b3e9b8a9ee1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Aug 2024 18:18:42 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 06 Aug 2024 18:18:42 GMT
CMD ["bash"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e4669f96b4d6920c1c88d460383b24621e38fdb672d91622b5435dc41713e8`  
		Last Modified: Tue, 13 Aug 2024 02:05:54 GMT  
		Size: 89.6 MB (89644805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9246b2845dd9f2f6bf65a392e8e3a4218cccd6b1dcbc03a828b579ac7aeea4f4`  
		Last Modified: Tue, 06 Aug 2024 22:56:14 GMT  
		Size: 67.3 MB (67346683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4588000f1c19583392b8d06b235e355581bade6c11ee8188364be9e678f97d4a`  
		Last Modified: Tue, 13 Aug 2024 02:05:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:425e83d1d3b06ce3b73f8949c903d3c2d0af15c1dda0754c7350880884f41def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ec430b42797e633af20f69939b8e992356d0ed7529d7790d1f9fed918fdaa2`

```dockerfile
```

-	Layers:
	-	`sha256:61c3ba7830526821359b0f7787c3c69103afa17d457ea63311ff76c3c0ac494c`  
		Last Modified: Tue, 13 Aug 2024 02:05:52 GMT  
		Size: 10.2 MB (10237667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2eda2aa089532985336b8a8a96265d1c160fc8bd863492342a9f964fb91b84`  
		Last Modified: Tue, 13 Aug 2024 02:05:51 GMT  
		Size: 27.5 KB (27474 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:b049b6223a09cc520d0306f25608b8a5d0b8bf92f0991d4e9a40e0cd7962e313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270095661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af592bd4eaf4633ff36c54afbb023e6ec8a4a3c292c66c4324312ab1ed723da9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b6025db3aeb726503a6d775307c4881743edbf88fbefd8a997f66bb236e568`  
		Last Modified: Tue, 23 Jul 2024 01:59:26 GMT  
		Size: 63.0 MB (62965755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384a4864817e575bb9be405b8211a736dc0d9f4c7a7a3f3a69362908649b06f1`  
		Last Modified: Tue, 06 Aug 2024 23:00:16 GMT  
		Size: 69.8 MB (69804406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec510b2b8fe8d60e2b414c455523b255d2db4e07537481fb550635278f8c2a`  
		Last Modified: Tue, 06 Aug 2024 23:00:16 GMT  
		Size: 64.1 MB (64125639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677390295ff7019b7fabc9ca6abd29b1c6fe12e2b57476435284656da6bd16b7`  
		Last Modified: Tue, 06 Aug 2024 23:00:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2feb75c909ebf27c1de5ac46c68fa91d3bb79bfa2168602f03babe51a3c75e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0e1f94cdd94e91d19ac71efbb35d1462c4ca885e11e767abee31600a762f0`

```dockerfile
```

-	Layers:
	-	`sha256:9c9d6c07df9800db780266279e283eb439bbf9f1148b285bb4417222353c4271`  
		Last Modified: Tue, 06 Aug 2024 23:00:09 GMT  
		Size: 27.4 KB (27407 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:98cb8c5a3ed3cb6eed1a8ec9b1360ae57df567db1b8642db60ab5f7c8d7b03da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305506568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d03303323dd8837781237a22bae82b2a1a3b9fb6a8716ccc49dbc3f26de261`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c6079496e8075450646b804bc7561fa8e5a51a5e6ea5ecc8bb95e91d1b70f`  
		Last Modified: Tue, 06 Aug 2024 22:57:05 GMT  
		Size: 90.2 MB (90217721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa907a73ecb9721e6fd07eeff45b3daafd73705b1b26a4ab050075d2da72289`  
		Last Modified: Tue, 06 Aug 2024 22:57:05 GMT  
		Size: 66.5 MB (66453881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a21c8cb3eff742a557bca6af5e67c7fb11c78c96a3ee5bb3605ab7b3c9bfbca`  
		Last Modified: Tue, 06 Aug 2024 22:56:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fb1a58d3db0e9b122017e81c5fc463e4d5292e8d8715cf2ccda5aeb407ccc776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10257855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6e3d2f3bbefe1a839f98ec9131cd8c4d9566b0c21fce53f0460ceed9f835a9`

```dockerfile
```

-	Layers:
	-	`sha256:93538a60a38af45702d55646c1d4c70d748872296e749031aebe3bf9355e588a`  
		Last Modified: Tue, 06 Aug 2024 22:57:03 GMT  
		Size: 10.2 MB (10230262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff1b3ef2842bf300bf20068757b5f7d562229efe3e0a459f851c74ea9b9c84b`  
		Last Modified: Tue, 06 Aug 2024 22:57:02 GMT  
		Size: 27.6 KB (27593 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bookworm` - linux; s390x

```console
$ docker pull golang@sha256:77e43fea0f4bbdd4138d56ba40e896f6b96069d700aae7e141f2c05d56ff3fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272330782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d47b27a7d325d4ae5591a6d9e053975a58c856937db2c29f4ed3b4fd205d975`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595192cc94e229d993517278145a78a10c23a885c080ffcd19e97a74f180eff`  
		Last Modified: Wed, 07 Aug 2024 01:54:05 GMT  
		Size: 68.8 MB (68804230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4f522c886389638258537d7ed45e62dbad030e5ed340cd291df30569fc9288`  
		Last Modified: Wed, 07 Aug 2024 01:54:06 GMT  
		Size: 68.4 MB (68420968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f7f1eb41bb96f5f742ac40dcc894d30f1b7995564bd1e690ef4a6d53c03e4`  
		Last Modified: Wed, 07 Aug 2024 01:54:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e6997e042ac3149006703f6cc9e62089a647d3be6caa33ca3917d791dea5316d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10121335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4676e8a7562f230e1785f021bc78edb2f97793ef6c2cbbff3e47e2a88c6c321b`

```dockerfile
```

-	Layers:
	-	`sha256:e59dfede12bb94fa3d1f68ec080ed96540be201102a0e815b96d6ae33e3008e9`  
		Last Modified: Wed, 07 Aug 2024 01:54:04 GMT  
		Size: 10.1 MB (10093808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4619ec6d32588ef6fbb317cbb131c2904c19ac3ce592f184eef3c9de66dabcc`  
		Last Modified: Wed, 07 Aug 2024 01:54:04 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json
