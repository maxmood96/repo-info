## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:eacfbf31285a85424ef93cc6ded82ba2fbe5b986a239fd69488c80f0f710945f
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
$ docker pull neurodebian@sha256:6a2235613045b70910bef31f95d400e4ea728d3d872c3eadf068ad6a5556e46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60059992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc43089ed9146b80ec6df0e482f668dacfa87f89c583de65af75120f18cf742`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:01:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a619bb3c1f14c591cc163d929ea3f43df5d6acebdd877fecaacf054d56531b3e`  
		Last Modified: Tue, 07 Apr 2026 00:11:23 GMT  
		Size: 48.6 MB (48587084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa628479b442faba1c1af937394fb683eb51cbbb599e6c4a61d0da961f2d7b3`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 11.4 MB (11380125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcd0304f3bf7b2e1d0efa613975496c67119b2c9e846c5e0c82ebd89a33967e`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce0cd7dafe8e8815c85d2c163d5ee73efaea39c8aa25dfd85fcf04a68c46fb0`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561ffd779e9b744ab3a7ec489f3193657675d1cc63c19bd41a103f810ae0d39`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 89.4 KB (89428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162049e1938cb0cd398aa0c3337a92e241d35b71469a0f3b4afdc6d8facf563`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ed69fb70e1162ba1fcf7caf8b043e147b224c0d768ac9281501a7da25ba4095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5525b32edfe7cca39b6fdd26484b40000d68927bd7d2b0d0a97afa4ef4c6ee3e`

```dockerfile
```

-	Layers:
	-	`sha256:918200918934c6226e2f5e22c79c036415cd438d8dffa4614ab7774fde9c2f2a`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 3.6 MB (3552063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8743c2342684b499a89a50ccc6eac5a1b7ca15b9de0b45b1483221a3422faf17`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ba0014eca13dbdc8c4c9695ee548e42bb17ed8f9a8fec425adbe0fcf9acb7eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b39cda1b57a54ebd323ebf1b4371137f41bf6723582d02109b35182b365179b`
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
# Tue, 07 Apr 2026 02:04:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8be2228c7df976aa0c1c2333d6e8d72b206ff7533d4625ffeae3663f7240d98e`  
		Last Modified: Tue, 07 Apr 2026 00:11:06 GMT  
		Size: 48.6 MB (48643356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b0a86641588b3f119195f4efde642f305d497d115b96e5242a1228f623b53d`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 11.1 MB (11075059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c36960bff1a2ead8dcab909b24198e7190f9e0116e4fe6e295d76f8078a6b8a`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c1b95f12a1663dc10a0cc935bb1a7e9a7c5991e3e62be7a88b1d82aa3beb00`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daedc55759c57539904ad5f302a8d8ac0ba365cada751eb464bce0e48e80211`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 90.0 KB (90012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f8aee6980d05907b17819acc5238181f4a4b97ed15b077d9c94676b52bc1e1`  
		Last Modified: Tue, 07 Apr 2026 02:04:34 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:10828bda83635ab4504a20c3acd44d301d95f70967ba4152cd754792d543519d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc48a161a9fcacbf8106a2b73a2a6a135fbbc570303e482b580cf3e410d897fa`

```dockerfile
```

-	Layers:
	-	`sha256:14e69e855ee2483f98fb85b5ff935450656ad764571383eec285973b6a0ad358`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 3.6 MB (3558048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcb49532153075f479fa9e706d3028ce305e2d853eba7e7ffabb7342c1fa372`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9bedad4528e45438d1623fafecc7ebd4869eb410b0dbb85e4a82aef61511431f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61577804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6518c25eacd6983972f820d07b0b03542e361c4746f0212991a4ab16af0c24ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad078a61f6e4be70ba6616078c3a30d7878e3c52bb074b890ccf08d7ba6c0c01`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 11.6 MB (11606394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d033c8c40129bbee090a07f5e1df4ee001c1ff1b1fd1e0e8fea876d4dfefe77`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6602b36874f6c218ec4f391df4b2e6eb6c4bfd9979f4f111c5fa69b47496ba2`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d50765ea499d27dee96965b634aa3a32c0fba2532d7f79e39a9119111c42be`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 89.7 KB (89666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedfedf99f96257ae9c575d353d0f5d352b036e3a8c97cf7a608eb3837152eb`  
		Last Modified: Tue, 07 Apr 2026 01:49:01 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4750e3e14c0f736243e2236c09b7da62c1b16042e8849a8a4da7588e6081eca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3479307f59614f39eb4a0fdeda1168462dd3a6ab17a49e6e26b68882d8a5e8fb`

```dockerfile
```

-	Layers:
	-	`sha256:e0ded4254441e42d507739c92b200d27c9f0e81de4f3ddb5ef6bdc0428724d01`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 3.6 MB (3550016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aea253b22bc3a5f64020d8dc3bdb1ea14d6dc3aeae1db43327b6b9d33432be8`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
