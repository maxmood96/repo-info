## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:1f0c2233ee4e3e910b8d2775973e59fe5e38dae0673101078a050048d9b6bfa6
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:14772804cbd86ff3a2582da8df85a0eb2b5235aa7e9a7d2fcc80984b261825e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12717cc97ef8208955d1fd53a7de46bc44d78e047d7e16ea484d3a05cbec920`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c4b9bbcf6fad0a880fd05f7fa445d181741ff350cc553dc736610b3c4570764b`  
		Last Modified: Tue, 24 Dec 2024 21:32:16 GMT  
		Size: 53.7 MB (53738955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaebc650da5a3a7ced9692a9c1c8c045c098a55e6d7f274593861e143b2b119`  
		Last Modified: Tue, 24 Dec 2024 22:13:47 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a8ad7bbb4860482b13183959a86cff82b16107c5557a5ba42af6025555545bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e832fefe606436adf0d36cb6cef87278857f363f0a0f8a1a92ee5c11cd7931f`

```dockerfile
```

-	Layers:
	-	`sha256:46421d3cbe271b20b78bc007000302349ceefc9c6af5e11297359592090726ba`  
		Last Modified: Tue, 24 Dec 2024 22:13:47 GMT  
		Size: 3.9 MB (3917518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f1b86ce0c99fb243b647f33bae0bc06236aca6f37703b72496d250cdaa80db`  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0811282a18bf29c88659b5ec1872a67d5d9d319e61bb4885ced1e092f2605c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49024990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef0b96c9007d8baaa217bb13b8f00978f4a127ed437b63b7790a513000184bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3822375ca5d4e4dffb5645a4d9dc3a3594cbfbf07aae5fb8a761410ac25f9369`  
		Last Modified: Tue, 24 Dec 2024 21:34:53 GMT  
		Size: 49.0 MB (49024767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353e94b2237c019527909cb53d04c2de0ba7125dc6cdc95cbaff8509c9f92a13`  
		Last Modified: Tue, 24 Dec 2024 22:17:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9772e626bcca6079fb8e2d9398c0cb7af029e15f3b5027344b4c4da1c67a944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b320ce048356c86191fd60d3e3ce922fb58b0aa1c16c1149b483e0ba400fe15`

```dockerfile
```

-	Layers:
	-	`sha256:8d26c5cc753c00279de427279665a3103945204575df6ba788d96c9d8f2409b4`  
		Size: 3.9 MB (3919080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaae392a7f85cd56edd497973f8e83ad2c4de7f5ba4448ae30d189d17c1c3476`  
		Last Modified: Tue, 24 Dec 2024 22:17:17 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:68530ebaba1a2296507452e079715ec1805795bab8a6ac8eba3f1fd92b05c287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52245920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee617d064531e0c0f5d5c27451b8526f9846a73e836d949bf2810dbeece2b65`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:61c72fb36d3498e4ad3a93fb365acfd11cd94c8b559e475f2dffcca4eea6ecda`  
		Last Modified: Tue, 24 Dec 2024 21:35:07 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f587ccdf194bf78f6b4ddb7a0a4263918ba39a45455249e3bc4774295de18`  
		Last Modified: Tue, 24 Dec 2024 22:18:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3850916187d15afffdec199318299ea4d4401c8f0bd96cf1841992d8d9592c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ad463400b688127fd887209e7ecb8fee770c847f181111af50b0977df30a59`

```dockerfile
```

-	Layers:
	-	`sha256:a9a65a5ad6d03d9f572e91c7b5005b310a2e5673f38e88d7c304a1034e30d74f`  
		Last Modified: Tue, 24 Dec 2024 22:18:05 GMT  
		Size: 3.9 MB (3917098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc6de3f5328f88706e45ad9be27059e70a3630dd6d74883e89f7bdac263a635`  
		Last Modified: Tue, 24 Dec 2024 22:18:05 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:4bd30a6b8f719fb84ad17f061ccdaa1f2eb616286546b05a8140505da4e0dad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54676237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a15c767f83d539b07269ae3db0c36588eb947e9440619d289d9015a1f0025c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4f03d4d81c4c24d44849861df3c9b360903300b2382910250746eaed59e0f3eb`  
		Last Modified: Tue, 24 Dec 2024 21:32:50 GMT  
		Size: 54.7 MB (54676013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7373abfc4798e78e93a222f213442cfa3661dc5ab15da7b30ca82fa296aeda29`  
		Last Modified: Tue, 24 Dec 2024 22:13:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6f5b72eb9ed09c400260177b0a0c87cf9eb7cd841173b1681f23cc86569e6333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7871d2dccced524315bf6454c47c38191025cbadfe703291f6250987f3e927`

```dockerfile
```

-	Layers:
	-	`sha256:b0871adb832c09e86699c4b627219e36cf5f99694f9fd32653b98edb612f1186`  
		Size: 3.9 MB (3914025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8344f4b9682bbaae5cdf725ac7c5fdb3faf6d5efe51fc1ce0325c9a90e617c`  
		Last Modified: Tue, 24 Dec 2024 22:13:59 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
