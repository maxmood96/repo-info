## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:5f0681666ccf763a91dbdcf213974b3f6916d59f21bcb4d9f85e56090aa7f268
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
$ docker pull neurodebian@sha256:53f8645f8bbf3bcdce3887a06d2aa2869341c28b2397f31a7471bf82786d0b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60207064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe24ebd4529e94cbf8859d1c21480465d735c0f9fad6e339b6709aca6ecff62`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
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
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507ba0d1af87c79eb5ed21e470daeb6651cd6fd35ac71c7f4316437bcf9838b`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 6.5 MB (6513412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea37e5d08e4432023f6c69cebd438dd20a209a3cd3b94eb789a8c4f80f5fb74`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7766e08b26d04d33fce1a14d04e2233cb4eb74cda5d72aaa29f51748001414e`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41352cbfcbfbb365bc31271939a7c8835966e68a87266f29c649ba4302e4f95`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 91.9 KB (91941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:91e12dc77cd69062c3a5fc7d25bca613c58b29f11cb31adef1fd79a935dfdc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c885ac5fdcd2a78cdb9066851152200accf3e10a11697fab5019a0fe07de241f`

```dockerfile
```

-	Layers:
	-	`sha256:147a5aa5deb953d5f8b7f4c13b3365171a7306962923d3fe3ee5a0bdbddd0129`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 3.5 MB (3539046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdbbd0c40a05bcb4a92f56dbda7232d95e7d4d3bd20dafc56a52e38ff5581810`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 13.6 KB (13601 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:16fd11b6cfdb9fa690598b6dae7f84931f21bf7666cde4285e93fb1a9eb35697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60824771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a2fbf3810c021671c9ae29eb911fd97e9c8a43986eeed40b0846901330c025`
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
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba5659d64325588b4a84d3c1b8c517318a047ef2e09978658a022f97d67f3b7`  
		Last Modified: Tue, 12 Nov 2024 02:15:16 GMT  
		Size: 6.6 MB (6635985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf8e3cf3654b722eeb19e2d68c89a05d0f97a1144fd06f65efea22e1f283ea3`  
		Last Modified: Tue, 12 Nov 2024 02:15:15 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f592776bdbe4553329727b8e38657f07591c55566c55cff9ff1ca0ebbdbf7e6e`  
		Last Modified: Tue, 12 Nov 2024 02:15:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c8ff2773363fcdca8df14781ca836f475929f2a2c5d159651acc6905cedfec`  
		Last Modified: Tue, 12 Nov 2024 02:15:16 GMT  
		Size: 91.6 KB (91641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e6b6eb09ec7e80f9d593216e59327ecf2d068b7b34ef798fcaf13768ba326984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033d4d50453458b36fbc73be878f522ef78525f73e6e13cceb51c69d8fd041d`

```dockerfile
```

-	Layers:
	-	`sha256:a311239e72e2d48545cb84e404204f7a4d243d35c055ee422cd0ee090b62d662`  
		Last Modified: Tue, 12 Nov 2024 02:15:16 GMT  
		Size: 3.6 MB (3565527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:791b8e79009489fb6f95b5fa305a489b6ee848a70702723036023b374e2378aa`  
		Last Modified: Tue, 12 Nov 2024 02:15:15 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.in-toto+json
