## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:73baaae66215cb3d0b66f0722e58500c55d4b8fdd89f654e6ec414a2ca5aeb79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3740f8d70dc59549d1fd176ba50ad31e0d2ae8eebbf59b82170b0c2f17cbd305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69553156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1d03355354b44f9e83292ec0fbcb51990641d14c462949f6f6e275ce8b0f96`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:37:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0ff4d4cf746a31c00387c43ae977fe8857c000814b13a0e845ac0ad9512cce`  
		Last Modified: Mon, 16 Mar 2026 22:37:31 GMT  
		Size: 15.8 MB (15790675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cd90b95e18d4e7c9911a8390977921b5ea40fd2c8efeab60c30a83d20ff1dd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3fd900bf9e1748553ca21def69610d86479809f9658b4b430792fba107ac4`

```dockerfile
```

-	Layers:
	-	`sha256:d80043c8dc53e5614526726dad11e03031540e8ec87ae8fb2d064e551076a1c9`  
		Last Modified: Mon, 16 Mar 2026 22:37:31 GMT  
		Size: 4.6 MB (4637519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47060af3d77d799bccdbf984f371f6be6a81aedc6f6c08dc3c4b026d0cb4580c`  
		Last Modified: Mon, 16 Mar 2026 22:37:30 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bbd5f6a57cbdbacbdc8d775677bae75a84860efab16e03f04645f5375b80b2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63952674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61a3bf0673893285e3ae1cfab0aca552e9eb956f01858efda03f9ed2777d285`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:02:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dada255a3ad6614e8b2a389545f0625a8ca4a68f069cd24789cbdcf7a89bee05`  
		Last Modified: Tue, 24 Feb 2026 18:42:25 GMT  
		Size: 49.0 MB (49047560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6350b59ed962425f695241e787bf8023af23ee4d06b078f82307ec998a697a`  
		Last Modified: Tue, 24 Feb 2026 20:02:14 GMT  
		Size: 14.9 MB (14905114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:794475307a915a157b32b19616e05272a82c4570f71d6ffa30ba284439bc714f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4647606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88dca60cc46e5720281b1fa8395c21fbd38a2e3f3ac8d4efbb16c031a89d1cf`

```dockerfile
```

-	Layers:
	-	`sha256:efe6e59f200c609424fecc39d03f802d509c154c6e5e14a318b3f279d2efc5fb`  
		Last Modified: Tue, 24 Feb 2026 20:02:14 GMT  
		Size: 4.6 MB (4640779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c09cd3ae87d03b8b439b57d67948984d367c9833d874d9c14aee707eb984a0ff`  
		Last Modified: Tue, 24 Feb 2026 20:02:14 GMT  
		Size: 6.8 KB (6827 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:503d6078db85c0ae55d210f009a0e925af83ebf4a5ef48920a40cb63980aa57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68022037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613f956c9f5f2cabe5c36c9d6173b87f0b0563d986e4f18f3f5c4ba11dbe59ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84fbb63fb33355ef8feb355101d06b509baa6abddd911e5e232c23e80b5d767`  
		Last Modified: Mon, 16 Mar 2026 22:39:50 GMT  
		Size: 15.8 MB (15774783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cafa29d79050daadac43b8e7398b805af1ee8a0f686287ac065ffe71cd6828ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec3a6fc9aca80cc32a0acc2f3975ac5c16aa8fd23e0504ce294157d4b2d3d5e`

```dockerfile
```

-	Layers:
	-	`sha256:1b77202bfffc04a34e027769d1496c9ade2ad951283d55a560b250733ef77f4f`  
		Last Modified: Mon, 16 Mar 2026 22:39:50 GMT  
		Size: 4.6 MB (4637133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64913a600699ed44decba36d8aad80484b054672b2d00ca6927ba2f4bc3485c7`  
		Last Modified: Mon, 16 Mar 2026 22:39:50 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2596b22ad7f742758ff4f06a53595d1521f3614bfe9e686712d2c99ffb864802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70997825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc60910a28aaa7c005b3d79dec95730c88f77766a8539e95111d8e4a94176c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:43:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ad236c87f3ff6b413233974bf5899e332a9ceee3a606736011b98ba6596c59ea`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 54.7 MB (54702245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acfe19e42191cd08e20b1140d1c12d03ada06096409a1802c622395bda4436f`  
		Last Modified: Mon, 16 Mar 2026 22:44:04 GMT  
		Size: 16.3 MB (16295580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:300ff43ddf90765593fc9aefbf4fef4efb7e589535f0c4990b1575f7fb1da4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4640764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd47fbb7dd46381e19aaf1c1382a66c74867c9a4d05fa2ed82820fcfc943e24`

```dockerfile
```

-	Layers:
	-	`sha256:f5312ab5486a7e034f09d451611de1e65c2a86fc5cfa5fc07a844bd603f39656`  
		Last Modified: Mon, 16 Mar 2026 22:44:04 GMT  
		Size: 4.6 MB (4634022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14158e2cb8fbcccabfcd98e01748e652a0ff831fb32822eddf2df64abd074a1d`  
		Last Modified: Mon, 16 Mar 2026 22:44:03 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
