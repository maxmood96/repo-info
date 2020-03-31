## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:77badbe2485926aed8aba5d548fffad0abb7d896bfdf19309aa6ad9dc0b3653f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:760dfa0949d136dd3d8ce38b851d7dbe1224e42a01bb9404d16b010ec2da4dab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70789709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22c72e270695960712b46c1bc16fbab3a8f9bd37a21743fed17b236451b2cd4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:09 GMT
ADD file:edfe2fd644e397f293f4634d48f0fbdadcbf9e5d3f226da6daa213811d4bfb90 in / 
# Tue, 31 Mar 2020 01:20:09 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:54:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:54:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ac0531d9afaea848836097ce37941ab7f0d2533a1b6c1cec0eefed4bb8d4d9cc`  
		Last Modified: Tue, 31 Mar 2020 01:25:55 GMT  
		Size: 51.9 MB (51922687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d3ba615f9226bd102b19db9df18370bdec917f3ea1a9f936592e6f52c8e445`  
		Last Modified: Tue, 31 Mar 2020 02:08:55 GMT  
		Size: 7.9 MB (7924126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565bca0dadc92e2cf00fe101b4193e199d780837062441b521c17415ea8f86df`  
		Last Modified: Tue, 31 Mar 2020 02:08:55 GMT  
		Size: 10.9 MB (10942896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d4b17f48c0c86359bc0e5b633ba19d6d4a3d2a35d68914a0158a8ec42e23112d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67331773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b631d46ff159e165daa0b3d743276c9e329adddfb8dac73716f01767e718adb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:46:25 GMT
ADD file:cd3f4cae9b31b83faef159941db546ad620281a9de9ad8b4c2e2230e329f629c in / 
# Wed, 26 Feb 2020 00:46:29 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:30:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:30:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b5f1b944f6f81b9832613484a0ab69b94fc4d7e69cec7cf9246276a84f198955`  
		Last Modified: Wed, 26 Feb 2020 00:58:09 GMT  
		Size: 49.9 MB (49859431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309dee70eab6e2c15144731cd3a34dc25e8045f43ccebd56bca46a938673eb9`  
		Last Modified: Wed, 26 Feb 2020 03:59:01 GMT  
		Size: 7.5 MB (7497952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebfbc2424c96e6f6b0bd4ccb126243789b984e1df82dfcc07372cbdd3c2ec46`  
		Last Modified: Wed, 26 Feb 2020 03:59:03 GMT  
		Size: 10.0 MB (9974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:93c2925c6cb8f7c58c2447f4684704fe094d27549ea7d975e0e1c425abcbc71e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64457440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d7acc7a1ac76cda28e524da9f79d3997a211f2a4e2811a15c44e5399766435`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:49:40 GMT
ADD file:516c2d0189c8132f97d954209787ec2c833e16a9d8a4056cc9ed22510c721b48 in / 
# Wed, 26 Feb 2020 00:49:43 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:07:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:07:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d46b4a12bd08cdd498cc190f7d350b7bfa151e105942f36a185990c238f53695`  
		Last Modified: Wed, 26 Feb 2020 01:06:24 GMT  
		Size: 47.6 MB (47581289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab620fe7c5ae5218251dd6127456072d85bebc5b47b3359937f36ce071d355df`  
		Last Modified: Wed, 26 Feb 2020 02:32:01 GMT  
		Size: 7.2 MB (7237740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba007f6e72abf7b8df1b3d1009db9b497e33953f02bd91c28566d6700b3e462`  
		Last Modified: Wed, 26 Feb 2020 02:32:01 GMT  
		Size: 9.6 MB (9638411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe352cabca4e55106c8d709e1c51dd2d81c826d00ab4ce1d36e8e311431668e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68858556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5744862282ca211f3e8d579b1e179b9eaeca0f103f3d93d752f7d763b7858711`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:45:20 GMT
ADD file:6771f02669c2a4d080cd86fa10f39851d26351e4a29f9ff3d63a76e1865f96ad in / 
# Wed, 26 Feb 2020 00:45:22 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:45:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:45:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f822750796cfd016baf6c8125f67a171683174c26da351c46b78a6cc9d234372`  
		Last Modified: Wed, 26 Feb 2020 00:55:10 GMT  
		Size: 50.8 MB (50808549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f2d34813aa8b1aea79c2e14a664c47e0950cb8413f1af463215020fbe6ad26`  
		Last Modified: Wed, 26 Feb 2020 04:03:59 GMT  
		Size: 7.8 MB (7797144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74820b1316f035b3f4e91222feb71d75980d5a8b243cd3ea1a4ef519acca4774`  
		Last Modified: Wed, 26 Feb 2020 04:04:00 GMT  
		Size: 10.3 MB (10252863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:de1471c713f1d5ae5408b31972d41e5e9202aaf5ac2e91a1c8d7a7a6d253ab69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72496965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d34d6313031595acccbf357525393006d8c2f1e6943370c64a6040ad966fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:38:46 GMT
ADD file:930e7a44cb4836bcd1f8f50505e46e4bf4fd398eaad8aaddac7c962b60ca7e44 in / 
# Tue, 31 Mar 2020 00:38:47 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:08:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:09:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3243f119e5f4c4b861f26f136c3e132ab2844145f46cb5d7b6cc9602b0086f3b`  
		Last Modified: Tue, 31 Mar 2020 00:44:42 GMT  
		Size: 53.1 MB (53061706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e2dd532613df680378f734636580b380c128d4698ca4b3fa4951dfe348eb9a`  
		Last Modified: Tue, 31 Mar 2020 01:27:42 GMT  
		Size: 8.1 MB (8100943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb8ef6d4279b94da7f069e17e431221e259d8eba9ab62fbab1fa2b13b383023`  
		Last Modified: Tue, 31 Mar 2020 01:27:42 GMT  
		Size: 11.3 MB (11334316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:689cf81c07f8daefa1bcc8040aed78a4a5441f0947fab031300d060086215fb7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74986853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a116ec8432551d31bbc1dee50a89056f0515c6e64f385f916eb6f6718087c467`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:27:16 GMT
ADD file:063d213502b9de933570a06d59fc9054327af22f028f43bf3dae3bb2337e65d3 in / 
# Wed, 26 Feb 2020 01:27:23 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 07:47:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 07:48:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:61866abd58bd3dfd0faa8b784006b357e3857249b9f14f991b94b177781a85f9`  
		Last Modified: Wed, 26 Feb 2020 01:45:39 GMT  
		Size: 55.7 MB (55696604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd4cf9557698766807ea94c033185ed83b6e04370a7816433b533ec6cb1e8c0`  
		Last Modified: Wed, 26 Feb 2020 08:45:46 GMT  
		Size: 8.4 MB (8354351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e797f591ebbce205ef19692c7c30651291d5798b87929267ac7cc8d78cefea8`  
		Last Modified: Wed, 26 Feb 2020 08:45:47 GMT  
		Size: 10.9 MB (10935898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:33d2a82018257e9e54e3977cc9d947d67872aac2b6f4b9ab54aac312e28e0cc2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68934499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109517adb8f09043e5d6b50a6154e0f0d2ca46587de9a17fb37bbabafd76be2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:08:23 GMT
ADD file:c425c02ec78c0d94b688067a35be5c57d71687cb603f9103c3c0736e2a469360 in / 
# Tue, 31 Mar 2020 01:08:25 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:18:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:18:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2c5824ffa7966a2d6d1b45b6cc8e3e0e844fd262d0efcd2ef5cf9a9277f65e8a`  
		Last Modified: Tue, 31 Mar 2020 01:12:00 GMT  
		Size: 50.5 MB (50522622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bbb2d8d7f0af1e7df5d27f860da9f4382c1c7710f9ae98e792a380cd0cb851`  
		Last Modified: Tue, 31 Mar 2020 02:27:44 GMT  
		Size: 7.6 MB (7591237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3b77d0e2a2b6911e2c546d532b0577fee7321c1bc99cd6a728b04571edcedb`  
		Last Modified: Tue, 31 Mar 2020 02:27:49 GMT  
		Size: 10.8 MB (10820640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
