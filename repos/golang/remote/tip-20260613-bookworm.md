## `golang:tip-20260613-bookworm`

```console
$ docker pull golang@sha256:2b71a932947117d5ae79ca781435891d2a158e0ad1c4f0d8c34cbdc8d697be10
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

### `golang:tip-20260613-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:7b80312aac40213d9b2d6cb6a017f1f866238a2d0395a0f2c12b0a2a73e07924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331536619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4ba61b163fb15cb333063e1628ca767735e5228531652e77051741770644bf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:27:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:29:04 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:29:04 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:29:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:29:04 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:29:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:29:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79976d841e0af0fa4d18b6ef6a605fc847632442e578a714741eee5cfd445d27`  
		Last Modified: Mon, 15 Jun 2026 23:29:35 GMT  
		Size: 92.5 MB (92481695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f299e0e3bd5e6acb73b7c4b5cab40f1e2dfe3ddb2a4bbbe05ceba99d84f0fdf`  
		Last Modified: Mon, 15 Jun 2026 23:29:20 GMT  
		Size: 102.1 MB (102104608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498407654e58721e8cde0fcc49b43feefbe5c236944292d87d7996763787f80`  
		Last Modified: Mon, 15 Jun 2026 23:29:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260613-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5beff9c92c3dd6af1b273907dc72b68d104ad364f0f960c6726e03ae82d35ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7441d20f4488210e8264ba4411aaad874a6eaaf6d24443d3f27e6e3167338d8e`

```dockerfile
```

-	Layers:
	-	`sha256:2bc4127bcb20bc541f4f8b32181244de908167a683429128d3f43b50d00ff089`  
		Last Modified: Mon, 15 Jun 2026 23:29:33 GMT  
		Size: 10.5 MB (10497073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1760b55fa6f5a5c43ce01c1919c66810581cf886434f5e952db8f400067c3e01`  
		Last Modified: Mon, 15 Jun 2026 23:29:32 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260613-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:447e57f6aaf82330eb074b9a6a9b8cfcb0a65e185bbf54fb7b006a26fb953590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289994794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7bbff3c360cb7adcbad169e06afb1b1affc0f34cbfebe2210c105fd8eba636`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:43:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:27:26 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:27:26 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:27:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:27:26 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:27:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:27:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f917f7c68aa5629a37a99de2287c5dada27c5ba0cd553e5b4f28471c0e6c213`  
		Last Modified: Thu, 11 Jun 2026 02:43:46 GMT  
		Size: 59.7 MB (59661587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a81c2e0f9c96877c26177eb49534a219e283b7be8b27117cb7012b571994555`  
		Last Modified: Mon, 15 Jun 2026 23:27:54 GMT  
		Size: 66.3 MB (66338931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f3afb2b46cd31bb80c259a8638a98ac035a8bd800ea0d4d4395dd90003ea00`  
		Last Modified: Mon, 15 Jun 2026 23:27:30 GMT  
		Size: 97.8 MB (97836180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21721aecb9d448b85c0932b7611b7dd9bea13b2f792f6a34263ad2d09788609`  
		Last Modified: Mon, 15 Jun 2026 23:27:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260613-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1635d0d1061bee1b22f0820270696715f50c5ff5c0b681440d701f507d5f636c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9712bf7e2fff6badca6195370f8d2e7f67a53138bbbae8f7c876eca0636223f`

```dockerfile
```

-	Layers:
	-	`sha256:0564be5732a3eac393644e8b2686ba074d2363742deb965e5eeaa339c8a9dd81`  
		Last Modified: Mon, 15 Jun 2026 23:27:53 GMT  
		Size: 10.3 MB (10303769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f118c848546aded851fa261d8111a389468f270c49109718c4f3b3193c4b61a3`  
		Last Modified: Mon, 15 Jun 2026 23:27:52 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260613-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ec48770b40ad132abb1d7c3309cd8faa7d3619f08ffde46f2775347acfbacd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 MB (319591012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ed16844683f18e129106b5810a9a895a58d087fa690223bec50f18546eee3c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:26:22 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:26:22 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:26:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:26:22 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:26:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:26:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733e69dc493fb8a60fc53a3ae5baf43da91bcbf4714af852165ea48d5a24e00`  
		Last Modified: Mon, 15 Jun 2026 23:26:52 GMT  
		Size: 86.6 MB (86554639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdc6f594300f89ac123e28e6396b82aeb7db11414dbbf3d120d335b23be9022`  
		Last Modified: Mon, 15 Jun 2026 23:26:34 GMT  
		Size: 96.5 MB (96546025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1e5212bfd066ef5806f2355a1aae9fca79d5583071a64391e73984f7f05a93`  
		Last Modified: Mon, 15 Jun 2026 23:26:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260613-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:04760899aa401478ab896f4324fe7efe971a8417522954f651f361a2431e8100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe414802a3762fe968e9d56619af8e0929c42a3d15a242b9609902c39a4da64`

```dockerfile
```

-	Layers:
	-	`sha256:bd814d5f756584619f8b2b45a7ba554c939f26ca119fadf69f1440d1d68b7389`  
		Last Modified: Mon, 15 Jun 2026 23:26:50 GMT  
		Size: 10.5 MB (10524897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0fa1974811ed94a10500bdd083a63e4698ca92375914953b21d4825b77f14a`  
		Last Modified: Mon, 15 Jun 2026 23:26:50 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260613-bookworm` - linux; 386

```console
$ docker pull golang@sha256:df5b1b2d6e2a708acb2ce5b19ec12829ba60a3f821651a2ca9c2eb906aa93660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330394007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fbbc4f35b3e0894fc23ff20c73c4c0ac6b3a16597665ba14d400c42b911bb5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:24:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:24:24 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:24:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:24:24 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:24:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:24:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1abb617cf69e81d401bea3de65ddcc50a1ac250e94890ec9ab61cb42a18679`  
		Last Modified: Thu, 11 Jun 2026 00:44:59 GMT  
		Size: 24.9 MB (24879714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cc4b12d03ab32e6c96be6bc5f6e0fc347b431b1f7686aa5f92f4cd1a5cccbc`  
		Last Modified: Thu, 11 Jun 2026 02:24:53 GMT  
		Size: 66.2 MB (66244000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89efeaa6018f8d19a98cacc97a61c17e528fb69ec9a1ba5eb1e6de362bfa873d`  
		Last Modified: Mon, 15 Jun 2026 23:24:52 GMT  
		Size: 89.9 MB (89903788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1792fe3654cd71494db1238d388e796cd8a11c55f4bdc3626b4c71f43b9583c8`  
		Last Modified: Mon, 15 Jun 2026 23:24:36 GMT  
		Size: 99.9 MB (99875141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb9b1259041e95bdee95a35ed14267d989c0fd704265829d1f267bb76982355`  
		Last Modified: Mon, 15 Jun 2026 23:24:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260613-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fa9a1a429b4d5948232a3574dea742dc3daa01ec7753da69ee0d4303fe23e206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10505005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5826cb280af4836aef9c9efe348feff58e013e1e7dac3777e90338fa8379fb`

```dockerfile
```

-	Layers:
	-	`sha256:6d3cfa2a03002827f41c273d1ac6011ad86dc60e608c96b57971d44da975d600`  
		Last Modified: Mon, 15 Jun 2026 23:24:50 GMT  
		Size: 10.5 MB (10476653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04d360e493c985c831f92744694fd65455c1ed2b965a2b9e1b0d13436a2dab9`  
		Last Modified: Mon, 15 Jun 2026 23:24:50 GMT  
		Size: 28.4 KB (28352 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260613-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:efbe1e21cedbfa15dbdb939e885dcc29e419fa7cd4ab312d8ffddb98d1d818ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301324856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e294df3fd5bb34023a71b7705985a235f7814e8a6c631982b27c3c22c420b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 17:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 01:00:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 01:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 00:07:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jun 2026 00:07:48 GMT
ENV GOPATH=/go
# Tue, 16 Jun 2026 00:07:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 00:07:48 GMT
COPY /target/ / # buildkit
# Tue, 16 Jun 2026 00:08:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jun 2026 00:08:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c4a18bb29be3659c76b4d9b55eb7f69e2b6fcb341523ef1670ac059503a592b9`  
		Last Modified: Wed, 10 Jun 2026 23:39:38 GMT  
		Size: 48.8 MB (48792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d391bb145fa329ccce2ad9a5e686a519ff55f48ee4a211ba2c146ad64db56d80`  
		Last Modified: Thu, 11 Jun 2026 17:09:36 GMT  
		Size: 23.6 MB (23624039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270c086020bbce3335fe9eece6ed9bd8f5bc1e45eed6579e81e64181addffb83`  
		Last Modified: Fri, 12 Jun 2026 01:02:23 GMT  
		Size: 63.3 MB (63315954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914bf280b1770cc8113eb19527c59fbb1740e0ce824cec4f0fd9e76670a4b8f6`  
		Last Modified: Fri, 12 Jun 2026 01:33:02 GMT  
		Size: 70.1 MB (70083997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f5753cbb93110824aac67c3cd67420ef2b33ce494467cc8178952565011f9`  
		Last Modified: Tue, 16 Jun 2026 00:10:34 GMT  
		Size: 95.5 MB (95507996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1084844b516e42f068eddf7b823e1a853c5c8c944125a3fae43f29e96dd0ef58`  
		Last Modified: Tue, 16 Jun 2026 00:10:23 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260613-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:61be201f4fb0a3fea89751a450b8a49dbbc58681248a2aa406acdb9ede15438d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35fd60e83e2a2b37401780a714e13cef33f93e9310d3d42979fd0c76c557396`

```dockerfile
```

-	Layers:
	-	`sha256:f83da85f58bfe9b3872b68328717b95eefb20d4b5046660a598c79cd3826d117`  
		Last Modified: Tue, 16 Jun 2026 00:10:23 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260613-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:ac15ae60b9b858d19cffba481eda63281892de1b3d1e9b69cf9df7e6e48f032d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336882277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d1f01967859af98ae2340e5b23f1af64634d7cb14cc629fbe251a938bb71bf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 04:43:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 10:26:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 12:51:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:35:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:35:08 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:35:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:35:08 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:35:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:35:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45654aeab75acaade8b0e13728139de28feb7f503c7e094076fcb9a6e4ed987e`  
		Last Modified: Thu, 11 Jun 2026 04:43:46 GMT  
		Size: 25.7 MB (25686794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b3af7c755dce470b1c44918153cc71bc2ea3bed1cbf9108bce1ad1d4579fb5`  
		Last Modified: Thu, 11 Jun 2026 10:27:04 GMT  
		Size: 69.9 MB (69853632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b4dd1efdd40c916f72d9997ac4a377751a99e14a9001e86722f39f10877da`  
		Last Modified: Thu, 11 Jun 2026 12:51:56 GMT  
		Size: 90.5 MB (90495547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89039b34d27b51562a15e0375b32ce61f3263152969c65f76567c3ed39aa8a9`  
		Last Modified: Mon, 15 Jun 2026 23:36:20 GMT  
		Size: 98.5 MB (98499477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca878ec77c20f872fba47e8c73d0470f18e7982b29fc2e6e6e075f2c5b2586`  
		Last Modified: Mon, 15 Jun 2026 23:36:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260613-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ed69e84a5e5bb76e6de2aa6df41dd9dde1d0b5a67aa130f290d180b842b48bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f575985d719478877c7c81a10b2f65f7df939bd7debd51d7f277ceea8ee3c2`

```dockerfile
```

-	Layers:
	-	`sha256:4ccb5ef0e70a83492c997de8240aead1471ec9b3c130aa2bcccac91b31e27750`  
		Last Modified: Mon, 15 Jun 2026 23:36:18 GMT  
		Size: 10.5 MB (10469558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17a07ceaf99d52a9184f429bf230a9aca6263ccb03a594587e44f4e785a3a901`  
		Last Modified: Mon, 15 Jun 2026 23:36:17 GMT  
		Size: 28.4 KB (28431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260613-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:9167866eeec117e00b7154ff6d21739559183ee058bbd451c08bfa5cef089481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304340326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f669f2283db144cbe0849952a0233f47122bda95c77a14c03c492befa077b606`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:24:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 23:24:06 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:24:06 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:24:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:24:06 GMT
COPY /target/ / # buildkit
# Mon, 15 Jun 2026 23:24:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Jun 2026 23:24:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0f0bf9684619796dace2f15b323a1fcec3fdfd4a5712e33f82ae28ed815bf`  
		Last Modified: Thu, 11 Jun 2026 01:43:58 GMT  
		Size: 24.0 MB (24038950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33cb3e3ab28182d2640ab8d60069099e6c4d1dd9ee3f806d20e366f1901797`  
		Last Modified: Thu, 11 Jun 2026 03:26:38 GMT  
		Size: 63.5 MB (63498201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd63bcef7a2a005c79bb533e5b0cb8ef95bff4e5327c05825fcbe1ece875e17e`  
		Last Modified: Mon, 15 Jun 2026 23:24:52 GMT  
		Size: 69.1 MB (69087760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0ac3a6fe312cf44641985605a72c55cfb44387624bfcf4ae9738ab565d3ad9`  
		Last Modified: Mon, 15 Jun 2026 23:24:39 GMT  
		Size: 100.6 MB (100553757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc404df8a5f023e8bbd790f1b654fa61dfd420240e2c6e8c838b955ff12b85c`  
		Last Modified: Mon, 15 Jun 2026 23:24:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260613-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7ac0af770e15345ab25fb16ae93271c13f7ab05909255f54c063554ee7304e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0429997dd678b3a048bd6be8dcb4f810b2ff79b5deaa9074d8ed0e2931faed7`

```dockerfile
```

-	Layers:
	-	`sha256:0d30409dda1e13abd6b03e2dd481193c87001c237b1a14935214355dd75525db`  
		Last Modified: Mon, 15 Jun 2026 23:24:51 GMT  
		Size: 10.3 MB (10329579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:784ff49223d88d30198801c247dc6360ac5e6ab6cfc04633c71471bbd718c6fb`  
		Last Modified: Mon, 15 Jun 2026 23:24:50 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json
