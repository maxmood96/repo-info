## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:574f90b63ebb78d8c923a124407fb1573530cdbab67b46ed5a92a4a3372ad22b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:2232750107c8bfc49bb93193550714a803da33eda58209d85a420673ac1c78f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66317020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48506232fa8180d8ecafd8f9ef54758c61b7ec5e58c2c808a3197123928de3df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfa11ef8c4aa3ade3aebc334b60d4d70e47c5dfb4df8cb3bb69af638f1012ed`  
		Last Modified: Tue, 12 Nov 2024 02:14:24 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e446eb6fa386c8e7218c2736b31102cbbed336088e6e52bb23b8ccbb00882`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c1a5b6fc7731b200d91a9a3531098229dae00f840ba97fd9e461511fe7fdff`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4fd44ed3bd40f10613a235d854263aad592ddd89228aa50676eb400c5d3f5a`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 101.2 KB (101189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:13746c2aaa1494df83c9e70f7025af1d4e73cc7d12b41a0b64902d09bfaa9b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251fab2583de867838dabca119850e404fb6efcc5be78496bacf71f1d8dee8a`

```dockerfile
```

-	Layers:
	-	`sha256:4bb29fc5223c99961577083a12229edba4481bf7d5e9c8dd566141f0793f7db0`  
		Last Modified: Tue, 12 Nov 2024 02:14:24 GMT  
		Size: 4.2 MB (4238918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14f66a1d7edddb9f5b9c6e38d917e7a9f4f903085ea5aabe3251890a5ebd252`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 13.7 KB (13692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8816f2a11a9a24a5ceb557b7510ac1f52e4380a0d1315fc114bccd78573753de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64943846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a779fc63603b730c637b15731a1e50df693e12e5b5dd77efe660f19eccbbff54`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa186315adacfb2b622451de8307f55c83bf74e5926cf7a13b2237e95e062145`  
		Last Modified: Thu, 17 Oct 2024 13:29:04 GMT  
		Size: 11.1 MB (11105848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3aef7bb5d567bc9ddb61f3ff5d2dea7cc2918d39c69a5122c9002662c4b91f`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb3afca1c9a390e8851a572c7497b59366792c63250de9dece52aaad7385c8e`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74a69755a92c3826c34c23ebbacc2bafd74218d37c26d56b22f2f565ea404a5`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60968a51d2dbbe8ddfd18d2179d21308e651bde252f4a4bcfb6b65b6876e1f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0e8d67435179a92167b9d4b586b64fab1c482c2a0e3cb6cf19b7a270df14d5`

```dockerfile
```

-	Layers:
	-	`sha256:1d5c77c580ab63b8233a862bf49c9e9fb9dbd695cce715b655519a0ae019c34e`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 4.2 MB (4223448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc7d369f1baadc307fa80e7fcd2482b6a6da3375ebbbbd347d5ca5692879ce8`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 13.6 KB (13635 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:f609c274c2618998d24c52a6df0441f5df0032e90e3f1a63b95b37ca6484704c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67697112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b76e2f6a3b11a04443a3080caae4e2c101b66dd1c25c336121874acfefabb07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d073a1c601e48b16b6148c0f2b74b5addc1206092570714a5dc88b69e85c8511`  
		Last Modified: Tue, 12 Nov 2024 02:14:17 GMT  
		Size: 11.5 MB (11500364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1586fd7ccc89fe18e9b4f40b0b184b6ef9d9769d8bb35dd6ae4f5f7a8eddaef9`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f8fe0c7aedc2a709542bc16b130dacdcaba65a2a616ff1c1d36dabde3ec385`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331f23be06d960a18a04fb88ca8d5843394679c00ae5ddb89c916f593605fbf2`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 101.1 KB (101080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a70195da17d31b1ab2a452e2cdd149967b05b10539b68e17dfc5075f59572da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e9e768b155ef0d4ea448b5e5cc7a300921fe2ed660e78c818d1d8d6a9447a6`

```dockerfile
```

-	Layers:
	-	`sha256:e0be0e44bd613d4907a7a5e80e795b4892345264f77ee55efba29073fd90ff16`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 4.2 MB (4235378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:901e1ce288d57a3a9099616eabda5520b086aae1e6d09cc03c1c0f3c2234ffac`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 13.7 KB (13664 bytes)  
		MIME: application/vnd.in-toto+json
