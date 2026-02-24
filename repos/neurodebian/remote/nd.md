## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:34915d95d92ea789e5f55db583bbca5ed254a5256be01c0e1af3c6cc730c0edc
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
$ docker pull neurodebian@sha256:3e3dc5e87d0f59b8eaba8f49188ae67c2227c44da88819919b64dd136e9a9b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60346064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e4e8b5c1795ff4c51f134ec8eebfaf4c522c6f4a0d5f9bed6b59523312f977`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:26:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:53 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d8aecb4bc7b9e58c615fe5a04f51a5710114ff668af7b4f56dd368d492375e7d`  
		Last Modified: Tue, 24 Feb 2026 18:43:47 GMT  
		Size: 48.7 MB (48666927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581bfb8a9f08741a9688cbd4847063a899dafe26de7e054402802e40c6c9264e`  
		Last Modified: Tue, 24 Feb 2026 19:27:05 GMT  
		Size: 11.6 MB (11585458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5587112c8a56e54d9ed2310e724d9192a98e6019b4307ef9ed30f6602c7f4dd5`  
		Last Modified: Tue, 24 Feb 2026 19:27:05 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d840470a70e0204721f6afdab18b5018d4a7158097c2482de57eee28b881fe03`  
		Last Modified: Tue, 24 Feb 2026 19:27:05 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d5e5971a139a090388ccae1b8304d58824c8c94c73d3afe79392b1756ed1b0`  
		Last Modified: Tue, 24 Feb 2026 19:27:05 GMT  
		Size: 90.8 KB (90778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b95b63e2a134f3e18d4e878cca85f390d3a93ac5f76d1bd65e85835033c6378f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c566102fae4474d5268d27f3d3694454899baaf102caa9ef1d1d025e862221`

```dockerfile
```

-	Layers:
	-	`sha256:cd128fea3ea21d65d2490404d0d3b1bc11361998b2008db663de2cc4799e8510`  
		Last Modified: Tue, 24 Feb 2026 19:27:05 GMT  
		Size: 3.6 MB (3604803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c14e19f829516721c08701c0421cb36e96e401ece1fc6f93c0abb422676c0c5`  
		Last Modified: Tue, 24 Feb 2026 19:27:05 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:30907069047c7e7d5885360cd5800c0d4c044ee2dae585a0ce3e5c3d469ed59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60090738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dc7d00ed6efcf25119063a3ce65ea3715d14cd75a89c5e07ae6e1a232c9130`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:31:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:31:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:31:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:61a95a2f6784ce634817550699b53ea6f85b093ca9ec55f99c5217b534acfb51`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 48.7 MB (48709262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c44f13dd6679024c4c30ef97c3bf7665c6b86aec2767bc75ae5f3530b99ae65`  
		Last Modified: Tue, 24 Feb 2026 19:31:47 GMT  
		Size: 11.3 MB (11287063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320ed8700bba358f6a26c78d547bb8e06cd9015a915f46d8a2ab6b4ca0ab28bb`  
		Last Modified: Tue, 24 Feb 2026 19:31:47 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2eee81cbf224eb2546024df1a4dfca82f2f441ace30b8cc28712617077f3147`  
		Last Modified: Tue, 24 Feb 2026 19:31:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e44a2d5200f5872bc2d8d48be75399ba3b40108ec56fe83767e2e0eb6d18e80`  
		Last Modified: Tue, 24 Feb 2026 19:31:47 GMT  
		Size: 91.5 KB (91506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:56fea7b826bdfc463c15a54406a0371fd55508de79ae76d15e6ab00bfb13f78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec52d8886a0def37a4236a2adeca1f0c23a914c3b5817948b4da31a162d60a9`

```dockerfile
```

-	Layers:
	-	`sha256:77c1a2fd4be0d60056fc9bc1758f38e0d6540cdfc8ff28e014c6a579c9f9ee94`  
		Last Modified: Tue, 24 Feb 2026 19:31:47 GMT  
		Size: 3.6 MB (3613066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d2d97974db05b7cd887cb8aa713a1f1b5d59ad2923cd79335798cd938e93d2`  
		Last Modified: Tue, 24 Feb 2026 19:31:47 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:605b2c498877f167e9f75f6ea18c80da511852741282e2b6ee8cc26ca0f74863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61943118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d2c716e30adba3eb29cf4901b695f43605ddd8ad54d1247b9a0af9269d9f19`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:27:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:27:13 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:27:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:def456773a4aeca49d4b978ec8b12f148f201cb7cf9c2174e05e9ced13435b6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:59 GMT  
		Size: 50.0 MB (50022115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5264e6d084f275a47e6db1c040eb960c6cdcc9f8632da3b263f3a732c90d4513`  
		Last Modified: Tue, 24 Feb 2026 19:27:25 GMT  
		Size: 11.8 MB (11827011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec990ed8e4ae5c803f69db7c65d159f49648fd281d828d678e04d4fc0fd31038`  
		Last Modified: Tue, 24 Feb 2026 19:27:24 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224ff852816d65da8f9dc02bbb73fac2000c3fa6cdb0efbc878d2ee2a05ddabb`  
		Last Modified: Tue, 24 Feb 2026 19:27:23 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b307aa6c2a8a0cb16d2485ebb98e5cd2d4582a566a0d3dc25755bc4b9004eab`  
		Last Modified: Tue, 24 Feb 2026 19:27:25 GMT  
		Size: 91.1 KB (91087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:47a161d410124f89be352a98f317ee630417d7e32af78e30c6d9e86c5484bd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5350774db78d431078e3969ed52ec7d29f9eef70a1901c18e790f7adfd1bc82`

```dockerfile
```

-	Layers:
	-	`sha256:e5425aee379664b9f166171d603e86274f591475b2875b19027cc2ad8d4b832b`  
		Last Modified: Tue, 24 Feb 2026 19:27:25 GMT  
		Size: 3.6 MB (3602748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1a9056f9b5589230a7898159f4aa8befb4becefc20dd5a0a5b39d144c33ad1`  
		Last Modified: Tue, 24 Feb 2026 19:27:25 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
