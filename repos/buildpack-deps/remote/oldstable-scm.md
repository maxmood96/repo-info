## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:d77a9a973f990a72e69204034d469ac3458f538c6bff02e8637f462025a8716e
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
$ docker pull buildpack-deps@sha256:ae9d9a071680ba3f4e8704f7797b3175fc260ee61177cc0584ce87de5426b359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124050958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108460fb893b506aee282d2e6fd521f67b030d044891f5eb6608e4505274bb63`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a0087ac5134123a5755cf1e611d454534c26d00fa8ba59463ad950ff7f781e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7715521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca30d201a63b4b9a2c8463c3af57a9af246d907074c4d12fcc71b678d1f8932`

```dockerfile
```

-	Layers:
	-	`sha256:967671d628ba5bbf4651dd8b8abf4e75bf832de3e33843b858765ff8dd0a474d`  
		Last Modified: Tue, 24 Dec 2024 23:16:04 GMT  
		Size: 7.7 MB (7708168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ea595a1268aa48d8479e892289be7dcf176d5af49a3311cc009bd517788490`  
		Last Modified: Tue, 24 Dec 2024 23:16:04 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:853932c378a68af781dfdb021b52471f8914959a043786d24fc427efb6ae69f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114339418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5d55fccd8bf93800b6e93de3924291352f03f28fe678734f75cb1a8fa7310a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:72a97ef17ea3ebee745e94ed10c064dff1f1f0ec1143c1066018ba1749c3e817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7716983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a36a04e3d1d5baac086362bdf876b17248f9fdc56b7caaa6a2257c299bef84d`

```dockerfile
```

-	Layers:
	-	`sha256:2cb9990835f0268a8419d8f0a0cafdce65638b1652c4067d6905f7a6cdf68a98`  
		Last Modified: Wed, 25 Dec 2024 13:01:47 GMT  
		Size: 7.7 MB (7709570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e83d0bd1598a3ccaf5d7857eb274807031f0005e64557af848e2b4810e16f97`  
		Last Modified: Wed, 25 Dec 2024 13:01:47 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ec7c9ac2ec70c27988bfed035c652126250238887cb5c0e8b1aeb9ef244425c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6794c41d93708d23010012d5e58a21ed2434c5c5daaaa3794a8d13449c410deb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28ae3ac11948f19b0d11359fde9772b326c4e1576181a79517d4b9e3791a7223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088488a71d48e9f33676b5c7908ccf30e2f7e937c594c355b5aba8044a10a15b`

```dockerfile
```

-	Layers:
	-	`sha256:16b3fc45dc06e3d8556aeba92e04bdba6589a0a93c9d7eb5199f2e95226b8498`  
		Last Modified: Wed, 25 Dec 2024 08:12:34 GMT  
		Size: 7.7 MB (7713902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a303f3cd20a4c4f48957b3ebc93d927c4ea1f0ec43af82c8f73a8e9b113f6a`  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b8f9d3783fe09d1fb009a7b526bdca58dc4a68af37c4abf182d234c01d57991e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126765073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2013b78e6793b756041c83ea7c42a21f7efd39e4dbf42e88276e7e04390f9979`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30483a4cb9e6228b018657587065a3e6487de3276661a2330332744722b7a439`  
		Last Modified: Tue, 24 Dec 2024 22:14:51 GMT  
		Size: 16.1 MB (16061993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a970a4937f3da89cf59e0bd2ab38633517b173866fbf02a490f384820768c5d`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 56.0 MB (56027064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5ff919b07dd9858aaa747f0bda352007544145964ce9ba3f015ea2149f9bf12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7710989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf55cd4504dc3f47ad9e845ae648d8737399d47fd1fb8a1ae049c525fe5aced0`

```dockerfile
```

-	Layers:
	-	`sha256:b9a28cd5067db3bf88112bc5f57fef324d427c6a451485da77af2947601a2a9d`  
		Last Modified: Tue, 24 Dec 2024 23:16:03 GMT  
		Size: 7.7 MB (7703658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107e5e52fde12553cdceb924f5b315f5052f8b6d660c7dc8fca9828b1b54744b`  
		Last Modified: Tue, 24 Dec 2024 23:16:03 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json
