## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:a42dfc3d51e442c3d9fbc9c24dbdc249908c7980ff82b326630e95261c49790e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:8c3d230da8412b55cbee364317a8731d25e763564e2b2be38227e36ab80f49b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66306966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b881ddb514a2c7e1be392d905f42277af7984786725250da09db422ca1dfcc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd2861cdf3fc21028b7711eeedfcbeca628a8fb7159acd01e5c714f9907f064`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 11.1 MB (11104983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f98edc86906c07c1cb7a049c416ac566310472faa84b7b12f4d7d80ce54180b`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd682b5f33a07d103c949299d4f7e391de2f1bbb31ec6cb40ac5e8b2b19417d`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861d284c071dde113b3c3bc5ebe3c17fbe19cfabaf785d6bba6baa1e0097cd12`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 100.8 KB (100803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f11568303fb84dc415fd2e336f2167108e7a516a5a11bd8f8a33ca178d3420b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b3c28b046c4ec02fa646eed9679953ae9da8e04a1d11f06b47dc0da095df6c`

```dockerfile
```

-	Layers:
	-	`sha256:8b509ec6faf6155da5f86947e6633d93b4ae43fb46ba472379ccc5f68df4b6b5`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 4.2 MB (4199042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d37245439748c860222eb66e886e381eafd4d896d2efd018d844d79cdf4e4b`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 13.8 KB (13786 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6375cf81339b4fe8833e60dd040bba97488912c84f70a27969bf2c02cb91eb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64948102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cccd4fdc6edb0a9eb9ba879aed966c878fa3c91107b142797379907bc3544c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ef66b54f3529cd7df198490a60a02b9a4e099ea4456cbc230affa6271d7be`  
		Last Modified: Thu, 13 Jun 2024 19:36:08 GMT  
		Size: 11.1 MB (11105804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf9da50bd694d2938f66745014033d7f272e00c04af58b00384767df0a68779`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d1d085e2488d140f07257a03441112598facbad0671d3f6d3aca4474943da`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6ba47d152985a5fc3c5a383c539496f19f49199c0ba685819566962b387f7`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 100.7 KB (100727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1c099f797210a667e7d6cad5d156c3d71f62da503f81a223646bcdd633e96a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8dc943f053d5cd12505c6b7e69aaee75831d571e6af2c7e94d81ad4f930220`

```dockerfile
```

-	Layers:
	-	`sha256:a87d80d664052af77129cd34468764c3ca1b059b7b914aa236360b86b3b423f3`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 4.2 MB (4198659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e892dffc23567a9acb656fd89cad3615575761a771ef3db6d1c63b06192d2edb`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 14.1 KB (14078 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:cabcf9350018fb62481d82da2d505e7435e413b523ffebfcc9b7d080ca3248d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88df1df83a11719da37c9375a2ec92d392548f66178495fbaa15ac872d52ce6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36508bc53306c02a9ef12049a2feecd1ebe42c6a54a9832472dc4a2dcf9f2c08`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 11.5 MB (11500070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650c52e044f44142bd08d3c99a7d5bb60aece0e021e835404c71f0536348cac7`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a9f7821bb8e6b0e0776e2b828f75a95c812314e6cb6a1c256c944d6ce720bd`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8868307403b220244baee51b838b348d00e384e65031382e9c786b28a9ec9f`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 100.6 KB (100649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea9a8508876015fc24d1696a07b00dee5dd053bf937c9f4480fd9c8c2b61ec11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b9051a1b5507153426df6c9faf52f91ef695a1e2b336bd9ba344c819261aae`

```dockerfile
```

-	Layers:
	-	`sha256:920dffb7e2a35971c60e1b62223af049b0b7015216e62ffd5b83c0c380c72d06`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 4.2 MB (4195497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082631cbc44059d106b213d5b38760209d1d120834d9b001cdb35972f003c889`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json
