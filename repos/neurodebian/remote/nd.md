## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:70ce97f6796d0bd1e6ea7d563d93fd9f0cf0bf63a8e127ac6cce87afe7284bf1
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
$ docker pull neurodebian@sha256:6d1fc426c529a7179490427ff1b139fc09928fc88d60bf4457cbebe436b25e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60149970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744a29bf828d9a897f7c0bdcd7643b2452b36aacb4109564bc3d3ec0b0650f40`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:44:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:224b32b461470cab0a5b83292cf42319369c28ec8beae34418e705d6d0530bb2`  
		Last Modified: Mon, 16 Mar 2026 21:52:47 GMT  
		Size: 48.7 MB (48676470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435378e6edfc7c12b4ed65b613af023d57fa606a0b2de1de8f50080d443f273f`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 11.4 MB (11381178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1875139f86f2f68b13903493d1a046622fa09ce497f13444a0e1eb58b29425b`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a527387d1617429a2a96c43d1624a92101db3a1b29ec5eb4b897ad7b8dced4a`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda3bfc8cab99ab329696b3337e16a74b175a67bf860a8a5e054ecfbf0501e9d`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 89.4 KB (89418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1d440ccd085c26be74202165cc3b1128954c2b3f47733236a0416fd8fd6ee623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77c3d0f0ba756177d09af10cadbeb017c39ffdfb8f4018efff68d41a8ecd8c`

```dockerfile
```

-	Layers:
	-	`sha256:3b9bd7caf2ea52ea4337edf4c858d40e68bb08754805df3c001c44a1c3eda640`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 3.6 MB (3552870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39e1f533aa58bd0505780c3952c186eaefa6e16ea70768cef347041446e1574`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a5602e206119d499ae31f37ec778d866c2517bc33939bd34c211c16addb7ead2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59885100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a6633bede2c6667f856a815cbfc4b9ec319fe7184a856765b980e6d2666885`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:47:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f8aa045b0b46f2987d2dfdc549957d53bf9eb7148b1452027f1bbe82759ee08b`  
		Last Modified: Mon, 16 Mar 2026 21:58:00 GMT  
		Size: 48.7 MB (48715175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5418123350c32272b46788d05723fde818111cd59f2e38fcc932ec52bf8fe8`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 11.1 MB (11077011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413fc3519da5d42e3e7a4e0720341191628348b309bc6ca103ece3f91c45cd1`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb5599a29b53a0abd1361980e40020e8cad1bc5b287ae4e26edd5449ec2b15c`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870365bc67ca6e2403c7a765994ce210adf4b8b4a446b30cf6e30e61908fa7f1`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 90.0 KB (90009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:083861651e2e24b282385211009a4b132faf832b34f12bec2441737e7994804f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f442457820b74fd771de15f04d68e4b00d5f3b50f05cb0bb400375043dd031`

```dockerfile
```

-	Layers:
	-	`sha256:d7dae46320117521fa0297a784b4d6534e8b02a980fd8163ab267cb9ae8fbe87`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 3.6 MB (3559671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d4098ea9ca794fa9b81557858d2f1014c06c9b6c06489190f9ad2f087e3a0b`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:0620854eff36c1edaf794aa0c06278a96d50219bfcb7effa5a679e55b95bdb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61646917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd87c508951df3df21c5f3f516ef4b475b9395aa986826cf33c665918650caa7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:45:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d910d8b21d9682e89de3d97b422096e3120f61049a143cd139a1c42e9bb8b77e`  
		Last Modified: Mon, 16 Mar 2026 21:53:09 GMT  
		Size: 49.9 MB (49948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b321b1e66d39564c47555de32d340a791425b7cce9bb9cec583222c8d7ca49c`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 11.6 MB (11606315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40be60bbfbb52b308f7a3da3d6ce45f2b45d390b3a218b8962d5d180766adfa9`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5a3927c9a8ad3f0340e06b2184345914a8af2da8f0e0b9cd871831857de9aa`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a63559a329af0724eb71b76ffc8a94493d39318fe64600142629c2796050b5`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 89.7 KB (89655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15308b6f9290ae75c8ead47e44c0f9e1615b18562b59e678ef8e14c24e21202f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a966c7f4dc6dc87414338959c6433f2a3b6764d554b8a92280eaccc04454fa59`

```dockerfile
```

-	Layers:
	-	`sha256:dfe0057bfe8bce433fe945340cdaf4eaefe8fe9f9b3e138240b50c5fe795735d`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 3.6 MB (3550822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751950bfb2649acce0e08fbef36c572123014cdb7a355ba165830660ca67048c`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
