## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:9eed6b58b84a550a5974629668891a7528c7538bb2eb7c3c961effa4073f6f6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f5fe87c1e1ad0cc109f0cf8f6a9d2c6474eaacbdb1477dfc6342d827eb111f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9184bde64f75bc0898f709fdf492555b74abd3086acfa010bcd4c6dd3130ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e573455d7fb5304cf7248f536b62a4140b90208a5690f4a3a85adc6e5547e5b`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 10.4 MB (10379740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b291dd14f83d964b7f57044bc7f4a04295df37ba77f9fb5dfc9bb9c7de1d8a`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2837bde73fa3149d81eb22fd9ff320d18a2c316af16da953569a16018bd3f9a`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c5c97b9334b4e50feeaa05190b4476afb1c64d57ae2a3336fbecf4267507ae`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 89.8 KB (89840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c03802ed8fc2f823aeb323ee3010b4ad1f995325a6947fecb7a0a0a9461d3`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a40e42eeaf5bd5622f29cb6a9dccd0f2036541929f187703eab2dcd3cb73fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3525f3a7effb0513b670c1151c6e814417883c77141c277e0dfaae15ca7ebd65`

```dockerfile
```

-	Layers:
	-	`sha256:bb336d527b6b81a8b19843c8b794c242c15418fb84454637d98af93a858b6d0c`  
		Last Modified: Tue, 30 Sep 2025 22:07:49 GMT  
		Size: 3.6 MB (3603579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8bfedbe13e8c850a9352ab07cb8c2451926c8b22fbbef681706adcbcc2380f`  
		Last Modified: Tue, 30 Sep 2025 22:07:50 GMT  
		Size: 16.0 KB (16002 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c965c49aa2b396e0101b42550f4800063f3fd56d517bec513e386066326ed80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60131972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ed496450d5563feac3099d0ade1c40efe2acb32ecfd970708e5e9ea282cfd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ed417fd581c20c18b8c6cfc58498c59128dd74498d5d6a89f9217103a4fbf9d4`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 49.9 MB (49879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c28b9bca2f1012ffe43d4eed07697f7da1ec3a47f388e1ab9fd4ec84b4e6268`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 10.2 MB (10158292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10b9f543673e23c7d03685762105c2796b3abb510f7e7108cef41bbbc9a9bfe`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233135e8a5c44543154aa30a4dcb42b38fda3e8ca06d93f639b9f507c3d4219`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384ab44da2640f654099b0207090ccab3d2b58cebd6b3258b13b298c5e3a926`  
		Last Modified: Tue, 30 Sep 2025 00:20:12 GMT  
		Size: 90.5 KB (90456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2747289e0447d3ae74f622064a865138a9eb14243918fc353cdbd2bf3d71df`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a2db88cd42eb7894e3e8a21855afe072e4bacb15736552d6bdff99769a6b19f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65795b979a2c217fe3c2025935d0c3f835af9f1520d745f2a112578257a83bb3`

```dockerfile
```

-	Layers:
	-	`sha256:6dc4931ed3e401fa42d22b976d0772f8eafaefc7add51f5418cb8196a0eb1155`  
		Last Modified: Wed, 01 Oct 2025 13:07:44 GMT  
		Size: 3.6 MB (3605094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb89734c2b1f04a1157e15fb2b072b93a1559445ebf22f509e9bd6d50f99abd0`  
		Last Modified: Wed, 01 Oct 2025 13:07:45 GMT  
		Size: 16.1 KB (16142 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f430324cf9cfaa124d9776470203aac188ea6774709949a77b63e213adfa7ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61745177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38ab08689612a8e95f9cc551ea0e8a30bda1c448048e882314e67c82e2d34da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec729a899466ae066afe6bfa44772bb49f12eb1ff9130de5775863dfce2fa5c`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 10.5 MB (10532172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016bd38ecc73b56e051fb135bc2f1b210de58690a65bd5202836c5e688c442a8`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b44b7f804d68298cf138540a3c3108a2814c8cc63932f7300357c68efe7054e`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e9b8bf1f68d7180b0cdf3058bac384f72680340471c2b07b70711bef9c350c`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 90.2 KB (90232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbf84aa702d16438adb1888b29adb0d130c0a91212dad4f8842d559e332ab6`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b490107fb10d10a6ec4ea0b23243b771a836b62a9ec8a2428a0dd7c4b38d4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48447039b9ee7cf8a837ef0de7f2fc8a4c3e43acdd0ac2c4ad657cbc9f7839ef`

```dockerfile
```

-	Layers:
	-	`sha256:62948bb3b9d5b778029c610a4efda1d2a480c111bf40184b640d8df7f51d9e93`  
		Last Modified: Tue, 30 Sep 2025 16:07:55 GMT  
		Size: 3.6 MB (3601540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153eff5adb942a4269e6f4cb5eb6afbaaab407c0686fde860d67023ab18eb4f2`  
		Last Modified: Tue, 30 Sep 2025 16:07:56 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json
