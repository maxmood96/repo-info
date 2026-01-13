## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:c60cba8106b8f359d07ebe24c1c5740a10c73b28f895863f5eec3a3793b6ec3f
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

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6dc0248df19fad593ed18278e61d9ba0b4a3af5c64e9c5a174a7f468071fa3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124275778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de5948b4487876e1cf78b0915d25ed5d3f629b2fe394607cb2152b66c2a1651`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:23:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac758735be4df7bbee87d37924a15ccc254964d763d0b8620fdba9dc6d6774b5`  
		Last Modified: Mon, 29 Dec 2025 23:45:40 GMT  
		Size: 15.8 MB (15764112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6512e35a226296c3166e8ce55b556c5fe6daeebccf71cdb13eccee234e17765e`  
		Last Modified: Tue, 30 Dec 2025 01:23:49 GMT  
		Size: 54.8 MB (54755226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c1864e62e88d39d39fffbcb4d8b16610d5976672292d547cc8fcf902f041f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607e45dcc163b6131497508f46e05f976fefbbedbf7627724ed00861c953cd41`

```dockerfile
```

-	Layers:
	-	`sha256:55f87e71f4db143b64f9b22249fc610527233daf025d430da62731c10ade5415`  
		Last Modified: Tue, 30 Dec 2025 05:20:50 GMT  
		Size: 7.9 MB (7912160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bc4ef940233543d57b183c8a5a8f9dd5b251eb15726ebd0bb0c645d7cb88323`  
		Last Modified: Tue, 30 Dec 2025 05:20:51 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:87793da8ee908c38b0913941d3c269833eae899940cdd7089c8001cbcbfea4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114556682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29fbdea33d157bb709828e150d60ce504a380e25e1faccd274e13fe54474cb0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:57:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d86a038b54ede2ada385178a3a13e9fc7833f9952c07b251c404c3aa117dcd4`  
		Last Modified: Tue, 13 Jan 2026 00:41:24 GMT  
		Size: 49.0 MB (49046458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd38532089c34c92931050565b084061d36d5f2907633b524122c2d6f089b42a`  
		Last Modified: Tue, 13 Jan 2026 02:57:41 GMT  
		Size: 14.9 MB (14879656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e704ca674385fc92cb2832f27a6cfada2b1b4e440bed4c77bded017641bb11e1`  
		Last Modified: Tue, 13 Jan 2026 04:25:10 GMT  
		Size: 50.6 MB (50630568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ff211456fba12d0ff4757864bd26168fa6ef5327c4e11c22d0e6bd2c865f7659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd55d1a8c510aaea6b2b1885e266a3c6d6bbe0dacd1aff156f625df456692f9e`

```dockerfile
```

-	Layers:
	-	`sha256:ba921e5bc3fb5d6d95c640db3844dc2de451131e6a6580241e33bb568947c6b5`  
		Last Modified: Tue, 13 Jan 2026 05:22:36 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:742ede317503edb057f1eb2db9eb03ca0099af02f3f89e3b10830c9f73234459`  
		Last Modified: Tue, 13 Jan 2026 05:22:37 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6a5dd71e5db27a75f436ccbed4ad6682976de4ca62af2124d83a1f3f222d5d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122872586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0f70d506eb00993ba2de64584fed4d8b2455745c48fc92889e45b3f733f17f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549a4595c672d6f3151acb8314dc1cf09736bd0b263013f6ec6856c4c63f19a`  
		Last Modified: Mon, 29 Dec 2025 23:46:10 GMT  
		Size: 15.7 MB (15749381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890aeb16c8cc7bc154fba2dfa61907bbdbcc96a5a7b348a6376fb17c7ab1fe61`  
		Last Modified: Tue, 30 Dec 2025 01:26:00 GMT  
		Size: 54.9 MB (54865435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:216ad49bfbf1851f8d25b82025997af2026bc6e01ee732b4ca52f86f71f7b6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011d931ea7eae6d28a5225250311bfef47297901b1c69cc73fc146448990c609`

```dockerfile
```

-	Layers:
	-	`sha256:868a1fd1cb4b9158ed9530814c3dd9c9574155b0425cc8d2bd959c41c65e67b4`  
		Last Modified: Tue, 30 Dec 2025 04:44:11 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ebd8684b5d67fc17f29df29b127685a0caedfa1a6c783c08f696b5a2ec10447`  
		Last Modified: Tue, 30 Dec 2025 04:44:12 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0e04a269d1cf6637725e5582260dc05b310aa284c56387dbebda68421168082a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127016325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6815b3aa6aefdecafba8f575089d8a83dfdd146184e942df2a22a45e16148c99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:42 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed43d5d71f701abde2a62df95258edf0ac9ef3046d49ca25c0f30e57af2985`  
		Last Modified: Tue, 13 Jan 2026 02:02:38 GMT  
		Size: 16.3 MB (16267780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50309e354294a6f81ebf1bf80c4203a79bc9374449993f7fb52ebf0640408262`  
		Last Modified: Tue, 13 Jan 2026 03:03:46 GMT  
		Size: 56.0 MB (56048907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f8303881651568734528b2aafcc346741530e1ef6b30aab5e6d4f31b4386a200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4ce379914825c166bf748763fe890f79b09b2e6607a7fb877de27989e3617a`

```dockerfile
```

-	Layers:
	-	`sha256:556d9759865dd27bdc48a52582a15d487b8232b3887e437c862374fd4b1f2a60`  
		Last Modified: Tue, 13 Jan 2026 05:22:52 GMT  
		Size: 7.9 MB (7907730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d6a87fb67cb5fb02545d66a5a65fc3906d2174c13247c97c0df0c375a241b26`  
		Last Modified: Tue, 13 Jan 2026 05:22:53 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
