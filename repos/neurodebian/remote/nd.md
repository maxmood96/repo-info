## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:efce4ea64f54ce4a5c6ed6882dae178fd70c24cfeeb45d63e709d00dcf8c93cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:d352e1bdaf20b107fa873d64a014ec03a55aef6211f5e056a6cd7f3ef5a88915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60018849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e0de86f6c90cc7f5b47e859e7f0734d0c0be75b51cc7cdd2e6b8ecce9e6673`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:edd38bdf09a62ab44ffab2a10058156dc336ea087cf3a73258758d9bc541ff85`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 48.4 MB (48376965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1964d781cff69dcbb8224608d47e77cbe0ca18c19fda7c500947ce54b349e439`  
		Last Modified: Tue, 30 Sep 2025 00:16:32 GMT  
		Size: 11.5 MB (11549277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8083c7a164d9c55e20112d87245a4ac7874df659703dae0592af0ea6dc17eec3`  
		Last Modified: Tue, 30 Sep 2025 00:16:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ec4cb897b141395739b755c043b36a97990c58c741b36add1af451669ac27`  
		Last Modified: Tue, 30 Sep 2025 00:16:30 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce650969fa61f99b87dc4e0c2355ec5b19b5ca0c605b89d71edb13e8210bdf`  
		Last Modified: Tue, 30 Sep 2025 00:16:30 GMT  
		Size: 89.7 KB (89708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e7f9cddb4bcb9e61947b1cbfe3d7283a24493ed40d524daf2d52203c8bcf6a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee385a97eca1722b360e37f2ea21db83a4ca65ddeeda1726838355898e459199`

```dockerfile
```

-	Layers:
	-	`sha256:3450fd91ed423943f5f1ccb0586891b2edc69f23515ac0c6df2af5f4ccf8ad17`  
		Last Modified: Tue, 30 Sep 2025 22:08:27 GMT  
		Size: 3.6 MB (3575185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7c306a879bd2d2a90c91968619437991d21396041c3e0a911e5cf413f8d409f`  
		Last Modified: Tue, 30 Sep 2025 22:08:28 GMT  
		Size: 13.9 KB (13947 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f276efd9172e11522046410af5ce0eb50a69e25afff35700d60c8301448a2281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59869090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5710290db43f8f232f408c6687165992caead41c0085fa62263a4362cb9db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f5aae340a376cad680dc8a41a7fd30a241ed4bae3e53125ebb424c8fc7996aaa`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 48.5 MB (48487991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc322d3092244931732034d2c756709c302b50f1227794a20a81109328519c7`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 11.3 MB (11287787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29113037dd1be00d90a636436bf0567190c0201bd65bbc714d71afbda2ab6950`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8fc058e5e886c0a4787a53a804e614a59df193c608a14fc339b41a0f5a7112`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe019269d1c4393a725d347c2717dfe5b5dde34b8369131e2a6ebb3f43c61181`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 90.4 KB (90409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:42c0f769a6605843de59dd9a117d96c8b7446f60fdebfc99b40a806828cd4cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3590133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0b0dd03b72ea4b6bf7ee568d8a3aee946316388d6e61e18483a3cb671d1a56`

```dockerfile
```

-	Layers:
	-	`sha256:6607e14c440cf1ec05381d57aab85c2f3e0692fc5eb4066035be42c25f0922e5`  
		Last Modified: Wed, 01 Oct 2025 13:07:53 GMT  
		Size: 3.6 MB (3576061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd0f3dce5e1f118d17d9bbbb63d168fd52f0fe2ccbc70d27cc2a73ce8c7c4605`  
		Last Modified: Wed, 01 Oct 2025 13:07:53 GMT  
		Size: 14.1 KB (14072 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:0622b7c8607a17ed3f062dcbbe2e5ce444ad89bd2e586f4142e8de5a0190ac11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61496239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7e383cde8bac028bea9bf478d11f6e67bf5fd643663cc161c83f71ffcd1d77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d00269cb73b9e4cfebd155b431da849e0072689663a0a658044389a50f9d989d`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.7 MB (49686171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6f6480fd49647a130c5672473eb706e570d0a7e2ffc738010f418159bb8f42`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 11.7 MB (11717042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bb6b77036d5b364bd2bb6f5016c7e6e6e1f51fd3acd6413ec0fffca6c7be09`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ead752bbeef4f8b6544c7e6da0e9c452da6e55d7f7bf44255bc5705f3e41be`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee98413e70c0108e75166cd1eab704dbccca336d46231839dd53c9b6e22b1d`  
		Last Modified: Tue, 30 Sep 2025 00:23:15 GMT  
		Size: 90.1 KB (90122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:83a99d285742e7df8821f912e07a2fdc81967eff6e1c18910effd26a40e17be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62902d1e1f48582360c7d309fa12760e834aea5cc58e13c631bcbb277337dbec`

```dockerfile
```

-	Layers:
	-	`sha256:cfa6aeb85429432a36111a8460eb077d4be2c8e303826ac96fdfe3489298992e`  
		Last Modified: Tue, 30 Sep 2025 16:08:22 GMT  
		Size: 3.6 MB (3573148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe777d0a54bde48dc55901a7c0d9b6fc6677cdd0df0f45a4aba0d526aa5e4078`  
		Last Modified: Tue, 30 Sep 2025 16:08:23 GMT  
		Size: 13.9 KB (13919 bytes)  
		MIME: application/vnd.in-toto+json
