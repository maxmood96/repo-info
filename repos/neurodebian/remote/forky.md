## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:e0ac28140a83fb06ee54e191601b7d268599f0739c3e06cfe597aeda0dc7edd8
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
$ docker pull neurodebian@sha256:c6830614fe4cc4524ffe6e75c9825331922282238dc42feb7bd2ea0870277c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bb614590a0e40464f7b59ad39ab48a4a01383dc84f3c9757f3311e5d0b539f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:13:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:13:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:13:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c7cbbee3050ecd826301596e459f3fa12ca32f5ba2b65d33b56172341d2cd3ff`  
		Last Modified: Mon, 08 Dec 2025 22:17:14 GMT  
		Size: 48.5 MB (48512511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c709524b9b4f60d6479e6f361c37809fddff50f5d9aaba924a6faeab62993b`  
		Last Modified: Mon, 08 Dec 2025 23:14:02 GMT  
		Size: 11.6 MB (11603089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00735bb4bf416296004ccc8e6b75023b364262de29cd5f1356eb8da57220af8`  
		Last Modified: Mon, 08 Dec 2025 23:14:01 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aed9715dbf8508deaa98ebcce8ba68925839761d64449cec310c401d8a646da`  
		Last Modified: Mon, 08 Dec 2025 23:14:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c412adf73b7c1a12db80ec96420760a9f51d03385e54867713640513b567ab2`  
		Last Modified: Mon, 08 Dec 2025 23:14:01 GMT  
		Size: 90.6 KB (90583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fefdb2a37f8666f8ae281b09486d01a7542ddae379131ccbfb25873f16add4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0d5820fdbd2962861adf5cc4f5a0712683136dcc06aeca2eb7f10ace95e315`

```dockerfile
```

-	Layers:
	-	`sha256:926f1ca3a7d1d801718666514505b675c5100204bc2bb060629cb85e51ca4999`  
		Last Modified: Tue, 09 Dec 2025 02:08:01 GMT  
		Size: 3.6 MB (3585578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f64f729a6e7ee74c5240ae13986134e4979c8fd563ae08f558b1937b3304bdc`  
		Last Modified: Tue, 09 Dec 2025 02:08:02 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0240320d50e0a735877ce9c1b680fc83383e5270c5252f3c5a6bf75773613d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f450dccc1910f9ea53442d037d9c07d6ea9730ad8afe22c7e145b5abbaedbbae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:54:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:54:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:54:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:54:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e8cb6f2050f012301a38350d5b24e1d46c45d720d48514c166af2fa18ea87b`  
		Last Modified: Tue, 18 Nov 2025 03:55:06 GMT  
		Size: 11.3 MB (11255308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12dbc4a5a7d2672202d31ee9d7b29cb5d29a06f08566f247a363e2a63cb672a`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccded1fb17ef0c142f8ae7bf64a99b345608c6adb5b81d14998da21c5d8e1a35`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b042a4e6d45996fb48df60228a59d091830538e87ac00c0c3658e24d51ff587`  
		Last Modified: Tue, 18 Nov 2025 03:55:05 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d3b1559336fbc2de9e0c6065656e01b75ce0df387ba7457fca8fe58753121d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8978b1b94f45f5e132e11ff42fb8cdcf5277ac0ced6a06a87f419ef33bf4098`

```dockerfile
```

-	Layers:
	-	`sha256:b86a5b4eac17beb5568c3a961e76e6ffd482a8fc5ec835e684237bf06a5cb8c3`  
		Last Modified: Tue, 18 Nov 2025 05:09:15 GMT  
		Size: 3.6 MB (3578277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1379a897c2fa408e0db91fe9afff334ac85006ef732f63644534ff4740f523`  
		Last Modified: Tue, 18 Nov 2025 05:09:15 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:ed17bf7744b05e17a7f5a07512b499f7853d80ca2634d1b3091f724ec12704c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61720534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4a7e442293c27bab1441b206d263cbbfda95db72021a246e34633483d87277`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:15:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cee8645950fcb2cac8e786ded94810e24e89ade2e4f5cc4099b37f01809d5`  
		Last Modified: Mon, 08 Dec 2025 23:16:12 GMT  
		Size: 11.8 MB (11752135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b16c5bf742f0f200c67b5041f2cf3e97f655ef571b984e5b607960988763c66`  
		Last Modified: Mon, 08 Dec 2025 23:16:07 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec3e51522085c44202103858e4b4bc149caf3ac8be3196028e5327cc90b577e`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a58fde9f6b48ef00bb0ab006f68aaa17d9c356d37254ac44110fe0f3dadc452`  
		Last Modified: Mon, 08 Dec 2025 23:16:07 GMT  
		Size: 90.9 KB (90913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ade3efb3c881d0f2aebde1a8dfd977b7cec6e59eadd851d32e96d5442cdd4c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31d7558920461a59e82693d3c70a6a3ec175dbf6017f477e182186218a2197`

```dockerfile
```

-	Layers:
	-	`sha256:16859a3d98038419a32fbc0eb7b4a65dfc2adab665a924d9bb3ff4e6dfb608c8`  
		Last Modified: Tue, 09 Dec 2025 02:08:11 GMT  
		Size: 3.6 MB (3583531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104b1ce751d490df8412608415756e6158e3a99cfc6d9d66a088c869af428201`  
		Last Modified: Tue, 09 Dec 2025 02:08:12 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json
