## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:116c5fbec75d95e47b76b3c8bf7b7b37e4f88b5682fe4274010077a47b7168a4
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
$ docker pull neurodebian@sha256:002f7fb8429812eb25298710a7653a0a06f2c9b122c6f1e6cdec699025eb2bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60158655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f010db1188288b639deb5a145a8914aa4fb9a0fcc1608fbaaa7f848463f1c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1747df0eb464e2466f732dbdce6dd13594b17aa4954ff2de6661db9bba7dc57f`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 11.4 MB (11368698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e9bbb5347613d12ad4629ce58ff03d6518d863d196c566ffe2b9438dbc2b81`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1358388c23a9da6d99c35767f0729ddcc9c8f5e34e1546ab07fda207f7f76442`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d52213fc877026fddaa9702eec5a54aaf090a257a494c9ec1a1ef372507e5`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 89.4 KB (89404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2a8511cf9858d39b173407e9f856956399afd006e514085607b952ba32adffcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f0196c883ebecb3e2e7e3daedcbd349d965708a2b495f6cf3eea2b727f1f67`

```dockerfile
```

-	Layers:
	-	`sha256:915ce8fda991d89afb68659ee3ea0879aba0c9c6ddff49a99f3fea9ad8cbc4a4`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 3.6 MB (3553159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b9ff0b8b58c94f8e910399c0d59d0516bc0f14000931a33590243c7214e270`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:edb2b53157537c2d2c02dfd8eece602261263f34335795b69eeb92d36f5af494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59811267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783523f0adabf2862579080f534b06b40e27599b5393c28a50d158d791522d5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8be2228c7df976aa0c1c2333d6e8d72b206ff7533d4625ffeae3663f7240d98e`  
		Last Modified: Tue, 07 Apr 2026 00:11:06 GMT  
		Size: 48.6 MB (48643356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697160fe466de149ab190bec6e9e1290ade0a79286096e7daa5c760e60197f5`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 11.1 MB (11075013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c36960bff1a2ead8dcab909b24198e7190f9e0116e4fe6e295d76f8078a6b8a`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c1b95f12a1663dc10a0cc935bb1a7e9a7c5991e3e62be7a88b1d82aa3beb00`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a92fcb7587a72995d5472a8ae08413c3262707d6d83ee78a4498382240cca9c`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 90.0 KB (89989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:df205eb13b6222d0b2746f3723e697c01e488e9b92727d7dea12dd97cf3656be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94c537e2f013c3777b8e6ed31123c1a89e866c06cb72480cbd9307cc2cb86a8`

```dockerfile
```

-	Layers:
	-	`sha256:65718c326ca36ce31873d1b5c78aa7554ad5f5bb91e9c8c5367648577e6deec4`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 3.6 MB (3558012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18963cf37800d3076a9518339af99dd3f02829ab9bc2067ecfe637935cb8616c`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:963e9e111e8de94cf6f0bc0fd6677f10f9d66bfcaa1ab43ea137bbbe888beb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61577258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d79aed3d5d0abe958e1d97fb8c77b27f9058782244428ed88556d34491bd44`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:48:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da53d68ed4a6c93e46a747a177c1be57f4bedc8509f9b442a53b6120f33a247`  
		Last Modified: Tue, 07 Apr 2026 01:48:55 GMT  
		Size: 11.6 MB (11606305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274d6db09e5125c5a1f35e35a167fb6e882923e24a15fdccfd52ae3c59f13988`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e4cdfef32a160c154e91fc59967a8b5ac1c481c4b43b670dd60dc11820f3c1`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9110c7b8d6c12b2a6cd0a52f39f4a960d1d3d9252246c30e1fa606d606b5d24a`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 89.7 KB (89656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f1b6fb33d3cc7c53d4c45383340dff8aa68b2541fafda6f159f57ee8a6edfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f3004b499770aae74ad966f0b5757ca7e53a5920485fa3968c47aebdb71fef`

```dockerfile
```

-	Layers:
	-	`sha256:2a79d047e2b4515eda42e50df12461392fed49171ad04a9ce1f1d75ae60fb003`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 3.5 MB (3549980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3bdd8d104ffc8e688a0c4a90fd13b9f18bcd3cfee4cf483f0a2a5a3114b82e`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json
