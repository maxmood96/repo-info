## `golang:tip-alpine3.23`

```console
$ docker pull golang@sha256:715a146ea89dec7edcca9b4434249be5e0697ebc6c99394c6478c7b7daea0b44
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

### `golang:tip-alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:1805d6afddff53ffd019259a63b4d058acf5b9e5d4066acc49d182adbfea4a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97822064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882c4ba166b71a1da94d0a4e25bddeb53cdf5c84d4cb9290bbc65f1144d5bece`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Mar 2026 18:36:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 18:36:29 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 18:36:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 18:36:29 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 18:36:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 18:36:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ded05a958a6487b88f04285907328a43844646b183c9de631f926d6b51d8fb`  
		Last Modified: Mon, 09 Mar 2026 18:36:45 GMT  
		Size: 296.1 KB (296093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a04c034b447c8996669d72bbe0e1d2cec1d82755b44408c364d44c021efa7f7`  
		Last Modified: Mon, 09 Mar 2026 18:36:47 GMT  
		Size: 93.7 MB (93663992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08a4828aa13bc1fa09bb607d9d60dd7b0c6aa7bfc5c4eec038f3d0f766595f1`  
		Last Modified: Mon, 09 Mar 2026 18:36:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:54e20cc589b185f0b53f117da1f0a902311f37c566e44118a5533ec9b889ea35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c8e7a01a500ee5710c57340920b7a240d27308d5c4665127871c8cd9cba1d0`

```dockerfile
```

-	Layers:
	-	`sha256:c738dbd50566faa51150ff2ce904f0711b134c596df1c759be559d1fbfd98836`  
		Last Modified: Mon, 09 Mar 2026 18:36:45 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e14920e0144d6fea358232dd945eb956b2d405cc84b2dd2f075a8a455491fb3d`  
		Last Modified: Mon, 09 Mar 2026 18:36:45 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:fff2bd1e7e47bf028e77138a4764b9617122793ee846f609e52bd66f3ac61feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93837837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcfdd48392e4fc282c9dc80301e7da44b82ff07f9bade483c2739c8316098976`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:59:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:02:16 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:16 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:16 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:02:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:02:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95401a161baa817f60753df76b1db2b8e113c6c233cd65ef651c862aeb213144`  
		Last Modified: Fri, 06 Mar 2026 02:02:31 GMT  
		Size: 297.3 KB (297254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f75482abeb648b9189b3f4696db6444fed715bf37c369ca85b2202c497f7c6`  
		Last Modified: Mon, 02 Mar 2026 22:04:54 GMT  
		Size: 90.0 MB (89970604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85942aa995db329eaf7a4047e785d023e70d38ae76dfe81d2e0975c74b35c4a`  
		Last Modified: Fri, 06 Mar 2026 02:02:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:ce89bf3229951b1f008b5c62a3b15ca623636d41f2d185e13df16d0739ec0ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893489728826a6f0757c4d5cea635b34b1a386d18eab180f5334f11c3ecdf39a`

```dockerfile
```

-	Layers:
	-	`sha256:cb1766603ab60973ddc44cb590ea8baeab5686c3921c482d5f1bdc2d72d2c632`  
		Last Modified: Fri, 06 Mar 2026 02:02:31 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:0fbd32b770ce6452c662bc9c1c12a887293ab36ddec4d501e505c64027e10c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93274747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5307d15933aec3e751a4b1c882a16c6fc11ce36836ad81367ffc30a585dab6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 02:00:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:03:06 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:03:06 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:03:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:03:06 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:03:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:03:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35538a47cbc8dc979f6a826d8c01d6a0762ebeae214a7fc706c37bd52149d7`  
		Last Modified: Fri, 06 Mar 2026 02:03:23 GMT  
		Size: 296.2 KB (296202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d47f42e49b5b1824f0c700b4d521593aedaa7278226bf8d2c8c937a0110183`  
		Last Modified: Mon, 02 Mar 2026 22:04:34 GMT  
		Size: 89.7 MB (89696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e4ee3c66fb363b3a420530f4e9a678fb2fc0971ee31ed77fa8fe21ffdb747f`  
		Last Modified: Fri, 06 Mar 2026 02:03:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:1240d225979d0193380f52f7877c5d453e6042e1cd20f5249860aa8065e69600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10260ca821584f37b150935f6805db82d55f21e2c58375c9a7a877fb6787b152`

```dockerfile
```

-	Layers:
	-	`sha256:f8199f72e87876fb5119d3b2809164b73ccbcf6fbf9b1817ff745fbb00cdc16c`  
		Last Modified: Fri, 06 Mar 2026 02:03:23 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b03739ec0cd711863553ec6ee4f4c813d20985384d09615357783e1d571696`  
		Last Modified: Fri, 06 Mar 2026 02:03:23 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:debc0585b84db2a0262c820246e43063284c5c8c4b0a6409ff5423d55beea910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93329773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af3ef19947259c4f3137cac865594ccce9558a3e89e237adb0b1f3965823540`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Mar 2026 18:37:59 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 18:37:59 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 18:37:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 18:37:59 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 18:38:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 18:38:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fd0efeb57505a0bb7bcc365f8e72538ad8c6e0068dc2387c4922200b8c472e`  
		Last Modified: Mon, 09 Mar 2026 18:38:17 GMT  
		Size: 298.8 KB (298842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1276795b08c8a192fe74bc0ca89800479d8cab1b3bb0e3b28f26af398b665fc3`  
		Last Modified: Mon, 09 Mar 2026 18:38:20 GMT  
		Size: 88.8 MB (88833682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b75353c1602d54dc692ce7e7496143df3825360f0a7c69451b63cd0681f14ce`  
		Last Modified: Mon, 09 Mar 2026 18:38:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:43f0015a566fbd7c36a40d8042215ebadef708d9e8d6fc7424bb148cb3d8d18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17471f24e7e4ef777c6143b7c29d2b36b9ae8c6fc4896e6de42099115794eb1`

```dockerfile
```

-	Layers:
	-	`sha256:d56205bf6aab90db194cba7038b724969ff42265dbf06ec6a21d6245cd7c1e66`  
		Last Modified: Mon, 09 Mar 2026 18:38:17 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f28d0c5d4ec7871ddeb64bffd4ad28b9cf54f0249a5e1e56e9f7c31ea1c68a02`  
		Last Modified: Mon, 09 Mar 2026 18:38:17 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:2eca0abc5b0a9ee05316d3db520ee3eff12c110ffcf10cc861883888cc0aad2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95499696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5736acfec8e030e0c2ce0b3433db915533e6430d66597fcf732d93ddf73cb475`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:21:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Mar 2026 18:23:44 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 18:23:44 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 18:23:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 18:23:44 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 18:23:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 18:23:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff95d433387aae44f4ee20581dd5980b40840e38cdac8cbfba06a364089fe3e`  
		Last Modified: Mon, 09 Mar 2026 18:24:00 GMT  
		Size: 296.7 KB (296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8181476688ce59990f6e1b32458c610684950481d47bcb0583cc777042e4e2`  
		Last Modified: Mon, 09 Mar 2026 18:23:47 GMT  
		Size: 91.5 MB (91515879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595653d9bf67a597fe1e0c19681b941f02c191255dcdcfe00938f2ce20c65bfd`  
		Last Modified: Mon, 09 Mar 2026 18:24:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:713d7e82c643413ca12ed6613a1de982701a3ea30fc7dd1b9108d939cd1d30d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee23314e3ba8a738486693fe19225f378110985a1c02dff1903aea06aca39bbb`

```dockerfile
```

-	Layers:
	-	`sha256:19eda5d87465861dc78e138b508ed783df8609b6b8187bcb753e4ed15fd2a823`  
		Last Modified: Mon, 09 Mar 2026 18:24:00 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660dc865e0385ed84092af0b144660501681efddf03f16ce362157b44b51ca64`  
		Last Modified: Mon, 09 Mar 2026 18:24:00 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:07c610aa23f17aeacc7e29c06976607a74505bd0a5cb7dc0a67eb64b917efc85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94444954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36271c84f0a975d3c2d3757c08e53eb4311cff5ef4d36aaab4986e12f870ffa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:02:04 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:04 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:04 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:06:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:06:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e662a4a3a7cbf153b23a38a961b2078122cec8354bbb9cc27381fb9fd6abd628`  
		Last Modified: Fri, 06 Mar 2026 01:12:55 GMT  
		Size: 299.3 KB (299266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcc3a57b0d1a4c549275152be846eeab1e4bfda9d363982944775991fe15219`  
		Last Modified: Mon, 02 Mar 2026 22:05:31 GMT  
		Size: 90.3 MB (90315888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982c155d3f447cc650e69555a85aa75d5c6a1952f54f1ba2fa5567809576c689`  
		Last Modified: Fri, 06 Mar 2026 02:07:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:dd4874a60b011ef20c9ef8577c6b2d9de3a9e4b1fed800ce4038eaffa9bc33d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9008aa5d1b211d8b03b212b98acd8647353d9f4a1830e8814c5d83dffec3b5`

```dockerfile
```

-	Layers:
	-	`sha256:e76aa4fd9b2b9cd10c6007cbda22a1bb20f0811cade0c8c053fae4923822f87c`  
		Last Modified: Fri, 06 Mar 2026 02:07:20 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53388c961adfe08adcf4c43e7d99d9a1abf18adebb87f0aad43fcd9fced26a57`  
		Last Modified: Fri, 06 Mar 2026 02:07:20 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:c876dc4c6da23a7bee07a9f76afb401303c54442e86ecd1aed53aabb2a10681c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94671232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81486afe7d6a886501ac8416e771824d53b5f913bb759805408610bc7406587d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Mar 2026 09:03:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Mar 2026 09:03:40 GMT
ENV GOPATH=/go
# Tue, 03 Mar 2026 09:03:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 09:03:40 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 03:21:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 03:21:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7550964df09cbec6e16da50f25098e25826ade610bf4557ad9371e12e9ced3d4`  
		Last Modified: Tue, 03 Mar 2026 09:10:27 GMT  
		Size: 90.8 MB (90789282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95f9d26c7202c75ed4be62cd3070f05c5fd9fa4ac8d126da86e234cb482bd9`  
		Last Modified: Fri, 06 Mar 2026 03:22:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:937902ed6c31df6c851f15b0f77815c549d4cdedf612ceb19bd087f9ca8f223b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b95a0f0d516fe8216fa4e9033b57a3217df19c83fc4fa7dc1adb0491ba8604e`

```dockerfile
```

-	Layers:
	-	`sha256:8cebbd8ddf93a6231a6ea31f7f359533341c7481cfb21dcc6b0dfa4b2d690b06`  
		Last Modified: Fri, 06 Mar 2026 03:22:27 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8fd5e2a6623cace46ff3fb2eabf896e4f068780093657b881a7687cbabcdd49`  
		Last Modified: Fri, 06 Mar 2026 03:22:27 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:f51ec2c6feb10fcdaac6eaffbbbf23d2a923d6fe2f205f9fe1487172d3c8c8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96889251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f375a634689f8037c88b3ce1882679bc4f67f953de55e0b5694be58686e73a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:36 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Mar 2026 19:05:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 19:05:14 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 19:05:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 19:05:14 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 19:05:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 19:05:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd5ab51b8e8f66169cffb9d96d967b9b6e4aee93adcc43791642e2fb0e431e5`  
		Last Modified: Fri, 06 Mar 2026 01:12:06 GMT  
		Size: 297.2 KB (297195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeaa76acf61a14d8cb194df2a407d1383d717722d6e254333be0cf42263af58`  
		Last Modified: Mon, 09 Mar 2026 19:05:28 GMT  
		Size: 92.9 MB (92866565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c399cb8c671225cb7f062381c5985a71474452ae569b7c559c046e4880c3c75`  
		Last Modified: Mon, 09 Mar 2026 19:05:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:d2981e533fc59aebcd9b1d2444c96e168fd6b0d2e747dca7dacff63b44ad309e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9b83d9afed829598c16e84117f011bcc51e44d49f37aca43d53a741e60d68a`

```dockerfile
```

-	Layers:
	-	`sha256:2075aaf4fc09eafeeb820439f67c05960e8692639e4470645c6554835d40ee0f`  
		Last Modified: Mon, 09 Mar 2026 19:05:38 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c473d1e7f7e582bda9ed2d84566248131d9af5f34d006870de67d424e9b52f`  
		Last Modified: Mon, 09 Mar 2026 19:05:38 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
