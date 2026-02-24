## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:e76b51520441102b305abdc1bea20ac9b24429ba4f73f1962579a87fa174f65d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:22ff68e02fc0e3ea687bbf2fda12c64f7e82d99bd02ed106657bdaf459936bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60316656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7000569296696fcbc6f97fc24d5c0a61676cd5a670779c0cc52c541e399c57aa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:26:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:501906f379a13fc3675791cbd6304f648074973affcb965be0bef8b0aaa34ab5`  
		Last Modified: Tue, 24 Feb 2026 18:43:03 GMT  
		Size: 48.7 MB (48677181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e77041f179e7ba990ffb7d8f963e6a2d8eb2e15a6986bd5d12773758bd2fc6`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 11.5 MB (11545754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e6ee33d9f6a7107961fe7ec05dfafa3e1535fcc1dcfaea38223af79f640fc8`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e123668c7ee8c6d4df45929450bc612423556dab24883776d1abadacd465f8a`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b39d3daa5e4e37dbb9fbcd0bd8358c909306b05c989ab8f52cec1fd09608495`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 90.8 KB (90816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a19a630d67553731d6c5794aa1358425facc586cc3373ffcec601f785ddd0abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0618de89db5b2472a7758358ec799c21053c6597a40038876c7b22000c5aed4a`

```dockerfile
```

-	Layers:
	-	`sha256:200c16243ec17f89097ac9418a1f933fee011fab28fbf4912ec2eac69d8ed19a`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 3.6 MB (3604393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e9406a8429c02066338889a24349ae076cc38a0495ead4f7a70389242bd545`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 13.9 KB (13931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:69fb6b8588b4665f38a6079afc7c3b28eccf86932191efe6bc01c938d196421c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60059027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157e1d3cb105ffed857b04dbb19b5075a7e9fa8cfaae3d16ea6c91852eef586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:31:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:31:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:31:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dc3ce43fbcc581a6cb3e0909e03d7e31c0ff1d4d76469e15d6610d1403f2a7e0`  
		Last Modified: Tue, 24 Feb 2026 18:42:39 GMT  
		Size: 48.7 MB (48705026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e66eeeecec37bb9f8db752d4583c383c755f7bf058549b36cdd09a23448fca`  
		Last Modified: Tue, 24 Feb 2026 19:31:37 GMT  
		Size: 11.3 MB (11259563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01672d550825ffb091b84d16923f1ba39f053f0e02a75f2a7ea9be4530f5c27a`  
		Last Modified: Tue, 24 Feb 2026 19:31:37 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c6479f5489d6445461da39aa0d2b1938d8f00c1aac777d7be50b1f369dccb4`  
		Last Modified: Tue, 24 Feb 2026 19:31:37 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56e9e317f49a16508deb62b60a222af80e49dbdc671cbedfc5a4a8009589f6a`  
		Last Modified: Tue, 24 Feb 2026 19:31:37 GMT  
		Size: 91.5 KB (91531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5764ed831677280e07b3c28985d32eb49fdc88dd3d0dc72619f7ffb1a08e59d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b4e7bcd23acfad2f143b0aeed9fd2a16db843a4175bd646ef8cc65b55797f3`

```dockerfile
```

-	Layers:
	-	`sha256:029535710ae15c2b1cab7e0605051ebd109cc559e41c483a7d59b5554a3a2912`  
		Last Modified: Tue, 24 Feb 2026 19:31:37 GMT  
		Size: 3.6 MB (3613293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b51f6dfc65640a4e53ce0cd9416b401ac4c748410b56dc34db21f49bb742e2`  
		Last Modified: Tue, 24 Feb 2026 19:31:37 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:39aeca43642753aaa5a044a2acd6bee77c73e5b8e09fb6b77f23650f18e1ab09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61897834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6671cb2b5a7919a9654f4e676d1d14d42c2e1b802318479f338a705ecc138989`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:26:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:143f133830d056570eb26009a5886b146c40a6e16bbee60113f54a6baa1643eb`  
		Last Modified: Tue, 24 Feb 2026 18:42:19 GMT  
		Size: 50.0 MB (50011968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becdbfb396492a346eccbbec20dadb7b92ca1073b79036e2e9ad42cb22f61f40`  
		Last Modified: Tue, 24 Feb 2026 19:26:57 GMT  
		Size: 11.8 MB (11791846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd152d464a03f855cc0d559a87585758842a4ccbfd95b14750709904028b0c9`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3b6c8f2d916d0738b22edbc9b0d3f8ddb62614f863de47027ae7a5168e781`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67959c29fe7c340629c76243f4a7b82130bda86198dbdd6a553dd7553331b384`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 91.1 KB (91113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:58e630b1fed3fbe9b290bd34ac4b953ef5f028c576bb3a12c8f250709664a408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3beaafa0ba3386ed67efce925cf782ead56a48f3724d40751b9cb94be2163cb`

```dockerfile
```

-	Layers:
	-	`sha256:d823f44023eb02c0f93de07786c55d3cf89e692d4179f7e720074d7e331ec9e0`  
		Last Modified: Tue, 24 Feb 2026 19:26:57 GMT  
		Size: 3.6 MB (3602337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:621655ddeb19c647f2007d6a270bece73dad36378a35992f78d395afcba8fd11`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json
