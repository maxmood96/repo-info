## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:9ef2b864e08a9fc59e03ce54521da82cdf329aeafcd4ff089ff08d763e27c722
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0f366899853a39f6d5bfefd3a1d87b9a6e77b0d1693f159852589bab14fa56de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124051506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03eddae311a28e3cdc3b1e06a73fec0df44fe8ffe18ec3cd0a6beaa3679a61`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb34ce34679cf6bc8738a0166300fb0af605abff20bb9c1c8008dbc48722061`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 54.8 MB (54753972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e95a5f98efdd6e08a12735a0fd6c4c5a3051965595a72f2c708ea4166ad4fd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7725686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d18063dd303c3df8c4bc0ba7ee19280ba8273ba222cdf8806418d7ae0614de0`

```dockerfile
```

-	Layers:
	-	`sha256:8f8714a5245415496d1184c9bf67324931b783e6e2576f6937a4fee947db486f`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.7 MB (7718333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea2d08ec39059b267a5fa537e634436554e564153de6341031fd87f0045d90b6`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:830b6954c70d048ff92b456e8ffe4dbcf182daca29b6b49bbbad09a984381271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115569782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caffbed5cce66c0c8982d81579513a17c884ca118b20af92b57ab9b49e776a51`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c18c6ef253e2b87a07739846b10eb333531241b80c23e3aec0643adc1b449e1a`  
		Last Modified: Tue, 12 Nov 2024 00:57:22 GMT  
		Size: 50.3 MB (50272340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b69db4cf1745187b07df647e4ed72539303d8747c006695c2bc15e5e1e185`  
		Last Modified: Tue, 12 Nov 2024 16:00:17 GMT  
		Size: 14.7 MB (14673306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b22721db94b1c5fff4e7c6f09aa650c06de76f3b42c9ec977d76b8bf11c268`  
		Last Modified: Wed, 13 Nov 2024 07:38:50 GMT  
		Size: 50.6 MB (50624136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b23e1865d916cdc8789829a0ee4c44af59b896f84418987afdef383043c7774f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7728947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22ce4c82e846985b53a61c5bf85aeb0485c78d1628b11dc2483be2c3c5f4439`

```dockerfile
```

-	Layers:
	-	`sha256:857879924c2b960fe7b46fc7a8050cc0041f2296d4f0c92eb836f4f1f9e277b3`  
		Last Modified: Wed, 13 Nov 2024 07:38:50 GMT  
		Size: 7.7 MB (7721534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc60bdeb8477a9b6c1efa83a7facc8d429596e00a4ee67eeb1dec64483bab87`  
		Last Modified: Wed, 13 Nov 2024 07:38:48 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fad764dca1afb9d5ed0c4a860ade11f9bf47e382ffef6c27585b54f76d1c1f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124142744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eebaef5f9ec18d565a0443d4a966e2bc5993c9b3c08fecbe3c128e5b11f2435`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e545ff305fe56558a94b064a901c16b373a3501daf5519f82ec19db6a3655`  
		Last Modified: Tue, 12 Nov 2024 11:16:34 GMT  
		Size: 15.5 MB (15543588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952be101e4ab063ff4eafa1d2809245e9ac9e713c342da9f201d2280d4a6c9b`  
		Last Modified: Wed, 13 Nov 2024 02:42:41 GMT  
		Size: 54.8 MB (54842084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ecf1d6096ee569b3305ca895d03f0cf4ed6853b5f2b012860cecd5f2ec9a0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7733308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa18e52374bf24b029c1eace5a916de6aca3fb9c70c7172d02810ab66ce5bbd`

```dockerfile
```

-	Layers:
	-	`sha256:6aad38936d8c50842283a826822caf2b85d3b0dd0cc9a1c657b1e75edcf44881`  
		Last Modified: Wed, 13 Nov 2024 02:42:39 GMT  
		Size: 7.7 MB (7725875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:224e45f9c93f64a7486b029f1a1a8f448f6aa6fb5143c96fabb7cc39e27208a5`  
		Last Modified: Wed, 13 Nov 2024 02:42:39 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eba00443a4dc065f45bcbede0181fa8dc5c28cbe1f55a18a9251feec5922c7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126765451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ac82b6418e195c7b206d1965a4d4632534d11a24c0e88216d341de0b6ae49a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac5b88f14d979c6f071eb85aa8a772f827338af23171657add5b5e4fc91e2e`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 16.1 MB (16062064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc99b34aeb38c1b23bfa1cbb2b4b9d6e5a643b78e7b238368942282890609c8`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 56.0 MB (56027112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2720d09566864abb3abb4f25253ebe3a61d88eb16747e675596008f1490ad5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58543cbb4d408bacf014776698e3640af6c46424a52d359af87b4aec6dc23232`

```dockerfile
```

-	Layers:
	-	`sha256:652571b4e42beeac87dbcf820f654e65b967d8c560bdc560c5df4ce567fbfef1`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 7.7 MB (7713821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d6dbfe0b90b6c9489145208f3876d82d9a5511a023b5420de9795b688a43e9`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json
