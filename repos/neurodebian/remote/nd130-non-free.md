## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:f955a86e449539e8ead8629e8efdc53e94b0a090a9ddb74c13aa532fe15a8dc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0200405ce96861754e151363cf5b3caf8d478628bd52110efb6efdbc6df18b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b1c13cb1413ba125982812e517a32f048a2cca19d8f18e2991bc55be35191f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac46d0e6db36768a29a55dcc7bbddb2e27c879a2740da03d27237f7a98601c42`  
		Last Modified: Tue, 21 Oct 2025 01:47:47 GMT  
		Size: 10.3 MB (10289352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094b1d2fac8c441b70dcee6cf26d3507cceb1d0d36655282f1ccf11d62ee85cf`  
		Last Modified: Tue, 21 Oct 2025 01:47:46 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04561aeb1d68e39c7a9ed4e3aadf107c4aa4e4a54af2d9ed1e8f65a722902e`  
		Last Modified: Tue, 21 Oct 2025 01:47:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0957df62327e9635324cbfe3c5c716f4ee6ff1898dac3875a11f74f0bdfe192`  
		Last Modified: Tue, 21 Oct 2025 01:47:46 GMT  
		Size: 90.2 KB (90160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48474af52ef120ab567f8d93575bc83ef6362d5d5f02cdaf2a0093c79e8b3781`  
		Last Modified: Tue, 21 Oct 2025 01:47:46 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7e23ab522bb042b4411d680ebe4c5301babaef8241426aaad153c35df9e6076d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f60f108eba2b25b93c0d5e8ce1f56eb266e71b8480ff2bf733256eb11f1fc4`

```dockerfile
```

-	Layers:
	-	`sha256:72e9c4cd42b8f6bb53c16013b2af76d5a5d77ed5519c16c5c8af98ea719b145b`  
		Last Modified: Tue, 21 Oct 2025 10:09:20 GMT  
		Size: 3.6 MB (3613075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8ddfa40a2997f1a10d69e5fdb20aa88bc698fc07d2f6683daedde6afa98c33`  
		Last Modified: Tue, 21 Oct 2025 10:09:21 GMT  
		Size: 16.3 KB (16325 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4427c9a1c3d6421fd1719f050c386a31e9e0496fdee2d99981ce94dc3521f17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59816971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e3b2540d0b7f3c25e66b37fbabb526cfb2375ae4b53b362457a6319571d837`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2bf8d2ddbdb7947d19c51a92785e04cb87858357dc72862f9c197cd8efd4e`  
		Last Modified: Tue, 21 Oct 2025 01:52:22 GMT  
		Size: 10.1 MB (10073050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eecf8e010aabc647fbe024ac7de7f587e4b8ab5a11f568efe16c24c0e0e0857`  
		Last Modified: Tue, 21 Oct 2025 01:52:21 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6b0b74b71d4616f6db0d6f6f1d2367648adf8133d413b72ef589736103c71a`  
		Last Modified: Tue, 21 Oct 2025 01:52:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f262e51504bfbb4685176b61a66673870476d142b13b250a0be34ca4ac01bbc`  
		Last Modified: Tue, 21 Oct 2025 01:52:21 GMT  
		Size: 90.8 KB (90833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8d25b7bca039e97d2b7a5e86f4906313f45e3b70e89240862e71ed3bab12c1`  
		Last Modified: Tue, 21 Oct 2025 01:52:21 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7287ffc2bf0b18c9c0666894def3576b65205874285f4fd13cb4e3b524c228d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96085a47406ea4edf5bf50516463d246cc44cc51cb92420daaba7f098b7c5658`

```dockerfile
```

-	Layers:
	-	`sha256:a7224bb14d7b127bc1a5ec1ecb40a09afea94b71dce7e0c3c572fd17bb3b5d31`  
		Last Modified: Tue, 21 Oct 2025 10:09:25 GMT  
		Size: 3.6 MB (3614602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b472e8d2da6deec1a10782b163e46e620e9996314ad5e056d50fe6658d577271`  
		Last Modified: Tue, 21 Oct 2025 10:09:26 GMT  
		Size: 16.5 KB (16477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:91ab281d39a7a47c2984681e71210c1baa124ff7d6c76b37ed38cdfaad499a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61357228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fd8b06572574356794c66c798d558a63052c993ba6681b2c5358431458b873`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b193ffd7768a198fe04525b8abc1fe925952a6ed54a72159f801abcf885995`  
		Last Modified: Tue, 21 Oct 2025 01:55:27 GMT  
		Size: 10.5 MB (10462706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3b2134b0cc3a0f9ddc27d0e6147aaf72a025265e2dbe55d6d36465d3052a01`  
		Last Modified: Tue, 21 Oct 2025 01:55:26 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acb083c0e1e751e6d215889e2c419eec5f971006a3f9dc2258b5b681b7d4361`  
		Last Modified: Tue, 21 Oct 2025 01:55:26 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ed4dfc2e0a9c64fec80a5a05a4c6c58e1dec0ab25ac65e3aa6b0cfdceb34d`  
		Last Modified: Tue, 21 Oct 2025 01:55:26 GMT  
		Size: 90.6 KB (90602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef650929500ecd2c2247d997d74b7722b0d10fadf4103550b48087c8233d4575`  
		Last Modified: Tue, 21 Oct 2025 01:55:26 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b6ab66a2db8ffa6319bcaebc644359caf516c576df6dcbf03a9ac9690f42abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda80bb9ea3120fb38f73d5997ae8815a0f5a74d324f84b22876a79413dd5d94`

```dockerfile
```

-	Layers:
	-	`sha256:5edd7d4a58ccb598aeb11cd40281017c46fc58b80910e5ae2e6571cc99c25433`  
		Last Modified: Tue, 21 Oct 2025 10:09:29 GMT  
		Size: 3.6 MB (3611024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f90852b64d4045ad732d1d87b6509ada5ac2b53bf70319bef22ccb4bbadcc065`  
		Last Modified: Tue, 21 Oct 2025 10:09:30 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json
