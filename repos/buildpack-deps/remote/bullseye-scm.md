## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:c8b63654cae326b1f4689478ed741bf6fa22a9aa547aac3dd75f4671304c7b94
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
$ docker pull buildpack-deps@sha256:06accb28625e1ecfbdc51b36109c09431cab2e1328bd56c948c00c11abff841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124272377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd07670e6c3b953bc58cc7657b120f96450d996a087e9806fee7fa902907ed43`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Wed, 21 May 2025 23:37:39 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8f16ba41407982904b6609707d25946f8db1fe8dc5259d73a4a3c1d0baceac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7750825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4eb4a40ca4402d9dce565e542703793e49fb679f7d64fd2875ac90a351f58`

```dockerfile
```

-	Layers:
	-	`sha256:78a59f38070feb3de58985341fab1bcdda112a4290148e92a622910ba285758a`  
		Last Modified: Wed, 21 May 2025 23:37:37 GMT  
		Size: 7.7 MB (7743472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5859a64ad811da8e15603fc815bbd6a3406b48825a0d1946567e80d9bf369177`  
		Last Modified: Wed, 21 May 2025 23:37:37 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6880023e221468ec08a71369d09be75f3a7915f20323729473bca57bdc00e6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114553829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7609eb6cc38e867fde0d22d03782c4a538b894289190968822d02a2d0ba6ff7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Thu, 22 May 2025 02:28:36 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Thu, 22 May 2025 12:12:20 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:66e67040e69c7613bc9ad430fbe093fdf5f87a69878730e9f74009b28441b15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7752287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c7cb257507df2e319c1fdca36f7fbc4e3a36c9bd9c07f720276bf4294fd584`

```dockerfile
```

-	Layers:
	-	`sha256:c329e8157a783253255627ec114109a3a7ebbbddc0efbe4fc47d131d3738aefd`  
		Last Modified: Thu, 22 May 2025 12:12:18 GMT  
		Size: 7.7 MB (7744874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67006883bfc194cfeb95d9294da05d4a6f754a7eff7418f4dfe3253fc9daeed6`  
		Last Modified: Thu, 22 May 2025 12:12:18 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0f2e100d8a1955fe9440084a0fb7d2b4137a92ac01b0c7d90bf7ce44b01d971e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122851373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199ea90c135e3fe228a5bc26707ae10d969d23075970f2593e53519ddf92242f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Thu, 22 May 2025 02:47:52 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Thu, 22 May 2025 09:18:36 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9fd9e7b71abd86a5109b2aa69a2278c86d071bd47c19acbf8204a468530ccb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8264a356bbaa18a6b1691b98d1ef2c26dff1843983d4485d1ddce21b6e60370d`

```dockerfile
```

-	Layers:
	-	`sha256:0fc15a0e5dbff4651ad9b3365a154c1fba17d38914b72a5ed72a2d78f414905e`  
		Last Modified: Thu, 22 May 2025 09:18:35 GMT  
		Size: 7.7 MB (7749206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ec98e3cf7e2dae04616001897e16cf5d176352f8c628d3562fcc5e725353c4`  
		Last Modified: Thu, 22 May 2025 09:18:34 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:142d8c9925122c888b01c6d342b8456b81f657ddd3abd1e8e60f37bfa1f1fd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127004048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6d60478bf71415baa5bb970c4c00d9250765b50f1f7cc1c25dedbdcb112a05`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Wed, 21 May 2025 23:19:38 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:729eba4b7016421a786cd270b0c7a271a56c364ca40c583d43c0846beb2a37d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7746373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bd1b777cd8c3b4291a421cf9f50b27f4d1d42f2ebd1965aac3a843a8d10bf9`

```dockerfile
```

-	Layers:
	-	`sha256:a9de30d82ca63f72a7c937de0b0e6fde9aa8b44da1eed37cf115c8c21ed6fd07`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 7.7 MB (7739042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1825376f03b85bff6c8eed3de31f3fa5a21776f67cab854d2dcd354afb169524`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json
