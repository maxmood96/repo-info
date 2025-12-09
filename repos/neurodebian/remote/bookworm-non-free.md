## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:3612fa73d61b88a611ef8920819359f1d15adde729539b14180e4adf68059c48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b31dd19cb8f532ab2efebcb499658eeb8d87dcdf6d4b04fcac4f6ab06f5d27cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edae1787bce8bcca4a166e0e2305d9d6e07bfda6b45407421f3b376449439f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:13:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:13:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:13:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a537fb8a33ce42164dd7b596a4be46383cced7f4c92cbd4dff2d24ff856b1bd6`  
		Last Modified: Mon, 08 Dec 2025 23:13:49 GMT  
		Size: 11.3 MB (11269667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78eec7b61036079905d905c492db01c46a58146aaffbc7e6bb04e42a28b73cc`  
		Last Modified: Mon, 08 Dec 2025 23:13:48 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2882acbf09d446257a309f5a59d2fe9d5d3595a634eeda3bc1c45f1507bb5872`  
		Last Modified: Mon, 08 Dec 2025 23:13:48 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772f528fca1d41d0791d3d09dd9f8cf9bf4b6aea90ed88432b03aeb9bd7348c0`  
		Last Modified: Mon, 08 Dec 2025 23:13:48 GMT  
		Size: 93.4 KB (93392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9dd7ec6230195925eded96ff45095318c728c365cc1a0459c45ac4677aece3`  
		Last Modified: Mon, 08 Dec 2025 23:13:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1d533824cb9b387db4130b89ac5e6c32f326da747b536ac78994cffb9f5b84b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fcac9ddcf40541d75b675c77977af00fc077c73f23a8654cef616f2c71b73c`

```dockerfile
```

-	Layers:
	-	`sha256:925b8ba99208a82e497782b0f43dcf7ebd995f247ae7e6b5b3b26bdac92fffca`  
		Last Modified: Tue, 09 Dec 2025 02:07:36 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85c2758b3d01dc9c93a7af03f9c86113cabd9d71ec848c506a6b787d34ead7d4`  
		Last Modified: Tue, 09 Dec 2025 02:07:37 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:799a9fdaeac12508072ad286af1e4e7af48fdb6b90fa105569d75c585522decb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9196b72b4cef17624139168cb8a29ac1a83af665a592f750bb3c2721486de148`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:52:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:52:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:52:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:52:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:52:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807214d6bb58ce93643f23da0d4f513c5ad5c1d7afbca79b7efed5365942ca8`  
		Last Modified: Tue, 18 Nov 2025 03:52:35 GMT  
		Size: 11.3 MB (11253434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c6e4641d306f35a7865dc55f0617616dc6b1fdffcb7dc3efedf0737835a76`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba37d77eb8f27c5b50207c5ded85c692607c6c8731c3646f7aa887fb707d9b4`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f35d356531128f85210ebbce70caffc3b026330c2f6cf599438d5cc6fd6ca6`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 93.5 KB (93515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a21ba5c85c56614c9af83a1aedff34ebaa1eb2f907abf5f9e128f2413b19b7`  
		Last Modified: Tue, 18 Nov 2025 03:52:34 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed1488b88f01f98361118e77ce3f25f9d4948315e0be7528e934b3f88bfb8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4703273c9e0ef5f78614bb8691d50f70c13a6b84a97abe62174461caddfb7da`

```dockerfile
```

-	Layers:
	-	`sha256:ff89c214db7039e198f750d1504e92a410cfd11dc52faaab1c904d28bfb17e10`  
		Last Modified: Tue, 18 Nov 2025 05:08:52 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb4ebb333c44656c1f30b692d638ce65ab8a9add9573811002d77ae7ef10360`  
		Last Modified: Tue, 18 Nov 2025 05:08:53 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9a32e796340a46ccaa79995c6356a8ee8907a0384617d3ca1d62bc7abbc519dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a7cf4fb69ad656303e0cbb42407cb0e78b11763a461bc4b707dc5d83aa0cf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:15:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:15 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfea0d8e4e48d2ed88857fa647a44ad0812430118aaf423ca71393709f1e738`  
		Last Modified: Mon, 08 Dec 2025 23:15:33 GMT  
		Size: 11.7 MB (11690094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9eb22c650699e169eb028f46c41221994a2556ec3bd4be0d2559aeb1d5fe1b`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b82668d4fe89353db6e2d50cb43e936051f8ebc7377922145ef6e183043053d`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c5501984a937c9a1905dfe66b2ebd4e0cbd9fe1232880dc1e283b1a8d0a14b`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 93.4 KB (93374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f029ba16f9cf3b81359ae9885b6449a1378e50b4f21041be43a2208e75f04`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8d24dd4a17c911e8f6b1d6df7fdd2a5884a56ddacd395ba9fe61b20d9b737d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914ea91f455df92d0644bf85fad635d2b920cfbc7b9cbd368e7c5abbbd7539f9`

```dockerfile
```

-	Layers:
	-	`sha256:ea5f6d542df3b6cf1041a0765816de213980e146ac726111d73f5413e827ca07`  
		Last Modified: Tue, 09 Dec 2025 02:07:46 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b94969bb82f97c4f66bf4ec317e7ef048252032a76a327ede5483777308620`  
		Last Modified: Tue, 09 Dec 2025 02:07:47 GMT  
		Size: 16.0 KB (15961 bytes)  
		MIME: application/vnd.in-toto+json
