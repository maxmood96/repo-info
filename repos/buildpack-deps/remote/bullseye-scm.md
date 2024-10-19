## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:ad35936e397b04c08fcb29f626ac9f199e513cb959a67d111a4060980c58e024
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f0485e10500024df9431d8de6763bdc6da543ca6ab1e5ab2057b421dcb7edaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125568212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51724573712708db097ecd36d4692d52fe503b6a5e588fa6d2f92d57448b75`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86518255b538a594e8e2238131f87aa1d67981e1263e4c18db09e788a30e0211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7727453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8114d198645a070bb880f41004b7e18eb9b532cd04d152554c2198c33bedad58`

```dockerfile
```

-	Layers:
	-	`sha256:8119449007c140ad3218cd87f4c75621c38e919438ce0347d51fa76951bc74ed`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.7 MB (7720100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a0a9c5343eacf41f82ce1d610c6b28aacd5cce7e62805b6bfc9ab1dbb20dac`  
		Last Modified: Sat, 19 Oct 2024 02:06:21 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0b27afdfd77d75f7daa15242cc63d12c81c15bef9bfdf3389220b78e4b71c5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115732934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fea1c1109f52736fe3129fe2d91df3883572414c5c1c122f693e794c1cca2a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d17122d5550612fcfb8bdb86e3884095b4bb789a98d27dec66b7b6363b515ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7728923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a8a3069eb6e9c82d3c4c18ddb245fd1e026f21f27ffd7382878abd6e0251e7`

```dockerfile
```

-	Layers:
	-	`sha256:6875125c6a3662c299a57970ecff8767213464540a3f4b2443f46582d4b59612`  
		Last Modified: Sat, 19 Oct 2024 06:37:58 GMT  
		Size: 7.7 MB (7721498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c133ef3869a8610514a32152844f53057e7d5043e5788c21cc57d2487ebb1a5`  
		Last Modified: Sat, 19 Oct 2024 06:37:57 GMT  
		Size: 7.4 KB (7425 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:663f17b029a1bf24ca58f209ff1577c2d1b9a7aed2ecadbfc6ba889c327a0382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124315342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2754992e17ca3179605d3f122e480a5b71db85b29892344fbaadb8f3fd43c5e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1965623055033a3db2cd3d6d55f03b896eeeca6c187d658624bfdb8ad6528736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7733284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6670f84a12848f56394136665a519aceecb0d2286466693304dc42e0605ca50a`

```dockerfile
```

-	Layers:
	-	`sha256:e2d1f70c81ca0b6cd23296d317fd5165b255a7e0a1572a49f179932ebb08e535`  
		Last Modified: Sat, 19 Oct 2024 05:18:17 GMT  
		Size: 7.7 MB (7725839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b826fcef0fc38aaa49e948810018ef936f777127503a8a92bbbab59aabd9f1c5`  
		Last Modified: Sat, 19 Oct 2024 05:18:17 GMT  
		Size: 7.4 KB (7445 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9890d2391771767d200b4cbf59d19803dc7325c67a668de520340c3585253ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128372778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfabefc5f8a6f86a4c1d0830952a6542af51cac814b2efcfecc61b068b812e6e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988574216ea21c2f3663e265b982dbde4c9e93258b6bcc9fd4ea3e5ab1c0326`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 16.3 MB (16266312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaed38ae0fbef304c5263999f070de89cac39bc284c57eb71df4b52535defd79`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 56.0 MB (56028643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97f2982c47b11589dc67c23f4654b6f5ade92e8c507c09443e2500ca71371690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7722919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8bc9ab9f9ff20301bfe16816c4cefce0e403721ff906a1f90392f09c200edc`

```dockerfile
```

-	Layers:
	-	`sha256:fe45d08f635e7da0980c4e3a17abd1d69bd81cad7123343b7c0a8bedfdacd121`  
		Last Modified: Sat, 19 Oct 2024 02:06:28 GMT  
		Size: 7.7 MB (7715588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc67396d6c2b39edc8f2c0e27392aabce73e953884562fb7a86e6187cfa784d`  
		Last Modified: Sat, 19 Oct 2024 02:06:27 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json
