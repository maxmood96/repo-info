## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:6ec025896934b7893111261284996bfafbadd85850a9c9ce64927486850b6997
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

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

### `neurodebian:sid` - unknown; unknown

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

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3473d74285345688dad026ef0917211d20aaac7a63891d8b253c51ac76c7f36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60205188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3780f0e6abc99ad711f80a483189a852bc2a1d2bd2d9ce913bc7f0a749388490`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
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
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67162de59cae8432f37018bdfca1926d8d40b34084a6e6ca535064ebafd11af7`  
		Last Modified: Tue, 23 Sep 2025 17:39:57 GMT  
		Size: 10.2 MB (10177061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bb81dbbd87423aed66a55483c3b6d0acb4129dabd3c0147e74c76b0addb550`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba3ff27e7afe1dc3962ba33f3faa4fbaba125ab630cb86d1125223c943c68d6`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03b9f2f2b5433c7d521cd2962c537a2863678d15ff9ec8e3d1f7d6a4677c1ca`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f6b3b64165dd6cf8115298360e079d70eadbd2cb05021d0f0e61c82e695744f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631b4c7bfa49457dfcdf6c8869cf60c5f244c01f22f3bab8aca7e9c5ff4d4d68`

```dockerfile
```

-	Layers:
	-	`sha256:7d39ac1ae9919d67a330944d83252b6fba745ae3f16dce0326e07afcfb619d25`  
		Last Modified: Tue, 23 Sep 2025 19:07:54 GMT  
		Size: 3.6 MB (3611455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b646a4ca03999ebf0a0e86482bbb39a1c31c084ad7112cd593dc386c8241932f`  
		Last Modified: Tue, 23 Sep 2025 19:07:55 GMT  
		Size: 14.1 KB (14072 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

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

### `neurodebian:sid` - unknown; unknown

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
