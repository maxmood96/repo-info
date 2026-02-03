## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:2d03b1d3fbee2907a38c3b5446d553cae3791503718072be575fd80bf58e538b
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
$ docker pull neurodebian@sha256:62557098c459de418b2e59e2e0374ded8453839c8dc8a8a635e934e25b272fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60289672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e09429446df5077bffdd30968e77332ee3dbad06f3b3bea0d5d4e95d262872`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2730c822ebcac3a15d3d766e879e3429b4f9adf6fe76271ccfc76c249537f502`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc7445e516a5d581aed9ea2f12b0eaeed7fb0988a1b7763124e12ff75af87a`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.6 KB (90648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6aed34d51bd5ea07823221ec742d4e2d9232789220b79efe8f13368675e3040f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3787c78d5c00b60dd7bf2b7563d0ab9a1f311b1efe8e20720192ef75f7123075`

```dockerfile
```

-	Layers:
	-	`sha256:5b86a2fd5679538630a28183b3b3ba91097d7d8705bb17616d47cf9348996af0`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d480378322cf7188821388658920d0bdc152a426690dd4aca8e70b9eb5cd12aa`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:20110e381f6b004aa11f066beb696aeca0000b8124cffac7191c4cf7022c6010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60198955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c078fc2e2f1689540c190a5373f9ca68722470fab192a2bd957f460ab642ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:36:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:36:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:36:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f0e1c9ce589fdc56e77162978a9037d5d8c63c2e5d6fb4fd4b325ce20394aa61`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 48.8 MB (48820809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9b4ae41d7233f89c118d44c566dbbb0830c66fb38efc746d17d7d8173a4882`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 11.3 MB (11284159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6245f8367a76c48a8d8d1f80c4b50d14bc2990b1511aa41472f5da8ce96dcc06`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865c6f91c38ef38d5b6ce69fc2f8327da1da6f39b1c6117b3cdd7009653db137`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dd28e59e9c284ee6ea9cd526634ccd93547489875f216d845eadcacd04c1ac`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 91.1 KB (91081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:88cff5449f9b674dfddf81f0ae1030542280eae60026af309ba965c62c3fae35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3d45e5e795a9de5b54de388dda9d9e8a9dd64086e65bd23593c7c589264a1f`

```dockerfile
```

-	Layers:
	-	`sha256:e29b98130b6dc6e456541688ff5b568dc4f6ccd4d3030133e5a4ac315d808cae`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 3.6 MB (3593356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630d99390d48575bc5839357287f4463cd0de213f9cbb7150049c3656c5f1a7a`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:1be3593202c67933b0299654e15c40a1f5f79745d476a49e0c57d40fbef93e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61816076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6906c266a1c4fcbea80e2940b2bc77724f1b671ab54ba960695b5a85da2ddff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:12:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:12:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0f5a7611eb50e1c295ff4c244485263852c6e6c8f18836cf55dc8b5a4162740c`  
		Last Modified: Tue, 13 Jan 2026 00:42:21 GMT  
		Size: 49.9 MB (49944546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6cfe728e8ad2478120bdf56f46f6e29d6f196368ee72600cf4cf563f852d0c`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 11.8 MB (11777884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b758bbfaadc4750b38dd2d7a2eed37620b79d23adad813edbadf9b54190aadad`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f53ad6cf16dbd5f68bc9d9322dbb7cf4cdc0b91cd81817c248463451194c32f`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f6d2e23e75837861e27bcb5f7a138da1aafb97f4d81476f5435b4f15a01e0`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 90.7 KB (90744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:68d058ecda648f3359c973d9e0cb54d24bf63c92d5ebb84d7583b7d42502e083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1f93b265c195fd17e70d6c5296f6e03fded2d2628ada0e80b976c5b095c0eb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b335683b09ca022d562f726c22c173d84b01acbd67aed48073df04de9fd807`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 3.6 MB (3590438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1f2b647f16426bffab845d28d772f826717c5d3650bc9437f5b6cbb3f22628`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json
