## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:fc4335fbf99cbbf1fbbaf8cb1241ff9d6144298ef1466422f14d843e68dc300e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:a7dec9889aa07f211ad822ba89bad5b6ce8709fb2662aab7acaeb9422f9cf4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118921d922eab791c13d7d4f706358625613c0466bb3ea1f9342a63c16c6df94`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f55ef76d9b4b35f21ab8fec574f6f36f7bd50def9bddc39211c4be1ecf5dcc`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 6.5 MB (6527854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e21780aeb7064d26fa740f8a4b9a09dfe743321ed8ccead5081f20808968b7`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3c1c54dc72253d17aa3a0747904e2f2cbeebe5381d98a4869ebfca8aad329c`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a759645cedce06316e780c1a68071850fdfad6eb284b6a5f289626fc23f9625`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 91.3 KB (91267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:924bb02286a421040b58de5bf703e0deac8f6386582a411747821f339ea70ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6625a391e9fbe8e0454e97d817ba5eac680a9cfe1a9d273a8f79ea499c655425`

```dockerfile
```

-	Layers:
	-	`sha256:ae98b6ac0554424512ec6baa4c19e7137ad6d019c0247b15234f27ba24fa55f3`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 3.5 MB (3538004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d175b07b1e4afad7f0cf9b37637c3cba14123dd767f1b33295271b7ef9010a6`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 13.5 KB (13483 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e045c8722a0d09fb924908b53557b97d64b916b1e5f7034d0d5f9fae67d5424a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59971880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00daadd7fcf3264abc9af0febccd9a59cf1e87e61f9c621afb2b7d106794a72`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23f6352824fd96c8c6b9838bfb904e1d7622f6bfe55b4c553cbf57ff483a36`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 6.3 MB (6261488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c0a4b3a15644d2d672fb44fb7ef754851b4b999ae2449d908d2bcb61514ef9`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620d3e5d3b378b7be79ad19c20bfcdc40531f8bf0971a901824a5e8be8263f1`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dce128f9ff7538248e2b5e2edcd6ca43e5feea1880d5b8a5290a08534c4e63`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 91.8 KB (91807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2a4489f748889ef85e038e010495eefa34e6dca07c0894d71860b17f81eb310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626360cf88fe014495b6a029a63b3915e45368305e7c9a89bb1cb126907c91e9`

```dockerfile
```

-	Layers:
	-	`sha256:542bbb008b88b55265ccbbf2227938f846127e85ae4c7737802a2427e4e3107e`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 3.5 MB (3543899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2b4a94f394589d2ff4a612422d51f4eb84d2ddbc340e5d3f3f6fe458774f1c`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:d2802c35bb0627592501ffc30f3df2daefbca9977542caff088c4f35229cab73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61045656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca83b56f3706b8d2edec74ddd0f12387138a0707a310844b3eb8da6b7fce1be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0104c3b9cfda50cdf3421866fc7eb610b28473908b8759e1240cb0d8ad183bc8`  
		Last Modified: Thu, 17 Oct 2024 01:14:33 GMT  
		Size: 6.9 MB (6875022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd9262fa2e041d173fd0c1c2e00f777d7a35128a6cfb880ba548f143f446f5`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d133c2bece8359e935db3b2875d562f307c53ceecbb48708378a24ef45b04c5`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46ff097c43ae4bf706c02448e2466bd9b8c5b37f55b1685a84e9ce94419bd80`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 91.2 KB (91193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9f1a937c597b21d6d3dcc90d05769817755c541905d0d7cd7abc73c2a3826d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b107b9695539bdcefef4858e73a9d9eaa93d90271cc4df926ae48ebaaa418605`

```dockerfile
```

-	Layers:
	-	`sha256:6af125565215ecef3d415be15edd88929016e26097df809146fee17a2974dce8`  
		Last Modified: Thu, 17 Oct 2024 01:14:33 GMT  
		Size: 3.5 MB (3535101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87d62435b91d7d078a1c9c759e6cc4625563ddd2f8d8070cdfd20a5465afaa05`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 13.5 KB (13457 bytes)  
		MIME: application/vnd.in-toto+json
