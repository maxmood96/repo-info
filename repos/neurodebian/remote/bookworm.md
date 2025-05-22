## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:2e568018d73892b21c1715a9e56e635e716350ac7b8cf61a8017981cee0916ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:ccfe6ca082745c97fa4ba00ac0fe25887b67c92d221e565744d35cf56c0a3625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed82c42a1fdc4026cc2c4ceeff7f950128e2011566e20783e15528b0668b750e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1479a7dfdd7bd71a331fb57263d63a48b18f362276a8d3507efc1dba468dc`  
		Last Modified: Wed, 21 May 2025 23:23:02 GMT  
		Size: 11.3 MB (11266844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3811163e1e52f20133f4a2f726f2743ad294c104a345c4ef4f4da69b9d078fd`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df351ef0700f87809686368ec3b0cfb7da8af39ae9d31bc006aa2bd60ac1ed9f`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1793f6f7307e57ec6794a674c75ce0ce2fd92331fdb2bc2df11fa0a20c8b713`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 93.2 KB (93191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e71bf24417e743e7203e3a4ed63b024a5503c29a6727c49b599ec8c813018f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd40900d4f9231c013ab72c0a9343ece65312a9276382d197774a7855aa9ccd`

```dockerfile
```

-	Layers:
	-	`sha256:e4f564ec6f91cac7f96d55a009199eaa0bb108fc7cd50780a733bf915c2fc0c1`  
		Last Modified: Wed, 21 May 2025 23:23:02 GMT  
		Size: 4.0 MB (3954822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895607a345c49ee9f2d34f2bd8ad0768f41e02c79dd16e5ce4b3c0005f3aecdf`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b99fc050dbe97fce7b2be84bbc74c98d5afa82adddac631d2d46606783d7dd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb89d84092ffa79c342c9d0ce96e517bb5e6f4c7740cb52c4308e59d29e7a39`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 93.4 KB (93443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:24a9982c45872ee44ad75c916770b6e54684d969af7c83f3976797a0f69b2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995ffd9cc5fdbc0dce9f2f9c92f5f9e09db94d23c707ed207103dea6e58ff697`

```dockerfile
```

-	Layers:
	-	`sha256:fe489f993345a9159847e68d85a3fff889d3bec20f51ae60371fdbabd7d6961b`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 4.0 MB (3955076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b54691e54bf95f0c8dac0cd29d7358fc539e3c85d5727d223011e9f57727b4`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:40b9766f674cbe18059a52d9132028b78d1d9732a101ffa3eacca866a11348b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61255830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52468f2219071593b803836c124a97455e373469ae1a6e9be7c13e5f895dfba0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b5e346146a229401e10471e4cbbe84a57931d3139ea0434147f07c663d432b`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 11.7 MB (11688893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1255468b95293fb1e60abbe6d77208b9625ac10eca1c246235c3ac7ddfb801f1`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cd2e2bf1a80e558d1befccd7dc91728b49d1c244d7da9339a06a4d7ac3af14`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcb862dadada5fb7f5ae18bd37f410686a49ba21bf2d7c577bae16a2ef16ed6`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 93.2 KB (93203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848686458fe8f432331e61cc40d34b67889f849657c2f6783f2a53c3a98753eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c148c8e5d098f166d5f6a24c1c83ec09679603cbbc8c6fd8c3efd9377a3b8bb`

```dockerfile
```

-	Layers:
	-	`sha256:5c09dd3adb1cb49760d6fb3a008b82184b82580e7331d7f6df9827955bfbfbe0`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 4.0 MB (3952790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915e7352977df39d05b78465ba9906fc5569734a50655cd7c22622a7105e20ae`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json
