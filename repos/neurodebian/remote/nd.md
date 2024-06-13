## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:7b10171b71a341f81d2db6867a5d45c17232a457064c0762e7aebdda3b94ad2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:9d6b76d38812539161f59c893466f5b49a8fd9591f8d2f2a01015142b1b7b216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60049164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9e6ae8e755fa691be543e87a19ceaaf5730a42a8b17045af0d7844f85e3ea4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b719a38bf4aed68db29b56d561e793f8400c5edee1406cefdc25ea0c72ae7`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 7.3 MB (7313247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a778cadd45e115aab99728a495443d9a0e22db2b4cac341924a9d85071fb5`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73059de92601721fef9ac2c3019771fb96130f0ef7280cc538253280cdf1ba92`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c97c37c295b1b834c6ff803661093e3f42e5e01f6c8a476778c58cfb56657`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 91.0 KB (91039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:388a04f898471e845839e7d41f20795d49ce13fa7087377c1fcd80379d946168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de95620c07d5b4bd87bc12d9b2921d0d89a03b37227a84549003b96bd538f2c2`

```dockerfile
```

-	Layers:
	-	`sha256:a4daf7efa1f24d0026d214c5a47303591dc8a26d4667e0022b33447e0bcbb444`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 3.6 MB (3592159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca62554e92aa67d490ef6f1f7c63bcff795065618587426f22dc4754279c1ab`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 13.3 KB (13348 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0bc06edf842750d1b8f488ba4dd6ce12a30c56db39f5770556bd2ef64474a267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60321222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6326bfb52a658f0caa666254da500a6cadce9719e0c53ec40a929200564b0269`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bdbf9908e45530061175939d20c6ded00e858fc7838427d8713e0ed59e84ea`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 7.3 MB (7297335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0922009db60c6f3c98281eecdef09a0c5ca68b58d2bf585b8ebbef25c57d30f`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26863f97217b3df00be0b9bbb64308b763fe60c3bcf24a1cfc8c16428395f03c`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bb75772d75f5c87c177220dd50d76572d354d75f97b9186a272610c1c9fa27`  
		Last Modified: Fri, 31 May 2024 14:45:21 GMT  
		Size: 91.6 KB (91620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bf6cd02827b2dd05aeb0613d98a66272fc567af92724bfccd95a38c27cf27ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cac57f1a7aa1101336c904343c777b772e3e3c16c662ea2deb1242cf1fded1`

```dockerfile
```

-	Layers:
	-	`sha256:1acaf9ef26e92ee887ebe48465d6d949355c6b19ad6a9c7529d7e63625abc3f8`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 3.6 MB (3593200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ea3f17838a54ab388d0a3af2242e54f2977a570e2fb3d32eaa408a183491f2`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 13.6 KB (13623 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:97b5f62de5f63780c6fb60c18fac80a4ae8cbcf56397376e609f8a665bd42094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59947484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df55d8fa11cb174de39000a2295c9dbf246bdfe3cb88605507a5506f7f2c7c05`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c7b81abba8966f408c068710549216ceee2b9d423c6a9411b04994eea156d6`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 6.6 MB (6551754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d3739f5e8659580229543579dfafaa8a624b3f230cc3c918f717afff60b7fe`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62789b7063d2d62b9591fffcf6f696ee77c7bde371b15b61b45647cc1c4139ec`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f020a648d73b4c99abcc87718351afc13962b285a67fb1149a89fbdd5789e6cd`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 89.5 KB (89451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c3a877c1de721606d524b8aaafcbee6ddbc5e18809486d6563c15c9eba88b2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaf78d03b9d7b700c0ec38992b872c759e77ea48b08ad2e0688433a71435d0e`

```dockerfile
```

-	Layers:
	-	`sha256:8e15cf37b593768d02d1e5e5ae9e91ac87a51f539dae42d421dcaf98d639257f`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 3.5 MB (3547113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29033c721523198453ef2a66dea5e3d3d2b8efe44b0c1bc7ea31d1db80dffb0c`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json
