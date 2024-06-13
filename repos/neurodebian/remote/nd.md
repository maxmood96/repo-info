## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:9942b0be46ba7acdec4252ef4f2312bc46ab6e7896200dee34506bd8c564e91d
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
$ docker pull neurodebian@sha256:8bb8a0a0b4172cc81e0fe271f7df5b9c1dff063cf2ba032e7ebcda3ff26dbe1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58743190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f2f07387e58e5da280ec0e304c87411507dbdd8d69c8a9237af8ba7065e245`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:06cf5b56eee98058acc2138b22939b094380deece3b7569cb8f72001a1b1ae81 in / 
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
	-	`sha256:5d01f86c265bdcd9ad24686bfb950b1af7886771bc1e983efedb66d6751451de`  
		Last Modified: Thu, 13 Jun 2024 01:28:09 GMT  
		Size: 52.4 MB (52429606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38311220b3b8476e69a4f621275c847b8b91e37268e1e3bf5af6e6dde5eabe5c`  
		Last Modified: Thu, 13 Jun 2024 18:29:07 GMT  
		Size: 6.2 MB (6222030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c73903f72f1ddbe009d17d68c3539cde81d8f0e1af16d8e53f5548b887f1b`  
		Last Modified: Thu, 13 Jun 2024 18:29:07 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba14c6e0ea14c75fe096c6a31f4e1258120e2f9ed3b24a92f8a283e371c94c9`  
		Last Modified: Thu, 13 Jun 2024 18:29:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f02e2820af45511998f1e2e42989079169f600d531590a87a0db1976a344b77`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 89.6 KB (89572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dde06d6834cf707d3dfdd193d861a1a4ec4c2690566ea5b94ed6ba3b98770184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec79f8c866c792cf830b6b1f936c589918efa9b00436fb634cf90f69801733`

```dockerfile
```

-	Layers:
	-	`sha256:c72dfc3a094ce0750956c2220c56f25d69fafe170599ae6612ecacea118f5783`  
		Last Modified: Thu, 13 Jun 2024 18:29:07 GMT  
		Size: 3.6 MB (3550014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68be5481e6113d87d34667a9273bccc36f157f8b2e62f6f027c8e8aeec85d126`  
		Last Modified: Thu, 13 Jun 2024 18:29:07 GMT  
		Size: 13.4 KB (13397 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:060a7c0436faa46bd6a80640e5efe27a2fba2e87a2ec14ae3a194cbd1732a7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58995087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d18c8ee4cc0fb6be602a515ae042e3a1c2e7fce195d4e9b83fba82b2567a2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
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
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012a9a0c6fc8e14dbae0dd211be74c76a40a0bdfe55e8fd25532fadc68dea49`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 6.2 MB (6219805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46829409c0895984dd0c82567ac3a739a6cf8e121453008052b2e558d75b2ab`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08328daef7cdf76f8df8778afcbc4c476fef35cd256705e6c768b9ce1033d6a5`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99980679ea6d0b863dc5d985d23bdce3df45e1f095ca22b3c2e45a70dbb5f47`  
		Last Modified: Thu, 13 Jun 2024 19:37:59 GMT  
		Size: 90.2 KB (90185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:43567836c2e3fbc3f88e6d669ec9fcea09c616929c8018cff46dc4cbb32ed3f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e656634f06db58f4ab04ef76d28bf2f9517e69b79fb6ed19dd970a964fe874`

```dockerfile
```

-	Layers:
	-	`sha256:0164ea5dfd6dc1d678da7b7547f4446613a7ee6e16627e3d591bfb6e89dc4ac1`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 3.6 MB (3551055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:078bd79380d023fc171fed9f97da85cf20d466f502004ad09885da2e0a4b9eb8`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 13.7 KB (13672 bytes)  
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
