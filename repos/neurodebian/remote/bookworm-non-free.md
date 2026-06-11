## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:66a48b7ccd20aecc1e9c9e01ebfdab2ea7295615de73b51bcf9d8ed7309f87cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:cb08d6507f123ee954428276008e9c83d04d678754198d693e50c143cd0b54c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59871456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b85951aa7d121d082ba9654faa3848cc4d7abf9356e2b05af37bf3798ee4a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316bf023637e8f75e24e3831fc88deec444a7edd9790e0f9f3402d9b29c326f`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 11.3 MB (11273410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c8c4f5224dcc00c21540e9ea367e0aa62a4761dce0b1fb4bb55e9ea5b3cdd8`  
		Last Modified: Thu, 11 Jun 2026 00:46:13 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6638a85f4456b72d34de42e7458e7601f3aaa7cb32e4f085f5d08630aeadca8`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5858bb9b664153533d17afecd315d9a495a8a206b90c5efb794f7c4092c1ffc9`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 93.4 KB (93384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38110510a4edc98696657cec2c2800964ccfc836ec056480be42cca91b0590df`  
		Last Modified: Thu, 11 Jun 2026 00:46:15 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef56c80fa9e728c7024ac666c2bf5202d16a781191412562676f1d6f20996382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24b93a1caca4355cbd5126916038afee65708be0cc9931b6318251c3a3be743`

```dockerfile
```

-	Layers:
	-	`sha256:9ef2dc0010e4906a38178c6a2967e978008ea697bdedf904b98653f49cfe61f4`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 4.1 MB (4075951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7730b62570a8ef5981814ef338e673077fa401a6a2344f13053e1964058ca884`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:790fdbd7c2371eb8b5a4027250b8a4b74df108263ee34284598e48689aa3d001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59737987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4997f84d1e861b3e56a7fcb35962903ed6088d800caf72b7705c80a7d0b9c2ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:47:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152f2e93026566c42f24a52213782e990addaef08acafed5aba4a4f0e9fba3d0`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 11.3 MB (11252819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5448acce891289851311b76fb4d92d758cda828f3c1df7f4e8055522e44a35a`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84827aab7e6cfbbe8fb22eb54023ada3db2c55f6c590f10460f04331d83a4b14`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fe5708fd6c1d49b9eb0bb8f71f6d6a7ce682aebe87de418fead20b403f39c6`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 93.5 KB (93528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40247c8de7fd661db84c3da66fac073f9af9b4e5ec60d78e06137a39f9bbb31a`  
		Last Modified: Thu, 11 Jun 2026 00:47:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c65b1c9f2a93cd41d6d12d3d078c3331d4a1300f4a3fc845c881942a25a4371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3d815e24ba35c3f2fe46f25e2b34685792def1dd62f2676edfb9032b4fc84b`

```dockerfile
```

-	Layers:
	-	`sha256:f14973f21ebd27849c67760c0605d4fd69ad40f3b377db94b406ceaaef164e24`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 4.1 MB (4076193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dab5eb8c34bd4bef3fa1de4b045659db9b0779ab5147ed7c0beb579e96e5f5e`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:916e6a70fbb08f3fecc0d5bb863f975a1fad071a1f0e71cfd96c6b0fab0dbe6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb2a0631090e80b21116193e79024329d08135c8e8716bf02fb7c1e283d1b77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810ad9db6f2b469efd6a3dc32f01d8bbee996fc9cf249f536349c428f775171`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 11.7 MB (11693049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4517a2fd68626a4b7d37f1281a4b8493f6bff6cf362388c70809494bf22763cc`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938bb31a07854edb8f445c0fbc48ceecba7c48afc745853f8166b847acd1f7e4`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8d694a50b5688ee05e4e6c70630b58d4a74b7e69244a495d9d6da6884f5988`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 93.4 KB (93427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d110e3d514a17608c947489dd7fcc1594c428802e040f83436725aa0326d819`  
		Last Modified: Thu, 11 Jun 2026 00:46:11 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:47006af36b58aff1f1d48edf468a341fe26cdb11c3f666f1ae7069444f6c4179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13db9167b04fc22de7de27b41be6646812bf36993db6a0cbe491979ac625d01d`

```dockerfile
```

-	Layers:
	-	`sha256:f293d710adabf57b11d93c677d8ec53b76b7dc7cdd43a0dd4638b26ed17742df`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 4.1 MB (4073918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9bf6c5d9a5fb8ec5c22c16692a1369bc9a9c93f4bedabc2e43c616ff5439475`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
