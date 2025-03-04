## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:ef73f4fd3736d84d8a184190bf9dd142ce914f4ba507a84a2648c1213696b7ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:acdba3e831fc0238f8615330459e4c8d23abe10ed55d5e23eb088251dac092bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64950196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0185abc5a5871af8006a05bf12e7800e67b96928bb2166b9053168b1de047a9a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffa168550a2cf7935e97231a2e441786f9bf876d0ed0fa5a8920841a0051253`  
		Last Modified: Tue, 04 Mar 2025 00:29:22 GMT  
		Size: 11.1 MB (11105051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc86d74781e58e9ada644877d2d2a2543898cdd098510b5784900b69194ae0`  
		Last Modified: Tue, 04 Mar 2025 00:29:22 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30e07a60a9d97189bfa1e3da2af05d52bb24d5e480a4a2394299c401beb633`  
		Last Modified: Tue, 04 Mar 2025 00:29:22 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05950d8fdf631b0de42c380f97a67bb74b9ba7d305538c6905d1ec2ac1d384c`  
		Last Modified: Tue, 04 Mar 2025 00:29:22 GMT  
		Size: 101.2 KB (101200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af26fd51fcd50e7bbfa997d46fbef7f595a0d0382687900f074c58884c578d`  
		Last Modified: Tue, 04 Mar 2025 00:29:22 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d85ba2af02abf4c61bf41234a915e0bffdf1befbef6ec76ef8a2b6e175ca1274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf86b7dc928424b254d468bef2d4488799f52b01cb06861aeac1226e9012f0f`

```dockerfile
```

-	Layers:
	-	`sha256:668357e64cfc265e06c397cf0d420cea57421c5cf7762681489ba0cd2e1a3497`  
		Last Modified: Tue, 04 Mar 2025 00:29:22 GMT  
		Size: 4.2 MB (4232832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d224e15dd331cab1c598e32f26d6568715a84dce2e23f18249bdc3bc50d851e`  
		Last Modified: Tue, 04 Mar 2025 00:29:22 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cef7758fdde9c68b1d750d5e72425dd9d92f477afa18e03703f75c20abd07043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3210c9b7d9d952da15af4bb9f2ac0cbd29d527aaa048d8203d9f20d7ea0992`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590f683099269b4e113e7ddfbbb01c0454829f5afb23e0c9ea423e20d2adf1bd`  
		Last Modified: Tue, 04 Mar 2025 00:36:07 GMT  
		Size: 11.1 MB (11106153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbca52b2ca49d721bbab5968bdca318fe2c5eb2e3afac103ac1ce7f3fadc610`  
		Last Modified: Tue, 04 Mar 2025 00:36:06 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1847f07697239223f4d89a58db0f9846c05f71c338e388a216a86ef561debf`  
		Last Modified: Tue, 04 Mar 2025 00:36:06 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575eca85e5253082cf8bfd49ce1c67b0b7e55719162a8e8220340784441b412`  
		Last Modified: Tue, 04 Mar 2025 00:36:06 GMT  
		Size: 101.1 KB (101135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce114d93cd2d1a276ec623f5e916be45d9db81cc8409c5f8a70d238660cca1d9`  
		Last Modified: Tue, 04 Mar 2025 00:36:07 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:06007c0693b5fdf4e69f9dcbeefa55e47abbea0f2d895740c3db69af8a6fa404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809e9497f7efc484f9d306249099ed6408cdc69d8541794779b616469b21b3a8`

```dockerfile
```

-	Layers:
	-	`sha256:2b5fe320bf5afebe6fe1f0e15ef4eefc101ccc0ae86d796b4459fa785fe29efd`  
		Last Modified: Tue, 04 Mar 2025 00:36:07 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55590fa267c9985787c77d2d0e6813adf0be32a293dbf3a5544d61badaea7ab`  
		Last Modified: Tue, 04 Mar 2025 00:36:06 GMT  
		Size: 16.2 KB (16176 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fef5a9a1326cc345f582541fb8d5345e397af162892634df4b7b229b2f952b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d179f2f048969753c039a54943b7c8419e1a1bc0fc262734238f81f71307808d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bff203b323c74838d7a1b8e2da8dc72f86f37728a5dc6a75862e14c492e27d0`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 11.5 MB (11500435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1d07b9fa521515d73bd0c7d455e510f60ea81333965461426bfc66d33baf2d`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cea4ff7b6be550af04767de051ec040c989aafc51b2f1b6e4aab6f2d85ccde9`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2217ef0228a520cc7b8e03470c9a7e0a9d37aa37b888970bcad09b009aafe606`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 101.1 KB (101077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d5ee3d0c51a6087577bd4e5930b09cda7acda32173e6a4e94a6d54223c2692`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bd99a38af651344e2350dfbe1688045072f3685a34fdda646542fc982749b6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a91b375f5b25a31a8ff62cd0ba7c48cdcbc45d48384af0d7cc53742d1699d5`

```dockerfile
```

-	Layers:
	-	`sha256:988b46603ed9dff294b51d2a266baedfd17b3a53d2bc13c0512aa9366a0f4d46`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 4.2 MB (4229294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd66fc9bc271c851b81807f47be7ae280fe243c058e805816175735276aaa2f8`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json
