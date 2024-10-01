## `golang:alpine3.19`

```console
$ docker pull golang@sha256:f6392ffebb028fed5ffe743ddb9716e38402c978779edd66474bb5d05f5e65e4
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

### `golang:alpine3.19` - linux; amd64

```console
$ docker pull golang@sha256:3be9996ceac2a435b4b1153b590c8fe6b902cf1afc2a86e36df8bcf922048f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77719122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65495b4dc1b161b6709cf03a747ebb306dc32845cb922ae996635a90fd0f13c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9342fca38021a3f712f893e2ad2d44bf5029abb88ae234f252b69df107e16a`  
		Last Modified: Tue, 01 Oct 2024 22:18:54 GMT  
		Size: 292.9 KB (292877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac1f1163629431c9f488c4d6ff6afb5c73021839723b50bafe245663ad3d9df`  
		Last Modified: Tue, 01 Oct 2024 22:18:51 GMT  
		Size: 74.0 MB (74006382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d3e5075e9ba6d191c007303d66cc5a3a7e860f63f3eac494a698e65154989a`  
		Last Modified: Tue, 01 Oct 2024 22:18:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:201668005bda2096b4b7ebfd1aac9001caedf5979cc60fe67aa23581be3451f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 KB (235352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff6014fc46216be176c5283f5cfb4c7885ca25a65630cccef5e72fd7164b970`

```dockerfile
```

-	Layers:
	-	`sha256:abeed14b21c5fcbc00b9dfc11f102de01e8e796db50fb3c18a5c897007b3894c`  
		Last Modified: Tue, 01 Oct 2024 22:18:54 GMT  
		Size: 210.7 KB (210724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94c1f748187976d9a4869cc2b64fc8247cf5531277a5accb7bc5e81ac7ecdae`  
		Last Modified: Tue, 01 Oct 2024 22:18:54 GMT  
		Size: 24.6 KB (24628 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm variant v6

```console
$ docker pull golang@sha256:c2e74739245919d6bef1db7846133b1195ee08f469b671c2dbce92aefc8bb255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75632143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106d8cec9301ecab4fc5135d47efeccc1bab0579d1502a0cddc866a5154c14bb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:26 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Fri, 06 Sep 2024 22:49:27 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163a189aaa8881b35f02064df0565f1c166dd7085fb308b5414059d2a5ec1777`  
		Last Modified: Sat, 07 Sep 2024 02:31:12 GMT  
		Size: 294.3 KB (294282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b1b9390cf2d540f3f141f77cdd7d696ac60b3ebfef2290308fa3bb76ea42c1`  
		Last Modified: Tue, 01 Oct 2024 22:19:57 GMT  
		Size: 72.2 MB (72161312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6bf611c65caa90c8831c1e95dce94a16565e258c709b3b40112b4559fe38c1`  
		Last Modified: Tue, 01 Oct 2024 22:20:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:da1ce3054bd33334573d20017dce879e5dfdead661896ee1f0eb044771fa10b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5dd7a0f675536f23170155ab6c6bec52f5d418eadab20fbf1c3cea557118fd`

```dockerfile
```

-	Layers:
	-	`sha256:11e27afb7a83d0c7a0d1e07b5db2e5c1f1c37015eb0f87cc352343aa700e25fd`  
		Last Modified: Tue, 01 Oct 2024 22:20:30 GMT  
		Size: 24.5 KB (24504 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm variant v7

```console
$ docker pull golang@sha256:36f74e61812b9d93725c887360600e5f829fd469d4e386fc9f61a562150acdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75382311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a924e0c0d7a9b574c65013b3bcce333fae59d91eb7b1f73ef03f6984508eac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4a709a6ccc9bfe9c2bbe83615d2081840b3b62a2e1e9dabcfffdcd83c365da`  
		Last Modified: Tue, 01 Oct 2024 22:25:15 GMT  
		Size: 293.1 KB (293104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda832285c268d03f9079f25d645da4f232d333a236aca4f5406f4294d01f183`  
		Last Modified: Tue, 01 Oct 2024 22:22:37 GMT  
		Size: 72.2 MB (72161385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f5130c66340204dbbd5b289e0eca0df2a78a1b4c5290285d84321b7d05a787`  
		Last Modified: Tue, 01 Oct 2024 22:25:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:7d7160a790306ced53b7feb9f68de65dfd54d882e782add2c8ee8cde567618b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 KB (235448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e6f40fed5523408ed21f7065843a4a690e6f91df28c951d5d084308a0521b6`

```dockerfile
```

-	Layers:
	-	`sha256:b1dbd45a6c50595ab065f4dd4d96afbf0ab5a71315e450110864aba911fe4e23`  
		Last Modified: Tue, 01 Oct 2024 22:25:15 GMT  
		Size: 210.7 KB (210724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a72845efa0a7a04498ad8f7f4f0ce1ea863aab25ba7817d1e576320440ec118`  
		Last Modified: Tue, 01 Oct 2024 22:25:14 GMT  
		Size: 24.7 KB (24724 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:beaa36ec798013aa83b3fd09ff72c9c19779efcc9cd2cc5eaa11e9cc300e1403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74299425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a24bdc58d436ab5d08049a73fd5f753aeb959c70d30b92b8de0ed81799338`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30962f4d5cba76c58d127c10562ba1f510fc792c8bfd09975b1d3eeb27d12fbb`  
		Last Modified: Tue, 01 Oct 2024 22:24:16 GMT  
		Size: 296.0 KB (296031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37a00ec5f007d0ae73647c82b7d81d98a44fb7d073d06e633d656bca79db62a`  
		Last Modified: Tue, 01 Oct 2024 22:22:17 GMT  
		Size: 70.6 MB (70644133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0ff4b800b52c620e73b196074971459baa115db429a2619ac625106ed527e`  
		Last Modified: Tue, 01 Oct 2024 22:24:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:948fc346be4d5eb828cb039bac663e6623df08d33eadc81d7d9509a247b2f0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 KB (235536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc0738a0fe375a3a47cda40e75846b623dac95a4d81b846e4054e2f88f7f960`

```dockerfile
```

-	Layers:
	-	`sha256:bfe428f61a6cd6b450d3bb47fd1858c64920fef2db4896e9f2bb0a080f819e49`  
		Last Modified: Tue, 01 Oct 2024 22:24:16 GMT  
		Size: 210.8 KB (210780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79ad0ee9ce18c5d225baf180d021591bc68f05f268b93fcfba51569793cedb1e`  
		Last Modified: Tue, 01 Oct 2024 22:24:15 GMT  
		Size: 24.8 KB (24756 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; 386

```console
$ docker pull golang@sha256:f584c2c8bff6b5c51bb5794f67fd937ef6339d8e3618f2a2b10586a6f7fc015b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75427512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ff17a5aa48419be39f0159b4555a3dbfef3af78ed007a8f1efe48eeb0c120c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970fb1f99a46f1a385040356390bf36945a19147836f8c8cbec60b5325c3f5d0`  
		Last Modified: Tue, 01 Oct 2024 22:18:58 GMT  
		Size: 293.5 KB (293536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d4de23fe72666a7f8131049dc36e9aa2ba3bb48644c246b44b0b9d60e95bfa`  
		Last Modified: Tue, 01 Oct 2024 22:19:00 GMT  
		Size: 71.9 MB (71880213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d3fd68230fab2c879e212da1384307c98969d61e05abefc881962b928f08c3`  
		Last Modified: Tue, 01 Oct 2024 22:18:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:e0ee7517a9e31f0c2d86b88f6cf93e9d34db84759d0a729cd13ec290e2e59729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 KB (235258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d28e084905e97b71413e7b2fdc2d83867111cfcca4f78ed2c1b3a0552af1dd8`

```dockerfile
```

-	Layers:
	-	`sha256:4924a99e2a9991e4ff0f0575214812c5266dbb3f7059d92331eee0956f4a94a5`  
		Last Modified: Tue, 01 Oct 2024 22:18:58 GMT  
		Size: 210.7 KB (210663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428fbd8676d9c1217c0e9c8dd732a9e2373f28da9df1f5b07bf53a7127ef838b`  
		Last Modified: Tue, 01 Oct 2024 22:18:58 GMT  
		Size: 24.6 KB (24595 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; ppc64le

```console
$ docker pull golang@sha256:7c41067eb80da75db6c7517ec1df87399be3a7ca7623f82563b246b9e5cf54dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74471579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49b3bb28e74a12446e188adf03f6aacea37cf2e7d5c9356e4e7546710ec6436`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3569cc4b384eefd26e81ca51d60ca74f84a00feb9860e482461c442f2f374a`  
		Last Modified: Tue, 01 Oct 2024 22:26:46 GMT  
		Size: 296.4 KB (296448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdc178eefce949e69fe38c13cce1ba17fa50a129169fc4241e2ca8280bdbc6c`  
		Last Modified: Tue, 01 Oct 2024 22:25:17 GMT  
		Size: 70.8 MB (70810506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb1bf630a83898732b2aab68824440c710eb2a8533201c7ae71d7f9ef3a7e0a`  
		Last Modified: Tue, 01 Oct 2024 22:26:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:70393bbaa0f7ed47b4195ceada2b80895346636b98d21d36275ff59a839dd5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 KB (233510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545d5a51e329913213d4e2c794b2cd653d1fab8528b6281ff68e492422059a35`

```dockerfile
```

-	Layers:
	-	`sha256:96778e2c4714803e678428b0c73932784a61ad9a87fb92dd7c49549b5fa6f8de`  
		Last Modified: Tue, 01 Oct 2024 22:26:46 GMT  
		Size: 208.8 KB (208840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d45176c3873bf6645315d6aeeb0d2f97ebfd8a0e3af744a7fe0c760a292622`  
		Last Modified: Tue, 01 Oct 2024 22:26:45 GMT  
		Size: 24.7 KB (24670 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.19` - linux; s390x

```console
$ docker pull golang@sha256:ddb46036d45416d239c0d822989467dbba71108dd9d855ef4bb1067fb3b05dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76483238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663cdc6cff7a0e98f0c5e87768139da5192926c4f1408838a74e7c0e12e77ac1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310cd18af315133cca72fd54e5204cd99436a12caa978c035866ba40e501674f`  
		Last Modified: Tue, 01 Oct 2024 22:23:28 GMT  
		Size: 294.1 KB (294073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb0f3540aaee2844fb7022ba44453797a29663928ffe252ed090c5b51b28634`  
		Last Modified: Tue, 01 Oct 2024 22:21:50 GMT  
		Size: 72.9 MB (72935651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11570d9a25468b342d756c9285f32cba2825bc08e2d6a33136d55918d0c6a8b1`  
		Last Modified: Tue, 01 Oct 2024 22:23:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:e6bf77ba1ab153de849f21e4ce0fb5195695f3ff42fc48b4abc77f1eda406077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 KB (233396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d9b7a74ddc68670fa24e9b404cd2042f01ad606de64e9a16bf8e67d5d0790e`

```dockerfile
```

-	Layers:
	-	`sha256:c146e16979df635583385380e89a56b94e917bb41d03927d5fc28d00db4ce058`  
		Last Modified: Tue, 01 Oct 2024 22:23:28 GMT  
		Size: 208.8 KB (208770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc21d70e77c310007461ade23382ec59fec5238ee225474e58e75b692c2cb094`  
		Last Modified: Tue, 01 Oct 2024 22:23:28 GMT  
		Size: 24.6 KB (24626 bytes)  
		MIME: application/vnd.in-toto+json
