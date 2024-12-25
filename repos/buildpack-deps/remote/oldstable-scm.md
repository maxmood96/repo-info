## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:c75c63b5365e70bb3c5090d2ccf661c02f36ed928558f9158e5a5c797c5a2eef
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
$ docker pull buildpack-deps@sha256:be78aa16820580cada63d809a8bfb504aa1276f7dd084f6c2f84e0bb02c007ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114339194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a03adb57e3f60161d493f8c8f2d91f2d2c5df173bd292bc160c9c579cceef9f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69dbedc8019388fd330866fcfa04c35d28f86d1ef986691ee290054433639992`  
		Last Modified: Tue, 03 Dec 2024 01:28:37 GMT  
		Size: 49.0 MB (49025021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370e6aa30e16daf07d99e3fb5cd8610cda77f49507a7b2ba76a646359cf7db6b`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 14.7 MB (14673759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54bf5af43178bf200a2aed84d9a42570d6bde94092c2ac746652561137c9a86`  
		Last Modified: Tue, 03 Dec 2024 17:16:41 GMT  
		Size: 50.6 MB (50640414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e492de4a1bcc068b39955b80d874bf462808c59bf0ec31bb6bd280d936713d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7727144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd315f13cbfceff99c6d58272b95dd096b9512de6dd7537f6d6afe2fd3e64d2d`

```dockerfile
```

-	Layers:
	-	`sha256:21a97e5fb320768479f40b78f22eaeeef9eb396a0aed03b8d41ca681056c0752`  
		Last Modified: Tue, 03 Dec 2024 17:16:40 GMT  
		Size: 7.7 MB (7719731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c5b9e593196a516856494c0dbea31bc158ff6fcc6058ea5e8c3d1a983de169`  
		Last Modified: Tue, 03 Dec 2024 17:16:40 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:96fa200ba907ff5f10dcad7d3e89a5fd73d7a5d5e9659f3ea75a0d9e5e39cb23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6c1ae1ad1d343f3ddbe86366b8189c8c804cebc4df7e87157d0ffa17f9d336`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749caeb5baae1b5e6316a6f02e57835aa548497fba6792be844c743a57c72a2`  
		Last Modified: Tue, 03 Dec 2024 11:51:00 GMT  
		Size: 54.9 MB (54852316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6f1b608089d0dcbf42f5fc54da8bb34eaf30baac382624cfcc5f1a0989e401a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7731504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dc80dda6eb42786edf9a0b24dc97cc6190d25aee82b1fd1276db616e8ccbc3`

```dockerfile
```

-	Layers:
	-	`sha256:30fed3f253d5a80620794c68dafe113a0924ca7001e8da4f4d974c019fa6166f`  
		Last Modified: Tue, 03 Dec 2024 11:50:58 GMT  
		Size: 7.7 MB (7724072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a78a3d3e15864eb8fa9847638a76c54bab0eec07868a25d3aa7add0d432da7e`  
		Last Modified: Tue, 03 Dec 2024 11:50:57 GMT  
		Size: 7.4 KB (7432 bytes)  
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
